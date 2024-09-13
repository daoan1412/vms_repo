# \[Quy tắc mã hóa thống nhất\]

## D.1 Quy tắc mã hóa A
>&emsp;&emsp;Quy tắc mã hóa A bao gồm mã trung tâm (8 ký tự), mã ngành (2 ký tự), mã loại (3 ký tự) và số thứ tự (7 ký tự), tổng cộng 20 ký tự số thập phân, tức là mã hệ thống = mã trung tâm + mã ngành + mã loại + số thứ tự.  
>&emsp;&emsp;Chi tiết về quy tắc mã hóa A được mô tả trong bảng D.1. Trong đó, mã trung tâm là mã của trung tâm giám sát mà người dùng hoặc thiết bị thuộc về, được xác định theo mã khu vực hành chính nơi trung tâm giám sát đặt trụ sở. Khi không phải là đơn vị cơ sở, các vị trí trống sẽ được điền bằng số 0. Mã khu vực hành chính được sử dụng theo quy định của GB/T2260—2007. Mã ngành là mã của ngành mà người dùng hoặc thiết bị thuộc về, bảng đối chiếu mã ngành được mô tả trong bảng D.3. Mã loại xác định loại cụ thể của thiết bị hoặc người dùng, trong đó thiết bị đầu cuối bao gồm thiết bị đầu cuối của hệ thống công an và thiết bị đầu cuối không thuộc hệ thống công an, người dùng cuối bao gồm người dùng cuối của hệ thống công an và người dùng cuối không thuộc hệ thống công an.   

| Mã đoạn   | Mã vị trí | Hàm ý                                  | Giá trị giải thích                                                                                        |
|----------|-----------|-----------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Trung tâm mã | 1, 2       | Mã cấp tỉnh                           | Được quy định bởi mã hành chính của khu vực mà trung tâm giám sát đặt trụ sở, phù hợp với yêu cầu GB/T 2260–2007 |
|          | 3, 4       | Mã cấp thành phố                        |                                                                                                           |
|          | 5, 6       | Mã cấp khu vực                          |                                                                                                           |
|          | 7, 8       | Mã đơn vị kết nối cơ sở                 |                                                                                                           |
| Mã ngành | 9, 10      | Mã ngành                               | Mã ngành đối chiếu với bảng D.3                                                                           |
|          | 111~130    | Hiển thị loại hình là thiết bị đầu cuối |                                                                                                           |
| Loại mã  | 11, 12, 13 | Loại thiết bị                           |                                                                                                           |
|          | 111        | Mã DVR                                  |                                                                                                           |
|          | 112        | Mã máy chủ video                        |                                                                                                           |
|          | 113        | Mã nén video                            |                                                                                                           |
|          | 114        | Mã giải nén video                       |                                                                                                           |
|          | 115        | Mã chuyển đổi video analog số           |                                                                                                           |
|          | 116        | Mã chuyển đổi số video analog           |                                                                                                           |
|          | 117        | Mã điều khiển báo động                  |                                                                                                           |
|          | 118        | Mã đầu ghi hình mạng (NVR)              |                                                                                                           |
|          | 119        | Mã máy ghi hình số hỗn hợp (HVR)        |                                                                                                           |
|          | 120        | Mã thiết bị mở rộng tín hiệu            |                                                                                                           |
|          | 131~199    | Hiển thị loại hình là thiết bị ngoại vi  |                                                                                                           |
|          | 131        | Mã camera                               |                                                                                                           |
|          | 132        | Mã camera mạng (IPC)                    |                                                                                                           |
|          | 133        | Mã hệ thống báo động                    |                                                                                                           |
|          | 134        | Mã hệ thống báo động (như hồng ngoại, khói, cảm biến cửa, v.v.) |                                                                                                           |


| Mã đoạn   | Mã vị trí | Hàm ý                                      | Giá trị giải thích                                                                                      |
|----------|-----------|---------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Loại mã  | 131~199    | Hiển thị loại hình là thiết bị ngoại vi đầu cuối |                                                                                                         |
|          | 135        | Mã thiết bị đầu ra hệ thống báo động (như đèn báo, còi báo động)                                                         |
|          | 136        | Mã thiết bị đầu vào âm thanh                                                                                           |
|          | 137        | Mã thiết bị âm thanh                                                                                                   |
|          | 138        | Mã thiết bị đầu ra di động                                                                                            |
|          | 139        | Mã các thiết bị ngoại vi khác                                                                                          |
|          | 140~199    | Mã mở rộng cho các thiết bị ngoại vi                                                                                   |
|          | 200        | Mã hệ thống dịch vụ hoàn chỉnh trung tâm giám sát                                                                      |
|          | 201        | Mã dịch vụ ứng dụng Web                                                                                                |
|          | 202        | Mã dịch vụ đa phương tiện                                                                                              |
|          | 203        | Mã dịch vụ đại lý                                                                                                      |
|          | 204        | Mã dịch vụ bảo mật                                                                                                     |
|          | 205        | Mã dịch vụ cảnh báo                                                                                                    |
|          | 206        | Mã dịch vụ GIS                                                                                                         |
|          | 207        | Mã dịch vụ quản lý                                                                                                     |
|          | 208        | Mã dịch vụ tiếp xúc người dùng                                                                                         |
|          | 209        | Mã dịch vụ đa phương tiện                                                                                              |
|          | 210        | Mã hệ thống mạng an toàn                                                                                               |
|          | 211        | Mã dịch vụ bảo mật Internet                                                                                           |
|          | 212~214    | Mã hệ thống nền tảng mở rộng                                                                                           |
|          | 215        | Mã dịch vụ chia sẻ                                                                                                     |
|          | 216        | Mã dịch vụ nền tảng ảo hóa                                                                                             |
|          | 300        | Mã trung tâm người dùng                                                                                                |
|          | 301~343    | Mã nhân vật trong ngành                                                                                               |
|          | 344~399    | Mã hệ thống người dùng mở rộng                                                                                         |
|          | 400~499    | Mã dành cho người dùng cuối cùng                                                                                       |
|          | 500~599    | Mã thiết bị mạng hệ thống giám sát video                                                                              |
|          | 600~999    | Mã thiết bị mở rộng                                                                                                   |


