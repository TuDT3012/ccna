# Vlan subnet mask ipv4
- <img src="http://prntscr.com/moorsd">


### 1. Subnet mask
- **Subnet mask (Subnetting)** hay mặt nạ mạng (theo cách hiểu tiếng Việt), là kỹ thuật sử dùng để xác định một địa chỉ IP thuộc lớp mạng nào hay thuộc một phân đoạn mạng (mạng con) nào và thuộc miền Broadcast nào. Như trong bài trước về phần địa chỉ ipv4 chúng ta đã biết địa này sử dụng 32 bit nhị phân hia thành 4 octet, IPv4 sẽ có hai phần là Network ID và Host ID. Theo tiêu chuẩn, mặc định thì phần Network ID của các lớp A, B và C lần lượt là 8 bit, 16 bit và 24 bit. Ở Subnet Mask các bit trong phần Network ID đều được bật lên 1. Dưới đây là bảng biểu diển các lớp địa chỉ mặc định khi biểu diển thành bit nhị phân và nhóm thành các nhóm 8 bit quy đổi thành số thập phân tương ứng.
- **Bên cạnh default subnet mask, người ta còn tiến hành chia mạng con với 2 lý do**:
		 -   Tiết kiệm và tối ưu hóa việc cấp địa chỉ IP. Ta lấy một ví dụ như sau: với các default subnet mask của lớp A có thể cung cấp 16 triệu địa chỉ, lớp B cung cấp 64 nghìn địa chỉ và lớp C với 254 địa chỉ trên mỗi mạng. Xong nếu một mạng bất kỳ có hơn 254 thiết bị và nó cần lấy một mạng thuộc lớp B để cấp phát IP nhưng việc này sẽ làm lãng phí hàng chục nghìn địa chỉ IP. Để giải quyết vấn đề, người ta sẽ phải phân chia subnet để có thể sử dụng tối ưu địa chỉ trong lớp B.
		 -   Cắt nhỏ miền quảng bá (Broadcast Domain), tối ưu hóa lưu lượng mạng và nâng cao hiệu năng của hệ thống mạng. Nếu bạn có một hệ thống mạng bao gồm hàng ngàn máy tính được kết nối với nhau, đối với mạng TCP/IP thì việc kết nối các máy tính và thiết bị cùng một Network ID thì cũng đầu nghĩa bạn sẽ phải kết nối chúng vào chung một hạ tầng vật lý duy nhất (Switch), việc này có nghĩa là hạ tầng này sẽ phải gánh tất cả các lưu lượng mạng rất lớn. Để giải quyết vấn đề này người ta sẽ chia nhỏ thành các mạng con (subnet) và sử dụng các thiết bị định tuyết (router) để cắt nhỏ các broadcast domain.
		  <img src="http://prntscr.com/moouis">
	-Như trong hình trên, chúng ta có thể thấy rằng ở mô hình đầu tiên là mô hình sử dụng lớp mạng B với default subnet mask, ở mô hình thứ hai là mô hình đã được chia mạng con (Subnet).
### 2. cách chia mạng con 
- Như chúng ta đã biết, địa chỉ IP có hai phần là Network ID và Host ID. Mặc định Network ID của các lớp A, B và C lần lượt là 8 bit, 16 bit và 24 bit, phần còn lại sẽ là Host ID, việc chia mạng con sẽ mượn thêm các bit ở vùng Host ID để làm Network ID.
`[Thisislink](http://github.com)`  `<img src="http://prntscr.com/moow2d">`
Ta lấy theo ví dụ ở hai mô hình mạng bên trên, với mạng ban đầu lấy mạng 144.28.0.0 thuộc lớp B để thiết lập cho hệ thống mạng với 16 bit phần Network ID thì subnet mask là 255.255.0.0. Nhưng ở đây phát sinh một nhu cầu là chia nhỏ hệ thống mạng ra và vẫn sử dụng mạng này, ta mượn thêm 4 bit ở phần Host ID như vậy ta sẽ có 20 bit làm Network ID, khi đó subnet mask mới sẽ là 255.255.240.0.
<img src="http://prntscr.com/moowot">
- cách xác định địa chỉ ip thuộc mạng nào  : Như đã nói ở phần mở đầu, Subnet mask là kỹ thuật dùng để xác định một địa chỉ IP thuộc Network ID nào. Để giải quyết vấn đề này, người ta sẽ đổi địa chỉ IP và subnet mark của chúng thành nhị phân, sau đó sẽ dụng phép toán logic AND các bit của IP và subnet mask, kết quả của phép toán này chính là Network ID cần tìm.
