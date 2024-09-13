<!-- 电子地图 -->
# Bản đồ điện tử
WVP cung cấp một bản đồ điện tử đơn giản để định vị thiết bị và thông tin hành trình của thiết bị di động, bản đồ điện tử được phát triển dựa trên công cụ bản đồ mã nguồn mở openlayers.
### Xem định vị thiết bị
1. Có thể nhấn nút "Định vị" trong danh sách thiết bị, tự động chuyển đến trang bản đồ điện tử;
2. Trong trang bản đồ điện tử, nhấn chuột phải vào thiết bị và chọn "Định vị" để lấy vị trí của tất cả các kênh dưới thiết bị/nền tảng.
3. Nhấn vào thông tin kênh để định vị đến kênh cụ thể.

### Truy vấn hành trình thiết bị
Truy vấn hành trình cần cấu hình trước tùy chọn save-position-history để bật lưu trữ thông tin hành trình, hiện tại WVP chưa hỗ trợ phân chia cơ sở dữ liệu, không thể xử lý lượng lớn thông tin hành trình, nếu có nhu cầu vui lòng tự phát triển hoặc đặt hàng phát triển tùy chỉnh.
Trong trang bản đồ điện tử, nhấn chuột phải vào thiết bị và chọn "Truy vấn hành trình" để lấy thông tin hành trình của thiết bị.

PS: Bản đồ nền hiện tại chỉ dùng để trình diễn và học tập, trong trường hợp sử dụng thương mại vui lòng tự mua bản quyền sử dụng.

### Thay đổi bản đồ nền và cấu hình bản đồ nền
Hiện tại WVP hỗ trợ thay đổi bản đồ nền, tệp cấu hình nằm trong `web_src/static/js/config.js`, vui lòng sửa đổi và biên dịch lại tệp frontend.
```javascript
window.mapParam = {
  // Bật/tắt chức năng bản đồ
  enable: true,
  // Hệ tọa độ GCJ-02 WGS-84,
  coordinateSystem: "GCJ-02",
  // Địa chỉ ô bản đồ
  tilesUrl: "http://webrd0{1-4}.is.autonavi.com/appmaptile?x={x}&y={y}&z={z}&lang=zh_cn&size=1&scale=1&style=8",
  // Kích thước ô
  tileSize: 256,
  // Mức độ phóng đại mặc định
  zoom: 10,
  // Tọa độ trung tâm bản đồ mặc định
  center: [116.41020, 39.915119],
  // Mức độ phóng đại tối đa của bản đồ
  maxZoom: 18,
  // Mức độ phóng đại tối thiểu của bản đồ
  minZoom: 3
}