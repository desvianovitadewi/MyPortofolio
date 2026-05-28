# Narasi Tutorial Portofolio untuk Pemula

## 1. Pembukaan
Halo semuanya. Pada tutorial ini, kita akan membuat halaman portofolio pribadi sederhana menggunakan HTML dan CSS. Portofolio ini bisa dipakai untuk memperkenalkan diri, menampilkan jadwal, hobi, lokasi,  dan form pesan.

Di tutorial ini kita memakai 2 file utama, yaitu `index.html` untuk halaman portofolio dan `style.css` untuk mengatur tampilan.

## 2. Menyiapkan Folder Project
Langkah pertama adalah menyiapkan folder project. Di dalam folder ini, simpan file `index.html` dan `style.css`. File HTML berisi struktur halaman, sedangkan file CSS berisi aturan tampilan seperti warna, jarak, bentuk kartu, ukuran teks, dan layout.

Setelah file siap, buka folder project menggunakan editor seperti Visual Studio Code. Jika ingin melihat hasilnya, cukup buka file `index.html` di browser.

## 3. Memahami Struktur Dasar HTML
Di bagian paling atas file HTML ada deklarasi `<!DOCTYPE html>`. Bagian ini memberi tahu browser bahwa dokumen yang kita buat adalah HTML modern.

Setelah itu ada tag `<html lang="id">`, yang menandakan bahwa bahasa utama halaman adalah Bahasa Indonesia. Di dalamnya ada dua bagian besar, yaitu `<head>` dan `<body>`.

Bagian `<head>` berisi informasi halaman, seperti karakter teks, tampilan responsif di perangkat mobile, judul halaman, dan link ke file CSS. Bagian `<body>` berisi semua konten yang akan terlihat di layar.

## 4. Menghubungkan HTML dengan CSS
Agar halaman punya tampilan yang rapi, file HTML harus terhubung dengan CSS. Caranya ada di bagian `<head>` dengan kode:

```html
<link rel="stylesheet" href="style.css">
```

Artinya, browser akan membaca aturan tampilan dari file `style.css`. Kalau file CSS tidak terhubung, halaman tetap muncul, tetapi tampilannya akan sangat polos.

## 5. Membuat Bagian Hero
Bagian pertama yang dilihat pengunjung adalah hero. Di sini kita menampilkan foto profil, nama, tagline, dan menu navigasi.

Foto profil memakai tag `<img>`. Jika ingin mengganti foto, simpan gambar di folder project, misalnya di folder `img`, lalu ubah bagian `src`. Contohnya:

```html
src="img/foto-saya.jpg"
```

Nama dan tagline bisa diganti langsung pada teks di dalam tag `<h1>` dan `<p class="tagline">`.

## 6. Membuat Menu Navigasi
Menu navigasi dibuat memakai tag `<nav>`. Setiap menu memakai tag `<a>` yang diarahkan ke id section tertentu. Contohnya:

```html
<a href="#tentang">Tentang Aku</a>
```

Kode tersebut akan membawa pengguna ke section yang memiliki `id="tentang"`. Jadi, nama pada `href` harus sama dengan id section tujuan.

## 7. Membuat Section Tentang Aku
Section Tentang Aku dipakai untuk memperkenalkan diri. Di bagian ini kita bisa menulis nama lengkap, nama panggilan, jurusan, kampus, asal daerah, dan alasan memilih jurusan.

Teks penting bisa ditebalkan dengan tag `<strong>`, sedangkan teks yang ingin diberi penekanan bisa memakai tag `<em>`. Bagian quote memakai tag `<blockquote>` agar tampil berbeda dan lebih menarik.

## 8. Menambahkan Skills
Bagian soft skills dipakai untuk menampilkan kemampuan non-teknis seperti kerja tim, komunikasi, dan manajemen waktu. Setiap skill dibuat dalam bentuk kartu kecil menggunakan class `skill-card`.

Strukturnya sederhana: satu ikon, lalu satu teks skill. Jika ingin mengganti skill, cukup ubah teks di dalam tag `<p>`. Jika ingin mengganti ikon, ubah emoji di dalam tag `<span class="skill-ikon">`.

## 9. Membuat Jadwal Harian
Jadwal harian dibuat memakai tabel. Tabel menggunakan tag `<table>`, lalu di dalamnya ada `<thead>` untuk judul kolom dan `<tbody>` untuk isi data.

