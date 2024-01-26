# Tìm hiểu HTML 24/01/2024

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