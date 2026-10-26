# Laporan Praktikum: DOM dan Event

## G.5 — Pengujian Script Tanpa Atribut defer

### Tujuan
Mengetahui pengaruh penempatan JavaScript di dalam tag `<head>` tanpa menggunakan atribut `defer`.

### Langkah Pengujian
1. Memindahkan tag `<script src="script.js" defer></script>` ke dalam bagian `<head>` tanpa atribut `defer`.
2. Menyimpan perubahan dan menjalankan kembali halaman web.
3. Mengamati hasil yang muncul pada halaman web dan Console browser.

### Hasil Pengamatan
Saat atribut `defer` dihapus, browser menjalankan JavaScript sebelum seluruh elemen HTML di bagian `<body>` dibaca. Akibatnya, elemen yang dicari menggunakan `document.getElementById()` belum tersedia sehingga menghasilkan nilai `null` dan menimbulkan error. Hal ini membuat fitur JavaScript tidak berjalan dengan benar.

### Kesimpulan
Atribut `defer` memastikan script dijalankan setelah dokumen HTML selesai diproses. Oleh karena itu, penggunaan `defer` diperlukan agar JavaScript dapat mengakses elemen HTML dengan benar.

## H. Pertanyaan Evaluasi

1. Apa yang dimaksud dengan DOM dan apa manfaatnya?
DOM (Document Object Model) adalah representasi struktur dokumen HTML dalam bentuk objek yang dapat diakses oleh JavaScript. Manfaatnya adalah mempermudah seleksi elemen, mengubah teks, mengatur tampilan, dan merespons interaksi pengguna.

2. Apa perbedaan `getElementById()`, `querySelector()`, dan `querySelectorAll()`?
- `getElementById()`: memilih satu elemen berdasarkan ID.
- `querySelector()`: memilih elemen pertama yang sesuai dengan selector CSS.
- `querySelectorAll()`: memilih semua elemen yang sesuai dengan selector CSS.

3. Apa fungsi `addEventListener()` dan sebutkan tiga contoh event?
`addEventListener()` digunakan untuk menghubungkan sebuah event ke fungsi yang akan dijalankan saat event terjadi.

Contoh event:
- `click`
- `input`
- `submit`

4. Mengapa `event.preventDefault()` digunakan pada event submit form?
Untuk mencegah tindakan bawaan browser, seperti pengiriman form yang memuat ulang halaman, sehingga data dapat diproses atau divalidasi terlebih dahulu melalui JavaScript.

5. Apa perbedaan `textContent` dan `innerHTML` dari sisi penggunaan dan keamanan?
- `textContent`: digunakan untuk membaca atau mengubah teks biasa tanpa menganggapnya sebagai HTML.
- `innerHTML`: digunakan untuk membaca atau mengubah isi HTML, termasuk markup.

`textContent` lebih aman untuk menampilkan input pengguna karena teks tidak diproses sebagai HTML.

6. Bagaimana `classList.toggle()` membantu mengubah tampilan elemen?
`classList.toggle()` menambahkan class jika belum ada dan menghapusnya jika sudah ada. Dengan demikian, tampilan elemen dapat berubah secara bergantian sesuai aturan CSS.

7. Sebutkan minimal tiga skenario pengujian validasi form.
- Semua kolom dikosongkan — form harus ditolak.
- Format email tidak valid — pesan kesalahan ditampilkan.
- Usia di bawah 17 tahun — form harus ditolak.
- Nama kurang dari tiga karakter — form harus ditolak.
- Semua data valid — pesan keberhasilan ditampilkan.

# Tujuan

Praktikum ini bertujuan untuk memahami penggunaan JavaScript DOM (Document Object Model) dan Event Handling dalam pengembangan halaman web. Praktikum ini juga bertujuan untuk mempelajari cara mengubah konten HTML, mengatur gaya elemen, memvalidasi formulir, membuat daftar tugas, serta menangani interaksi pengguna pada halaman web.

# Struktur File
Struktur file pada proyek praktikum ini adalah sebagai berikut:
![img19](<images/img 19.png>)

# screenshot hasil praktikum
(index.html)

# Struktur Dasar HTML
![img1](<images/img 1.png>)

# DOM, Event, Form Pendaftaran, dan To-do List
![img2](<images/img 2.png>)
![img3](<images/img 3.png>)

# Form Workshop dan Tombol Tampil/Sembunyi
![img4](<images/img 4.png>)
![img5](<images/img 5.png>)
![img6](<images/img 6.png>)

# screenshot hasil praktikum
( script.js )

# Manipulasi DOM dan Event Handling
![img7](<images/img 7.png>)

# Validasi Form Pendaftaran
![img8](<images/img 8.png>)

# To-do List
![img9](<images/img 9.png>)
![img10](<images/img 10.png>)

# Validasi Workshop dan Fitur Tampil/Sembunyi
![img11](<images/img 11.png>)
![img12](<images/img 12.png>)
![img13](<images/img 13.png>)

# screenshot hasil praktikum
( style.css )

# Gaya Teks dan To-do List
![img14](<images/img 14.png>)

# Tampilan Workshop dan Responsif
![img15](<images/img 15.png>)
![img16](<images/img 16.png>)
![img17](<images/img 17.png>)
![img18](<images/img 18.png>)

# Tampilan hasil di web
![img20](<images/img 20.png>)

# Cara Menjalankan

Pastikan file index.html, style.css, dan script.js berada dalam folder yang sama.

Buka folder proyek menggunakan Visual Studio Code.

Pastikan file HTML sudah terhubung dengan file CSS dan JavaScript.

Jalankan file index.html menggunakan browser, atau melalui ekstensi Live Server di Visual Studio Code.

Uji setiap fitur yang tersedia pada halaman web untuk memastikan semuanya berfungsi dengan baik.

# Langkah Kerja

1. Membuat struktur halaman web pada file `index.html` yang berisi elemen HTML untuk manipulasi DOM, tombol interaksi, form pendaftaran, daftar tugas, dan form workshop.
2. Membuat file `script.js` untuk mengatur interaksi halaman menggunakan JavaScript DOM dan event handling.
3. Menambahkan event `click` untuk menjalankan aksi tombol dan mengubah teks pada halaman.
4. Menambahkan fitur perubahan gaya teks dan penghitung jumlah karakter menggunakan event `input`.
5. Membuat validasi form pendaftaran untuk memeriksa nama, email, dan usia sebelum menampilkan pesan hasil validasi.
6. Membuat fitur To-do List agar pengguna dapat menambahkan tugas, menandai tugas sebagai selesai, dan menghapus tugas.
7. Membuat validasi form workshop, menampilkan sesi yang dipilih, dan menghitung jumlah karakter nama.
8. Menambahkan fitur tampil/sembunyi paragraf menggunakan JavaScript dan kelas CSS.
9. Membuat file `style.css` untuk mengatur tampilan elemen, formulir, tombol, daftar tugas, serta menyesuaikan tampilan pada perangkat mobile.
10. Menjalankan halaman web di browser dan menguji setiap fitur untuk memastikan semuanya berjalan dengan baik.
11. Mengambil screenshot hasil program dan kode sebagai dokumentasi praktikum.