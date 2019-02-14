## OSI
**Mô hình OSI** (_Open Systems Interconnection Reference Model_, viết ngắn là _OSI Model_ hoặc _OSI Reference Model_) - tạm dịch là **Mô hình tham chiếu** ***kết nối các hệ thống mở*** là một thiết kế dựa vào nguyên lý tầng cấp, lý giải một cách trừu tượng kỹ thuật kết nối truyền thông giữa các máy vi tính và thiết kế giao thức mạng giữa chúng. Mô hình này được phát triển thành một phần trong kế hoạch **kết nối các hệ thống mở** (_Open Systems Interconnection_) do IOS và IUT-T khởi xướng. Nó còn được gọi là **Mô hình bảy tầng của OSI**.
## 1. Mô hình OSI
- Gồm có 7 tầng lớp :
				- lớp application
				- Lớp Presentation
				- Lớp session
				- Lớp Transport
				- Lớp mạng Network
				- Lớp Data Link
				- Lớp vật lý Physical
## 2. Transport layer
- Lớp Transport hay lớp giao vận chịu trách nhiệm chuyển dữ liệu giữa các hệ thống đầu cuối hoặc máy chủ (host). Hệ điều hành Windows cho phép người dùng có thể chạy nhiều ứng dụng một cách đồng thời, chính vì vậy mà nhiều ứng dụng, và bản thân hệ điều hành cần phải truyền thông trên mạng đồng thời. Lớp Transport lấy dữ liệu từ mỗi ứng dụng và tích hợp tất cả dữ liệu đó vào trong một luồng. Lớp này cũng chịu trách nhiệm cho việc cung cấp vấn đề kiểm tra lỗi và thực hiện khôi phục dữ liệu khi cần thiết. Bản chất mà nói, lớp Transport chịu trách nhiệm cho việc bảo đảm tất cả dữ liệu được truyền từ máy gửi đến máy nhận.

Ví dụ về lớp Transport là SPX, TCP, UDP.
## 3. Network layer
- Lớp mạng Network là lớp có trách nhiệm quyết định xem dữ liệu sẽ đến máy nhận như thế nào. Lớp này nắm những thành phần như việc định địa chỉ, định tuyến, và các giao thức logic. Do loạt bài này dành cho những người mới bắt đầu làm quen với các kiến thức về mạng nên sẽ không đi chuyên sâu vào kỹ thuật, tuy nhiên chúng tôi nói qua rằng lớp mạng này tạo các đường logic được biết đến như các mạch ảo giữa máy nguồn và máy đích. Mạch ảo này cung cấp các gói dữ liệu riêng lẻ để chúng có thể đến được đích của chúng. Bên cạnh đó lớp mạng cũng chịu trách nhiệm cho việc quản lý lỗi của chính nó, cho việc điều khiển xếp chuỗi và điều khiển tắc nghẽn.

Việc sắp xếp các gói là rất cần thiết bởi mỗi một giao thức giới hạn kích thước tối đa của một gói. Số lượng dữ liệu phải được truyền đi thường vượt quá kích thước gói lớn nhất. Chính vì vậy mà dữ liệu được chia nhỏ thành nhiều gói nhỏ. Khi điều này xảy ra, lớp mạng sẽ gán vào mỗi gói nhỏ này một số thứ tự nhận dạng.

Khi dữ liệu này đến được máy tính người nhận thì lớp mạng lại kiểm tra số thứ nhận dạng của các gói và sử dụng chúng để sắp xếp dữ liệu đúng như những gì mà chúng được chia lúc trước từ phía người gửi, bên cạnh đó còn có nhiệm vụ chỉ ra gói nào bị thiếu trong quá trình gửi.

Nếu bạn chưa hiểu kỹ về khái niệm này, hãy hình dung rằng bạn cần gửi mail một tài liệu có dung lượng lớn đến một người bạn của mình, nhưng không có một phong bì đủ lớn. Để giải quyết vấn đề này thì bạn phải chia nhỏ một số trang vào các phong bì nhỏ, sau đó dán nhãn các phòng bì này lại để bạn của bạn có thể biết được thứ tự của các trang trong đó. Điều này cũng tương tự như những gì mà lớp mạng thực hiện.

Ví dụ về lớp Network là Apple Talk DDP, IP, IPX
