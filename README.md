WEB INVENTARIS BARANG

Deskripsi
Aplikasi untuk membantu pengelolaan Peminjaman Perangkat Elektronik & IT yakni mencakupi Laptop/Notebook, Mouse, proyektor, Layar Proyektor, kamera digital, speaker portable, dan printer. Aplikasi ini dibuat untuk untuk menunjang kemudahan dalam peminjaman barang.

Setiap perangkat dicatat sebagai unit tersendiri lengkap dengan kode aset, nomor seri, spesifikasi, tanggal pembelian, masa garansi, lokasi penyimpanan, dan kondisinya. Setiap unit dilengkapi QR code agar pencarian dan pencatatan di lapangan lebih cepat.

Alur utama sistem adalah peminjam mengajukan permintaan, petugas atau admin menyetujui, perangkat diserahkan setelah pemeriksaan kelengkapan dan kondisi, lalu dikembalikan dan diperiksa ulang. Seluruh tahapan tercatat otomatis, termasuk perhitungan keterlambatan, denda, dan riwayat perawatan tiap unit. Dashboard dan laporan membantu pengelola melihat ketersediaan, perangkat yang terlambat, serta perangkat yang sering rusak.

Latar Belakang

Perangkat elektronik dan IT merupakan aset bernilai tinggi yang menunjang kegiatan belajar mengajar, penelitian, maupun operasional kerja. Seiring bertambahnya jumlah perangkat dan jumlah pengguna, pengelolaan aset ini menjadi semakin kompleks. Di banyak instansi, pencatatan inventaris dan peminjaman masih dilakukan secara manual melalui buku catatan atau lembar spreadsheet yang terpisah-pisah. Pengelolaan manual tersebut menimbulkan sejumlah permasalahan, contohnya seperti data tidak akurat dan sulit ditelusuri, resiko kehilangan dan kerusakan, adanya jadwal bentrok, keterlambatan pengembalian tidak terpantau, perawatan tidak terjadwal, dan pelaporan yang memakan waktu.

Tujuan 
1. Membuat sistem peminjaman online inventaris barang berbasis web 
2. Memudahkan dalam pengelolaan data kategori barang
3. Memudahkan dalam mengetahui barang masuk dan keluar
4. Mengetahui status barang peminjaman dan riwayat barang peminjaman
5. membuat data peminjaman lebih efisien dan terstruktur

Target Pengguna
- Admin: mengelola data, user , laporan, dan pengaturan sistem
- Peminjam: melihat katalog perangkat, mengajukan atau memesan peminjaman, dan memantau status serta riwayat pinjamannya.
- Petugas: memproses serah terima dan pengembalian, memeriksa kondisi perangkat, serta mencatat perawatan dan perbaikan.

Fitur Utama
- Login, registrasi, dan logout
- Dashboard 
- Katalog Barang beserta jumlah unit tersedia
- Detail Barang
- Form Peminjaman
- Pengelolaan data barang (tambah, ubah, hapus)
- Pengelolaan data kategori, jenis, dan lokasi
- Pengelolaan data peminjaman
- Status Peminjaman (diajukan, disetujui, dipinjam, dikembalikan, terlambat, ditolak)
- Perhitungan denda keterlambatan atau kerusakan
- Manajemen pengguna
- Riawayat Transaksi
- Laporan dan cetak bukti peminjaman

Fitur Tambahan:
- Scan QR Code untuk cek barang atau proses pinjam dengan cepat
- Search bar
- Notifikasi dan pengingat jatuh tempo
- ID/kode asetr unik untuk setiap barang
- Batas waktu peminjaman 3 hari 
- Log aktivitas sistem 

Data Utana
1. Users: Data pengguna dan peran (admin, petugas, peminjaman)
2. Kategori barang: Laptop/Notebook, Mouse, proyektor, Layar Proyektor, kamera digital, speaker portable, dan printer
3. Asset: Unit fisik: kode aset, nomor seri, spesifikasi, tanggal beli, garansi, kondisi, lokasi
4. Loans: Transaksi peminjaman: peminjam, unit, tanggal pinjam, jatuh tempo, tanggal kembali, status, kondisi keluar/kembali
5. Fines: Denda keterlambatan atau kerusakan
6. Logs: Catatan altivitas pengguna


Teknologi 
- HTML5 untuk struktur halaman
- CSS3 untuk tampilan dan responsivitas
- JavaScript untuk tanggal/waktu, validasi ringan, atau interaksi antarmuka
- PHP native untuk logika aplikasi
- MySQL atau MariaDB untuk penyimpanan data
- jQuery dan AJAX untuk pagination data
- Git dan GitHub/GitLab untuk version control
- Hosting untuk publikasi aplikasi akhir

Struktur Folder Awal

pinjamin/
├── index.php
├── config/
│   └── database.php
├── includes/
│   ├── auth.php              # session + cek role
│   ├── header.php
│   ├── footer.php
│   └── functions.php         # hitung denda, catat log, format tanggal
├── auth/
│   ├── login.php
│   ├── register.php
│   └── logout.php
├── admin/
│   ├── dashboard.php
│   ├── master/
│   │   ├── categories.php
│   │   ├── locations.php
│   │   └── users.php
│   ├── models/               # CRUD jenis perangkat
│   │   ├── index.php
│   │   ├── create.php
│   │   ├── edit.php
│   │   └── delete.php
│   ├── assets/               # CRUD unit fisik
│   │   ├── index.php
│   │   ├── create.php
│   │   ├── edit.php
│   │   ├── delete.php
│   │   ├── detail.php        # riwayat pinjam + servis unit ini
│   │   └── qr.php            # cetak label QR
│   ├── loans/
│   │   ├── index.php
│   │   ├── approve.php
│   │   ├── handover.php      # serah terima (kondisi keluar)
│   │   ├── return.php        # pengembalian (kondisi kembali + denda)
│   │   └── print.php         # cetak bukti peminjaman
│   ├── maintenance/
│   │   ├── index.php
│   │   ├── create.php
│   │   └── finish.php
│   ├── fines.php
│   ├── reports.php
│   └── logs.php
├── staff/                    # halaman petugas (atau pakai folder admin dengan cek role)
│   ├── dashboard.php
│   └── scan.php              # scan QR serah terima/pengembalian
├── user/
│   ├── dashboard.php
│   ├── catalog.php           # daftar model + jumlah unit tersedia
│   ├── model_detail.php
│   ├── borrow.php
│   ├── my_loans.php
│   └── notifications.php
├── api/                      # endpoint AJAX (pagination, search, notifikasi)
│   ├── search.php
│   └── paginate.php
└── assets-web/               # supaya tidak bentrok dengan folder admin/assets
    ├── css/style.css
    ├── js/app.js
    └── uploads/

Ide pengembangan Sesuai Target
- Sekolah/Kampus: peminjaman alat lab, proyektor, ruang kelas
- Kantor: inventaris laptop, kendaraan operasional
- Komunitas/Perpustakaan: peminjaman buku dan alat
- Rental kecil: kamer

  
Halaman Awal 


Status Pengembangan


Repository

Pengembangan Lanjutan 
