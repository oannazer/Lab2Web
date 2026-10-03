# Laporan Praktikum 1 - Pemrograman Web

**Nama:** Oan Najmi Zertho  
**NIM/Kelas:** 321510027 / I.25.3A  
**Prodi:** Teknik Informatika  
**Mata Kuliah:** Pemrograman Web  
**Dosen:** Agung Nugroho S.Kom, M.Kom

## Langkah Praktikum

### Persiapan deklarasi dokumen HTML

Persiapan dokumen menggunakan deklarasi:
Pada bagian `<head>` berisi `metadata` seperti penggunaan `charset`, `viewport`, dan lainnya.
Judul halaman web juga diisi di bagian ini dengan tag `<title>`.
Lalu berikan elemen semantik yang mempermudah pembacaan struktur HTML seperti `<header>` yang memiliki makna bagian atas di suatu halaman / judul

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Biodata Mahasiswa</title>
  </head>
  <body>
    <header>
      <h1>Biodata Mahasiswa</h1>
    </header>
  </body>
</html>
```

![Screenshot screenshot-1](screenshots/screenshot-1.png)

### 1. Membuat navigasi

Buat elemen semantik navigasi untuk berpindah antar halaman dengan tag `<nav>` dan tag `<a>` sebagai hyperlink.

```html
<nav>
  <a href="index.html">Beranda</a>
  <a href="contact.html">Kontak</a>
</nav>
```

![Screenshot screenshot-2](screenshots/screenshot-2.png)

### 2. Membuat konten utama dan tabel data

Berikan elemen `<main>` untuk membungkus konten utama dari laman web, tambahkan elemen `<section>` sebagai pemisah antar konten dan tambahkan atribut `id` yang berfungsi sebagai anchor atau jangkar tujuan dari link navigasi `<nav>` lalu berikan judul section tersebut dengan tag `<h2>`.

Buat elemen `<table>` dengan ukuran border 1px (pixel) untuk menampilkan data dalam bentuk tabel. Tambahkan `<tr>` sebagai baris baru, `<th>` judul baris (header), dan `<td>` sebagai data baris tersebut.

```html
<main>
  <section id="biodata">
    <h2>Data Mahasiswa</h2>
    <table border="1">
      <tr>
        <th>Data</th>
        <th>Keterangan</th>
      </tr>
      <tr>
        <td>NIM</td>
        <td>312510027</td>
      </tr>
      <tr>
        <td>Nama</td>
        <td>Oan Najmi Zertho</td>
      </tr>
      <tr>
        <td>Program Studi</td>
        <td>Teknik Informatika</td>
      </tr>
    </table>
  </section>
</main>
```

![Screenshot screenshot-3](screenshots/screenshot-3.png)

### 3. Menambahkan gambar profil

Berikan gambar profil dengan memasukkan tag `<img>` dan rujukan file `.jpg` dengan atribut `src`.

```html
<img src="images/foto.jpg" alt="Foto Mahasiswa" width="200" />
```

Atribut `alt` berfungsi sebagai nama atau caption dari foto tersebut, namanya akan muncul jika user klik/membuka foto.

![Screenshot screenshot-4](assets/screenshot-4.png)

### 4. Menambahkan subjudul dan data diri

Berikan subjudul dengan tag `<h2>`, lalu di bawahnya tambahkan data diri berupa nama dan program studi dengan tag `<p>`. Gunakan tag `<strong>` agar tulisan judul menjadi **bold**.
Gunakan pemformatan teks dengan elemen `<strong>` agar judul atau suatu karakter menjadi lebih tebal atau **bold**. Ada juga format teks lain seperti `<italic>` yang bisa membuat karakter menjadi huruf miring.

```html
<h2>Data Diri</h2>
<p><strong>Nama:</strong> Oan Najmi Zertho</p>
<p><strong>NIM:</strong> 312510027</p>
<p><strong>Program Studi:</strong> Teknik Informatika</p>
<hr />
```

Elemen `<hr>` berfungsi untuk membuat garis horizontal sebagai pembatas antar konten.

![Screenshot screenshot-5](assets/screenshot-5.png)

### 5. Membuat daftar keahlian

Berikan subjudul keahlian dengan tag `<h2>` dan buat list bullet menggunakan tag `<ul>` dan `<li>`.
Unordered List atau `<ul>` merupakan tipe list tanpa urutan seperti titik atau **bullet** dan tag `<li>` untuk menampilkan konten list.

```html
<!-- Tambahkan informasi tambahan di sini -->
<h2>Keahlian</h2>
<ul>
  <li>HTML, CSS, JavaScript</li>
  <li>Pengembangan Game</li>
  <li>Basis Data</li>
</ul>
<hr />
```

Tag komentar yaitu `<!-- isi komentar -->` bisa dipakai untuk petunjuk pengembangan atau batas konten yang akan dibuat.

![Screenshot screenshot-6](assets/screenshot-6.png)

### 6. Membuat target belajar

Buat list target belajar secara berurutan menggunakan tag `<ol>` dan `<li>`.
Ordered List atau `<ol>` merupakan tipe list yang berurutan seperti angka `1, 2, 3, dst` dan tag `<li>` untuk menampilkan konten list.

```html
<ol>
  <li>Meningkatkan kemampuan pemrograman</li>
  <li>Menguasai Game Development</li>
  <li>Meng</li>
</ol>
```

![Screenshot screenshot-7](assets/screenshot-7.png)
