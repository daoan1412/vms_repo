<!-- 启动时报错 -->
Khi khởi động gặp lỗi, phần lớn là do cấu hình của bạn có vấn đề, ví dụ như mysql không kết nối được, redis không kết nối được, cổng 18080/15060 bị chiếm dụng, những điều này đều sẽ dẫn đến lỗi khi khởi động, sau khi sửa cấu hình đều có thể giải quyết;
Dưới đây là một số lỗi thường gặp, mọi người có thể đối chiếu để kiểm tra đơn giản.

> **Lỗi thường gặp**  

![_media/img.png](_media/img.png)
**Nguyên nhân lỗi:** Cấu hình redis sai, có thể do: redis chưa khởi động/ip sai/cổng sai/mạng không thông  
---
![_media/img_1.png](_media/img_1.png)
**Nguyên nhân lỗi:** Cấu hình redis sai, có thể do: mật khẩu sai
---
![_media/img_2.png](_media/img_2.png)
**Nguyên nhân lỗi:** Cấu hình mysql sai, có thể do: mysql chưa khởi động/ip sai/cổng sai/mạng không thông  
---
![_media/img_3.png](_media/img_3.png)
**Nguyên nhân lỗi:** Cấu hình mysql sai, có thể do: tên người dùng/mật khẩu sai
---
![_media/img_4.png](_media/img_4.png)
**Nguyên nhân lỗi:** Cấu hình SIP sai, có thể do: cổng SIP bị chiếm dụng
---
![_media/img_5.png](_media/img_5.png)
**Nguyên nhân lỗi:** Cấu hình cổng WVP Tomcat sai, có thể do: cổng server.port bị chiếm dụng
---