| Mã đoạn     | Mã vị trí | Hàm ý                       | Giá trị giải thích                                                                                               |
|-------------|-----------|-----------------------------|------------------------------------------------------------------------------------------------------------------|
| Mã mạng     | 14        | Mã nhận dạng mạng           | 0, 1, 2, 3, 4 là mạng giám sát điều khiển chuyên dụng, 5 là mạng thông tin an ninh công cộng, 6 là mạng dịch vụ, 7 là mạng Internet, 8 là mạng kết nối tài nguyên xã hội, 9 dự trữ |
| Số thứ tự   | 15~20     | Mã số thiết bị hoặc mã số người dùng |                                                                                                                  |


## D.2 Quy tắc mã hóa B
>&emsp;&emsp;Quy tắc mã hóa B bao gồm mã trung tâm (8 ký tự), mã ngành (2 ký tự), số thứ tự (4 ký tự) và mã loại (2 ký tự), tổng cộng 16 ký tự, tức là mã hệ thống = mã trung tâm + mã ngành + số thứ tự + mã loại. Chi tiết về quy tắc mã hóa B được mô tả trong bảng D.2.

| Mã đoạn     | Mã vị trí  | Hàm ý                              | Giá trị giải thích                                                                                  |
|-------------|------------|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Trung tâm mã | 1, 2       | Mã cấp tỉnh                         | Được quy định bởi mã hành chính của khu vực mà trung tâm giám sát đặt trụ sở, phù hợp với yêu cầu GB/T 2260–2007 |
|             | 3, 4        | Mã cấp thành phố                    |                                                                                                     |
|             | 5, 6        | Mã cấp khu vực                      |                                                                                                     |
|             | 7, 8        | Mã đơn vị kết nối cơ sở             |                                                                                                     |
| Mã ngành    | 9, 10       | Mã ngành                           | Mã ngành đối chiếu với bảng D.3                                                                     |
| Số thứ tự   | 11~16       | Mã thiết bị hoặc mã số người dùng   |                                                                                                     |
| Loại mã     | 17, 18      | Mã loại thiết bị                    |                                                                                                     |
|             |             | Thiết bị âm thanh và video số (00~19) |                                                                                                     |
|             | 00          | Thiết bị video số (không có bộ nhớ cục bộ)                                                                      |
|             | 01          | Thiết bị ghi hình video số (có bộ nhớ cục bộ)                                                                  |
|             | 02          | Thiết bị đầu ghi số                                                                                           |
|             | 03~19       | Dự trữ (Thiết bị âm thanh số)                                                                                 |
|             |             | Thiết bị máy chủ (20~39)            |                                                                                                     |
|             | 20          | Máy chủ mạng giám sát video                                                                                  |
|             | 21          | Máy chủ video                                                                                                 |
|             | 22          | Máy chủ ứng dụng Web                                                                                          |
|             | 23          | Máy chủ quản lý ghi hình                                                                                      |
|             | 24~39       | Dự trữ (Thiết bị máy chủ)                                                                                     |
|             |             | Thiết bị số khác (40~59)            |                                                                                                     |
|             | 40          | Ma trận giám sát mạng                                                                                         |
|             | 41          | Bộ điều khiển giám sát                                                                                       |
|             | 42          | Công tắc mạng                                                                                                 |
|             | 43~59       | Dự trữ (Thiết bị số khác)                                                                                     |


