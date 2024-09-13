# Giới thiệu

> Nền tảng video giao thức 28181 sẵn sàng sử dụng

# Tổng quan
- WVP-PRO dựa trên tiêu chuẩn GB/T 28181-2016 để thực hiện nền tảng phát trực tuyến, dựa vào dịch vụ phát trực tuyến mã nguồn mở xuất sắc [ZLMediaKit](https://github.com/ZLMediaKit/ZLMediaKit), cung cấp các chức năng phong phú và hoàn chỉnh.
- GB/T 28181-2016 là tiêu chuẩn quốc gia về yêu cầu kỹ thuật truyền tải, trao đổi và kiểm soát thông tin của hệ thống giám sát video an ninh công cộng. Được sử dụng rộng rãi trong các nền tảng video của chính phủ.
:- Thông qua giao thức 28181, bạn có thể kết nối camera IPC vào nền tảng, có thể xem và sử dụng các giao thức 28181/rtsp/rtmp/flv để phân phối luồng video đến các nền tảng khác.

# Đặc điểm
- Thực hiện tín hiệu 28181 tiêu chuẩn, tương thích với các thiết bị thương hiệu phổ biến như IPC, NVR của Hikvision, Dahua, Uniview và các nền tảng khác.
- Hỗ trợ kết nối thiết bị quốc gia với các nền tảng quốc gia khác, cũng như hỗ trợ đẩy hình ảnh hoặc phát trực tiếp từ các thiết bị không hỗ trợ quốc gia đến các nền tảng quốc gia khác.
:- Giao diện hoàn chỉnh, đi kèm với trang giao diện đầy đủ, không cần phát triển lại có thể triển khai và sử dụng ngay.
:- Hoàn toàn mã nguồn mở và sử dụng giấy phép MIT. Có thể sử dụng cho các dự án thương mại với điều kiện giữ nguyên bản quyền.
- Hỗ trợ cân bằng tải nhiều nút phương tiện truyền thông.

# Cộng đồng trả phí
[![Cộng đồng](_media/shequ.png "shequ")](https://t.zsxq.com/0d8VAD3Dm)
> Phí là để cung cấp dịch vụ tốt hơn và cũng là động lực lớn hơn cho tác giả. Người dùng tham gia vào nhóm sau ba ngày có thể nhắn tin riêng cho tôi để lại số WeChat, tôi sẽ thêm mọi người vào nhóm. Nếu không hài lòng trong ba ngày đầu tiên, bạn có thể yêu cầu hoàn tiền ngay lập tức, không cần lo lắng, bạn có thể thử miễn phí trong ba ngày.

# Chúng tôi đã thực hiện những chức năng quốc gia nào
# Chúng tôi đã thực hiện những chức năng quốc gia nào
**Là nền tảng cấp trên**
:- [X] Đăng ký
- [X] Hủy đăng ký
- [X] Phát trực tiếp âm thanh và video
  - [X] Điều khiển thiết bị
  :- [X] Điều khiển PTZ
  - [X] Khởi động từ xa
  - [X] Điều khiển ghi hình
  - [X] Báo động bật/tắt
  - [X] Đặt lại báo động
  :- [X] Khung hình bắt buộc
  :- [X] Phóng to khung hình
  :- [X] Thu nhỏ khung hình
  - [X] Điều khiển vị trí giám sát
:- [X] Thông báo và phân phối sự kiện báo động
- [X] Đăng ký danh mục thiết bị
- [X] Truy vấn thông tin thiết bị mạng
  - [X] Truy vấn danh mục thiết bị
  - [X] Truy vấn trạng thái thiết bị
  - [X] Truy vấn cấu hình thiết bị
  - [X] Truy vấn vị trí đặt trước của thiết bị
- [X] Báo cáo thông tin trạng thái
:- [X] Tìm kiếm tệp âm thanh và video của thiết bị
- [X] Phát lại âm thanh và video lịch sử
  :- [X] Phát
  :- [X] Tạm dừng
  :- [X] Tiến/lùi
  :- [X] Dừng
- [X] Tải xuống tệp âm thanh và video
- [X] Đồng bộ thời gian
- [X] Đăng ký và thông báo
  - [X] Đăng ký sự kiện
    :- [X] Đăng ký vị trí thiết bị di động
    - [X] Đăng ký báo động
    - [X] Đăng ký danh mục
:- [X] Phát thanh
- [X] Gọi thoại

**Là nền tảng cấp dưới**
:- [X] Đăng ký
- [X] Hủy đăng ký
- [X] Phát trực tiếp âm thanh và video
- [X] Điều khiển thiết bị
  :- [X] Điều khiển PTZ
  - [X] Khởi động từ xa
  - [X] Điều khiển video
  - [X] Báo động bật/tắt
  - [X] Đặt lại báo động
  :- [X] Khung hình bắt buộc
  :- [X] Phóng to khung hình
  :- [X] Thu nhỏ khung hình
  - [X] Điều khiển vị trí giám sát
  :- [ ] Cấu hình thiết bị
- [X] Thông báo và phân phối sự kiện báo động
- [X] Đăng ký danh mục thiết bị
:- [X] Truy vấn thông tin thiết bị mạng
  - [X] Truy vấn thông tin thiết bị mạng
  :- [X] Truy vấn trạng thái thiết bị
  - [X] Truy vấn cấu hình thiết bị
  :- [X] Truy vấn vị trí đặt trước của thiết bị
- [X] Báo cáo thông tin trạng thái
:- [X] Tìm kiếm tệp âm thanh và video của thiết bị
- [X] Phát lại âm thanh và video lịch sử
  :- [X] Phát
  :- [X] Tạm dừng
  :- [X] Tiến/lùi
  :- [X] Dừng
- [X] Tải xuống tệp âm thanh và video
:- [ ] Đồng bộ thời gian
- [X] Đăng ký và thông báo
  - [X] Đăng ký sự kiện
    :- [X] Đăng ký vị trí thiết bị di động
    - [X] Đăng ký báo động
    :- [X] Đăng ký danh mục
- [X] Phát thanh
- [X] Gọi thoại

   


# Cộng đồng
Mã nguồn hiện đang được lưu trữ trên GitHub và Gitee, Gitee hiện được sử dụng như một kho lưu trữ tăng tốc, không chấp nhận issue.
GitHub： [https://github.com/648540858/wvp-GB28181-pro](https://github.com/648540858/wvp-GB28181-pro)  
Gitee： [https://gitee.com/pan648540858/wvp-GB28181-pro](https://gitee.com/pan648540858/wvp-GB28181-pro)