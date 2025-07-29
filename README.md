# 2B-PakAR-DasarAlgoritmaDanPemograman

**1. Dokumentasi Teknis
   struktur file/kode**
Aplikasi ini terdiri dari satu file Python utama, inventory_app.py, dan satu file data inventory.json yang akan dibuat secara otomatis saat aplikasi dijalankan dan data ditambahkan.
1. inventory_app.py:
   1. berisi semua logika aplikasi, termasuk fungsi untuk menanbah, menampilkan, mengedit,mengahapus, mencari mengekspor, dan membuat laporan barang.
   2. Fungsi main() mengelola menu interaktif dan alur aplikasi
  
2. Inventory,ison:
   1. File ini digunakan untuk menyimpan data inventory secara persisten dalam format JSON. Setiap kali aplikasi ditutup dan dibuka kembali, data akan tetep tersedia


**2. Library yang Digunakan**
Aplikasi ini menggunakan library standar phyton berikut:
1. json: Digunakan untuk membaca dan menulis data inventori ke/dari file inventory.json.
2. os: Digunakan untuk memeriksa keberadaan file inventory.json saat aplikasi pertama kali dijalankan atau saat memuat data


**Diagram Alur Kerja Aplikasi**
+----------------+
|     Mulai      |
+----------------+
        |
        v
+----------------+
| Muat Inventori |
| (inventory.json)|
+----------------+
        |
        v
+----------------+
|   Tampilkan    |
|      Menu      |
+----------------+
        |
        v
+----------------+
|   Pilih Opsi   |
+----------------+
        |
        |---- 1. Tambah Barang ----> +----------------+
        |                            |   Input Data   |
        |                            | (Nama, Stok, Harga) |
        |                            +----------------+
        |                                   |
        |                                   v
        |                            +----------------+
        |                            | Simpan Data    |
        |                            | ke Inventori   |
        |                            +----------------+
        |                                   |
        |                                   v
        |                            +----------------+
        |                            | Simpan Inventori|
        |                            | (inventory.json)|
        |                            +----------------+
        |                                   |
        |-----------------------------------+
        |
        |---- 2. Tampilkan Daftar Barang --> +----------------+
        |                                    | Tampilkan Semua|
        |                                    | Barang         |
        |                                    +----------------+
        |                                           |
        |-------------------------------------------+
        |
        |---- 3. Edit Barang --------> +----------------+
        |                             | Pilih Barang   |
        |                             | (berdasarkan No.)|
        |                             +----------------+
        |                                   |
        |                                   v
        |                             +----------------+
        |                             | Input Data Baru|
        |                             +----------------+
        |                                   |
        |                                   v
        |                             +----------------+
        |                             | Perbarui Data  |
        |                             | di Inventori   |
        |                             +----------------+
        |                                   |
        |                                   v
        |                             +----------------+
        |                             | Simpan Inventori|
        |                             | (inventory.json)|
        |                             +----------------+
        |                                   |
        |-----------------------------------+
        |
        |---- 4. Hapus Barang -------> +----------------+
        |                             | Pilih Barang   |
        |                             | (berdasarkan No.)|
        |                             +----------------+
        |                                   |
        |                                   v
        |                             +----------------+
        |                             | Konfirmasi     |
        |                             | Penghapusan    |
        |                             +----------------+
        |                                   |
        |                                   v
        |                             +----------------+
        |                             | Hapus Data     |
        |                             | dari Inventori |
        |                             +----------------+
        |                                   |
        |                                   v
        |                             +----------------+
        |                             | Simpan Inventori|
        |                             | (inventory.json)|
        |                             +----------------+
        |                                   |
        |-----------------------------------+
        |
        |---- 5. Cari Barang --------> +----------------+
        |                             | Input Nama     |
        |                             | Barang Dicari  |
        |                             +----------------+
        |                                   |
        |                                   v
        |                             +----------------+
        |                             | Tampilkan Hasil|
        |                             | Pencarian      |
        |                             +----------------+
        |                                   |
        |-----------------------------------+
        |
        |---- 6. Ekspor ke CSV ------> +----------------+
        |                             | Tulis Data     |
        |                             | ke inventory_report.csv |
        |                             +----------------+
        |                                   |
        |-----------------------------------+
        |
        |---- 7. Laporan Inventori ----> +----------------+
        |                               | Hitung Total   |
        |                               | Barang & Nilai |
        |                               +----------------+
        |                                     |
        |-------------------------------------+
        |
        |---- 8. Keluar -------------------> +----------------+
        |                                    |     Selesai    |
        +------------------------------------+----------------+



**2. User Manual**
**Cara Menjalankan Aplikasi**
1. Pastikan Python Terinstal: Anda perlu memiliki Python 3.x terinstal di komputer Anda. Anda bisa mengunduhnya dari python.org.
2. Simpan Kode: Salin kode Python yang disediakan ke dalam sebuah file dan simpan dengan nama inventory_app.py (atau nama lain dengan ekstensi .py).
3. Buka Terminal/Command Prompt: Navigasikan ke direktori tempat Anda menyimpan file inventory_app.py menggunakan terminal (Linux/macOS) atau Command Prompt/PowerShell (Windows).
4. Contoh: cd C:\Users\NamaAnda\Documents\ProyekInventori
Jalankan Aplikasi: Ketik perintah berikut dan tekan Enter:
python inventory_app.py
5. Aplikasi akan menampilkan menu utama di terminal.


