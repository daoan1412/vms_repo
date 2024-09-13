<!-- 节点管理 -->
# Quản lý nút
WVP hỗ trợ một WVP với nhiều ZLM để mở rộng khả năng đồng thời của video WVP. Việc đồng thời phát lại video là do băng thông và hiệu suất, một nút ZLM đơn lẻ chỉ có thể hỗ trợ một số lượng kết nối hạn chế, vì vậy WVP đã thêm cụm ZLM để mở rộng khả năng đồng thời và đảm bảo tính khả dụng cao của ZLM.
## Nút mặc định
Trong WVP, để đảm bảo tính toàn vẹn của chức năng, ít nhất phải có một nút ZLM mặc định. Nút này không được thêm vào trang quản lý mà được cấu hình trong tệp cấu hình của WVP. Nút này không thể bị xóa trên trang. Mỗi lần khởi động sẽ tự động đọc cấu hình từ tệp cấu hình và ghi vào cơ sở dữ liệu để dự phòng.
## Thêm nút mới
Khởi động nút zlm mà bạn muốn thêm, sau đó nhấp vào nút "Thêm nút" và nhập ip của zlm, cổng http, SECRET. Nhấp vào kiểm tra, sau khi kiểm tra hoàn tất, bạn có thể bắt đầu cấu hình chi tiết cho nút. Nếu zlm của bạn được khởi động bằng docker, có thể có trường hợp cổng zlm sử dụng không khớp với cổng của máy chủ, cần cấu hình từng cổng một tại đây.
## Nguyên lý sử dụng nhiều nút của wvp
wvp sẽ ghi lại các nút kết nối trong redis và ghi lại tình trạng tải của zlm. Khi có yêu cầu mới đến, nó sẽ lấy zlm có tải thấp nhất để sử dụng. Điều này đảm bảo cân bằng tải cho các nút.