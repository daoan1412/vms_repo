# Nền tảng video giao thức 28181 sẵn sàng sử dụng

[![Build Status](https://travis-ci.org/xia-chu/ZLMediaKit.svg?branch=master)](https://travis-ci.org/xia-chu/ZLMediaKit)
[![license](http://img.shields.io/badge/license-MIT-green.svg)](https://github.com/xia-chu/ZLMediaKit/blob/master/LICENSE)
[![JAVA](https://img.shields.io/badge/language-java-red.svg)](https://en.cppreference.com/)
[![platform](https://img.shields.io/badge/platform-linux%20|%20macos%20|%20windows-blue.svg)](https://github.com/xia-chu/ZLMediaKit)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-yellow.svg)](https://github.com/xia-chu/ZLMediaKit/pulls)

WEB VIDEO PLATFORM là một nền tảng video mạng sẵn sàng sử dụng dựa trên tiêu chuẩn GB28181-2016, chịu trách nhiệm thực hiện tín hiệu cốt lõi và phần quản lý thiết bị, hỗ trợ NAT xuyên qua, hỗ trợ kết nối IPC, NVR của các thương hiệu Hikvision, Dahua, Uniview. Hỗ trợ liên kết tiêu chuẩn quốc gia, hỗ trợ chuyển tiếp camera/luồng trực tiếp/luồng phát trực tiếp không có chức năng tiêu chuẩn quốc gia sang các nền tảng tiêu chuẩn quốc gia khác.
Dịch vụ truyền thông dựa trên @夏楚 ZLMediaKit [https://github.com/ZLMediaKit/ZLMediaKit](https://github.com/ZLMediaKit/ZLMediaKit)   
Trình phát sử dụng @dexter jessibuca [https://github.com/langhuihui/jessibuca/tree/v3](https://github.com/langhuihui/jessibuca/tree/v3)  
Trang web phía trước dựa trên @Kyle MediaServerUI [https://gitee.com/kkkkk5G/MediaServerUI](https://gitee.com/kkkkk5G/MediaServerUI) đã được chỉnh sửa.

# Ứng dụng:
Hỗ trợ phát video camera trên trình duyệt mà không cần plugin.
Hỗ trợ kết nối thiết bị tiêu chuẩn quốc gia (camera, nền tảng, NVR, v.v.)
Hỗ trợ kết nối thiết bị không tiêu chuẩn quốc gia (onvif, rtsp, rtmp, thiết bị phát trực tiếp, v.v.), tận dụng tối đa. 
Hỗ trợ liên kết tiêu chuẩn quốc gia. Liên kết đa nền tảng. Xem trước video qua mạng.
Hỗ trợ kết nối nền tảng qua mạng.

# Tài liệu
Tài liệu sử dụng wvp [https://doc.wvp-pro.cn](https://doc.wvp-pro.cn)  
Tài liệu sử dụng ZLM [https://github.com/ZLMediaKit/ZLMediaKit](https://github.com/ZLMediaKit/ZLMediaKit)
# Cộng đồng trả phí
[![Cộng đồng](doc/_media/shequ.png "shequ")](https://t.zsxq.com/0d8VAD3Dm)
> Thu phí để cung cấp dịch vụ tốt hơn và cũng là động lực lớn hơn cho tác giả. Người dùng tham gia vào nhóm sau ba ngày có thể nhắn tin riêng cho tôi để lại số WeChat, tôi sẽ thêm mọi người vào nhóm. Nếu không hài lòng trong ba ngày đầu tiên, bạn có thể yêu cầu hoàn tiền ngay lập tức, không cần lo lắng, bạn có thể thử miễn phí ba ngày.

# Kho đồng bộ gitee
https://gitee.com/pan648540858/wvp-GB28181-pro.git

# Ảnh chụp màn hình
![index](doc/_media/index.png "index.png")
![2](doc/_media/2.png "2.png")
![3](doc/_media/3.png "3.png")
![3-1](doc/_media/3-1.png "3-1.png")
![3-2](doc/_media/3-2.png "3-2.png")
![3-3](doc/_media/3-3.png "3-3.png")
![build_1](https://images.gitee.com/uploads/images/2022/0304/101919_ee5b8c79_1018729.png "2022-03-04_10-13.png")
# Tính năng 
- [X] Tích hợp giao diện web
- [X] Tương thích tốt
- [X] Hỗ trợ bản đồ điện tử, hỗ trợ kết nối hai hệ tọa độ WGS84 và GCJ02, tự động chuyển đổi sang hệ tọa độ phù hợp để hiển thị và phân phối
- [X] Kết nối thiết bị
  - [X] Xem trước video
  - [X] Hỗ trợ chuyển đổi luồng chính và luồng phụ
  - [X] Không giới hạn số lượng kết nối, số lượng thiết bị kết nối chỉ phụ thuộc vào hiệu suất máy chủ của bạn
  - [X] Điều khiển PTZ, điều khiển hướng thiết bị, phóng to, thu nhỏ
  - [X] Truy vấn vị trí đặt trước, sử dụng và cài đặt
  - [X] Truy vấn và phát lại video trên NVR/IPC, hỗ trợ phát lại và tải xuống theo thời gian chỉ định
  - [X] Tự động ngắt kết nối khi không có người xem, tiết kiệm băng thông
  - [X] Đồng bộ thông tin thiết bị video
  - [X] Giám sát trạng thái trực tuyến/ngoại tuyến
  - [X] Hỗ trợ xuất trực tiếp địa chỉ luồng RTSP, RTMP, HTTP-FLV, Websocket-FLV, HLS
  - [X] Hỗ trợ xem camera trực tiếp qua một địa chỉ luồng mà không cần đăng nhập hoặc gọi bất kỳ API nào
  - [X] Hỗ trợ hai chế độ truyền tín hiệu tiêu chuẩn quốc gia UDP và TCP
  - [X] Hỗ trợ hai chế độ truyền luồng tiêu chuẩn quốc gia UDP và TCP
  - [X] Hỗ trợ tìm kiếm, lọc kênh
  - [X] Hỗ trợ truy vấn thư mục con của kênh
  - [X] Hỗ trợ lọc âm thanh, ngăn chặn tiếng ồn ảnh hưởng đến việc xem
  - [X] Hỗ trợ đồng bộ thời gian mạng tiêu chuẩn quốc gia
  - [X] Hỗ trợ phát lại H264 và H265
  - [X] Xử lý thông tin cảnh báo, hỗ trợ đẩy thông tin cảnh báo đến phía trước
  - [X] Đàm thoại hai chiều
  - [X] Hỗ trợ phương pháp đăng ký và thông báo
    - [X] Đăng ký vị trí di chuyển
    - [X] Xử lý thông báo vị trí di chuyển
    - [X] Đăng ký sự kiện cảnh báo
    - [X] Xử lý thông báo sự kiện cảnh báo
    - [X] Đăng ký danh mục thiết bị
    - [X] Xử lý thông báo danh mục thiết bị
  -  [X] Truy vấn và hiển thị vị trí di chuyển
  - [X] Hỗ trợ thêm thiết bị thủ công và đặt mật khẩu riêng cho thiết bị
-  [X] Hỗ trợ kết nối nền tảng
-  [X] Hỗ trợ liên kết tiêu chuẩn quốc gia
  - [X] Kênh tiêu chuẩn quốc gia liên kết lên cấp trên
    - [X] Thêm nền tảng cấp trên qua WEB
    - [X] Đăng ký
    - [X] Giữ kết nối
    - [X] Lựa chọn kênh
    - [X] Đẩy kênh
    - [X] Phát lại
    - [X] Điều khiển PTZ
    - [X] Truy vấn trạng thái nền tảng
    - [X] Truy vấn thông tin nền tảng
    - [X] Khởi động từ xa nền tảng
    - [X] Thư mục ảo tùy chỉnh cho mỗi nền tảng liên kết
    - [X] Đăng ký và thông báo danh mục
    - [X] Xem và phát lại video
    - [X] Đăng ký và thông báo GPS (phát trực tiếp)
    - [X] Đàm thoại hai chiều
- [X] Hỗ trợ cấu hình tự động dịch vụ truyền thông ZLM, giảm thiểu các vấn đề do cấu hình sai;  
- [X] Nhiều nút truyền thông, tự động chọn nút có tải thấp nhất để sử dụng.
- [X] Hỗ trợ chế độ nhiều cổng UDP, cải thiện hiệu suất truyền thông UDP;
- [X] Hỗ trợ triển khai công khai; 
- [X] Hỗ trợ triển khai riêng biệt wvp và zlm, nâng cao khả năng xử lý đồng thời của nền tảng
- [X] Hỗ trợ kéo luồng RTSP/RTMP, phân phối thành các định dạng luồng khác nhau, hoặc đẩy sang các nền tảng tiêu chuẩn quốc gia khác
- [X] Hỗ trợ đẩy luồng RTSP/RTMP, phân phối thành các định dạng luồng khác nhau, hoặc đẩy sang các nền tảng tiêu chuẩn quốc gia khác
- [X] Hỗ trợ xác thực đẩy luồng
- [X] Hỗ trợ xác thực API
- [X] Ghi lại video trên đám mây, phát trực tiếp/đại lý/video tiêu chuẩn quốc gia đều có thể ghi lại trên máy chủ đám mây, hỗ trợ xem trước và tải xuống
- [X] Hỗ trợ đóng gói thành file thực thi jar và war
- [X] Hỗ trợ yêu cầu chéo miền, hỗ trợ triển khai tách biệt phía trước và phía sau
- [X] Hỗ trợ Mysql, Postgresql, Kingbase và các cơ sở dữ liệu khác
- [X] Hỗ trợ Onvif (hiện tại trên nhánh onvif, cần cài đặt dịch vụ onvif, dịch vụ có sẵn trên Knowledge Planet)
# Nội dung không mã nguồn mở
- [X] Hỗ trợ thiết bị Onvif, hỗ trợ yêu cầu, điều khiển PTZ, phân cấp quốc gia và yêu cầu tự động. Tại [Cộng đồng tri thức](https://t.zsxq.com/10WAnH2MP) có gói cài đặt thử nghiệm và hướng dẫn sử dụng, không giới hạn thời gian sử dụng. Nếu cần mã nguồn, có thể liên hệ qua tin nhắn riêng hoặc email.
- [X] Hỗ trợ chuẩn quốc gia 28181-2022, hỗ trợ truy vấn hành trình tuần tra, điều khiển PTZ chính xác, định dạng thẻ nhớ, nâng cấp phần mềm thiết bị, cấu hình OSD, h265+aac, hỗ trợ dòng phụ, phát ngược video, v.v. Danh sách tính năng cụ thể có thể xem tại [Cộng đồng tri thức](https://t.zsxq.com/18GXkpkqs). Nếu cần mã nguồn và thử nghiệm, có thể liên hệ qua tin nhắn riêng hoặc email.

# Giấy phép
Dự án này sử dụng giấy phép MIT, với mã nguồn có thể được tự do ứng dụng vào các dự án thương mại hoặc phi thương mại, miễn là giữ nguyên thông tin bản quyền. Tuy nhiên, dự án này cũng sử dụng một số mã nguồn mở khác, trong trường hợp sử dụng cho mục đích thương mại, hãy tự thay thế hoặc loại bỏ chúng; Các tranh chấp thương mại hoặc hành vi vi phạm pháp luật phát sinh từ việc sử dụng dự án này không liên quan đến dự án và nhà phát triển. Bạn cần tự chịu trách nhiệm pháp lý. Khi sử dụng mã nguồn dự án, bạn cũng nên thể hiện rõ giấy phép của các thư viện bên thứ ba mà dự án phụ thuộc vào.

# Hỗ trợ kỹ thuật  

Danh sách chuyên đề trên [Cộng đồng tri thức](https://t.zsxq.com/0d8VAD3Dm):
- [Hướng dẫn cơ bản 1: WVP-PRO có thể làm gì](https://t.zsxq.com/0dLguVoSp)

Hỗ trợ kỹ thuật trả phí, vui lòng gửi email đến 648540858@qq.com.

# Cảm ơn
Xin cảm ơn tác giả [Hạ Sở](https://github.com/xia-chu) đã cung cấp một framework dịch vụ truyền thông nguồn mở tuyệt vời và hỗ trợ trong quá trình phát triển.  
Cảm ơn tác giả [dexter langhuihui](https://github.com/langhuihui) đã mở mã một trình phát WEB rất hữu ích.  
Cảm ơn tác giả [Kyle](https://gitee.com/kkkkk5G) đã mở mã một trang web frontend rất tiện lợi.  
Cảm ơn tất cả những người đã đóng góp cho dự án thông qua các cách thức khác nhau như đóng góp mã nguồn, phản hồi lỗi, tài trợ tài chính, và sự hỗ trợ khác! Xin cảm ơn không phân biệt thứ tự.