<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<h1>QUAN TRỌNG</h1>


<p>CÁCH ĐỌC CÁC THƯ MỤC CON VÀ TỆP TRONG MỘT PATH CỤ THỂ</p>

<h2>Lưu ý Quan Trọng</h2>

<p>Xem qua lí thuyết cơ bản về đệ quy</p>

<img src="https://github.com/Duycan17/TA-Java/assets/117552281/5cc63520-8bf8-4bdd-ad53-853661ec7f09" alt="Ví dụ">

<hr>
<h2>Code mẫu</h2>
<img width="902" alt="image" src="https://github.com/Duycan17/TA-Java/assets/117552281/4cb03103-d2cc-4be4-980a-31a12a979b8c">
<img width="705" alt="image" src="https://github.com/Duycan17/TA-Java/assets/117552281/0208f00e-bcb8-4d5e-9b4b-64bafe298347">

<h3>Khai Báo Phương Thức</h3>

<pre>
<code>private static void displayDirectoryContents(File directory, int depth)</code>
</pre>

<p>Phương thức này có hai tham số:</p>
<ul>
  <li><code>directory</code>: Một đối tượng <code>File</code> đại diện cho thư mục cần duyệt.</li>
  <li><code>depth</code>: Một số nguyên đại diện cho độ sâu của thư mục hiện tại trong cấu trúc thư mục. Nó được sử dụng để thêm dấu cách vào đầu dòng trong kết quả hiển thị.</li>
</ul>

<h3>Giải Thích Code</h3>

<p>
  Dòng này lấy ra một mảng các đối tượng <code>File</code> đại diện cho các tệp và thư mục trong thư mục đã cho.
</p>

<pre>
<code>
File[] files = directory.listFiles();
</code>
</pre>

<p>Điều kiện này kiểm tra xem mảng <code>files</code> có khác null hay không. Nếu mảng này null, có nghĩa là thư mục đó trống hoặc không tồn tại.</p>

<pre>
<code>
if (files != null) {
</code>
</pre>

<p>Vòng lặp này duyệt qua từng đối tượng <code>File</code> trong mảng <code>files</code>.</p>

<pre>
<code>
for (File file : files) {
</code>
</pre>

<p>Vòng lặp này in ra các khoảng trắng dựa trên tham số <code>depth</code> để đại diện cho độ sâu của thư mục hiện tại trong cấu trúc thư mục.</p>

<pre>
<code>
for (int i = 0; i &lt; depth; i++) { 
    System.out.print(" "); 
}
</code>
</pre>

<p>Dòng này in ra dấu đường ống kèm theo hai dấu gạch ngang để thể hiện cấp bậc.</p>

<pre>
<code>
System.out.print("|-- "); 
</code>
</pre>

<p>Dòng này in ra tên của tệp hoặc thư mục.</p>

<pre>
<code>
System.out.print(file.getName());
</code>
</pre>

<p>Điều kiện này kiểm tra xem đối tượng <code>File</code> hiện tại có đại diện cho một thư mục không. Nếu đúng, nó gọi đệ quy để đọc các thư mục con bên trong nó. Nếu là một tệp (ví dụ: txt, docx, xml), nó chỉ in ra tên.</p>

<pre>
<code>
if (file.isDirectory()) { 
    // Gọi đệ quy để đọc các thư mục con bên trong nó
}
</code>
</pre>

<h2>Sử Dụng</h2>

<p>Hãy thoải mái sao chép repository này và khám phá ví dụ được cung cấp.</p>

<pre>
<code>
git clone https://github.com/Duycan17/TA-Java.git
</code>
</pre>

<h2>Giấy Phép</h2>

<p>Dự án này được cấp phép theo Giấy Phép MIT - xem tệp <a href="LICENSE">LICENSE</a> để biết chi tiết.</p>

</body>
</html>
