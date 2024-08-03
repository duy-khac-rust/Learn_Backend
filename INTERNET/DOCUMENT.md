# How does the internet work?

- **Packet**: một đơn vị dữ liệu nhỏ được truyền qua internet.
- **Router**: định hướng Packets giữa networks khác nhau.
- **IP Address**: mã định danh duy nhất cho từng thiết bị, được sử dụng để định tuyến dữ liệu đến đích chính xác.
- **Domain Name**: tên mà con người đọc được dưới dạng một trang web.
- **DNS (Domain Name System)**: hệ thống tên miền dịch Domain Name thành IP Address.
- **HTTP (Hypertext Transfer Protocol)**: truyền dữ liệu giữa Client và Server.
- **HTTPS**: HTTP được mã hóa cung cấp an toàn liên lạc Client và Server.
- **SSL/TLS (Secure Sockets Layer/Transport Layer Security)**: cung cấp liên lạc an toàn qua internet.
****
# A. Vai trò của các giao thức internet

> Giao tiếp và trao đổi dữ liệu.

- **Giao thức**: một tập hợp các quy tắc và tiêu chuẩn xác định các thông tin trao đổi giữa thiết bị và hệ thống.
- **IP -> Router -> Packet -> IP Address**
  - *TCP/UDP*: đảm bảo các Packet truyền đáng tin cậy và hiệu quả.
  - *DNS*: Domain Name -> IP Address và HTTP truyền data giữa Client và Server.

# B. IP Address/Domain Name

- **IP Address**: 192.168.1.1
- **Domain Name**: [google.com](https://google.com)
- **Domain Name** -> DNS (Domain Name System) -> IP Address

# C. HTTP/HTTPS

- **HTTP**: Client -->  <-- Server
- **HTTPS**: Client --> SSL/TLS <-- Server

# D. Building Application with TCP/IP (Transmission Control Protocol/Internet Protocol)

> Phân phối dữ liệu đáng tin cậy, có trật tự và kiểm tra lỗi giữa các thiết bị.

- **Port**: xác định ứng dụng và dịch vụ đang chạy trên mỗi thiết bị.
- **Sockets**: kết hợp giữa IP Address và Port, đại diện cho một điểm cuối liên lạc. Dùng để kết nối giữa các thiết bị và truyền dữ liệu giữa các ứng dụng.
- **Connections**: kết nối giữa các Sockets với nhau:
  - Kích thước tối đa.
  - Kích thước cửa sổ.
  - Xác định dữ liệu được truyền.
- **Data Transfer**: khi Connections được thiết lập, dữ liệu được truyền theo từng phân đoạn (số thứ tự, siêu dữ liệu khác để đảm bảo việc phân phối đáng tin cậy).

# E. Communication with SSL/TLS

- **Certificates**: chứa thông tin danh tính Server và được ký bởi bên thứ 3 (cơ quan cấp chứng chỉ) để xác minh tính xác thực của chúng.
- **Handshake**: thuật toán mã hóa và các tham số khác cho kết nối an toàn.
- **Encryption**: khi kết nối an toàn dữ liệu sẽ được mã hóa bằng thuật toán đã thỏa thuận và có thể được truyền một cách an toàn giữa Client và Server.

****
#  What is HTTP?
        
> HTTP là giao thức truyền siêu văn bản, là một giao thức được sử dụng để lấy các tài nguyên như tệp HTML. HTTP cung cấp một tiêu chuẩn nhắn tin để tạo điều kiện trao đổi thông tin giữa các Client và Server.
