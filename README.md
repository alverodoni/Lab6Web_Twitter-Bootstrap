# Lab6Web_Twitter-Bootstrap
Nama: Doni Alvero <p>
Nim: 312410663 <P>
Kelas: TI.24.A.5 <P>
Jurusan: Teknik Informatika <p>
Mata Kuliah: Pemograman Web 1 <p>

### 1.Setup Bootstrap
Menunjukkan halaman web berhasil memuat Bootstrap, ditandai dengan tombol Primary (biru) yang sudah ter-style dengan benar `(.btn .btn-primary)`.
<img width="1917" height="1018" alt="Setup Bootstrap" src="https://github.com/user-attachments/assets/e7b0cc6b-25f6-4515-96f9-24d730f42f55" />

### 2.Container
Menunjukkan perbedaan layout antara Standard Container `(.container)`, yang membatasi lebar konten dan memusatkannya, dan Fluid Container `(.container-fluid)`, yang merentang selebar viewport.
<img width="1917" height="1017" alt="Container" src="https://github.com/user-attachments/assets/bb314d63-b00d-4f1a-8fd6-154fe4797d09" />

### 3.Komponen: Button `(Tombol)`
Menambahkan bilah navigasi Navbar `(.navbar-expand-lg .bg-dark)` di atas. Di bawahnya, terlihat Grid System yang menunjukkan tata letak kolom `(misalnya, 4+4+4 atau 8+4)`.
<img width="1918" height="1020" alt="Grid System" src="https://github.com/user-attachments/assets/ce832be8-a045-4c2a-9688-9bfe0ddf4302" />

### 4.Komponen: Navbar `(Navigasi)`
Menampilkan berbagai macam Tombol `(.btn)` dengan warna kontekstual `(Primary, Success, Danger, dll.)` yang berasal dari kelas-kelas Bootstrap.
<img width="1918" height="1020" alt="Komponen Navbar " src="https://github.com/user-attachments/assets/d3c0bc3f-ddee-47e8-8027-77a0b2a3f442" />

### 5.Komponen: Card `(Kartu)`
Menunjukkan implementasi Komponen Card `(.card)` yang digunakan untuk mengelompokkan konten `(gambar, judul, teks, dan tombol)` menjadi unit yang rapi.
<img width="1918" height="1017" alt="Komponen Card " src="https://github.com/user-attachments/assets/e40e127d-d8df-4c2c-8389-4a38edadc5eb" />

### 6.Komponen: Form `(Formulir)`
Menampilkan Formulir yang rapi dengan input email dan textarea. Komponen ini menggunakan kelas .form-control untuk input dan .form-label untuk label agar terlihat modern dan responsif.
<img width="1918" height="1017" alt="Komponen Form " src="https://github.com/user-attachments/assets/13f81dd4-ec6e-41d4-a77c-73de3d2ae074" />

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Praktikum 6 Bootstrap - Contoh Container dan Grid</title>
    <link
        href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
        rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
        crossorigin="anonymous">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Praktikum 6</a>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Artikel</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Kontak</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <div class="container">
        <h1 class="mt-4">Halo, Bootstrap!</h1>
        <button class="btn btn-primary mb-4">Ini Tombol Bootstrap</button>
    </div>

    <hr>

    <div class="container container-example">
        <h3>Standard Container (`.container`)</h3>
        <p>Konten ini berada di tengah dan memiliki lebar maksimum yang disesuaikan pada ukuran layar tertentu.</p>
    </div>

    <div class="container-fluid container-fluid-example">
        <h3>Fluid Container (`.container-fluid`)</h3>
        <p>Konten ini memenuhi seluruh lebar viewport (layar) tanpa batas.</p>
    </div>

    <hr>

    <div class="container mt-4 mb-4">
        <h2>Sistem Grid Bootstrap (12 Kolom)</h2>
        <p>Sistem grid dibagi menjadi 12 kolom virtual. Semua kolom dalam satu baris harus berjumlah 12.</p>

        <div class="row">
            <div class="col-4">Kolom 4</div>
            <div class="col-4">Kolom 4</div>
            <div class="col-4">Kolom 4</div>
        </div>

        <p class="mt-3">Responsif: Kolom 8 dan Kolom 4 (berlaku untuk layar Medium/Tablet ke atas)</p>
        <div class="row">
            <div class="col-md-8">Kolom 8 (Di bawah Medium, akan menjadi 12)</div>
            <div class="col-md-4">Kolom 4 (Di bawah Medium, akan menjadi 12)</div>
        </div>
    </div>

<hr>

    <div class="container mt-4 mb-5">
        <h2>Komponen Tombol (Buttons)</h2>
        <p>Tombol-tombol Bootstrap menggunakan kelas **`.btn`** dasar, diikuti oleh kelas konteks warna seperti **`.btn-primary`**.</p>
        
        <div class="d-grid gap-2 d-md-block">
            <button class="btn btn-primary me-2">Primary</button>
            <button class="btn btn-secondary me-2">Secondary</button>
            <button class="btn btn-success me-2">Success</button>
            <button class="btn btn-danger me-2">Danger</button>
            <button class="btn btn-warning me-2">Warning</button>
            <button class="btn btn-info me-2">Info</button>
            <button class="btn btn-light me-2">Light</button>
            <button class="btn btn-dark">Dark</button>
        </div>
    </div>
<hr>
    <div class="container mt-4 mb-5">
        <h2>Komponen Card (Kartu)</h2>
        <p>Card adalah wadah yang fleksibel dan dapat diperluas untuk menampilkan konten seperti gambar, judul, dan teks.</p>
        
        <div class="card" style="width: 18rem;">
            <img src="https://via.placeholder.com/286x180?text=Gambar+Card" class="card-img-top" alt="Placeholder image">
            
            <div class="card-body">
                <h5 class="card-title">Judul Card</h5>
                <p class="card-text">Ini adalah deskripsi singkat di dalam card. Sangat bagus untuk mempresentasikan informasi ringkas.</p>
                <a href="#" class="btn btn-primary">Lihat Detail</a>
            </div>
        </div>
    </div>
<hr>
    <div class="container mt-4 mb-5">
        <h2>Komponen Formulir (Form)</h2>
        <p>Formulir menggunakan kelas **`.form-control`** untuk *input* dan **`.form-label`** untuk *label* agar terlihat rapi dan lebar penuh.</p>
        
        <form>
            <div class="mb-3">
                <label for="emailInput" class="form-label">Alamat Email</label>
                <input type="email" class="form-control" id="emailInput" placeholder="nama@contoh.com">
            </div>
            
            <div class="mb-3">
                <label for="pesanText" class="form-label">Pesan</label>
                <textarea class="form-control" id="pesanText" rows="3"></textarea>
            </div>
            
            <button type="submit" class="btn btn-primary">Kirim</button>
        </form>
    </div>
    <script
        src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous">
    </script>
</body>
</html>
```
