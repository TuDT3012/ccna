# sự khác nhau về ip public và ip private
### 1. IP public
- Địa chỉ IP public là địa chỉ được gán cho thiết bị điện toán để cho phép truy cập trực tiếp qua Internet. Một máy chủ web, máy chủ email và bất kỳ thiết bị máy chủ nào có thể truy cập trực tiếp từ Internet là ứng cử viên cho một địa chỉ IP public. Địa chỉ IP public là duy nhất trên toàn cầu và chỉ có thể được gán cho một thiết bị duy nhất.
### 2. IP private
- Địa chỉ IP riêng là không gian địa chỉ được phân bổ bởi InterNIC để cho phép các tổ chức tạo mạng riêng của họ. Có ba khối IP (1 lớp A, 1 lớp B và 1 lớp C) dành riêng cho sử dụng riêng. Các máy tính, máy tính bảng và điện thoại thông minh ngồi sau nhà bạn và các máy tính cá nhân trong một tổ chức thường được gán địa chỉ IP riêng. Một máy in mạng trong nhà bạn được chỉ định một địa chỉ riêng để chỉ gia đình bạn có thể in ra máy in cục bộ của bạn.
- http://prntscr.com/mo7x4t
- Khi một máy tính được gán một địa chỉ IP riêng, các thiết bị cục bộ sẽ nhìn thấy máy tính này thông qua địa chỉ IP riêng đó. Tuy nhiên, các thiết bị nằm ngoài mạng cục bộ của bạn không thể giao tiếp trực tiếp qua địa chỉ IP riêng mà sử dụng địa chỉ IP công cộng của bộ định tuyến để liên lạc. Để cho phép truy cập trực tiếp vào thiết bị cục bộ được gán địa chỉ IP riêng, nên sử dụng Trình dịch địa chỉ mạng (NAT).
=> **Tóm lại**: - **IP Public** còn được gọi là IP công cộng, nhiều Server/VPS dùng IP Public thì tạo thành dải mạng Public Network
**IP Private** gọi là IP riêng, nhiều IP Private tao thành dải mạng Private Network. Nhiều người còn gọi lại IP LAN, IP Localhost.
+ tuy khác nhau nhưng chúng được gọi chung là **IPV4**
# tcp và http protocol
- **TCP/IP** là viết tắt của **Transmission Control Protocol / Internet Protocol** và dùng để chỉ 1 số giao thức . Và phần **IP** của giao thức là viết tắt của **Internet protocol**  được TCP và UDP sử dụng để vận chuyển từ mạng này sang mạng khác, hãy tưởng tượng **IP** như một đường cao tốc cho phép các giao thức này tìm đường đi đến các máy tính khác.
- TCP và UDP là "xe tải" trên đường cao tốc và "tải" mà chúng đang mang là các giao thức như HTTP, FTP, ...
- Mặc dù cả TCP và UDP đều được sử dụng để vận chuyển các giao thức khác, chúng có một điểm khác biệt đáng kể; TCP cung cấp vận chuyển dữ liệu được đảm bảo, trong khi UDP thì không. Điều này có nghĩa là TCP có một cơ chế đặc biệt đảm bảo dữ liệu được truyền an toàn mà không có lỗi từ điểm này sang điểm khác, trong khi UDP không cung cấp bất kỳ bảo hiểm nào như vậy.
- ** HTTP (HyperText Transfer Protocol)** là giao thức sử dụng TCP để truyền thông tin của nó giữa các máy tính (thường là máy chủ Web và máy khách). Máy khách tạo một yêu cầu HTTP đến máy chủ Web bằng trình duyệt Web và máy chủ Web sẽ gửi thông tin được yêu cầu (trang web) đến máy khách.
=> **Lưu ý ** : IP là cần thiết để kết nối tất cả các mạng; TCP là một cơ chế cho phép chúng ta truyền dữ liệu một cách an toàn; và HTTP, sử dụng TCP để truyền dữ liệu của nó, là một giao thức cụ thể được sử dụng bởi các máy chủ và máy khách Web.
