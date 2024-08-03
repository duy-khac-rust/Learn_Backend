# 1️.How does the internet work?

    - **Packet**: một đơn vị dữ liệu nhỏ được truyền qua internet.
    - **Router**: định hướng Packets giữa networks khác nhau.
    - **IP Address**: mã định danh duy nhất cho từng thiết bị, được sử dụng để định tuyến dữ liệu đến đích chính xác.
    - **Domain Name**: tên mà con người đọc được dưới dạng một trang web.
    - **DSN (Data Source Name)**: hệ thống tên miền dịch Domain Name thành IP Address.
    - **HTTP (Hypertext Transfer Protocol)**: truyền giữ liệu Client và Server.
    - **HTTPS**: HTTP được mã hóa cung cấp an toàn liên lạc Client và Server.
    - **SSL/TLS (Secure Sockets Layer/ Transport Layer Security)**: cung cấp liên lạc an toàn qua internet.

## A. Vai trò của các giao thức internet.

        > Giao tiếp và trao đổi dữ liệu.
        - **Giao thức**: một tập hợp các quy tắc và tiêu chuẩn xác định các thông tin trao đổi giữa thiết bị và hệ thống.
        - IP -> Router -> Packet -> IP Address
            - *TCP/UDP*: đảm bảo các Packet truyền đáng tin cậy và hiệu quả.
            - *DNS*: Domain Name -> IP Address và HTTP truyền data Client và Server.

## B. IP Address/Domain Name

        - **IP Address**: 192.168.1.1
        - **Domain Name**: [google.com](https://google.com)
        - **Domain Name** -> DSN (Data Source Name) -> IP Address

## C. HTTP/HTTPS

        - **HTTP**:  Client -->  <-- Server
        - **HTTPS**: Client --> SSL/TLS <-- Server

## D. Building Application with TCP/IP(Transmission Control Protocol/Internet Protocol): 
        > Phân phối dữ liệu đáng tin cậy, có trật tự và kiểm tra lỗi giữa các thiết bị.

        - **Port**: xác định ứng dụng và dịch vụ đang chạy trên mỗi thiết bị.
        Sockets: kết hợp giữa IP Address và Port, đai diện cho 1 điểm cuối liên lạc. Dùng để kết nối giữa các thiết bị và truyền dữa liệu giữa các ứng dụng.
        - **Connections**: kết nỗi giữa các Sockets with nhau:
            - Kích thước tối đa.
            - Kích thước cửa sổ.
            - Xác định dữ liệu được truyền.
        - **Data Transfer**: Connections được thiết lập thì truyền dữ liệu theo từng phân đoạn(số thứ tự, siêu dữ liệu khác để đảm bảo việc phân phối đáng tin cậy).

## E. Communication with SSL/TLS

        - **Certificates**: chứa thông tin danh tính Server và được ký bởi bên thứ 3(cơ quan cấp chứng > chỉ) để xác minh tính xác thực của chúng.
        - **Handshake**: thuật toán mã hóa và các tham số khác cho kết nối an toàn.
        - **Encryption**: khi kết nối an toàn dữ liệu sẽ được mã hóa bằng thuật toán đã thỏa thuận và có thể được truyền một cách an toàn Client và Server.

# 2. What is HTTP?
        
        > HTTP là một giao thức  