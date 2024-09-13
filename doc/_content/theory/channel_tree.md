# Cấu trúc cây của kênh

GB/T 28181 quy định hai cách tổ chức cây thiết bị
1. **Phân vùng hành chính**  
   Trong chế độ phân vùng hành chính, chủ yếu là sử dụng phân vùng hành chính làm nút thư mục, ví dụ: Tỉnh Hà Bắc -> Thành phố Hàm Đan -> Huyện Quảng Bình  
   ![_media/img_8.png](_media/img_8.png)  
2. **Nhóm nghiệp vụ**  
   Nhóm nghiệp vụ chủ yếu là một hình thức tổ chức cây thư mục tùy chỉnh, nhưng có một số yêu cầu nhất định đối với mã số quốc gia của thư mục được định nghĩa.  
   Cấp độ đầu tiên cần phải là loại nhóm nghiệp vụ, tức là mã quốc gia trong 11, 12, 13 là 215, ví dụ: 65010200002150000001;  
   Dưới nhóm nghiệp vụ là tổ chức ảo, tức là mã quốc gia trong 11, 12, 13 là 216, ví dụ: 65010200002160000002.  
   Dưới tổ chức ảo không thể là nhóm nghiệp vụ, dưới tổ chức ảo có thể tiếp tục thêm tổ chức ảo.  
   ![_media/img_9.png](_media/img_9.png)