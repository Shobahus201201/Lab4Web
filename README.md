| Nama      | Shobahus Solichin |
| ----------- | ----------- |
| NIM     | 312010076       |
| Kelas   | TI.20.A.1        |

## **Langkah langkah praktikum**
Persiapan membuat dokumen HTML dengan nama file lab4_box.html seperti berikut.
```html <br>
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Box Element</title>
</head>
<body>
	<header>
		<h1>Box Element</h1>
	</header>
</body>
</html>
```
## **Membuat Box Element**
Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut.
```html <br>
<section>
		<div class="div1">Div 1</div> 
		<div class="div2">Div 2</div> 
		<div class="div3">Div 3</div>
</section>
```
## **CSS Float Property**
Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut.
```css <br>
<style> 
		div{
			float:left;
		    padding: 10px;
		}
		.div1{
			background: red;
		}
		.div2{
		    background: yellow;
		}
		.div3{
			background: green;
		}
</style>
```
Kemudian buka browser untuk melihat hasilnya

![Foto](Foto/foto1.png)

## **Mengatur Clearfix Element**
Clearfix digunakan untuk mengatur element setelah float element. Property `clear` digunakan untuk
mengaturnya.

Tambahkan element div lainnya seteleah div3 seperti berikut.

```html <br>
<section>
		<div class="div1">Div 1</div> 
		<div class="div2">Div 2</div> 
		<div class="div3">Div 3</div>
		<div class="div4">Div 4</div>
</section>
```
Kemudian atur property clear pada CSS, seperti berikut.
```css <br>
.div4 {
			background-color: blue;
			clear: left;
			float: none;
}
```

Selanjutnya buka browser dan refresh kembali

![Foto](Foto/foto2.png)

Lakukan eksperimen terhadap penggunaan property clear dengan nilai lainnya (`left, both, right`),
dan amati perubahannya.

## **Membuat Layout Sederhana**

Buat folder baru dengan nama **lab4_layout**, kemudian buatlah file baru didalamnya dengan nama
**home.html**, dan file css dengan nama **style.css**.

```html <br>
<!DOCTYPE html>
<html lang="end">
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Layout Sederhana</title>
	<link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
	<div id="container">

        </div>
</body>
</html>
```
Kemudian tulis kode berikut.

```html <br>
<header>
    <h1>Layout Sederhana</h1>
</header>
<nav>
    <a href="home.html" class="active">Home</a>
    <a href="artikel.html">Artikel</a>
    <a href="about.html">About</a>
    <a href="kontak.html">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
    <section id="main"></section>
    <aside id="sidebar"></aside>
</section>
<footer>
    <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
```
Kemudian buka browser dan lihat hasilnya.

![Foto](Foto/foto4.png)

Kemudian tambahkan kode CSS untuk membuat layoutnya.

```css <br>
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400 ;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0 ,300;0,700;1,300&display=swap');
/* Reset CSS */
*{
	margin: 0;
	padding: 0; 
}
body{ 
	line-height:1;
	font-size:100%;
	font-family:'Open Sans', sans-serif; 
	color:#5a5a5a;
}
#container{
    width: 980px;
    margin: 0 auto;
	box-shadow: 0 0 1em #cccccc; 
}

/* header */
header{
    padding: 20px;
}
header h1{
    margin: 20px 10px;
    color: #b5b5b5;
}
```
Kemudian lihat hasilnya pada browser.

![Foto](Foto/foto5.png)

## **Membuat Navigasi**
Kemudian selanjutnya mengatur navigasi.
```css <br>
/* navigasi */
nav{
    display: block;
	background-color: #1f5faa; 
}
nav a {
	padding: 15px 30px; 
	display: inline-block; 
	color: #ffffff; 
	font-size: 14px; 
	text-decoration: none; 
	font-weight: bold;
}
nav a.active, 
nav a:hover{
	background-color: #2b83ea; 
}
```
Kemudian lihat hasilnya.

![Foto](Foto/foto6.png)

## **Membuat Hero Panel.**
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.
```html <br>
<section id="hero">
			<h1>Hello World!</h1>
			<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
			<a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section> 
```
```css <br>
/* Hero Panel */
#hero{
	background-color: #e4e4e5; 
	padding: 50px 20px; 
	margin-bottom: 20px;
}
#hero h1{ 
	margin-bottom: 20px; 
	font-size: 35px;
}
#hero p{ 
	margin-bottom: 20px; 
	font-size: 18px; 
	line-height: 25px;
}
```
![Foto](Foto/foto%207.png)

## **Mengatur Layout Main dan Sidebar**
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.
```css <br>
/* main content */
#wrapper {
    margin: 0;
}
#main {
    float: left;
    width: 640px;
    padding: 20px;
}
/* sidebar area */
#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
}
```
## **Membuat Sidebar Widget**
Kemudian selanjutnya menambahkan element lain dalam sidebar.
```html <br>
<aside id="sidebar">
    <div class="widget-box">
        <h3 class="title">Widget Header</h3>
        <ul>    
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
        </ul>
    </div>
    <div class="widget-box">
        <h3 class="title">Widget Text</h3>
        <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
        arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
        pharetra est nunc, nec pretium nunc pretium ac.</p>
    </div>
</aside>
```
Kemudian tambahkan CSS.
```css <br>
/* widget */
.widget-box{
border:1px solid #eee; 
margin-bottom:20px;
}
.widget-box 
.title{ 
	padding:10px 16px; 
	background-color:#428bca; 
	color:#fff;
}
.widget-box ul{ 
	list-style-type:none;
}
.widget-box li{ 
	border-bottom:1px solid #eee;
}
.widget-box li a{ 
	padding:10px 16px; 
	color:#333; 
	display:block; 
	text-decoration:none;
}
.widget-box 
li:hover a{ 
	background-color:#eee;
}
.widget-box p{ 
	padding:15px;
	line-height:25px; 
}
```
![Foto](Foto/foto9.png)

