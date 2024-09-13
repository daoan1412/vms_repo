<!-- 点播流程 -->

# Quy trình phát sóng
> Dưới đây là quy trình phát thanh cấp liên của WVP-PRO.

```
@startuml
"Platform cấp trên"  -> "Platform cấp dưới": 1. Gửi yêu cầu phát thanh
"Platform cấp trên" <--  "Platform cấp dưới": 2. 200OK
"Platform cấp trên" <- "Platform cấp dưới": 3. Trả lời Result OK
"Platform cấp trên" -->  "Platform cấp dưới": 4. 200OK

"Platform cấp dưới"  -> "Thiết bị": 5. Gửi yêu cầu phát thanh
"Platform cấp dưới" <--  "Thiết bị": 6. 200OK
"Platform cấp dưới" <- "Thiết bị": 7. Trả lời Result OK
"Platform cấp dưới" -->  "Thiết bị": 8. 200OK

"Platform cấp dưới"  <- "Thiết bị": 9. invite(broadcast)
"Platform cấp dưới"  --> "Thiết bị": 10. 100 trying
"Platform cấp dưới"  --> "Thiết bị": 11. 200OK SDP
"Platform cấp dưới"  <-- "Thiết bị": 12. ack

"Platform cấp trên"  <- "Platform cấp dưới": 13. invite(broadcast)
"Platform cấp trên"  --> "Platform cấp dưới": 14. 100 trying
"Platform cấp trên"  --> "Platform cấp dưới": 15. 200OK SDP
"Platform cấp trên"  <-- "Platform cấp dưới": 16. ack

"Platform cấp trên"  -> "Platform cấp dưới": 17. Đẩy RTP
"Platform cấp dưới"  -> "Thiết bị": 18. Đẩy RTP

@enduml
```

##  Mô tả quy trình đăng ký như sau:
1. Người dùng từ trang web hoặc gọi giao diện để gửi yêu cầu phát sóng;
2. WVP-PRO gửi tin nhắn Invite đến camera, trong tiêu đề tin nhắn có chứa trường Subject, biểu thị ID nguồn video phát sóng, số thứ tự luồng phương tiện của người gửi, IP sử dụng để nhận luồng của ZLMediaKit, số thứ tự luồng phương tiện của người nhận, v.v., trong phần thân tin nhắn SDP, trường s là “Play” đại diện cho phát sóng trực tiếp, trường y mô tả giá trị SSRC, trường f mô tả các tham số phương tiện.
3. Camera trả lời WVP-PRO bằng 200OK, trong phần thân tin nhắn mô tả IP, cổng, định dạng phương tiện, trường SSRC của người gửi phương tiện.
4. WVP-PRO trả lời thiết bị bằng Ack, phiên làm việc được thiết lập thành công.
5. Thiết bị gửi luồng trực tiếp đến ZLMediaKit.
6. ZLMediaKit gửi sự kiện thay đổi luồng đến WVP-PRO.
7. WVP-PRO trả lời người dùng WEB bằng địa chỉ phát sóng.
8. ZLMediaKit gửi sự kiện không có người xem luồng đến WVP.
9. WVP-PRO trả lời thiết bị bằng Bye, kết thúc phiên làm việc.
10. Thiết bị trả lời bằng 200OK, kết thúc phiên làm việc thành công.