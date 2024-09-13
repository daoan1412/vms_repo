<!-- 抓包 -->
# Bắt gói tin

Nếu nói về lập trình mạng, có công cụ nào mà bạn phải biết, tôi nghĩ bắt gói tin chắc chắn là một trong số đó. Là phương tiện quan trọng nhất trong quá trình gỡ lỗi GB/T 28181, tôi nghĩ nếu bạn thực sự quan tâm đến nó, hoặc hệ thống gặp vấn đề có thể được giải quyết nhanh nhất, thì bạn nhất định phải học cách bắt gói tin.

## Lựa chọn công cụ bắt gói tin
### 1. Wireshark
Trên các hệ thống có giao diện đồ họa, như Windows, các bản phân phối Linux như Ubuntu, OpenSUSE, tôi thường sử dụng Wireshark để bắt gói tin, cũng tiện lợi để xem nội dung.

### 2. Tcpdump
Trên các hệ thống sử dụng dòng lệnh, như máy chủ Linux, tôi thường sử dụng Tcpdump để bắt gói tin, không cần cài đặt thêm, hệ thống thường có sẵn, file bắt gói tin có thể mở bằng Wireshark để xem nội dung trên giao diện đồ họa.

## Cài đặt công cụ
Cài đặt Wireshark rất đơn giản, chỉ cần làm theo hướng dẫn từng bước. Trên Linux cần giải quyết vấn đề quyền hạn, nếu bạn sử dụng bản phân phối Linux có giao diện đồ họa như tôi, có thể tham khảo các bước sau; người dùng Windows có thể bỏ qua.

```shell
# 1. Thêm nhóm người dùng wireshark
sudo groupadd wireshark
# 2. Thay đổi nhóm của dumpcap thành nhóm wireshark
sudo chgrp wireshark /usr/bin/dumpcap
# 3. Cho phép nhóm wireshark có quyền root để sử dụng dumpcap
sudo chmod 4755 /usr/bin/dumpcap
# 4. Thêm tên người dùng cần sử dụng vào nhóm wireshark
sudo gpasswd -a $USER wireshark
```

Tcpdump thường có sẵn trên Linux, không cần cài đặt, có thể kiểm tra bằng cách sau; hiển thị thông tin phiên bản tức là đã cài đặt.

```shell
tcpdump --version
```

## Bắt đầu bắt gói tin
### Sử dụng Wireshark
Trong GB/T 28181, tôi thường chỉ quan tâm đến gói tin SIP và RTP, vì vậy tôi thường lọc trực tiếp SIP và RTP, có thể nhập vào ô lọc `sip or rtp`, nếu có nhiều thiết bị có thể thêm lọc IP và cổng ` (sip or rtp) and ip.addr==192.168.1.3 and udp.port==5060`. Quy tắc lọc chi tiết có thể tự tìm kiếm, tôi có thể cung cấp một số quy tắc thông dụng để tham khảo.

![img.png](_media/img.png)  
**Chỉ lọc SIP:**
```shell
sip
```
**Chỉ lấy dữ liệu RTP:**
```shell
rtp
```
**Cách mặc định:**
```shell
sip or rtp
```
**Lọc IP:**
```shell
sip and ip.addr==192.168.1.3
```
**Lọc cổng:**
```shell
sip and udp.port==5060
```

Sau khi nhập lệnh bắt gói tin, có thể thực hiện các thao tác như phát lại, xem lại video, sau khi hoàn thành quay lại Wireshark nhấn nút dừng màu đỏ, nếu cần lưu file có thể nhấn `File -> Export Specified Packets` để xuất dữ liệu đã lọc, hoặc `File -> Save As` để lưu dữ liệu chưa lọc.

### Sử dụng tcpdump
Đối với bắt gói tin trên máy chủ, để có được dữ liệu đầy đủ, tôi thường yêu cầu bắt trực tiếp dữ liệu của card mạng mà không lọc, như sau:

Đầu tiên cần lấy tên card mạng, trên Linux tôi thường sử dụng `ip addr` để lấy thông tin card mạng, như sau:

![img_1.png](_media/img_1.png)
```shell
sudo tcpdump -i wlp3s0 -w demo.pcap
```
![img_2.png](_media/img_2.png)  
Dòng lệnh sẽ dừng lại ở vị trí này, có thể thực hiện các thao tác như phát lại, xem lại video, sau khi hoàn thành quay lại dòng lệnh sử dụng `Ctrl+C` để kết thúc, trong thư mục hiện tại sẽ có file demo.pcap, tải file này về hệ thống có giao diện đồ họa để xem bằng Wireshark.

Tham khảo thêm: [https://www.cnblogs.com/jiujuan/p/9017495.html](https://www.cnblogs.com/jiujuan/p/9017495.html)
