<!-- Triển khai -->

# Triển khai
**Vui lòng đọc kỹ nội dung sau**
1. WVP-PRO và ZLM hỗ trợ triển khai riêng biệt;
2. Các cổng cần mở
| Dịch vụ | Cổng                       | Loại          | Bắt buộc |
|--------|:---------------------------|---------------|----------|
| wvp    | server.port                | tcp           | Có       |
| wvp    | sip.port                   | udp và tcp    | Có       |
| zlm    | http.port                  | tcp           | Có       |
| zlm    | http.sslport               | tcp           | Không    |
| zlm    | rtmp.port                  | tcp           | Không    |
| zlm    | rtmp.sslport               | tcp           | Không    |
| zlm    | rtsp.port                  | udp và tcp    | Không    |
| zlm    | rtsp.sslport               | udp và tcp    | Không    |
| zlm    | rtp_proxy.port             | udp và tcp    | Mở một cổng |
| zlm    | rtp.port-range (cấu hình trong wvp) | udp và tcp | Mở nhiều cổng |

3. Đề xuất triển khai môi trường thử nghiệm trên một máy chủ, tắt tường lửa để giảm thiểu khả năng gặp sự cố mạng;
4. Môi trường sản xuất mở cổng theo nhu cầu, nhưng đề xuất thay đổi cổng mặc định, đặc biệt là cổng 5060, dễ bị tấn công;
5. Trường hợp sử dụng docker để triển khai zlm, vui lòng sử dụng chế độ host hoặc ánh xạ cổng nhất quán, ví dụ ánh xạ 5060, nên ánh xạ cổng bên ngoài cũng là 5060;
6. ZLM và WVP sẽ duy trì tần suất giao tiếp cao, vì vậy không nên đặt WVP và ZLM ở hai mạng khác nhau, ví dụ WVP ở mạng nội bộ, ZLM lại ở mạng công cộng.
7. Khởi động dịch vụ, ví dụ trên linux
**Khởi động WVP-PRO**
```shell
nohup java -jar wvp-pro-*.jar &
```
**Gói war:**
Tải xuống Tomcat và đặt gói war vào thư mục webapps, khởi động Tomcat để giải nén gói war, sau đó dừng Tomcat, xóa thư mục ROOT và gói war, đổi tên thư mục đã giải nén thành ROOT, cấu hình thuộc tính Server.port trong tệp cấu hình trùng với cổng của Tomcat. Sau đó khởi động Tomcat.
**Khởi động ZLM**
```shell
nohup ./MediaServer -d -m 3 &
```
### Triển khai tách biệt frontend và backend
Triển khai frontend và backend hiện đã được hỗ trợ trong phiên bản mới nhất, vui lòng sử dụng phiên bản sau ngày 15 tháng 3 để triển khai.
Các tệp đã biên dịch của frontend nằm trong `src/main/resources/static`, triển khai các tệp trong thư mục này.
WVP mặc định mở tất cả các giao diện hỗ trợ cross-origin. Triển khai tệp frontend vào container WEB và đặt địa chỉ truy cập là địa chỉ của WVP.
**Cấu hình máy chủ frontend**
1. Cấu hình địa chỉ máy chủ trong `src/main/resources/static/static/js/config.js`, tức là địa chỉ dịch vụ wvp
```javascript
window.baseUrl = "http://xxx.com:18080"
```
`Địa chỉ này cần được máy khách truy cập, vì yêu cầu được khởi tạo từ máy khách, không giống như proxy`
[Tiếp nối thiết bị](./_content/ability/device.md)
### Tài khoản và mật khẩu mặc định
Sau khi triển khai xong, có thể truy cập WVP thông qua địa chỉ IP và cổng, tài khoản và mật khẩu đăng nhập mặc định của WVP đều là admin.