## **Mengatur Footer**
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.
```css <br>
/* footer */
footer {
    clear:both;
	background-color:#1d1d1d; 
	padding:20px;
	color:#eee;
}
```
![Foto](Foto/foto10.png)

## **Menambahkan Elemen lainnya pada Main Content**
```html <br>
<section id="main">
	<div class="row">
		<div class="box">
			<img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
				<h3>Heading</h3>
				<p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
				<a href="#" class="btn btn-default">View detail</a>
		 </div>
		<div class="box">
			<img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
				<h3>Heading</h3>
				<p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
				<a href="#" class="btn btn-default">View detail</a>
	   </div>
	 <div class="box">
		<img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
				<h3>Heading</h3>
			     <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
				<a href="#" class="btn btn-default">View detail</a>
		 </div>
	</div>
</section>
```
Kemudian tambahkan CSS.
```css <br>
/* box */
.box { 
	display:block;
	float:left;
	width:33.333333%; 
	box-sizing:border-box; 
	-moz-box-sizing:border-box; 
	-webkit-box-sizing:border-box;
	padding:0 10px;
	text-align:center; 
}
.box h3 {
	margin: 15px 0;
}
.box p {
	line-height: 20px; 
	font-size: 14px; 
	margin-bottom: 15px;
}
box img {
	border: 0;
	vertical-align: middle; 
}
.image-circle { 
	border-radius: 50%;
}
.row {
	margin: 0 -10px;
	box-sizing: border-box; 
	-moz-box-sizing: border-box; 
	-webkit-box-sizing: border-box;
}
.row:after, 
.row:before, 
.entry:after, 
.entry:before {
	content:'';
    display:table;
}
.row:after, 
.entry:after {
    clear:both;
}
```
Lihat hasilnya dibrowser.

![Foto](Foto/foto11.png)

## **Menambahkan Content Artikel**
Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.
```html <br>
<hr class="divider" />
<article class="entry">
   <h2>First featurette heading.</h2>
	<img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
	<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
</article>
<hr class="divider" />
<article class="entry">
	<h2>First featurette heading.</h2>
	<img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
	<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
</article>
```
Kemudian tambahkan CSS.
```css <br>
.divider { border:0;
border-top:1px solid #eeeeee;
    margin:40px 0;
}
/* entry */
.entry {
	margin: 15px 0;
}
.entry h2 { 
	margin-bottom: 20px;
}
.entry p { 
	line-height: 25px;
}
.entry img { 
	float: left;
	border-radius: 5px;
	margin-right: 15px; 
}
.entry .right-img { 
	float: right;
}
```
![Foto](Foto/foto12.png)

## **Pertanyaan dan Tugas**
1. Tambahkan Layout untuk menu About
=> buat single layout yang berisi deskripsi, portfolio, dll
2. Tambahkan layout untuk menu Contact
=> yang berisi form isian: nama, email, message, dll

## Jawaban
1. Buat HTML seperti berikut

![Foto](Foto/Foto12.1.png)

Kemudian tambahkan CSS.

![Foto](Foto/foto12.2.png)

Lalu lihat hasilnya

![Foto](Foto/foto13.png)

2. Buat HTML seperti berikut

![Foto](Foto/12.3.png)

Kemuadian tambahkan CSS
```CSS <br>
/* Layout Kontak */
.kontak-body {
    margin: 0;
    font-family: -apple-system, Arial, sans-serif;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    text-align: left;
    padding: 30px;
    padding-bottom: 10px;
    border: 1px solid #ced4da;
    border-radius: 0.25rem;
    max-width: 100%;
}
.kontak-form-group {
    margin-bottom: 1rem;
}

.kontak-input-group {
    position: relative;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    -ms-flex-align: stretch;
    align-items: stretch;
    width: 100%;
}

.kontak-form-control {
    display: block;
    width: 100%;
    height: calc(1.5em + 0.75rem + 2px);
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid #ced4da;
    outline: none;
    border-radius: 0.25rem;
    transition: border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}

.kontak-form-control:focus {
    border: 1px solid #313131;
}


textarea.kontak-form-control {
    height: auto;
}

label.kontak-label {
    display: inline-block;
    margin-bottom: 0.5rem;
}


.kontak-btn {
    display: inline-block;
    font-weight: 400;
    color: #212529;
    text-align: center;
    vertical-align: middle;
    cursor: pointer;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    background-color: transparent;
    border: 1px solid transparent;
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    line-height: 1.5;
    border-radius: 0.25rem;
    transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out, border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}

.kontak-btn-primary {
    color: #fff;
    background-color: #007bff;
    border-color: #007bff;
}

.kontak-btn-lg, 
.kontak-btn-group-lg>
.kontak-btn {
    padding: 0.5rem 1rem;
    font-size: 1.25rem;
    line-height: 1.5;
    border-radius: 0.3rem;
}


input[type="submit"].kontak-btn-block, 
input[type="reset"].kontak-btn-block, 
input[type="button"].kontak-btn-block {
    width: 100%;
}
```
Lalu lihat hasilnya

![Foto](Foto/terakhir.png)