<!-- 编译 -->
# Biên dịch
WVP-PRO không chỉ thực hiện giao thức GB28181 mà còn là một nền tảng video hoàn chỉnh. Vì vậy, đối với người mới, bạn có thể cần một chút kiên nhẫn để hoàn thành. Nếu gặp vấn đề, đừng lo lắng, bạn có thể
1. Tìm kiếm trên Baidu
2. Tham gia hỏi đáp trên [Zhishi Xingqiu](https://t.zsxq.com/0d8VAD3Dm)
3. Gửi email cho tác giả 648540858@qq.com để tìm kiếm hỗ trợ kỹ thuật (có phí);

WVP-PRO được phát triển bằng Spring Boot và quản lý phụ thuộc bằng Maven. Đối với những người quen thuộc với phát triển Spring, việc biên dịch, triển khai và chạy sẽ rất dễ dàng.  
Dưới đây là một phương pháp chung để giúp mọi người chạy dự án.
## 1 Giới thiệu dịch vụ
| Dịch vụ         | Chức năng                                      | Bắt buộc                  |
|----------------|------------------------------------------|-------------------------|
| WVP-PRO        | Thực hiện tín hiệu GB28181 và các chức năng liên quan đến nền tảng video | Có                       |
| ZLMediaKit     | Cung cấp phần phương tiện của GB28181 cho WVP-PRO và hỗ trợ phân phối các định dạng luồng video khác nhau | Có                       |

## 2 Cài đặt phụ thuộc
| Phụ thuộc | Phiên bản     | Mục đích          | Cần cho môi trường phát triển | Cần cho môi trường sản xuất |
|--------|------------|-------------|--------|--------|
| jdk    | >=1.8      | Chạy và biên dịch mã Java | Có      | Có      |  
| maven  | >=3.3      | Quản lý phụ thuộc mã Java  | Không      | Không      |
| git    || Tải xuống/cập nhật/đẩy mã | Không           | Không      |
| nodejs || Biên dịch và chạy tệp frontend  | Không           | Không      |
| npm    || Quản lý phụ thuộc tệp frontend   | Không           | Không      |

Nếu bạn là người mới, khuyên bạn nên sử dụng nền tảng Linux hoặc macOS. Không khuyến khích sử dụng Windows.

Môi trường Ubuntu, ví dụ với Ubuntu 18:
``` bash
apt-get install -y openjdk-11-jre git maven nodejs npm
```
Môi trường CentOS, ví dụ với CentOS 8:
```bash
yum install -y java-1.8.0-openjdk.x86_64 git maven nodejs npm
```
Môi trường Windows, ví dụ với Windows 10:
```bash
Ở đây không nói chi tiết, bạn có thể tìm kiếm trên Baidu hoặc Google, hầu hết đều là nhấn "Next" và sau đó cấu hình biến môi trường.
```
## 3 Cài đặt MySQL và Redis
Ở đây bạn có thể tham khảo các hướng dẫn trên mạng để tự cài đặt.

## 4 Biên dịch ZLMediaKit
Tham khảo [WIKI](https://github.com/ZLMediaKit/ZLMediaKit/wiki) của ZLMediaKit, nếu cần sử dụng chức năng đàm thoại, hãy tham khảo [Hướng dẫn biên dịch WebRTC của ZLM](https://github.com/ZLMediaKit/ZLMediaKit/wiki/zlm%E5%90%AF%E7%94%A8webrtc%E7%BC%96%E8%AF%91%E6%8C%87%E5%8D%97) để kích hoạt chức năng WebRTC của ZLM. Dưới đây là các bước quan trọng:
```bash
# Người dùng trong nước khuyến nghị tải xuống từ trang gương đồng bộ Gitee 
git clone --depth 1 https://gitee.com/xia-chu/ZLMediaKit
cd ZLMediaKit
# Đừng quên thực hiện lệnh này
git submodule update --init
```
## 5 Biên dịch WVP-PRO
### 5.1 Có thể clone qua git hoặc tải xuống từ dự án
![Tải xuống](_media/img_1.png)
![Tải xuống](_media/img_2.png)
Clone từ Gitee
```bash
git clone https://gitee.com/pan648540858/wvp-GB28181-pro.git
```
Clone từ GitHub
```bash
git clone https://github.com/648540858/wvp-GB28181-pro.git
```

### 5.2 Biên dịch trang frontend
```shell script
cd wvp-GB28181-pro/web_src/
npm --registry=https://registry.npmmirror.com install
npm run build
```
Nếu biên dịch gặp lỗi, thường là do vấn đề mạng, dẫn đến việc tải xuống gói phụ thuộc thất bại  
Sau khi biên dịch hoàn tất, thư mục `static` sẽ xuất hiện trong `src/main/resources`
**Biên dịch hoàn tất thường trông như thế này, không có thông báo lỗi màu đỏ**
![Biên dịch thành công](_media/img.png)

### 5.3 Tạo file jar thực thi
```bash
cd wvp-GB28181-pro
mvn package
```
### 5.4 Tạo file war
```bash
cd wvp-GB28181-pro
mvn package -P war
```
Nếu biên dịch gặp lỗi, thường là do vấn đề mạng, dẫn đến việc tải xuống gói phụ thuộc thất bại  
Sau khi biên dịch hoàn tất, file `wvp-pro-***.jar` hoặc `wvp-pro-***.war` sẽ xuất hiện trong thư mục `target`.  
Tiếp theo [cấu hình dịch vụ](./_content/introduction/config.md)
