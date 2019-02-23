# Config Ipv4

### 1. sơ đồ mạng 
- <img src="http://prntscr.com/mp3b93">
### 2. config router
- Ta tiến tới giao diện config của router
-<img src="https://prnt.sc/mp3c73">
- chuyển sang chế độ configure terminal (Conf)
- ta vào cổng f0/0 và đặt ip theo câu lệnh
- <img src="http://prntscr.com/mp3d8r">
- nhớ gõ câu lệnh **no shut**  để cổng chuyển trạng thái hoạt động 
- để chắc chắn ta gõ câu lệnh ** Show ip**
- <img src="http://prntscr.com/mp3e3c">
 ### 3. config switch layer 3
- Ta vào bảng config và  chế độ configure terminal và cấu hình tương tự nhưng có thêm câu no switchport vì nết không nhập câu này switch sẽ  tự động bật tính năng mode switch của cổng 
- <img src="http://prntscr.com/mp3evv">
### 4. config ipv4 trên máy tính 
- sẽ có 2 loại ip được config trên máy tính đó là ip động và tĩnh 
- ip động thì máy tính sẽ tự động nhận ip do dhcp cấp
- còn ip tĩnh thì mình phải tự config bằng tay
### 5. Một số lỗi thường gặp khi cấu hình mạng
- Đặt subnet mask sai và địa chỉ ip sai: xem lại cấu hình và cấu hình lại
- cấu hình nhưng không ping được với nhau : kiểm tra lại kết nối và đường mạng 
- không đặt được ip trên switch layer 3 , kiểm tra xem có phải thiếu câu lênh no switchport
