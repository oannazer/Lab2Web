# Laporan Praktikum 2 - Pemrograman Web

**Nama:** Oan Najmi Zertho  
**NIM/Kelas:** 321510027 / I.25.3A  
**Prodi:** Teknik Informatika  
**Mata Kuliah:** Pemrograman Web  
**Dosen:** Agung Nugroho S.Kom, M.Kom

## Langkah Praktikum - HTML Lanjutan

### Persiapan deklarasi dokumen HTML

Persiapan dokumen menggunakan deklarasi:
Pada bagian `<head>` berisi `metadata` seperti penggunaan `charset`, `viewport`, dan lainnya.
Judul halaman web juga diisi di bagian ini dengan tag `<title>`.
Dalam tag `<body>` berikan elemen semantik yang mempermudah pembacaan struktur HTML seperti `<header>` yang memiliki makna bagian atas di suatu halaman atau judulnya.

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
<!-- Navigasi digunakan sebagai kontrol tujuan dalam halaman-->
<nav>
  <a href="index.html">Beranda</a>
  <a href="#biodata">Biodata</a>
  <a href="#form">Form</a>
</nav>
<hr />
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

### 3. Memuat media ke dalam web

Media dalam website bisa berupa audio (hanya suara) maupun video. Buat elemen semantik `<media>` yang berisi `<video>` lalu tambahkan atribut `width` dan `height` untuk mengatur ukuran default, tambahkan juga atribut `controls` agar audio/video tersebut memiliki tombol kontrol untuk diakses user. dalam tag `<video>` berikan tag `<source> sebagai sumber data yang bisa berupa url, atau berupa file path.

```html
<media>
  <caption>
    <h2>Video Capture Python</h2>
  </caption>
  <video width="320" height="240" controls>
    <source src="media/Capture python.mp4" type="video/mp4" />
    Your browser does not support the video tag.
  </video>
</media>
```

![Screenshot screenshot-4](screenshots/screenshot-4.png)

### 4. Menbuat elemen form

Buat form biodata dengan tag `<form>` yang berfungsi sebagai area input dari user.
Gunakan `<label>` untuk penamaan field input sebagai identitas area input, atribut `for` sebagai identitas label tersebut yang akan diarahkan ke field inputnya.
Selanjutnya tag `<input>` sebagai area input usernya, beberapa atribut yang ada dalam tag ini yaitu :

1. type -> tipe input user, diantaranya text, email, password, radio, checkbox, submit dan lainnya.
2. id -> sebagai jangkar atau identitas unik dari area input tersebut
3. name -> nama area input tersebut, atribut ini dipakai sebagai penghubung antara label dan area inputnya, contoh user meng-klik pada labelnya (Nama Mahasiswa) maka sistem akan mengarahkan user untuk masuk area input yang sesuai.
4. placeholder -> kalimat atau kata petunjuk berjenis background (opsional).
5. required -> berfungsi mewajibkan user untuk mengisi area tersebut sebelum submit data.

Contoh `label` dan `input` tipe text :

```html
<label for="nama">Nama Mahasiswa : </label><br />
<input
  type="text"
  id="nama"
  name="nama"
  placeholder="Input nama lengkap.."
  required
/><br /><br />
```

Contoh `label` dan `input` tipe email :

```html
<label for="email">Email : </label><br />
<input
  type="email"
  id="email"
  name="email"
  placeholder="example@gmail.com"
  required
/><br /><br />
```

Contoh `label` dan `input` tipe password :

```html
<label for="password">Password : </label><br />
<input
  type="password"
  id="password"
  name="password"
  placeholder="Input password.."
  required
/><br /><br />
<label for="konfirmasi_password">Konfirmasi Password : </label><br />
<input
  type="password"
  id="konfirmasi_password"
  name="konfirmasi_password"
  placeholder="Ulangi password.."
  required
/><br /><br />
```

Selain input tipe ketik, atau inputan dengan keyboard, ada juga input bertipe pilihan seperti `radio`, `select`, dan `checkbox`.

Contoh input bertipe `radio` yang memastikan user memilih salah satu dari beberapa pilihan :

```html
<label for="gender">Jenis Kelamin : </label><br />
<input type="radio" id="laki-laki" name="gender" value="laki-laki" required />
<label for="laki-laki">Laki-laki</label>
<input type="radio" id="perempuan" name="gender" value="perempuan" required />
<label for="perempuan">Perempuan</label><br /><br />
```

Contoh input user berupa pilihan dropdown dengan elemen `<select>` dan `<option>` :

```html
<label for="prodi">Program Studi : </label><br />
<select id="prodi" name="prodi" required>
  <option value="">--Pilih Program Studi--</option>
  <option value="TIK">Teknik Informatika</option>
  <option value="SI">Sistem Informasi</option>
  <option value="TIN">Teknik Industri</option></select
><br /><br />
```

Contoh input user berupa beberapa pilihan yaitu `checkbox`.

Jika checkbox ingin menjadi beberapa kolom, agar tidak seterusnya ke bawah, gunakan `<table>` lalu pada header `<thead>` berikan atribut `colspan"jumlah kolom"`. Lalu pada elemen `<tbody>` tiap baris-nya dengan `<tr>` masukkan beberapa `<td>` sesuai jumlah kolom yang diinginkan. Maka checkbox akan ditampilkan dengan struktur tabel agar lebih rapih.

```html
<table>
  <thead>
    <tr>
      <th colspan="2">Minat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <input type="checkbox" id="web" name="minat" value="web" /><label
          for="web"
          >Web Development</label
        >
      </td>
      <td>
        <input type="checkbox" id="game" name="minat" value="game" /><label
          for="game"
          >Game Development</label
        >
      </td>
    </tr>
    <tr>
      <td>
        <input type="checkbox" id="data" name="minat" value="data" /><label
          for="data"
          >Data Science</label
        >
      </td>
      <td>
        <input type="checkbox" id="ai" name="minat" value="ai" /><label for="ai"
          >Artificial Intelligence</label
        >
      </td>
    </tr>
  </tbody>
</table>
<br /><br />
```

Terakhir input tipe tombol yang memiliki 2 jenis, yaitu `<button>` dan `<input>` dengan tipe `submit`, tombol yang disarankan untuk mengirim data dari form biasanya tag `<input type="submit">`.

```html
<input type="submit" value="Submit" />
```

Atribut value dalam input type submit merupakan kata yang akan ditampilkan pada tombol, bisa diganti menjadi kata lain seperti `Kirim` atau `Enter` sesuai keinginan.

Hasil akhir form akan terlihat seperti berikut :

![Screenshot screenshot-5](assets/screenshot-5.png)

### 5. Menambahkan elemen footer

Footer biasa ditempatkan di bagian terbawah dari suatu halaman HTML, biasanya berfungsi sebagai kontak, media sosial, copyright, dan ucapan terimakasih terhadap orang atau grup yang membantu development.

```html
<h2>Data Diri</h2>
<p><strong>Nama:</strong> Oan Najmi Zertho</p>
<p><strong>NIM:</strong> 312510027</p>
<p><strong>Program Studi:</strong> Teknik Informatika</p>
<hr />
```

Elemen `<hr>` berfungsi untuk membuat garis horizontal sebagai pembatas antar konten.

![Screenshot screenshot-6](assets/screenshot-6.png)