**Contoh Input**
Setelah aplikasi berjalan, Anda akan melihat menu utama. Berikut adalah contoh interaksi:

Menambah Barang:

Pilih opsi 1 (Tambah Barang).

Aplikasi akan meminta:

Masukkan Nama Barang: (misal: susu nasional)
Masukkan Stok Barang: (misal: 7)
Masukkan Harga Barang: (misal: 1000)
Barang akan ditambahkan dan disimpan.
Menampilkan Daftar Barang:

Pilih opsi 2 (Tampilkan Daftar Barang).
Aplikasi akan menampilkan semua barang yang ada di inventori dalam bentuk tabel.

Cara Edit & Hapus Data
Mengedit Data Barang:

Pilih opsi 3 (Edit Barang).
Aplikasi akan menampilkan daftar barang dengan nomor urut.
Masukkan Nomor Barang yang ingin diedit: (misal: 1 untuk barang pertama).
Aplikasi akan menampilkan detail barang tersebut dan meminta input untuk nama, stok, dan harga baru.
Anda bisa mengosongkan input (tekan Enter langsung) jika Anda tidak ingin mengubah nilai tersebut.
Setelah Anda memasukkan perubahan, data barang akan diperbarui.

Menghapus Data Barang:
11. Pilih opsi 4 (Hapus Barang).
12. Aplikasi akan menampilkan daftar barang dengan nomor urut.
13. Masukkan Nomor Barang yang ingin dihapus: (misal: 2 untuk barang kedua).
14. Aplikasi akan meminta konfirmasi: Anda yakin ingin menghapus 'Nama Barang'? (ya/tidak):
* Ketik ya dan tekan Enter untuk mengonfirmasi penghapusan.
* Ketik tidak atau apapun selain ya untuk membatalkan.
15. Jika dikonfirmasi, barang akan dihapus dari inventori.


Fitur Bonus
Pencarian Barang:

Pilih opsi 5 (Cari Barang).
Masukkan Nama Barang yang dicari: (misal: susu nasional).
Aplikasi akan menampilkan semua barang yang namanya mengandung kata "susu" (tidak peka huruf besar/kecil).

Laporan Ringkas:

Pilih opsi 6 (Laporan Inventori).
Aplikasi akan menampilkan ringkasan seperti jumlah total barang unik, total stok, dan total nilai inventori.

.**3. Pengujian & Evaluasi (Contoh Skenario)**
Berikut adalah contoh skenario pengujian yang dapat Anda lakukan:
1. Skenario 1: Tambah dan Hapus Barang
  Mulai Aplikasi: Jalankan python inventory_app.py.
2. Tambah Barang 1:
Pilih 1.
Nama: susu nasional, Stok: 7, Harga: 1000.
Verifikasi pesan "Barang 'susu nasional' berhasil ditambahkan."
3. Tampilkan Daftar Barang:
Pilih 1.
4. Pastikan "susu nasional" muncul dalam daftar dengan stok dan harga yang benar.
Hapus Barang 1 (susu nasional):
Pilih 4.
Masukkan nomor 1 (untuk susu nasional.
Konfirmasi ya.
Verifikasi pesan "Barang 'susu nasional' berhasil dihapus."
5. Tampilkan Daftar Barang:
Pilih 2.
Pastikan hanya "susu nusantara dan susu latte" yang tersisa dalam daftar.
6. Keluar: Pilih 8.
7. jalankan Ulang Aplikasi: Jalankan python inventory_app.py lagi.
8. Tampilkan Daftar Barang:
Pilih 2.
Pastikan "susu naional" masih ada, menunjukkan data berhasil disimpan dan dimuat.


**Skenario 2: Edit Barang dan Laporan**
1. Mulai Aplikasi: Jalankan python inventory_app.py. (Pastikan ada data, jika tidak, tambahkan beberapa barang terlebih dahulu).
2. Tambah Barang (jika inventori kosong):
Pilih 1. Nama: susu nasional, Stok: 7, Harga: 1000.
3. Tampilkan Daftar Barang:
Pilih 2. Catat nomor urut untuk "susu nasional".
4. Edit Barang "susu nasional":
Pilih 3. Masukkan nomor urut "1".
Nama Baru: (kosongkan)
Stok Baru: (kosongkan)
Harga Baru: (kosongkan)
5. Tampilkan Daftar Barang:
Pilih 1. Pastikan "susu nasional" sekarang memiliki Stok 7 dan Harga 1000.
6. Generate Laporan:
Pilih 7.
Periksa Jumlah Barang Unik, Total Stok Semua Barang, dan Total Nilai Inventori sesuai dengan data yang ada (termasuk perubahan pada "susu").
7.Keluar: Pilih 8.







   
