# Lab6Web
# CSS Framework (Twitter Bootstrap)
Repository ini berisi hasil praktikum CSS Framework menggunakan Twitter Bootstrap untuk membuat layout web responsif.

## Tujuan Praktikum
Memahami dasar dari web framework CSS.
Membangun layout web dengan komponen Bootstrap.
## Langkah Praktikum
1. Persiapan Folder: Membuat folder `Pratikum 6`.

2. Membuat Dokumen HTML dengan Bootstrap:

- Menyusun layout sederhana dengan Bootstrap, termasuk navbar, grid system, dan footer.
3. Struktur Layout dengan Komponen Bootstrap:

- Navbar: Menambahkan navigasi dengan warna gelap.
- Konten: Menggunakan grid system untuk membuat dua kolom berukuran 50%.
- Footer: Menambahkan footer dengan latar belakang gelap dan teks putih.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout dengan Bootstrap</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <a class="navbar-brand" href="#">My Web</a>
    </nav>
    
    <!-- Content -->
    <div class="container mt-4">
        <div class="row">
            <div class="col-md-6">
                <h2>Kolom 1</h2>
                <p>Ini adalah kolom pertama.</p>
            </div>
            <div class="col-md-6">
                <h2>Kolom 2</h2>
                <p>Ini adalah kolom kedua.</p>
            </div>
        </div>
    </div>
    
    <!-- Footer -->
    <footer class="bg-dark text-white mt-4 p-4 text-center">
        &copy; 2024 My Web
    </footer>
</body>
</html>
```

![image](https://github.com/user-attachments/assets/52a8bf95-4a5c-4f64-9286-615d2d2e34a7)


# Lab7Web
Repository ini berisi hasil praktikum jQuery untuk memahami efek animasi dan event handling.

## Tujuan Praktikum
- Menggunakan jQuery untuk manipulasi efek dan event pada halaman web.
- Menerapkan efek slide dan animasi pada elemen.
  
## Langkah Praktikum
1. Persiapan Folder: Membuat folder `Pratikum 7`

2. Membuat Dokumen HTML:

- Membuat file `index.html` yang berisi elemen button dan kotak dengan id `box`.

3. Menambahkan Script jQuery:

- Menambahkan jQuery melalui CDN di bagian <head>.
- Membuat efek toggle untuk menampilkan dan menyembunyikan kotak.
- Menambahkan animasi pada kotak saat mouse masuk dan keluar.
- Membuat efek hide pada kotak ketika diklik.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>jQuery Effects and Events</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
    <style>
        .box {
            width: 200px;
            height: 200px;
            background-color: #007bff;
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 20px;
        }
    </style>
</head>
<body>
    <div class="container text-center">
        <h1>jQuery Effects & Event Handling</h1>
        <button id="toggleBtn" class="btn btn-primary mb-3">Toggle Box</button>
        <div id="box" class="box">Click Me</div>
    </div>

    <script src="app.js"></script>
</body>
</html>
```
```java
$(document).ready(function() {
    // Toggle efek slide pada kotak
    $("#toggleBtn").click(function() {
        $("#box").slideToggle();
    });

    // Event animasi dengan mouseenter dan mouseleave
    $("#box").mouseenter(function() {
        $(this).animate({ width: "300px", height: "300px" }, "fast");
    }).mouseleave(function() {
        $(this).animate({ width: "200px", height: "200px" }, "fast");
    });

    // Menambahkan event klik untuk menyembunyikan kotak
    $("#box").click(function() {
        $(this).hide();
    });
});
```

![image](https://github.com/user-attachments/assets/bc13978e-7e13-4e78-87a0-49b07dbd7fe8)