Pada tabel ini juga digunakan `colspan` dan `rowspan`. `colspan` dipakai untuk menggabungkan beberapa kolom secara horizontal, sedangkan `rowspan` dipakai untuk menggabungkan beberapa baris secara vertikal.

Contohnya, jika hari Senin punya dua kegiatan, maka kolom hari bisa dibuat satu kali saja dengan `rowspan="2"`.

## 10. Membuat Section Hobi
Section hobi dibuat menggunakan beberapa kartu gambar. Setiap kartu memiliki gambar, nama hobi, dan deskripsi singkat. Untuk mengganti gambar, ubah bagian `src` pada tag `<img>`.

Jika memakai gambar sendiri, sebaiknya buat folder `img`, lalu simpan gambar di sana. Contoh:

```html
src="img/hobi-musik.jpg"
```

Jangan lupa ubah juga teks `alt`, karena `alt` membantu menjelaskan isi gambar jika gambar tidak berhasil tampil. Contoh hobi yang bisa ditulis adalah musik, menonton film, membaca, olahraga, menggambar, atau coding.

## 11. Menambahkan Google Maps
Bagian lokasi memakai tag `<iframe>` dari Google Maps. Untuk menggantinya, buka Google Maps, cari kota atau lokasi yang ingin ditampilkan, klik Share, pilih Embed a map, lalu salin kode HTML-nya.

Setelah itu, ganti tag `<iframe>` lama dengan iframe baru dari Google Maps. Jika tidak ingin membagikan alamat lengkap, cukup gunakan nama kota atau daerah saja.

## 13. Membuat Form Pesan
Form pesan dibuat menggunakan tag `<form>`. Di dalamnya ada input untuk nama, email, pilihan sumber kenal, tujuan menghubungi, topik, dan pesan.

Input teks memakai `<input type="text">`, input email memakai `<input type="email">`, pilihan tunggal memakai radio button, pilihan banyak memakai checkbox, dan pesan panjang memakai `<textarea>`.

Saat tombol kirim ditekan, JavaScript sederhana akan menampilkan popup. Fungsi ini dibuat agar halaman terasa lebih interaktif.

## 14. Memahami JavaScript Popup
Di bagian bawah HTML ada kode JavaScript. Fungsi `kirimPesan(event)` mencegah halaman reload, lalu menambahkan class `aktif` pada popup. Saat class ini aktif, popup akan muncul.

Fungsi `tutupPopup()` dipakai untuk menutup popup dengan cara menghapus class `aktif`. Popup juga bisa ditutup ketika pengguna mengklik area gelap di luar kotak popup.

## 15. Mengatur Tampilan dengan CSS
File `style.css` mengatur semua tampilan halaman. Misalnya warna latar, bentuk kartu, ukuran teks, bayangan, jarak antar elemen, tabel, form, kartu hobi, dan tampilan mobile.

Bagian `.hero` mengatur tampilan header. Bagian `.kartu` mengatur bentuk setiap section. Bagian `.galeri-grid` membuat kartu tersusun dalam grid, termasuk kartu soft skills dan hobi. Bagian `@media` membuat tampilan tetap rapi di layar kecil seperti HP.

Jika ingin mengganti warna utama, cari warna seperti `#1e3a8a` atau `#4f46e5`, lalu ubah sesuai warna yang diinginkan.

## 16. Mengecek Hasil di Browser
Setelah mengedit, simpan file lalu buka `index.html` di browser. Periksa apakah nama, foto, soft skills, jadwal, hobi, maps, video, dan form sudah tampil dengan benar.

Jika ada bagian yang tidak muncul, cek kembali nama file, lokasi gambar, tanda kutip, dan tag HTML yang mungkin belum tertutup.

## 17. Bonus Emmet untuk Menulis Lebih Cepat
Emmet adalah fitur di Visual Studio Code yang membantu kita menulis HTML lebih cepat. Cara pakainya sederhana: ketik singkatan Emmet, lalu tekan `Tab` atau `Enter`. Setelah kode muncul, kita tinggal mengganti teks, link, gambar, dan isi kontennya.

### Struktur HTML Dasar
Untuk membuat struktur HTML lengkap dari awal, ketik:

```emmet
!
```

Emmet akan otomatis membuat struktur seperti `<!DOCTYPE html>`, `<html>`, `<head>`, dan `<body>`.

Untuk menghubungkan CSS, ketik:

```emmet
link:css
```

Lalu ubah nama file CSS-nya menjadi:

