#  IPv4 (Unicast, Broadcast, Multi cast)
http://prntscr.com/mn96li


### 1. Unicast là gì ?? 
-  Địa chỉ **Unicast** được sử dụng để phân biệt các host đơn lẻ trên một mạng.  
-  Unicast là các nhóm địa chỉ IP thuộc các lớp  
A, B, C mà trong quá trình truyền và nhận  
dữ liệu chỉ xảy ra giữa hai điểm địa chỉ  
nguồn và địa chỉ đích. 
- Một địa chỉ Unicast cho phép thiết bị gửi dữ  
liệu đến một nơi nhận duy nhất.  
-  Chỉ cho phát tín hiệu từ một máy đến một  
máy.  
- Một host sẽ nhận tất cả các dữ liệu truyền từ một host nào đó.
 **Các dạng địa chỉ Unicast** 
1. Địa chỉ đặc biệt **(Special Address - SA)**  
0:0:0:0:0:0:0:0:0 viết gọn “::” là dạng địa chỉ không xác định, được sử dụng để  
xác nhận rằng hiện tại node không có địa chỉ, không bao giờ địa chỉ này được gắn  
cho giao diện hoặc sử dụng làm địa chỉ đích.  
0:0:0:0:0:0:0:1 hay “::1” địa chỉ xác định giao diện **loopback**, tương đương với  
địa chỉ 127.0.0.1 của IPv4. Các gói tin có địa chỉ đích ::1 không được gởi trên  
đường link hay forward đi bởi router. Phạm vi của địa chỉ này là phạm vi node.  
2. Địa chỉ Link Local (Link Local Adress - LLA)  
Sử dụng bởi các node khi giao tiếp với các node lân cận (Neighbor Node).  
Phạm vi của dạng địa chỉ Unicast này là trên một đường kết nối (phạm vi link).  
LLA luôn được cấu hình một cách tự động.  
Cấu trúc LLA  
LLA bắt đầu bởi 10 bit prefix là FE80::/10, tiếp theo là 54 bit 0, 64 bit còn lại là  
phần định danh giao diện (interface ID).  
LLA bắt đầu bởi 10 bit prefix là FE80::/10, tiếp theo là 54 bit 0, 64 bit còn lại là  
phần định danh giao diện (interface ID).
### 2. Broadcast là gì ?
http://prntscr.com/mn9b6x
- **Broadcast là** thuật ngữ được sử dụng **trong mạng** máy tính để mô tả cách thức truyền tin được gửi từ 1 điểm đến tất cả các điểm khác **trong** cùng một **mạng**. ... Do đó **broadcast** nên được giới hạn **trong** những phần riêng của **mạng**, và không được router chuyển tiếp.
- Mỗi máy nhận broadcast quyết định trong thẩm quyền của mình hoặc tiếp nhận thông điệp hoặc loại bỏ. Broadcast có trên nhiều tầng khác nhau của mô hình **OSI**
- Giao thức liên mạng **ipv4** cũng hỗ trợ kiểu truyền broadcast, cho phép các gói tin được gửi đến mọi thiết bị trong cùng 1 mạng.
- phiên bản **ipv6** không còn hỗ trợ giao thức truyền tin broadcast, Multicast được dùng để thay thế.
**Ứng dụng** : 
- Broadcast được sử dụng trong một mạng máy tính, trong số những thứ khác, khi của địa chỉ ip của máy nhận vẫn chưa được biết tới. Kỹ thuật này được sử dụng trong mô hình OSI ở tầng mạng
### 3. Multi cast là gì ?
http://prntscr.com/mn9h89
- Một số yêu cầu cần phải thực hiện để có thể đáp ứng được mục đích của multicast:  
	 + Phải có một dải địa chỉ dành riêng cho hoạt động Multicast.  
   + Các host muốn nhận lưu lượng Multicast nào thì phải được cài ứng dụng cho  
Multicast đó.
- Các host phải có một cơ chế báo hiệu cho router gần nhất (cùng subnet) là nó  
muốn nhận lưu lượng Multicast hoặc không muốn nhận lưu lượng này nữa.  
- Phải có các giao thức định tuyến Multicast để phân bổ thông tin Multicast một  
cách tối ưu qua một mạng định tuyến.  
- Phải có cơ chế tương quan địa chỉ IP – MAC dành riêng cho các địa chỉ  
Multicast trong Ethernet LAN.  
- Phải có cơ chế tối ưu việc phân bổ dữ liệu Multicast trên Ethernet LAN.  
- Dải địa chỉ dành riêng cho Multicast: 244.0.0.0 đến 239.255.255.255 (Lớp D)  
- IGMP – Internet Group Management Protocol: Version 1, Version 2, Version 3.
- OUI dành riêng cho Multicast 01-00-5e  
- CGMP, IGMP snooping, RGMP.  
- Định tuyến Multicast: PIM – DM, PIM – 5M, DVMRP, MOSPF.
- Địa chỉ Multicast đại diện cho ứng dụng Multicast và còn được gọi là địa chỉ  
nhóm Multicast.  
- Loại địa chỉ này không bao giờ được gán cho một thiết bị cụ thể và không bao  
giờ được phép là địa chỉ nguồn trong các gói tin.  
- IANA – Internet Assigned Numbers Authority đã quy định dải IP lớp D được sử dụng cho kỹ thuật Multicast 244.0.0.0 đến 239.255.255.255 (4 Bit đầu luôn là  
1110).
