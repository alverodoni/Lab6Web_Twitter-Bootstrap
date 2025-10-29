# Lab6Web_Twitter-Bootstrap
Nama: Doni Alvero <p>
Nim: 312410663 <P>
Kelas: TI.24.A.5 <P>
Jurusan: Teknik Informatika <p>
Mata Kuliah: Pemograman Web 1 <p>

### 1.Setup Bootstrap
Menunjukkan halaman web berhasil memuat Bootstrap, ditandai dengan tombol Primary (biru) yang sudah ter-style dengan benar `(.btn .btn-primary)`.
<img width="1917" height="1018" alt="Setup Bootstrap" src="https://github.com/user-attachments/assets/e7b0cc6b-25f6-4515-96f9-24d730f42f55" />
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Praktikum 6 Bootstrap - Contoh Lengkap</title>
    <link
        href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
        rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
        crossorigin="anonymous">
    </head>
<body>
    <script
        src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous">
    </script>
</body>
</html>
```
### Setup Bootstrap `(CSS dan JS)`
`Bagian ini mencakup pemanggilan file CSS Bootstrap, struktur dasar Container, dan penggunaan Grid System (row dan col)`.
```html
<head>
    <link
        href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
        rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
        crossorigin="anonymous">
    
    </head>
<body>
    <script
        src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous">
    </script>
    </body>
```

### 2.Container
Menunjukkan perbedaan layout antara Standard Container `(.container)`, yang membatasi lebar konten dan memusatkannya, dan Fluid Container `(.container-fluid)`, yang merentang selebar viewport.
<img width="1917" height="1017" alt="Container" src="https://github.com/user-attachments/assets/bb314d63-b00d-4f1a-8fd6-154fe4797d09" />
```html
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
```
### Container dan Grid System `(Struktur Utama)`
`Ini adalah kerangka utama yang menggunakan kelas .container dan membagi konten menjadi kolom utama (8 kolom) dan sidebar (4 kolom) menggunakan kelas .row, .col-lg-8, dan .col-lg-4`.
```html
<div class="container bg-white shadow-lg my-4 p-4 p-md-5"> 
    <header class="pb-3 border-bottom">
        <h1>Pembersih Halaman Sekitar Rumah</h1>
    </header>
    <div class="row pt-4">
        <div class="col-lg-8">
            </div> 
        <div class="col-lg-4 mt-4 mt-lg-0">
            </div> 
    </div> 
</div>
```


### 3.Komponen: Button `(Tombol)`
Menambahkan bilah navigasi Navbar `(.navbar-expand-lg .bg-dark)` di atas. Di bawahnya, terlihat Grid System yang menunjukkan tata letak kolom `(misalnya, 4+4+4 atau 8+4)`.
<img width="1918" height="1020" alt="Grid System" src="https://github.com/user-attachments/assets/ce832be8-a045-4c2a-9688-9bfe0ddf4302" />
```html
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
```
### Tombol Utama `(Lihat Layanan)`
`Beberapa contoh penggunaan tombol Bootstrap dengan kelas seperti .btn, .btn-primary, .btn-lg, .btn-outline-secondary, dan .btn-sm`.
```html
<a href="#artikel" class="btn btn-primary btn-lg">Lihat Layanan »</a>
```
### Tombol Sekunder `(Lihat detail)`
```html
<div class="col-md-4 mb-4 mb-md-0">
    <a href="#" class="btn btn-outline-secondary btn-sm">Lihat detail</a>
</div>
```
### Tombol Formulir `(Kirim Pesan)`
```html
<button type="submit" class="btn btn-primary w-100">Kirim Pesan / Booking</button>
```

### 4.Komponen: Navbar `(Navigasi)`
Menampilkan berbagai macam Tombol `(.btn)` dengan warna kontekstual `(Primary, Success, Danger, dll.)` yang berasal dari kelas-kelas Bootstrap & Bagian ini juga menunjukkan penggunaan komponen Navbar dengan kelas .navbar, .navbar-brand, dan .navbar-nav untuk navigasi utama.
<img width="1918" height="1020" alt="Komponen Navbar " src="https://github.com/user-attachments/assets/d3c0bc3f-ddee-47e8-8027-77a0b2a3f442" />
```html
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
```

```html
<nav class="navbar navbar-expand-lg navbar-dark" style="background-color: #181819;">
    <div class="container">
        <a class="navbar-brand" href="#beranda">Pembersih Halaman</a>

        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item">
                    <a class="nav-link nav-link-custom active" aria-current="page" href="#beranda">Beranda</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link nav-link-custom" href="#artikel">Artikel</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link nav-link-custom" href="#tentang">Tentang</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link nav-link-custom" href="#kontak">Kontak</a>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

