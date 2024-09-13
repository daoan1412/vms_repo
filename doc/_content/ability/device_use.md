<!-- 设备使用 -->
# Sử dụng thiết bị  
### Cập nhật kênh thiết bị  
  Nhấn nút "Làm mới" ở cuối danh sách, bạn sẽ thấy một thanh tiến trình tròn, đợi đến khi tiến trình kết thúc và thông báo thành công thì việc cập nhật hoàn tất. Nếu số lượng kênh thay đổi, bạn có thể nhấn vào biểu tượng ![Làm mới](_media/img_14.png) ở góc trên bên trái để thấy sự thay đổi số lượng kênh; nếu số lượng kênh vẫn là 0, có thể là do phía đối tác chưa đẩy kênh cho bạn.
### Xem kênh thiết bị  
  Nhấn nút "Kênh" ở cuối danh sách.
### Xem vị trí thiết bị  
  Nhấn nút "Định vị" ở cuối danh sách để chuyển đến trang bản đồ và xem vị trí của thiết bị.
### Chỉnh sửa một số chức năng của thiết bị trong WVP
Nhấn nút "Chỉnh sửa" ở cuối danh sách để mở cửa sổ bật lên và chỉnh sửa các chức năng của thiết bị.
- Tên thiết bị  
  Nếu không thể đọc được tên thiết bị từ thiết bị hoặc cần đổi tên, bạn có thể chỉnh sửa tùy chọn này.
- Bộ ký tự  
  Chỉnh sửa bộ ký tự sử dụng khi đọc dữ liệu từ thiết bị, mặc định là GB2312, nhưng GB2312 không bao gồm tất cả các ký tự tiếng Trung, do đó đôi khi sẽ gặp lỗi mã hóa, bạn có thể đổi sang UTF-8 để giải quyết.
- Hệ tọa độ địa lý  
  Sử dụng hệ tọa độ nào để phân tích kinh độ và vĩ độ khi hiển thị thông tin định vị của thiết bị, thường không cần chỉnh sửa, nếu gặp vấn đề định vị không chính xác, bạn có thể thử chỉnh sửa tùy chọn này để giải quyết.
- Cấu trúc danh mục  
  Sử dụng thiết bị làm cơ sở cho cấu trúc cây khi hiển thị thông tin kênh của thiết bị, tiêu chuẩn quốc gia 28181 định nghĩa hai cấu trúc cây, chi tiết xem [Cấu trúc cây của tiêu chuẩn quốc gia 28181](./_content/theory/channel_tree.md);
- Đăng ký danh mục  
  Điền chu kỳ đăng ký để bật đăng ký danh mục cho thiết bị, nếu thiết bị hỗ trợ đăng ký danh mục thì khi thông tin kênh thay đổi, thiết bị sẽ thông báo cho WVP những thay đổi nào đã xảy ra, bao gồm thêm/xóa/cập nhật kênh, kênh trực tuyến/ngoại tuyến, mất video, lỗi. 0 để hủy đăng ký.
  Thường NVR và nền tảng kết nối có thể bật tùy chọn này, kết nối trực tiếp với camera thì không có nhiều ý nghĩa.
- Đăng ký vị trí di động  
  Bật đăng ký vị trí di động cho thiết bị, nếu thiết bị hỗ trợ đăng ký danh mục thì khi vị trí thiết bị thay đổi, thiết bị sẽ thông báo cho WVP, thường bật tùy chọn này cho camera hành trình, không có nhiều ý nghĩa cho thiết bị cố định.
- Kiểm tra SSRC  
  Để giải quyết một số vấn đề về luồng của thiết bị, bạn có thể bật tùy chọn này. ZLM sẽ xử lý luồng video theo SSRC được cung cấp. Một số thiết bị có thông tin luồng không chuẩn, bật tùy chọn này có thể dẫn đến không thể phát lại.
### Xóa thiết bị  
  Bạn có thể xóa thông tin thiết bị trong WVP, nếu cấu hình 28181 của thiết bị không thay đổi, thiết bị sẽ đăng ký lại vào lần đăng ký tiếp theo.
### Phát video theo yêu cầu  
  Vào danh sách kênh, nhấn nút "Phát" ở cuối danh sách, đợi một chút để trang phát video bật lên.
### Ghi hình thiết bị  
  Vào danh sách kênh, nhấn nút "Ghi hình thiết bị" ở cuối danh sách, hoặc nhấn vào "Tìm kiếm ghi hình" trên trang phát video để vào trang xem ghi hình, chọn ngày muốn xem để phát và tải về ghi hình.
### Điều khiển PTZ  
  Bạn có thể điều khiển thiết bị hỗ trợ chức năng PTZ để xoay lên/xuống/trái/phải và phóng to/thu nhỏ.
### Lấy địa chỉ trình phát video  
  Sau khi phát video theo yêu cầu thành công, trên trang video trực tiếp, nhấn "Thêm địa chỉ" để xem tất cả các địa chỉ phát, địa chỉ có thể phát hay không phụ thuộc vào việc bạn đã biên dịch đầy đủ và bật chức năng zlm hay chưa, và còn phụ thuộc vào mạng.