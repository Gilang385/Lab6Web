# Lab5Web
# Membuat script untuk melakukan validasi pada isian form.
## Langkah-Langkah Membuat Form Validasi
1. Buat File HTML
Buat file HTML baru, misalnya `form_validation.html`. Buka file ini di editor teks seperti VSCode.

2. Struktur Dasar HTML
Buat struktur dasar HTML dengan `<!DOCTYPE html>`, `<html>`, `<head>`, dan` <body>`. Tambahkan judul pada elemen `<title>` di bagian `<head>`.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Validation</title>
</head>
<body>
````
Membuat Formulir Input
Di dalam elemen `<body>`, tambahkan form dengan beberapa elemen input (`name`, `email`, dan `password`). Setiap input diberi `name` dan `required` untuk menandakan bahwa mereka wajib diisi. Form juga diberi atribut `onsubmit="return validateForm()"`, yang menghubungkan form dengan fungsi JavaScript bernama validateForm.
```html
    <h2>Form Registrasi</h2>
    <form name="registrationForm" onsubmit="return validateForm()">
        Nama: <input type="text" name="name" required><br><br>
        Email: <input type="email" name="email" required><br><br>
        Password: <input type="password" name="password" required><br><br>
        <input type="submit" value="Submit">
    </form>
```
Penjelasan Kode:
- `name="registrationForm"`: Memberi nama pada form agar mudah diakses di JavaScript.
- `onsubmit="return validateForm()"`: Menjalankan fungsi `validateForm()` setiap kali form akan disubmit. Jika fungsi ini mengembalikan false, form tidak akan dikirim.
- `required`: Menandai bahwa input harus diisi sebelum bisa disubmit.

4. Menambahkan Script JavaScript untuk Validasi Form
Tambahkan skrip JavaScript di bagian bawah sebelum penutup tag `<body>` untuk memvalidasi input form.
```html
    <script>
        function validateForm() {
            // Mendapatkan nilai dari setiap input form
            let name = document.forms["registrationForm"]["name"].value;
            let email = document.forms["registrationForm"]["email"].value;
            let password = document.forms["registrationForm"]["password"].value;
            
            // Memvalidasi apakah kolom "Nama" kosong
            if (name === "") {
                alert("Nama harus diisi.");
                return false; // Menghentikan pengiriman form jika kosong
            }

            // Memvalidasi apakah kolom "Email" kosong
            if (email === "") {
                alert("Email harus diisi.");
                return false; // Menghentikan pengiriman form jika kosong
            }

            // Memvalidasi apakah kolom "Password" kosong
            if (password === "") {
                alert("Password harus diisi.");
                return false; // Menghentikan pengiriman form jika kosong
            }

            return true; // Jika semua validasi lolos, form dapat dikirim
        }
    </script>
</body>
</html>

```
Penjelasan Kode:

- `function validateForm()`: Fungsi yang akan dijalankan ketika form disubmit. Fungsi ini mengecek tiap input untuk memastikan tidak ada yang kosong.
- `let name = document.forms["registrationForm"]["name"].value;`: Mengambil nilai dari input `name` pada form `registrationForm`.
- `if (name === "")`: Mengecek apakah input `name` kosong. Jika kosong, fungsi menampilkan alert dan mengembalikan `false`, sehingga form tidak dikirim.
- `alert("Nama harus diisi.");`: Menampilkan pesan jika input name kosong.
- `return false;`: Mencegah pengiriman form saat ada kolom kosong.
- `return true;`: Mengizinkan pengiriman form jika semua input terisi.

Ringkasan
1. Membuat struktur HTML dan form.
2. Menghubungkan form dengan fungsi validasi JavaScript menggunakan onsubmit.
3. Memvalidasi input menggunakan JavaScript dan menampilkan pesan kesalahan jika ada kolom yang kosong.

Ketika form disubmit, JavaScript akan memeriksa tiap kolom input. Jika semua kolom terisi, form dikirim. Jika ada yang kosong, muncul alert yang memberi tahu pengguna untuk mengisi kolom tersebut.

FULL CODE
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Validation</title>
</head>
<body>
    <h2>Form Registrasi</h2>
    <form name="registrationForm" onsubmit="return validateForm()">
        Nama    : <input type="text" name="name" required><br><br>
        Email   : <input type="email" name="email" required><br><br>
        Password: <input type="password" name="password" required><br><br>
        <input type="submit" value="Submit">
    </form>

    <script>
        function validateForm() {
            let name = document.forms["registrationForm"]["name"].value;
            let email = document.forms["registrationForm"]["email"].value;
            let password = document.forms["registrationForm"]["password"].value;
            
            if (name === "") {
                alert("Nama harus diisi.");
                return false;
            }
            if (email === "") {
                alert("Email harus diisi.");
                return false;
            }
            if (password === "") {
                alert("Password harus diisi.");
                return false;
            }
            return true; // Jika semua validasi lolos
        }
    </script>
</body>
</html>
```

Hasil gambar
![image](https://github.com/user-attachments/assets/747e23f9-e929-414c-bf56-a4081b6b34db)


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

