# AplikasiPenghitungUmur
 Latihan 2 - Ferdhyan Dwi Rangga Saputra (2210010171)
 
Aplikasi Penghitung Umur yaitu aplikasi GUI berbasis Java yang memungkinkan pengguna untuk menghitung umur berdasarkan tanggal lahir dan mendapatkan informasi tentang peristiwa penting pada tanggal ulang tahunnya. Aplikasi ini juga dapat menerjemahkan deskripsi peristiwa penting ke dalam bahasa Indonesia.

## Fitur Utama

1. Menghitung Umur: Aplikasi menghitung umur dalam format tahun, bulan, dan hari.
2. Menampilkan Hari Ulang Tahun Berikutnya: Menunjukkan kapan ulang tahun berikutnya dan hari apa ulang tahun itu jatuh.
3. Mendapatkan Peristiwa Penting: Mengambil peristiwa sejarah penting pada tanggal ulang tahunnya menggunakan API eksternal.
4. Terjemahan Deskripsi Peristiwa: Deskripsi peristiwa penting yang didapatkan diterjemahkan ke dalam bahasa Indonesia.

## Struktur Kode

### 1. `PenghitungUmurFrame.java`

File utama yang berfungsi sebagai GUI dari aplikasi. Kelas ini menampilkan antarmuka pengguna, menangani input, dan menampilkan hasil.

#### Komponen Penting

- `dateChooserTanggalLahir`: Digunakan untuk memilih tanggal lahir pengguna.
- `txtUmur`: Menampilkan umur pengguna.
- `txtHariUlangTahunBerikutnya`: Menampilkan hari dan tanggal ulang tahun berikutnya.
- `txtAreaPeristiwa`: Menampilkan peristiwa penting pada tanggal ulang tahunnya.

#### Metode Utama

- `jButton1ActionPerformed()`: Menghitung umur pengguna, hari ulang tahun berikutnya, dan memulai thread untuk mengambil data peristiwa penting secara asinkron.
- `jButton2ActionPerformed()`: Keluar dari aplikasi.
- `dateChooserTanggalLahirPropertyChange()`: Membersihkan hasil saat tanggal lahir diubah.

### 2. `PenghitungUmurHelper.java`

Kelas helper untuk menghitung umur, mendapatkan tanggal ulang tahun berikutnya, dan mengambil data peristiwa penting dari API eksternal.

#### Metode Utama

- `hitungUmurDetail()`: Menghitung umur dalam tahun, bulan, dan hari.
- `hariUlangTahunBerikutnya()`: Menghitung kapan ulang tahun berikutnya berdasarkan tanggal lahir.
- `getDayOfWeekInIndonesian()`: Mengembalikan hari dalam bahasa Indonesia.
- `getPeristiwaBarisPerBaris()`: Mengambil peristiwa penting berdasarkan tanggal dan menampilkannya di `txtAreaPeristiwa`.
- `translateToIndonesian()`: Menerjemahkan deskripsi peristiwa ke dalam bahasa Indonesia menggunakan API eksternal.

## API Eksternal

1. **byabbe.se API**: Mengambil data peristiwa penting pada tanggal tertentu.
2. **Lingva Translate API**: Menerjemahkan deskripsi peristiwa ke dalam bahasa Indonesia.

### Catatan

Aplikasi ini memerlukan koneksi internet aktif untuk mengambil data peristiwa penting dan menerjemahkan deskripsi.
