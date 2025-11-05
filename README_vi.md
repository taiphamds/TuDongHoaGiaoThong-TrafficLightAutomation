# Tự động hóa giao thông bằng YOLO – Dự án cá nhân
Đặt vấn đề ở ngã tư đèn giao thông: khi mật độ giao thông dày đặc thì số giây mặc định là tầm 60s vì cân bằng giữa xả hết xe chính và không làm chậm hướng khác. Nhưng khi mật độ giao thông thưa thớt, đặt tình huống rằng bên kia chỉ 1 người chờ đèn đỏ mà số giây min vẫn tầm 20s => để tối ưu tôi đề suất thuật toán bỏ giây đèn đỏ và tính giây đèn xanh dựa trên trung bình cộng số lượng và loại phương tiện giao thông(xe máy: 3s, ô-tô: 4s, xe tải/buýt: 5s) của hai tuyến đường đối nhau đang chờ đèn đỏ. 

### Ví dụ:
tại ngã tư Đông-Tây-Nam-Bắc(Đông-Tây đối diện nhau, Nam-Bắc đối diện nhau), chu kỳ đèn là xanh, vàng, đỏ. 
Khi đèn xanh tại tuyến đường Bắc-Nam hết và chuyển vàng lúc đó camera tại tuyến đường Đông-Tây liền nhận diện/đếm số lượng người đang chờ đèn đỏ và tính số giây đèn xanh bằng trung bình cộng sớ lượng và loại phương tiện. Khi đèn xanh Đông-Tây hết và chuyển vàng tiếp tục đến camera tại đèn Bắc-Nam làm điều tương tự tiếp tục chu kỳ.

### Kết quả
https://github.com/user-attachments/assets/b390e1da-6e31-496d-8123-d4b302bb2c91

### Yolov8 
từ Huy Ngô https://www.kaggle.com/code/vhn1305/traffic-detection/output?select=yolov8n.pt
