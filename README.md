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
- ID/kode aset unik untuk setiap barang
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

PinjamIn
|___ LOGIN
|____|___ USER (PEMINJAM)
|____|____|____ Dashboard
|____|____|____ Katalog Barang
|____|____|____|_____ Form Peminjaman
|____|____|____ Peminjaman saya
|____|____|____ Riwayat
|____|____|____ Profil
|____|____ADMIN
     |____|____ Dashboard admin
     |____|____ Data barang (data barang)
     |____|____ Peminjaman (kelola peminjaman)
     |____|____ |____ Proses pengembalian
     |____|____ Riwayat
     |____|____ Profil

Ide pengembangan Sesuai Target
- Sekolah/Kampus: peminjaman alat lab, proyektor, ruang kelas
- Kantor: inventaris laptop, kendaraan operasional
- Komunitas/Perpustakaan: peminjaman buku dan alat
  
Halaman Awal 
Halaman awal ini dirancang untuk mempermudah user dalam memantau dan meminjam fasilitas atau aset yang tersedia. User dapat mengecek ketersediaan barang secara real-time, mengajukan permohonan pinjam, serta melihat riwayat pengembalian secara mandiri di sini. Terdapat tombol Login/Daftar, serta ringkasan katalog perangkat yang tersedia. 

Status Pengembangan
1. Perancangan database (SELESAI)
2. Login dan manajemen pengguna (PROSES)
3. Data master (kategori barang, model, unit) (PROGRES)
4. Katalog dan from peminjaman (PROGRES)
5. Persetujuan, pengembalian (PROGRES)
6. Denda dan perawatan (BELUM)
7. QR code (BELUM)
8. Pengujian dan hosting (PROGRES)

Repository
1. Repository: https://github.com/Fachrycyber17/Project-web-Inventaris-barang/edit/main/README.md
2. Tautan web: 
3. Akun uji coba: user (peminjam), admin, petugas (CANTUMKAN USERNAME, PASSWORD)

Pengembangan Lanjutan 
1. Kalender reservasi untuk melihat jadwal pemakaian barang
2. Ekspor laporan ke PDF dan Excel
3. Penjadwalan perawatan berkala otomatis
