api/:
Chứa logic BE, hay chứa M, C trong MVC
    - controller: logic BE xử lý yêu cầu đến
    - helpers: chứa các ghàm có thể được gọi từ bất kỳ đâu
    - hooks: module mở rộng chứa năng cho sails cỏe. có thể sd hooks để chạy mã tùy chỉnh khi ứng dụng được khở động và trước khi xử lý yêu cầu đến. Hooks cũng có thể được cài đặt như plugin nhưng hook phải luôn là tùy chỉnh.
    - models: cấu trúc dữ liệu cho ứng dụng
    - policies: middleware giới hạn quyền truy cập vào các action cụ thể
    - responses: Các phản hồi tùy chỉnh có thể giúp duy trì mã trạng thái HTTP và hành vi nhất quán trên toàn bộ ứng dụng. (Vì không phải mọi ứng dụng Sails đều cần định nghĩa các phản hồi tùy chỉnh riêng, nên thư mục này đôi khi được loại bỏ.)


assets/
Đây là thư mục “assets” của bạn. Nó chứa tất cả các tệp tin tĩnh mà ứng dụng của bạn cần để lưu trữ. Bạn có thể tạo tệp tin và thư mục của riêng mình ở đây. Sau khi khởi động, một tệp tin có tên “assets/newFolder/data.txt” có thể được truy cập tại địa chỉ “your_host_url/newFolder/data.txt”.


config/
Thư mục này chứa các tệp tin khác nhau cho phép bạn tùy chỉnh và cấu hình ứng dụng Sails của mình.

 
tasks/
Thư mục “tasks/” là một bộ Grunt tasks và các cấu hình tương ứng, được đóng gói để tiện lợi cho bạn. Việc tích hợp Grunt chủ yếu hữu ích để gói lại tài sản phía front-end (như các stylesheet, script và các template markup), nhưng cũng có thể được sử dụng để chạy các công việc phát triển khác nhau, từ biên dịch Browserify đến di chuyển cơ sở dữ liệu.


views/
Đây là thư mục chứa tất cả các view tùy chỉnh của bạn.

Để tạo một view tùy chỉnh, hãy tạo một thư mục mới bên trong thư mục này, sau đó tạo một tệp tin .ejs mới. Để hiển thị view này cho client, bạn cần đặt một định tuyến trong tệp tin config/routes.js hoặc sử dụng phương thức res.view() bên trong một hành động điều khiển tùy chỉnh.

 

app.js
Tệp tin “app.js” là tệp tin chính đóng vai trò là điểm khởi đầu của ứng dụng trong môi trường production.

Khi phát triển trên máy local của bạn và chạy lệnh sails lift, mã trong tệp tin “app.js” không được thực thi. Thay vào đó, tệp tin này tồn tại để cung cấp một cách dễ dàng và sẵn sàng để chạy ứng dụng của bạn mà không cần gõ lệnh sails lift. Đây rất có thể là cách bạn sẽ khởi động ứng dụng của mình(ví dụ: chạy “node app” hoặc “npm start”).

