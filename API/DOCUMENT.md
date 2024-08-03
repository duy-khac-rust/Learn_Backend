# 1 API (Application Programming Interface) Concept

> **API cho phép tương tác giữa các hệ thống bằng cách tuân theo một tiêu chuẩn và giao thức để chia sẻ các tính năng, thông tin và dữ liệu.**

# 2 REST Fundamentals

> **REST là một kiểu kiến trúc để phát triển các dịch vụ web, sử dụng giao thức HTTP làm giao diện truyền thông(G,P,P,P,D) để truyền dữ liệu thông qua các phương thức HTTP.**

> **Kiến trúc REST có 6 ràng buộc và một API được điều khiển bởi điều đó có thể gọi là RESTful.**

## 2.1 Client-Server

> **Client gửi yêu cầu nó hoàn toàn độc lập với Server trả về phản hồi.**

## 2.2 Stateless

> Server không lưu trữ bất kỳ dữ liệu nào trong quá trình giao tiếp Client-Server có nghĩa **là mọi yêu cầu là một yêu cầu độc lập.**

## 2.3 Cache

> Bộ nhớ cache là một cấu trúc lưu trữ tính toán tập trung vào việc giữ dữ liệu lưu trữ thường xuyên được truy cập, cải thiện hiệu suất và hiệu quả mạng.
> **Do đó thông qua bộ nhớ đệm, có thể giảm hoặc thậm chí lọai bỏ nhu cầu Client gửi yêu cầu lên Server.**

## 2.4 Interface Uniform

> **Một hợp đồng giữa Client và Server xác định các tiêu chuẩn cho giao tiếp của họ.**

-**Có 4 ràng buộc:**

    - **Identification of Resources** : nó được sử dụng trong một yêu cầu để xác định những gì Client muốn truy cập trong Server.

    - **URL** : http://facebook.com/khac-duy -> khac-duy

    - **Manipulation of Resources Through Representation** : Client phải có đủ yêu cầu đến Server đủ thông tin để thao tác(create, retrieve, update, delete) tài nguyên được thông báo, có thể được biểu diễn bằng nhiều định dạng, chẳng hạn như Json, XML, HTML,...

    - **Self-descriptive Messages** :  Phải có thông báo tự mô tả đảm bảo giao tiếp bằng cách chứa tất cả thông tin mà Client - Server cần để hiểu yêu cầu và phản hồi chỉ bằng cách kiểm tra ngữ nghĩa của thông báo

    - **HATEOAS (Hypertext As The Engine Of Application State)** : phản hồi được gửi từ Server phải chứa thông tin về những gì khách hàng có thể thực hiện trong các yêu cầu tiếp theo.

## 2.5 Layered System

**Hệ thông phân lớp liên quan đến thực tế là có thể có nhiều thành phần và hệ thống con hơn giữa Client - Server**

## 2.6 Code On Demand

**Server có thể gửi mã thực thi dưới dạng phản hồi cho Client.**

# 3 Request

**Client request có 4 yếu tố chính cấu trúc thành tất cả các thông tin cần thiết để tương tác với Server**

## 3.1 URL (Uniform Resource Locator)

**Địa chỉ để xác định tài nguyên mà còn chỉ định các truy cập tài nguyên đó**

**For Example** : *http://facebook.com*

## 3.2 URI (Uniform Resource Identifier)

**Sử dụng trong URL để chỉ định tài nguyên nào khách hàng muốn truy cập trong một yêu cầu**

**For example** : *http://facebook.com/khac-duy* -> khac-duy

## 3.3 Parameters

**Thông tin có thể được gửi trong một yêu cầu của khách hàng để ảnh hưởng đến phản hồi của Server**

**Có 4 loại Parameters: Body Params, Route Params, Query Params, Headers**

## 3.4 Body Params

**Phần thân của yêu cầu chứa tất cả dữ liệu mà Server cần để xử lý thành công yêu cầu: Create of Update**

**For example** : {
                    "name": "Banana",
                    "price": 2.4
                  }

## 3.5 Router Params

**Các params được chèn vào URL cùng với thông tin để xác định một tài nguyên cụ thể**

**For Example** : *http://facebook.com/khac-duy/story* -> story

## 3.6 Query Params

**Các tham số được chèn vào URL, nhưng điểm khác biệt chính là các trường hợp sử dụng của nó có liên quan đến việc lọc và tìm kiếm thông tin về một tài nguyên hoặc thậm chí phân trang và sắp xếp các kết quả.**

**For example** : *http://facebook.com/khac-duy?story=public&active=true* -> ?story=public&active=true

## 3.7 Headers

**Tiêu đề cho phép gửi thông tin bổ sung trong yêu cầu.**

**For example** : *Authorization: Bearer token*
                  *Accept: application/json*

# 4 HTTP PROTOCOL

**Tiêu chuẩn giao tiếp thống trị thế giới Internet bằng cách xác định các mẫu tương tác giữa Client và Server**

                    ----HTTP Request --->
    *HTTP Client*                           *HTTP Server*
                    <---HTTP Response----

# 5 HTTP Methods

**Có 5 phương thức chính mà khách hàng có thể sử dụng trong yêu cầu nhằm thao tác tài nguyên API**

## 5.1 Get

**Truy xuất dữ liệu**

## 5.2 POST

**Tạo tài nguyên mới trong Server**

## 5.3 PUT

**Cập nhật hoặc tạo dữ liệu từ tài nguyên trong Server**

## 5.4 PATCH

**Cập nhật dữ liệu tài nguyên trong Server bằng cách xác định dữ liệu nhưng điểm khác biệt chính là chỉ cập nhật một thông tin cụ thể.**

## 5.5 DELETE

**Xóa tài nguyên trong Server**

# 6 HTTP Status Code

**Server trả về Status Code để biết loại phản hồi trong yêu cầu của khách hàng**

## 6.1 Group 2

**200(Ok)** : yêu cầu thành công.

**201(Created)** : Yêu cầu đã thành công và tạo tài nguyên.

**204(No Content)** : Yêu cầu đã thành công và không có nội dung bổ sung nào trong nội dung phản hồi.

## 6.2 Group 3

**301(Moved Permanently)** : Tài nguyên được yêu cầu đã thay đổi vĩnh viễn và một URL mới được cung cấp trong phản hồi.

**304(Not Modified)** : Tài nguyên được yêu cầu không được sửa đổi và có thể sử dụng cùng một phiên bản đã lưu trong bộ nhớ đệm.

**307(Temporary redirect)** : tài nguyên được yêu cầu đã tạm thời được chuyển hướng đến một URL khác.

## 6.3 Group 4

**400(Bad Request)** : Máy chủ không thể hiểu được yêu cầu.

**401(Unauthorized)** : Khách hàng không được xác thực để truy cập tài nguyên.

**403(Forbidden)** : Khách hàng không được phép truy cập tài nguyên.

**404(Not Found)** : Máy chủ không thể tìm thấy tài nguyên được yêu cầu.

## 6.4 Group 5

**500(Internal Server Error)** : Cho biết rằng Máy chủ gặp phải lỗi không mong muốn và không thể trả về phản hồi yêu cầu.

**503(Service Unavailable)** : Cho biết rằng Máy chủ không thể xử lý yêu cầu vì nó không khả dụng, quá tải hoặc đang bảo trì.