\# 📋 ANSWERS — PBT\_01 HTML Fundamentals



\---



\## PHẦN A



\### Câu A1



\*\*a) Các bước xảy ra khi truy cập https://shopee.vn:\*\*



Nguồn: 01\_introduction\_html\_universe.md



1\. Trình duyệt thực hiện DNS Lookup để tìm địa chỉ IP của domain shopee.vn  

2\. Thiết lập kết nối TCP với server (3-way handshake)  

3\. Thực hiện TLS Handshake để mã hóa kết nối HTTPS  

4\. Trình duyệt gửi HTTP Request (GET) đến server  

5\. Server xử lý request và trả về HTTP Response (HTML, CSS, JS)  

6\. Trình duyệt nhận dữ liệu, phân tích HTML để tạo DOM  

7\. Tải CSS và tạo CSSOM  

8\. Kết hợp DOM và CSSOM để tạo Render Tree  

9\. Thực hiện Layout và Paint để hiển thị trang web  



\---



\*\*b) Tab Network trong DevTools:\*\*



Tab Network cho phép:



\- Xem danh sách tất cả request (HTML, CSS, JS, hình ảnh...)  

\- Kiểm tra Status Code (200, 404, 500...)  

\- Xem thời gian load từng tài nguyên  

\- Xem thông tin chi tiết như headers và response  



Yêu cầu thực hành:

\- Chụp screenshot tab Network  

\- Đánh dấu:

&#x20; - Status Code của request đầu tiên  

&#x20; - Tổng thời gian load trang  

&#x20; - Một request file CSS  



\---



\### Câu A2



Nguồn: 04\_semantic\_html.md



Trang web bị đánh giá SEO thấp vì không sử dụng semantic HTML đúng cách.



\*\*Các lỗi semantic:\*\*



1\. Dùng <div> thay vì <header>  

2\. Menu không dùng <nav> 

3\. Nội dung chính không dùng <main> 

4\. Sản phẩm không dùng <article> 

5\. Tiêu đề không dùng thẻ heading (<h1>, <h2>)  

6\. Footer không dùng <footer>  



\---



\*\*Code sửa:\*\*



```html

<header>

&#x20;   <h1>ShopTLU</h1>

&#x20;   <nav>

&#x20;       <a href="/">Trang chủ</a>

&#x20;       <a href="/products">Sản phẩm</a>

&#x20;   </nav>

</header>



<main>

&#x20;   <article>

&#x20;       <h2>iPhone 16 Pro</h2>

&#x20;       <p>25.990.000đ</p>

&#x20;       <figure>

&#x20;           <img src="iphone.jpg" alt="iPhone 16 Pro">

&#x20;       </figure>

&#x20;   </article>

</main>



<footer>

&#x20;   <p>© 2026 ShopTLU</p>

</footer>



\### Câu A3

Kết quả hiển thị:

Hộp 1



Text A Text B



Hộp 2



Text C Text D



Hộp 3



Giải thích:



\-Thẻ <div> là block element nên luôn xuống dòng

\-Thẻ <span> và <strong> là inline nên hiển thị cùng dòng

\-Vì vậy các đoạn text A, B, C, D nằm cùng dòng theo từng nhóm



\### Câu A4



Nguồn: 05\_tables\_hyperlinks.md



Sự khác nhau:

\-<thead>: chứa tiêu đề bảng

\-<tbody>: chứa dữ liệu chính

\-<tfoot>: chứa phần tổng kết



Không nên dùng table làm layout vì:

\-Không responsive tốt

\-Code khó đọc và khó bảo trì

\-Không tốt cho SEO

\-Accessibility kém



\## PHẦN C

\### Câu C1



<!DOCTYPE html>

<html lang="vi">

<head>

&#x20;   <meta charset="UTF-8">

&#x20;   <meta name="viewport" content="width=device-width, initial-scale=1.0">

&#x20;   <title>Chi tiết sản phẩm</title>

</head>

<body>



<header>

&#x20;   <h1><a href="#">ShopLogo</a></h1>

&#x20;   <nav aria-label="main navigation">

&#x20;       <ul>

&#x20;           <li><a href="#">Trang chủ</a></li>

&#x20;           <li><a href="#">Danh mục</a></li>

&#x20;       </ul>

&#x20;   </nav>

</header>



<nav aria-label="breadcrumb">

&#x20;   <ol>

&#x20;       <li><a href="#">Trang chủ</a></li>

&#x20;       <li><a href="#">Điện thoại</a></li>

&#x20;       <li>iPhone 16</li>

&#x20;   </ol>

</nav>



<main>



<section>

&#x20;   <h2>Hình ảnh sản phẩm</h2>

&#x20;   <img src="#" alt="Ảnh 1">

&#x20;   <img src="#" alt="Ảnh 2">

&#x20;   <img src="#" alt="Ảnh 3">

&#x20;   <img src="#" alt="Ảnh 4">

&#x20;   <img src="#" alt="Ảnh 5">

</section>



<section>

&#x20;   <h1>iPhone 16</h1>

&#x20;   <p>25.990.000đ</p>

&#x20;   <p>★★★★☆</p>

&#x20;   <p>Mô tả sản phẩm</p>

</section>



<section>

&#x20;   <h2>Thông số kỹ thuật</h2>

&#x20;   <table>

&#x20;       <thead>

&#x20;           <tr>

&#x20;               <th>Thông số</th>

&#x20;               <th>Chi tiết</th>

&#x20;           </tr>

&#x20;       </thead>

&#x20;       <tbody>

&#x20;           <tr>

&#x20;               <td>Chip</td>

&#x20;               <td>A18</td>

&#x20;           </tr>

&#x20;       </tbody>

&#x20;   </table>

</section>



<section>

&#x20;   <h2>Đánh giá</h2>

&#x20;   <article>

&#x20;       <h3>Người dùng</h3>

&#x20;       <p>Rất tốt</p>

&#x20;   </article>

</section>



<aside>

&#x20;   <h2>Sản phẩm tương tự</h2>

</aside>



</main>



<footer>

&#x20;   <p>\&copy; 2026 Shop</p>

</footer>



</body>

</html>



\### Câu C2



\-Việc sử dụng semantic HTML thay vì chỉ dùng thẻ div mang lại nhiều lợi ích quan trọng. Về SEO, các công cụ tìm kiếm như Google sử dụng cấu trúc semantic để hiểu nội dung trang web tốt hơn, từ đó cải thiện thứ hạng tìm kiếm. Về accessibility, các công cụ hỗ trợ như screen reader có thể đọc nội dung chính xác hơn nhờ các thẻ như header, nav, article.



\-Ví dụ, khi sử dụng thẻ <article> cho một sản phẩm, công cụ tìm kiếm có thể hiểu đây là một nội dung độc lập.



\-Tuy nhiên, thẻ <div> vẫn hữu ích trong các trường hợp chỉ cần container để áp dụng CSS mà không mang ý nghĩa nội dung.



\## PHẦN B3 — Debug HTML

1\.<!DOCTYPE> sai → sửa thành <!DOCTYPE html>

2\.Thiếu </title>

3.charset="utf8" → sửa thành utf-8

4\.<h1> không đóng

5\.<a> không đóng

6\.<img> thiếu dấu ngoặc kép

7\.<b> đóng sai → dùng <strong>

8\.Table thiếu <thead> và <tbody>

9\.Có 2 thẻ <main> → thay 1 bằng <aside>

10.<p> trong footer chưa đóng

11\.Thiếu thuộc tính alt cho <img>