| Mã đoạn     | Mã vị trí  | Hàm ý                                          | Giá trị giải thích                                             |
|-------------|------------|-------------------------------------------------|---------------------------------------------------------------|
| Loại mã     | 17, 18     | Mã loại thiết bị                                |                                                               |
|             |            | Thiết bị âm thanh và video analog (60~74)       |                                                               |
|             | 60         | Máy quay analog                                 |                                                               |
|             | 61         | Ma trận video analog                            |                                                               |
|             | 62~74      | Dự trữ (Thiết bị âm thanh và video analog)      |                                                               |
|             |            | Thiết bị analog khác (75~89)                    |                                                               |
|             | 75         | Bộ điều khiển analog                            |                                                               |
|             | 76         | Máy ghi hình analog                             |                                                               |
|             | 77~89      | Dự trữ (Thiết bị analog khác)                   |                                                               |
|             |            | Người dùng (90~99)                              |                                                               |
|             | 90         | Quản lý hệ thống                                |                                                               |
|             | 91         | Quản trị viên hệ thống                          |                                                               |
|             | 92         | Người dùng cấp cao                              |                                                               |
|             | 93         | Người dùng phổ thông                            |                                                               |
|             | 94         | Người dùng duyệt                               |                                                               |
|             | 95         | Người dùng có quyền                             |                                                               |
|             | 96~99      | Dự trữ                                           |                                                               |


## D.3 Bảng đối chiếu mã ngành
>&emsp;&emsp;Bảng đối chiếu mã ngành được mô tả trong bảng D.3.  

| Loại tiếp nhận | Mã loại | Tên gọi                     | Chủ thể xây dựng           | Ghi chú                                                                |
|----------------|---------|-----------------------------|----------------------------|-------------------------------------------------------------------------|
| 00             | 00      | Người tiếp nhận an ninh xã hội đường phố | Cơ quan chính phủ           | Bao gồm đường phố thành phố, khu thương mại, khu vực công cộng, khu vực trọng điểm, v.v. |
| 01             | 01      | Người tiếp nhận an ninh xã hội khu cộng đồng |                            | Bao gồm khu vực cộng đồng, tòa nhà, mạng lưới, v.v.                      |
| 02             | 02      | Người tiếp nhận an ninh xã hội nội bộ   |                            | Bao gồm văn phòng công an, cơ quan lưu trữ, v.v.                          |
| 03             | 03      | Người tiếp nhận an ninh xã hội khác    |                            |                                                                         |
| 04             | 04      | Người tiếp nhận giao thông đường bộ    |                            | Bao gồm đường cao tốc, đường quốc lộ, giám sát điều kiện giao thông trên các tuyến chính |
| 05             | 05      | Người tiếp nhận tại các trạm giao thông |                            | Bao gồm các đường giao thông, “cảnh sát điện tử”, các trạm thu phí, cổng giao thông, v.v. |
| 06             | 06      | Người tiếp nhận tại các khu vực giao thông khác |                            | Bao gồm các văn phòng cơ quan quản lý giao thông                         |
| 07             | 07      | Người tiếp nhận khác trong lĩnh vực giao thông |                            |                                                                         |
| 08             | 08      | Người tiếp nhận quản lý đô thị          |                            |                                                                         |
| 09             | 09      | Người tiếp nhận vệ sinh môi trường      |                            |                                                                         |
| 10             | 10      | Người tiếp nhận lĩnh vực thương mại     |                            |                                                                         |
| 11             | 11      | Người tiếp nhận trong ngành giáo dục    |                            |                                                                         |
| 12~39          |         | Dự trữ 1                             |                            |                                                                         |



| Mã loại tiếp nhận | Tên gọi                           | Chủ thể xây dựng      | Ghi chú      |
|-------------------|-----------------------------------|-----------------------|--------------|
| 40                | Tiếp nhận doanh nghiệp nông lâm mục|                       |              |
| 41                | Tiếp nhận doanh nghiệp khai khoáng |                       |              |
| 42                | Tiếp nhận doanh nghiệp sản xuất    |                       |              |
| 43                | Tiếp nhận doanh nghiệp luyện kim  |                       |              |
| 44                | Tiếp nhận doanh nghiệp điện lực   |                       |              |
| 45                | Tiếp nhận doanh nghiệp khí đốt    |                       |              |
| 46                | Tiếp nhận doanh nghiệp xây dựng   |                       |              |
| 47                | Tiếp nhận doanh nghiệp logistics  |                       |              |
| 48                | Tiếp nhận doanh nghiệp bưu chính  |                       |              |
| 49                | Tiếp nhận doanh nghiệp thông tin  |                       |              |
| 50                | Tiếp nhận doanh nghiệp lưu trú và ẩm thực |             |              |
| 51                | Tiếp nhận doanh nghiệp tài chính  |                       |              |
| 52                | Tiếp nhận doanh nghiệp bất động sản|                       |              |
| 53                | Tiếp nhận doanh nghiệp dịch vụ thương mại |             |              |
| 54                | Tiếp nhận doanh nghiệp thủy lợi   |                       |              |
| 55                | Tiếp nhận doanh nghiệp giải trí   |                       |              |
| 56~79             | Xây dựng tự do của cư dân         | Dự trữ 2              |              |
| 80~89             | Xây dựng tự do của cư dân         | Dự trữ 3              |              |
| 90~99             | Chủ thể khác                      | Dự trữ 4              |              |