### 5.Komponen: Card `(Kartu)`
Menunjukkan implementasi Komponen Card `(.card)` yang digunakan untuk mengelompokkan konten `(gambar, judul, teks, dan tombol)` menjadi unit yang rapi.
<img width="1918" height="1017" alt="Komponen Card " src="https://github.com/user-attachments/assets/e40e127d-d8df-4c2c-8389-4a38edadc5eb" />
```html
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
```
### Card Sidebar
```html
<div class="card mb-4">
    <div class="card-header bg-primary text-white fw-bold">Link Cepat</div>
    <ul class="list-group list-group-flush">
        <li class="list-group-item"><a href="#tentang" class="sidebar-link text-decoration-none text-dark">Tentang Kami</a></li>
        </ul>
</div>
<div class="card mb-4">
    <div class="card-header bg-info text-white fw-bold">Informasi Singkat</div>
    <div class="card-body bg-light">
        <p class="card-text small text-muted">
            Kami melayani area Sekitar dangga. Jam operasional layanan: Senin-Sabtu, 08:00 - 21:00. Hubungi kami untuk jadwal di luar jam tersebut.
        </p>
    </div>
</div>
```
### Card Portofolio
```html
<div class="row g-4 mt-2 mb-5">
    <div class="col-md-4">
        <div class="card text-center h-100 shadow-sm border-0">
            <div class="card-body">
                <div class="circle-placeholder mx-auto" style="background-color: #7d52a2;">Rumah A</div>
                <p class="card-text mt-3">Pembersihan Area Sekitar Rumah.</p>
            </div>
        </div>
    </div>
    </div>
```

### 6.Komponen: Form `(Formulir)`
Menampilkan Formulir yang rapi dengan input email dan textarea. Komponen ini menggunakan kelas .form-control untuk input dan .form-label untuk label agar terlihat modern dan responsif.
<img width="1918" height="1017" alt="Komponen Form " src="https://github.com/user-attachments/assets/13f81dd4-ec6e-41d4-a77c-73de3d2ae074" />
```html
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
```

```html
<section id="kontak" class="content-section">
    <h2 class="mb-4 text-primary">Hubungi Kami / Booking Layanan</h2>
    <p class="lead">Silakan isi formulir di bawah ini untuk mendapatkan penawaran atau mengajukan pertanyaan.</p>
    
    <form action="#" method="POST" class="contact-form p-4 border rounded shadow-sm">
        <div class="mb-3">
            <label for="nama" class="form-label">Nama Lengkap</label>
            <input type="text" class="form-control" id="nama" name="nama" required>
        </div>
        
        <div class="mb-3">
            <label for="email" class="form-label">Email</label>
            <input type="email" class="form-control" id="email" name="email" required placeholder="nama@contoh.com">
        </div>
        
        <div class="mb-3">
            <label for="message" class="form-label">Pesan Anda / Detail Booking (Jenis Layanan, Alamat, Tanggal)</label>
            <textarea class="form-control" id="message" name="message" rows="5" required></textarea>
        </div>
        
        <button type="submit" class="btn btn-primary w-100">Kirim Pesan / Booking</button>
    </form>
</section>
```

### Codingan Keseluruhan
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pembersih Halaman Sekitar Rumah - Bootstrap Layout</title>
    <link
        href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
        rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
        crossorigin="anonymous">
    
    <style>
        /* Gaya untuk Featurette Circles - Dibuat kustom karena Bootstrap tidak memiliki komponen lingkaran ini */
        .circle-placeholder {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            margin: 0 auto 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 0.9em;
            font-weight: bold; /* Ditambahkan agar lebih menarik */
        }

        .circle-1 { background-color: #e5944d;} 
        .circle-2 { background-color: #4d7fe5;} 
        .circle-3 { background-color: #4de5c2;} 

        /* Gaya untuk Featurette Image Placeholders */
        .featurette-img-left, .featurette-img-right {
            width: 150px;
            height: 150px;
            background-color: #7ba27a;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 0.8em;
            border-radius: 5px;
            float: none !important; /* Nonaktifkan float kustom untuk responsivitas */
        }
        
        /* Teks di dalam circle-placeholder pada About/Portfolio */
        .portfolio-item .circle-placeholder {
            width: 100px;
            height: 100px;
        }

        /* Navigasi dan Konten (untuk JS agar fungsionalitas hide/show tetap berjalan) */
        .content-section {
            display: none; 
        }
        
        .content-section.active {
            display: block;
        }

        /* Header kustom agar mirip dengan aslinya */
        header h1 {
            color: #aaa;
            margin: 0;
            font-size: 2em;
            font-weight: normal;
            padding: 20px 0 0;
        }
    </style>
</head>
<body>
    
    <nav class="navbar navbar-expand-lg navbar-dark" style="background-color: #181819;">
        <div class="container">
            <a class="navbar-brand" href="#beranda">Pembersih Halaman</a>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <a class="nav-link nav-link-custom active" aria-current="page" href="#beranda">Beranda</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link nav-link-custom" href="#artikel">Artikel</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link nav-link-custom" href="#tentang">Tentang</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link nav-link-custom" href="#kontak">Kontak</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    
    <div class="container bg-white shadow-lg my-4 p-4 p-md-5"> 
        
        <header class="pb-3 border-bottom">
            <h1>Pembersih Halaman Sekitar Rumah</h1>
        </header>
        
        <div class="row pt-4">
            
            <div class="col-lg-8">
                
                <section id="beranda" class="content-section active">
                    <div class="p-3 border-bottom mb-4">
                        <h2>Selamat Datang!</h2>
                        <p class="lead">
                            Kami adalah penyedia layanan kebersihan yang berdedikasi untuk memberikan kebersihan terbaik bagi rumah.
                        </p>
                        <a href="#artikel" class="btn btn-primary btn-lg">Lihat Layanan »</a>
                    </div>

                    <h3 class="mt-4 mb-3 text-secondary">Keunggulan Kami</h3>
                    <div class="row text-center mb-5 pb-4 border-bottom">
                        <div class="col-md-4 mb-4 mb-md-0">
                            <div class="circle-placeholder circle-1">Cepat</div>
                            <h4 class="fw-normal">Layanan Cepat</h4>
                            <p>Kami hadir dengan respons cepat dan pekerjaan tuntas tepat waktu.</p>
                            <a href="#" class="btn btn-outline-secondary btn-sm">Lihat detail</a>
                        </div>
                        <div class="col-md-4 mb-4 mb-md-0">
                            <div class="circle-placeholder circle-2">Profesional</div>
                            <h4 class="fw-normal">Tim Handal</h4>
                            <p>Kami terlatih dan profesional dalam setiap penanganan kebersihan.</p>
                            <a href="#" class="btn btn-outline-secondary btn-sm">Lihat detail</a>
                        </div>
                        <div class="col-md-4">
                            <div class="circle-placeholder circle-3">Aman</div>
                            <h4 class="fw-normal">Peralatan Aman</h4>
                            <p>Kami menggunakan peralatan dan cairan pembersih yang aman lingkungan.</p>
                            <a href="#" class="btn btn-outline-secondary btn-sm">Lihat detail</a>
                        </div>
                    </div>
                </section>
                
                <section id="artikel" class="content-section">
                    <h2 class="mb-4 text-primary">Artikel & Layanan Kami</h2>
                    <p class="lead">Temukan tips, trik, dan informasi mendalam mengenai layanan kebersihan yang kami tawarkan.</p>
                    
                    <div class="row featurette-block border-top pt-4">
                        <div class="col-md-3 d-flex align-items-center justify-content-center">
                            <div class="featurette-img-left">Alat Pel Lantai</div>
                        </div>
                        <div class="col-md-9">
                            <h3 class="fw-normal text-success">Teknik Membersihkan Lantai.</h3>
                            <ol class="list-unstyled">
                                <li>1. Hilangkan dulu semua kotoran padat, debu, rambut, dan serpihan kasar.</li>
                                <li>2. Gunakan air bersih (bisa air hangat) dan cairan pembersih lantai yang sesuai.</li>
                                <li>3. Pastikan kain pel tidak terlalu basah & Pel dengan pola teratur.</li>
                                <li>4. Segera ganti air pel jika sudah terlihat kotor/keruh.</li>
                                <li>5. Keringkan: Biarkan lantai kering sepenuhnya sebelum diinjak.</li>
                            </ol>
                        </div>
                    </div>

                    <div class="row featurette-block border-top pt-4 mt-4">
                        <div class="col-md-3 order-md-2 d-flex align-items-center justify-content-center">
                            <div class="featurette-img-right">Vakum Debu</div>
                        </div>
                        <div class="col-md-9 order-md-1">
                            <h3 class="fw-normal text-success">Pentingnya Vakum Rutin untuk Kesehatan.</h3>
                            <p>Vakum rutin merupakan langkah kunci untuk menciptakan lingkungan hidup yang sehat dan aman, melindungi kesehatan keluarga dari penyakit pernapasan yang dipicu oleh polutan dan                                     alergen di rumah.</p>
                        </div>
                    </div>
                </section>

                <section id="tentang" class="content-section">
                    <h2 class="mb-4 text-primary">Tentang Kami & Portofolio</h2>
                    
                    <h3 class="text-secondary">Deskripsi Peralatan Pembersih </h3>
                    <p>Kami hanya menggunakan peralatan pembersih dan mudah digunakan untuk membersihkan halaman sekitar rumah. alat & bahan yang digunakan seperti:</p>
                    <ul class="list-group list-group-flush mb-4">
                        <li class="list-group-item">Vakum Pembersih.</li>
                        <li class="list-group-item">Sapu.</li>
                        <li class="list-group-item">Alat Pel.</li>
                        <li class="list-group-item">Ember.</li>
                        <li class="list-group-item">Kain Lap.</li>
                    </ul>
                    
                    <h3 class="text-secondary">Portofolio Proyek Terakhir</h3>
                    <div class="row g-4 mt-2 mb-5">
                        <div class="col-md-4">
                            <div class="card text-center h-100 shadow-sm border-0">
                                <div class="card-body">
                                    <div class="circle-placeholder mx-auto" style="background-color: #7d52a2;">Rumah A</div>
                                    <p class="card-text mt-3">Pembersihan Area Sekitar Rumah.</p>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4">
                            <div class="card text-center h-100 shadow-sm border-0">
                                <div class="card-body">
                                    <div class="circle-placeholder mx-auto" style="background-color: #a25252;">Rumah B</div>
                                    <p class="card-text mt-3">Pembersihan Area Halaman Depan.</p>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4">
                            <div class="card text-center h-100 shadow-sm border-0">
                                <div class="card-body">
                                    <div class="circle-placeholder mx-auto" style="background-color: #52a27d;">Rumah C</div>
                                    <p class="card-text mt-3">Sanitasi dan kebersihan Area Halaman Belakang.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>
                
                <section id="syarat" class="content-section">
                    <h2 class="mb-4 text-primary">Syarat & Ketentuan Layanan</h2>
                    
                    <div class="accordion" id="accordionSyarat">
                        <div class="accordion-item">
                            <h2 class="accordion-header" id="headingOne">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
                                1. Kebijakan Pemesanan
                                </button>
                            </h2>
                            <div id="collapseOne" class="accordion-collapse collapse" aria-labelledby="headingOne" data-bs-parent="#accordionSyarat">
                                <div class="accordion-body">
                                    Semua pemesanan harus dilakukan minimal 1 hari sebelumnya. Pembatalan dalam waktu 1 jam sebelum jadwal akan batal
                                </div>
                            </div>
                        </div>
                        <div class="accordion-item">
                            <h2 class="accordion-header" id="headingTwo">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                                2. Jangkauan Area
                                </button>
                            </h2>
                            <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo" data-bs-parent="#accordionSyarat">
                                <div class="accordion-body">
                                    Layanan kami saat ini mencakup area Sekitar Dangga. Untuk lokasi di luar area tersebut, mungkin akan dikenakan biaya transportasi tambahan.
                                </div>
                            </div>
                        </div>
                        <div class="accordion-item">
                            <h2 class="accordion-header" id="headingThree">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                                3. Jam Operasional
                                </button>
                            </h2>
                            <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree" data-bs-parent="#accordionSyarat">
                                <div class="accordion-body">
                                    Layanan reguler tersedia Senin-Sabtu, pukul 08:00 - 21:00 WIB. Pemesanan di luar jam tersebut tergantung pada ketersediaan tim.
                                </div>
                            </div>
                        </div>
                        <div class="accordion-item">
                            <h2 class="accordion-header" id="headingFour">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
                                4. Garansi Kebersihan
                                </button>
                            </h2>
                            <div id="collapseFour" class="accordion-collapse collapse" aria-labelledby="headingFour" data-bs-parent="#accordionSyarat">
                                <div class="accordion-body">
                                    Kami menjamin hasil kebersihan yang memuaskan. Jika ada keluhan, harap laporkan dalam waktu 3 jam setelah layanan selesai untuk peninjauan ulang.
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <section id="kontak" class="content-section">
                    <h2 class="mb-4 text-primary">Hubungi Kami / Booking Layanan</h2>
                    <p class="lead">Silakan isi formulir di bawah ini untuk mendapatkan penawaran atau mengajukan pertanyaan.</p>
                    
                    <form action="#" method="POST" class="contact-form p-4 border rounded shadow-sm">
                        <div class="mb-3">
                            <label for="nama" class="form-label">Nama Lengkap</label>
                            <input type="text" class="form-control" id="nama" name="nama" required>
                        </div>
                        
                        <div class="mb-3">
                            <label for="email" class="form-label">Email</label>
                            <input type="email" class="form-control" id="email" name="email" required placeholder="nama@contoh.com">
                        </div>
                        
                        <div class="mb-3">
                            <label for="message" class="form-label">Pesan Anda / Detail Booking (Jenis Layanan, Alamat, Tanggal)</label>
                            <textarea class="form-control" id="message" name="message" rows="5" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn btn-primary w-100">Kirim Pesan / Booking</button>
                    </form>
                </section>
                
            </div> 
            
            <div class="col-lg-4 mt-4 mt-lg-0">
                
                <div class="card mb-4">
                    <div class="card-header bg-primary text-white fw-bold">Link Cepat</div>
                    <ul class="list-group list-group-flush">
                        <li class="list-group-item"><a href="#tentang" class="sidebar-link text-decoration-none text-dark">Tentang Kami</a></li>
                        <li class="list-group-item"><a href="#kontak" class="sidebar-link text-decoration-none text-dark">Booking Layanan</a></li> 
                        <li class="list-group-item"><a href="#artikel" class="sidebar-link text-decoration-none text-dark">Layanan Kami</a></li>
                        <li class="list-group-item"><a href="#syarat" class="sidebar-link text-decoration-none text-dark">Syarat & Ketentuan</a></li>
                    </ul>
                </div>
                
                <div class="card mb-4">
                    <div class="card-header bg-info text-white fw-bold">Informasi Singkat</div>
                    <div class="card-body bg-light">
                        <p class="card-text small text-muted">
                            Kami melayani area Sekitar dangga. Jam operasional layanan: Senin-Sabtu, 08:00 - 21:00. Hubungi kami untuk jadwal di luar jam tersebut.
                        </p>
                    </div>
                </div>
                
            </div> 
        </div> 
        </div>
    
    <footer class="bg-dark text-white p-3 text-center mt-5">
        &copy; 2021 - Universitas Pelita Bangsa
    </footer>

    <script
        src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous">
    </script>
    
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const navLinks = document.querySelectorAll('.nav-link-custom'); // Gunakan kelas baru
            const sidebarLinks = document.querySelectorAll('.sidebar-link'); 
            const allLinks = document.querySelectorAll('.nav-link-custom, .sidebar-link');
            const sections = document.querySelectorAll('.content-section');
            
            // Fungsi untuk mengaktifkan tautan pada navigasi utama
            const setActiveNav = (targetId) => {
                navLinks.forEach(l => l.classList.remove('active'));
                navLinks.forEach(l => l.removeAttribute('aria-current'));

                const navTarget = document.querySelector(`.nav-link-custom[href="${targetId}"]`);
                if (navTarget) {
                    navTarget.classList.add('active');
                    navTarget.setAttribute('aria-current', 'page');
                }
                
                // Set kelas 'active' pada Sidebar Link yang sesuai (untuk penanda visual)
                sidebarLinks.forEach(l => l.classList.remove('active'));
                const sidebarTarget = document.querySelector(`.sidebar-link[href="${targetId}"]`);
                if (sidebarTarget) {
                    sidebarTarget.classList.add('active');
                }
            };
            
            // Fungsi untuk menampilkan/menyembunyikan konten
            const showSection = (targetId) => {
                sections.forEach(section => {
                    section.classList.remove('active');
                });
                
                const targetSection = document.querySelector(targetId);
                if (targetSection) {
                    targetSection.classList.add('active');
                    // Scroll ke atas halaman saat pindah section
                    window.scrollTo({ top: 0, behavior: 'smooth' });
                }
            };
            
            // Atur event listener untuk setiap tautan
            allLinks.forEach(link => {
                link.addEventListener('click', (e) => {
                    e.preventDefault();
                    
                    const targetId = link.getAttribute('href');
                    
                    setActiveNav(targetId);
                    showSection(targetId);
                });
            });

            // Pastikan halaman dimulai di #beranda
            showSection('#beranda');
        });
    </script>
</body>
</html>
```
