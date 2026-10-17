# Lab4Web – Praktikum 4: CSS Layout
 
**Mata kuliah:** Pemrograman Web  
**Nama / NIM:** [isi nama dan NIM]  
**Kelas:** [isi kelas]
 
## Struktur Folder
 
```
Lab4Web/
├── lab4_box.html
├── lab4_layout/
│   ├── home.html
│   ├── artikel.html
│   ├── about.html      (Tugas 1)
│   ├── kontak.html     (Tugas 2)
│   └── style.css
├── screenshots/        (isi dengan screenshot hasil)
└── README.md
```
 
---
 
## Bagian 1 – Box Element (`lab4_box.html`)
 
### 1.1 Membuat dokumen HTML dasar
Dibuat dokumen HTML5 dengan `<header>` berisi `<h1>Box Element</h1>`.
 
### 1.2 Membuat Box Element
Di dalam `<section>` dibuat tiga `<div>` dengan class `div1`, `div2`, `div3`. Secara default `<div>` bersifat *block*, sehingga tersusun ke bawah memenuhi lebar halaman.
 
### 1.3 CSS Float
Selector `div { float: left; padding: 10px; }` membuat ketiga div "mengambang" ke kiri sehingga tersusun **berdampingan** dan lebarnya menyesuaikan isi. Warna latar: merah, kuning, hijau.
 
📷 `screenshots/01-box-float.png`
 
### 1.4 Clearfix
Ditambahkan `div4` setelah `div3`. Pada CSS:
 
```css
.div4 { background-color: blue; clear: left; float: none; }
```
 
Property `clear` menghentikan efek float sehingga Div 4 pindah ke baris baru di bawah Div 1–3 dan melebar penuh.
 
**Eksperimen nilai `clear`:**
 
| Nilai | Hasil |
|-------|-------|
| `left` | Div 4 turun ke bawah elemen float kiri (Div 1–3). |
| `right` | Tidak ada float kanan, jadi Div 4 tetap berada di sisi float (tidak turun). Pada contoh ini Div 4 menjadi `float: none` sehingga kotaknya berada di belakang div yang mengambang. |
| `both` | Div 4 turun di bawah semua elemen float (kiri maupun kanan). Hasilnya sama dengan `left` pada contoh ini. |
 
📷 `screenshots/02-clearfix.png`
 
---
 
## Bagian 2 – Layout Web Sederhana (`lab4_layout/`)
 
### 2.1 Persiapan file
Dibuat folder `lab4_layout` berisi `home.html` dan `style.css`. `home.html` memuat `<div id="container">` sebagai pembungkus dan menautkan `style.css`.
 
### 2.2 Kerangka layout dengan HTML5 Semantic Element
Kerangka: `<header>`, `<nav>`, `<section id="hero">`, `<section id="wrapper">` (berisi `<section id="main">` dan `<aside id="sidebar">`), dan `<footer>`.
 
📷 `screenshots/03-kerangka.png`
 
### 2.3 CSS dasar, container, dan header
- Import font **Open Sans** dari Google Fonts.
- Reset CSS (`* { margin:0; padding:0 }`).
- `#container` lebar 980px, rata tengah (`margin: 0 auto`), diberi `box-shadow`.
- `header` diberi padding dan judul `h1` berwarna abu-abu.
📷 `screenshots/04-header.png`
 
### 2.4 Navigasi
`nav` berlatar biru `#1f5faa`. Link `a` dibuat `inline-block` dengan padding sehingga tersusun horizontal. Kelas `.active` dan `:hover` berlatar `#2b83ea`.
 
📷 `screenshots/05-navigasi.png`
 
### 2.5 Hero Panel
`#hero` berlatar abu-abu berisi judul, paragraf, dan tombol "Learn more ». Tombol memakai class `.btn .btn-large`.
 
📷 `screenshots/06-hero.png`
 
### 2.6 Layout Main dan Sidebar
`#main` (640px + padding 20px) dan `#sidebar` (260px + padding 20px) sama-sama `float: left`, sehingga total lebarnya 980px dan tersusun berdampingan.
 
### 2.7 Sidebar Widget
Dua `.widget-box` di dalam `<aside>`: satu berisi daftar link, satu berisi teks. Judul widget berlatar biru `#428bca`, item list memiliki efek hover.
 
📷 `screenshots/07-sidebar.png`
 
### 2.8 Footer
`footer { clear: both; }` memastikan footer berada di bawah elemen float (main dan sidebar). Latar gelap `#1d1d1d`, teks terang.
 
📷 `screenshots/08-footer.png`
 
### 2.9 Elemen pada Main Content
Tiga `.box` (lebar 33.33%, `float: left`, `box-sizing: border-box`) berisi gambar bulat (`border-radius: 50%`), heading, paragraf, dan tombol "View detail". Dibungkus `.row`, yang memakai *clearfix* `:before/:after` agar tinggi pembungkus tetap benar.
 
📷 `screenshots/09-content.png`
 
### 2.10 Content Artikel
Dua `<article class="entry">` dipisahkan `<hr class="divider">`. Gambar pada artikel pertama `float: left`, pada artikel kedua memakai class `right-img` (`float: right`).
 
📷 `screenshots/10-artikel.png`
 
---
 
## Bagian 3 – Pertanyaan dan Tugas
 
### Tugas 1 – Halaman About (`about.html`)
Single layout dengan struktur yang sama (header, nav, hero, main + sidebar, footer). Isi:
- **Deskripsi** diri disertai foto profil bulat (float kiri).
- **Keahlian** berupa daftar "tag" (HTML5, CSS3, dst).
- **Portfolio**: grid 2 kolom dari 4 proyek (gambar, judul, deskripsi) memakai float.
- Sidebar berisi **Data Diri**.
📷 `screenshots/11-about.png`
 
### Tugas 2 – Halaman Kontak (`kontak.html`)
Layout yang sama dengan form isian: **Nama, Email, No. Telepon, Subjek (select), Message (textarea)**, serta tombol **Kirim** dan **Reset**. Sidebar berisi informasi kontak dan jam layanan. Input diberi style border, padding, dan efek `:focus`.
 

---
 

 
📷 `screenshots/13-validasi.png`
 
