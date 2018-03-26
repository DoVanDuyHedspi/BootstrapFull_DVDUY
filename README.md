# Bài tập Trainee Colombo 2018

## Bootstrap Full website

Sử dụng draw.io vẽ lại mockup

Sử dụng bootstrap, sass, kết hợp các thư viện js/css để hoàn thiện giao diện đầy đử của 1 sản phẩm

Thực hiện bởi [Duy](https://github.com/DoVanDuyHedspi)

## Liên kết

- Đề bài:[tại đây](https://docs.google.com/spreadsheets/d/1AcPRWhkGZsbpEEnysr7i6qq9YZHvAOyGe_X_DFYu2TE/edit?ts=5a7807d7#gid=1068631537)
- Khóa học bootstrap 4:[tại đây](https://www.youtube.com/playlist?list=PLUoqTnNH-2XyNhhLuYrrmrmV46jVw6RHF)
- Thiết kế : [tại đây](https://drive.google.com/file/d/1zcNSNAoxY9Y_rBG42-EEukNDPfcBIbmV/view?usp=sharing)
- Mockup draw.io: [tại đây](https://drive.google.com/file/d/10tPtvGLhUpZY_AReNyOGciz2uzJoGr_6/view?usp=sharing)
- Bài làm: [tại đây](https://dovanduyhedspi.github.io/BootstrapFull_DVDUY/)

## Hướng dẫn sử dụng 

- Hướng dẫn sử dụng bootstrap 4 có trong Tutorial[#1] của khóa học trên.
- Lưu ý trên video là BS4 beta, người xem phải sử dụng BS4 stable, nếu có khác biệt tự tìm cách fix
- Hướng dẫn cài ruby [tại đây](https://sass-lang.com/install).
## Kiến thức nắm được

- Áp dụng kiến thức đã học vào 1 bài tập mang tính production hơn


## Kiến thức nhận được

### 1. Tại sao không nên dùng bản alpha cho dự án của mình ?

Vì bản alpha là bản dùng để thử nghiệm, vẫn còn nhiều lỗi, và update phiên bản alpha liên tục, dùng vào dự án thật thì rủi ro cao.
Nếu bạn muốn ổn định thì nên sử dụng bản beta, còn bạn muổn thử nghiệm và đóng góp vào bootstrap 4 thì có thể trải nghiệm vs bản alpha.

### 2. Underlying stylesheet preproccessor(USP) thay đổi từ BS3->4 như thế nào? Optional: nêu vài điểm khác biệt giữa 2 loại USP?

Sass thay vì Less. Bootstrap 3 sử dụng LESS là engine để tiền xử lý (preprocessor) cho CSS, nhưng đến phiên bản 4, bootstrap đã được refactor để sử dụng SASS. SASS dễ sử dụng đồng thời cung cấp nhiều khả năng tùy biến hơn. Đồng thời, nhờ vào việc [Libsass Sass Compiler](https://github.com/sass/libsass) được viết bằng C/C++ mà bootstrap 4 sẽ được biên soạn(compile) nhanh hơn trước nhiều.

### 3.  Ngoài USP mới ra thì BS4 có những gì mới? 
- Nhỏ hơn, nhẹ hơn (bootstrap 3 (3.3.7), 121KB (file bootstrap.min.css), thì phiên bản 4.0.0 alpha bootstrap.min.css chỉ có 88KB)
- Hệ grid mới:Bootstrap 3 hiện tại có 4 dạng grid dành cho cột, .col-xs-XX dành cho mobile, .col-sm-XX dành cho tablet, .col-md-XX dành cho máy tính, và .col-lg-XX dành cho máy tính có kích cỡ màn hình lớn hơn. Bootstrap 4 tiến thêm một bước và giới thiệu dạng grid thứ 5 col-xl-XX giúp developer xây dựng layout hoạt động tốt trên tất cả các thiết bị.

![grid](https://i2.wp.com/agecode.co.jp/wp-content/uploads/2016/10/Grid-System-e1444291529140.png?resize=500%2C328)
- Bỏ support IE8 (không cần nói nhiều, tuyệt vời)
- Bootstrap card: Bootstrap giới thiệu component mới là cards. Cards sẽ thay thế wells,thumbnails và panels trong bootstrap 3. Bạn có thể đọc docs [ở đây](http://v4-alpha.getbootstrap.com/components/card/)
- Support flexbox:  flexbox là 1 trong những tiêu chuẩn WC3 mới giúp developer xây dựng layout trên những applications hiện đại. Flexbox đảm bảo các thành phần nằm trong container được sắp xếp, căn chỉnh và phân phối hợp lý ngay cả khi kích thước của thành phần chưa được biết. Flexbox thích hợp nhất khi sử dụng với responsive design, vì nó cung cấp container linh hoạt có thể mở rộng hoặc co lại tùy thuộc vào không gian được cung cấp.
-  Các class tiện ích mới:Bootstrap 4 tiến thêm 1 bước với việc giới thiệu spacing class để thay đổi margin và padding cho các thành phần. Ở bootstrap 3, bạn phải thay đổi nhưng style này trong file css hoặc tự tạo class tiện ích
Nhưng class tiện ích này được đặt tên theo luật như sau:
[margin hoặc padding]-[hướng]-[kích thước]
Ví dụ để set margin là 0 cho tất cả các hướng của 1 thành phần ta chỉ cần đơn giản thêm .m-all-0 cho thành phần đó. Và còn nhiều tiện ích khác.

### 4. Nêu các ưu điểm của flexbox?
- Một số ưu điểm của flexbox đã được nói ở trên.
- Lí do nên dùng flexbox:

![flexbox](https://blog.haposoft.com/content/images/2017/08/Capture.JPG)

### 5. Nêu 1 số khác nhau giữa ES6 với ES5? BS4 sử dụng gì để compile Javascript

### 6. Cách ghi đè variable của bootstrap.

- Tạo một file _variables.scss mới trong thư mục style. Copy và comment toàn bộ file scss/_variable.scss của bootstrap vào file _variables.scss của mình. Nếu muốn ghi đè biến nào thì bỏ comment biến đó rồi ghi đè. Khi import thì import file _variables.scss của bootstrap trước file _variables.scss của mình.


### 7. Mô tả  basic workflow của sass với bs4 được giới thiệu trong video?
* Cài ruby vào máy và cái sass vào dự án như hướng dẫn [tại đây](https://sass-lang.com/install). Tải file bootstrap 4 vào dự án. Tạo các thư mục như cấu trúc dưới đây.

````
	- bootstrap/
	- images/
	- js/
	- style/
		- css/
		- _base.scss
		- _variables.scss
		- app.scss
	- index.html
````


	+ _base.scss là file mình sẽ code css của mình.
	+ _variables.scss là file như đã nói ở mục (6) và ghi thêm biến của mình.
	+ app.scss để import các file scss của bootstrap và 2 file _base.scss, _variables.scss của mình.
* Trong thư mục bootstrap/ copy và comment toàn bộ file bootstrap.scss, _mixins.scss, _utilities.scss vào file style/app.scss. import file style/_variables.scss vào app.css như mục (6) và import file _base.scss vào cuối cùng file. Khi làm việc, nhận thấy cần import những file scss nào thì sẽ bỏ comment ở import đó.

* Câu lệnh compile file scss thành css: sass --watch style:style/css . Sau câu lệnh thì scss sẽ được compile vào file css/app.css. Trong html thì ta link css đến file css/app.css.



## Credit

- Không có
