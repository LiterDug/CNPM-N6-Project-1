# Tìm hiểu HTML 28/01/2024

## Các thẻ cơ bản
- mở thẻ: ```<tên_thẻ>```
- đóng thẻ: ```</tên_thẻ>```
- comment: ```<!-- Đây là chú thích -->```

- thẻ ```<head>``` gồm:
	+ ```<title>```
	+ ```<meta>```, trong đó ```<meta charset="utf-8">```  hỗ trợ tiếng Việt phần ```<body>```
- thẻ <body>
	+ ```<h1>,<h2>,...,<h6>```: các thẻ heading
	+ ```<p>```: thẻ đoạn văn
	+ ```<img src="link_nguồn" alt="tên_ảnh">```: alt không cần thiết, nếu ảnh bị lỗi thì alt được hiển thị
	+ ```<a href="link_nguồn">Nhập_comment</a>```: thẻ điều hướng được mask bởi Nhập_comment
	+ ```<ul>```									: unorder list
		```<li>shdfdfjdfhj</li>```				: list item
      ```</ul>```
	+ Tương tự <ul>, có <ol>: order list
	+ ```<table>```: tạo bảng
		```<thead>: đề mục của bảng
			<th>abc</th>
			<th>abc</th>	
			<th>abc</th>
			...
		</thead>
		
		<tbody>
			<tr>
				<td>...</td>
				<td>...</td>
				...
			</tr>
		</tbody>
		```
	+ ```<input type="text">```: lấy dữ liệu vào là text từ bàn phím
	+ ```<input type="checkbox">```: ô tick hcn tròn góc
	+ ```<input type="radio">```:	ô tick tròn, tick được nhiều cùng lúc. Muốn chỉ tick được 1 ô thì đặt tên cho input:
		+ ```<input name="tên_gì_đó" type="radio">```
	+ ```<button>Login</button>```: tạo button có hướng dẫn "Login" bên trong
	
## Thêm thuộc tính (attribute) vào thẻ
- Vị trí thêm: trong thẻ mở
- VD: ```<h1 title="Đây_là_thuộc tính">ABCDEFGH</h1>```, chú ý ```title``` trong ```<h1>``` khác ```<title>``` trong ```<head>```

# Tìm hiểu CSS với HTML
Có 3 kiểu CSS vs HTML là: Internal, External, Inline
## Internal
- cho phép viết CSS trong HTML
- vị trí viết: trong thẻ ```<head> </head>```
- VD:
```
<head>
	<title>Thí chủ có link không ?</title>
	<meta charset="utf-8">
	<style>
		h1 {
			color: green;
			font-size: 100px;
		}
		ol {
			color: red;
			font-size: 30px;
		}
	</style>
</head>
```

## External
- cho phép viết CSS ở một file riêng rẽ, thường có tên là main.css, style.css
- file main.css được link vào file index.html trong thẻ ```<head> </head>```
	+ Cú pháp link: ```<link rel="stylesheet" href="đường_dẫn/main.css">```
	+ Trong main.css, không cần viết thẻ ```<style> </style>```, viết trực tiếp luôn: ```h1{	...		}```

## Inline
- cho phép viết trực tiếp trong thẻ mở của index.html
- là thuộc tính của thẻ
- VD: ```<h1 style="color: red; font-size: 100px;">Thí chủ có link không ?</h1>```
dấu ```;``` cần có nếu nhiều thuộc tính để ngăn cách

## CSS Selector

### ID
- mục đích: chỉ định cho các thẻ với ID riêng
- là thuộc tính của thẻ
- VD:
```
<h1 id="h1_1">Thí chủ có link không ?</h1>
<h1 id="h1_2">Kó</h1>
```
- Tên các ID phải khác nhau
- Trong main.css thì dùng dấu ```#``` chẳng hạn ```#h1_1{ ... }```

### Class
- Mục đích như ID nhưng áp dụng cho nhiều đối tượng, chỉ cần cùng tên class thì style sẽ được áp dụng
- VD khai báo: ```<h1 class="h1_1">Thí chủ có link không ?</h1>```
- Trong main.css dùng dấu ```.``` chẳng hạn ```.h1_1{ ... }```

### Thứ tự ưu tiên dùng CSS
- Đặc biệt nhất: ```!IMPORTANT```
- 1st: Inline
- 2nd: ID
- 3rd: Class
- 4th: Tag

## CSS Variable
- Sử dụng lớp giả:
```
:root {
	<!--viết_vào_đây-->
}
```
- Khai báo biến: ```--tên_biến: thuộc tính```
- VD: ```--text_color: violet```
- Nếu là biến toàn cục thì viết vào lớp giả trên, ngược lại là biến cục bộ viết vào thân tag cần dùng.

## CSS Units
### Đơn vị tuyệt đối

- pixel: ```px```

### Đơn vị tương đối
- ```%```
- ```rem```
- ```em```
- ```vh, vw```

## Thuộc tính Padding (phần đệm)
- Padding-Top:
- Padding-Bottom:
- Padding-Left:
- Padding-Right:
- Padding: