<!-- 7*24不间断录像 -->
# Ghi hình liên tục 7*24

Hiện tại nếu muốn thực hiện ghi hình liên tục, chỉ tắt tính năng dừng đẩy luồng khi không có người xem là không đủ, thiết bị có thể gặp phải tình trạng mất kết nối mạng, khởi động lại, dẫn đến gián đoạn ghi hình. Hiện tại, chúng tôi cung cấp một giải pháp tạm thời có thể sử dụng.

**Nguyên lý:** wvp hỗ trợ sử dụng địa chỉ luồng để tự động phát, tức là bạn có thể lấy một địa chỉ luồng và phát trực tiếp, ngay cả khi thiết bị đang ở trạng thái chưa phát, wvp sẽ tự động giúp bạn phát; ZLM
của proxy kéo luồng sẽ thử lại vô hạn, chỉ cần luồng khôi phục là có thể kéo lên, dựa trên hai nguyên lý này.

**Giải pháp như sau:**
1. Trong cấu hình của wvp, đặt `user-settings->auto-apply-play` thành `true`, bật tự động phát;
2. Nhấp vào kênh bạn muốn ghi hình, nhấp vào "Thêm địa chỉ" ở góc dưới bên trái của trang phát, nhấp vào `rtsp`, lúc này sao chép địa chỉ `rtsp` vào clipboard;
3. Thêm một luồng vào proxy kéo luồng, điền địa chỉ bạn đã sao chép, kích hoạt thành công là được.

**Điều kiện tiên quyết:**
1. wvp sử dụng nhiều cổng để nhận luồng, nếu không bạn sẽ không thể có được một địa chỉ luồng cố định, và không thể thực hiện tự động phát.

