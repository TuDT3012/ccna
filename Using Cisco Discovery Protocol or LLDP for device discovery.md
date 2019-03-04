# Device management
### I. Configure and verify device management
- Configure device management gồm có :
    - Backup and restore device configuration
    - Using Cisco Discovery Protocol or LLDP for device discovery
    - Licensing
    - Logging
    - Timezone
    - Loopback
### 1. Backup and restore device configuration
- Nhằm mục địch bảo vệ tài sản quý giá của công ty , doanh nghiệp. Chúng ta cần phải Backup
dữ liệu thường xuyên để bảo vệ dữ liệu của công ty, nhằm tạo ra 1 bản sao khi bị mất dữ liệu
ta có thể khôi phục lại kịp thời mà không ảnh hưởng gì nhiều với công ty
- cách config backup dữ liệu : 
    ![1](https://i.imgur.com/sO1FxGB.png)

- cách restore
    ![https://i.imgur.com/ZilfVwY.png]
### 2. Using Cisco Discovery Protocol or LLDP for device discovery
- LLDP có khả năng hỗ trợ một tập hợp của các thuộc tính được sử dụng để khám phá ra những 
thiết bị hàng xóm (neighbor)
- Phát hiện các thiết bị router, switch lân cận được kết nối trực tiếp đến thiết bị 
- Trên cisco có 2 giao thức CDP và LLDP, với CDP thì được khởi động sẵn, còn với LLDP thì
enable.
- cách khởi động LLDP : ![3](https://i.imgur.com/4sZ88pF.png)
### 3. Licensing
- tham khảo giấy phép tại (https://bom.to/D8vkg)
### 4. Logging
- ![00](https://i.imgur.com/EWStSV9.png)
- ![5](https://i.imgur.com/EWStSV9.png)
### 5. Timezone
- cài đặt : ![6](https://i.imgur.com/W2nUo1y.png)
### 6. Loopback 
- Loopback là kênh liên lạc chỉ có một điểm cuối. Mạng TCP/IP chỉ định một loopback cho phép
client software giao tiếp với phần mềm máy chủ trên cùng một máy tính. Người dùng có thể 
chỉ định một địa chỉ IP,  thường là 127.0.0.1, sẽ quay lại cấu hình mạng **TCP/IP**. Phạm 
vi địa chỉ cho chức năng **loopback** là phạm vi từ 127.0.0.0 đến  127.255.255.255. Tương 
tự như **ping** . loopback cho phép người dùng kiểm tra **network** riêng của mình để 
đảm bảo **IP Stack** hoạt động đúng. 
- Cách cấu hình  : 
                    ![7](https://i.imgur.com/qMJUBZK.png)