```html
href="style.css"
```

### Hero Portfolio
Untuk membuat bagian hero yang berisi foto, nama, tagline, kontak cepat, dan navigasi, gunakan:

```emmet
header.hero>.hero-inner>img.foto-hero+h1+p.tagline+.kontak-cepat>span*4^nav.hero-nav>a*6
```

Setelah muncul, isi bagian `span` dengan Instagram, nomor HP, kota, dan GitHub. Isi juga menu navigasi seperti Tentang Aku, Jadwal Harian, Hobi, Lokasi, Fav Video, dan Kirim Pesan.

### Section Tentang Aku
Untuk membuat kartu Tentang Aku, gunakan:

```emmet
section.kartu#tentang>h2+p*2+blockquote
```

Setelah itu, isi judul dengan `Tentang Aku`, lalu tulis paragraf perkenalan diri dan quote favorit.

### Skills
Untuk membuat bagian soft skills seperti di portfolio dan CV, gunakan:

```emmet
p>strong{Soft Skills:}^.galeri-grid>.skill-card*3>span.skill-ikon+p
```

Setelah kode muncul, isi tiga kartu dengan contoh soft skills seperti Kerja Tim, Komunikasi, dan Manajemen Waktu.

### Tabel Jadwal Harian
Untuk membuat kerangka tabel jadwal, gunakan:

```emmet
section.kartu#jadwal>h2+p.sub+.table-scroll>table>thead>tr>th[colspan=4]^tr>th*4^^tbody>tr*4>td*4
```

Setelah tabel muncul, ubah judul kolom menjadi Hari, Jam, Kegiatan, dan Keterangan. Jika perlu menggabungkan baris atau kolom, tambahkan atribut `rowspan` atau `colspan` secara manual.

### Hobi
Untuk membuat section hobi dengan tiga kartu, gunakan:

```emmet
section.kartu#hobi>h2+p.sub+.galeri-grid>.galeri-card*3>img+.galeri-caption>h3+p
```

Setelah itu, ganti `src` pada gambar, isi nama hobi, dan tulis alasan singkat kenapa kamu menyukai hobi tersebut.

### Lokasi Google Maps
Untuk membuat section lokasi, gunakan:

```emmet
section.kartu#lokasi>h2+p.sub+.map-wrapper>iframe^p.lokasi-nama
```

Setelah muncul, tempel kode iframe dari Google Maps ke dalam bagian `<iframe>`, lalu isi nama kota di `p.lokasi-nama`.


### Form Pesan Sederhana
Untuk membuat form pesan dengan input nama, email, textarea, dan tombol, gunakan:

```emmet
section.kartu#pesan>h2+p.sub+form[action=#][method=post][onsubmit="kirimPesan(event)"]>label[for=nama]{Nama kamu:}+input:text#nama[name=nama][placeholder="Siapa namamu?"][required]+label[for=email]{Email kamu:}+input:email#email[name=email][placeholder="emailkamu@contoh.com"][required]+label[for=pesan-isi]{Pesanmu:}+textarea#pesan-isi[name=pesan][rows=4]+.tombol-area>input:submit[value="Kirim Pesan"]+input:reset[value=Hapus]
```

Singkatan ini memang agak panjang, tetapi sangat membantu karena langsung membuat banyak elemen form sekaligus.

### Tips Emmet untuk Pemula
- Tanda `>` artinya membuat elemen di dalam elemen lain.
- Tanda `+` artinya membuat elemen sejajar.
- Tanda `*3` artinya mengulang elemen sebanyak tiga kali.
- Tanda `.` dipakai untuk class, contohnya `.kartu`.
- Tanda `#` dipakai untuk id, contohnya `#tentang`.
- Tanda `{}` dipakai untuk langsung mengisi teks.
- Tanda `[]` dipakai untuk menambahkan atribut, seperti `src`, `href`, atau `placeholder`.

## 18. Penutup
Jadi, portofolio ini dibuat dengan konsep sederhana: HTML untuk struktur, CSS untuk tampilan, dan sedikit JavaScript untuk interaksi. Walaupun sederhana, halaman ini sudah cukup lengkap untuk memperkenalkan diri secara online.

Setelah memahami dasar ini, kita bisa mengembangkan portofolio lebih jauh, misalnya menambahkan halaman project, animasi, mode gelap, atau mengunggahnya ke GitHub Pages agar bisa diakses orang lain melalui internet.
