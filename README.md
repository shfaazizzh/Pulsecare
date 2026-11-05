# PULSECARE: SISTEM INFORMASI MANAJEMEN PASIEN RAWAT JALAN 
PulseCare merupakan sistem informasi pelayanan pasien rawat jalan yang dirancang untuk mempermudah proses administrasi dan pelayanan kesehatan. Sistem ini mencakup pengelolaan data pasien, pendaftaran kunjungan, antrean, pemeriksaan dokter, pencatatan rekam medis, diagnosis, serta resep obat sehingga proses pelayanan pasien dapat berjalan lebih teratur dan terstruktur.

# Fitur Utama Program
- Login dan Logout - Pegawai masuk dan keluar sesuai hak akses.
- Pengelolaan Akun Pegawai - Admin mengelola akun dan menetapkan role.
- Pengelolaan Data Pasien - Petugas menambah dan mengelola data pasien.
- Pendaftaran Kunjungan - Petugas mendaftarkan kunjungan pasien.
- Pemberian Nomor Antrean -  Sistem memberikan nomor antrean saat pendaftaran.
- Pengelolaan Antrean Dokter - Dokter melihat dan memilih pasien yang akan diperiksa.
- Catatan Tindak Lanjut - Dokter mencatat rekomendasi setelah pemeriksaan.
- Pembaruan Status Kunjungan - Status kunjungan diperbarui sesuai proses pelayanan.

# Tech Stack

| Teknologi | Keterangan |
|---|---|
| Java | Bahasa pemrograman untuk membangun aplikasi desktop. |
| MySQL | Database untuk menyimpan dan mengelola data sistem. |
| SQL | Digunakan untuk mengelola data dalam database. |
| Java Swing | Digunakan untuk membuat tampilan antarmuka aplikasi desktop. |

# Perancangan Sistem
## Use Case 
<details>
<summary>Use Case </summary>
  <img width="1683" height="1515" alt="Usecase dan Flowchart-Menu Utama drawio" src="https://github.com/user-attachments/assets/4fe3982d-48cd-493e-9433-550a107547ef" />
Sistem PulseCare memiliki tiga pengguna, yaitu Admin, Petugas, dan Dokter yang wajib melakukan login sebelum menggunakan sistem. Admin bertugas mengelola akun dan menetapkan role pengguna, Petugas mengelola data pasien serta pendaftaran kunjungan, sedangkan Dokter melakukan pemeriksaan dan mencatat hasil pemeriksaan serta diagnosis. Selain itu, Dokter dapat membuat resep obat dan catatan tindak lanjut jika diperlukan. Petugas dan Dokter juga dapat melihat riwayat serta memperbarui status kunjungan pasien agar proses pelayanan dapat dipantau dengan baik.
</details>



## Flowchart
<details>
<summary>1. Flowchart Login</summary>

<img width="1683" height="1515" alt="Usecase dan Flowchart-Menu Utama drawio" src="https://github.com/user-attachments/assets/a56831da-64b2-425a-b42e-c7c6b56778d1" />

pada flowchart ini mengambarkan proses login pada sistem PulseCare, dimulai dari pengguna memasukkan username dan password yang kemudian divalidasi oleh sistem melalui database. Pengguna diberikan maksimal tiga kali percobaan login, dan jika seluruhnya gagal, akun akan dikunci sementara selama 10 detik. Jika login berhasil, sistem akan memeriksa role pengguna dan mengarahkannya ke Dashboard Admin, Petugas, atau Dokter sesuai hak akses masing-masing. Pengguna juga dapat keluar dari sistem melalui fitur logout.
</details>

<details>
<summary>2. Flowchart Dashboard admin</summary>
<img width="1040" height="348" alt="Usecase dan Flowchart-Dashboard Admin drawio" src="https://github.com/user-attachments/assets/a8567bf9-d8c7-4201-9eda-f799d117c1e4" />

Pada flowchart ini menggambarkan proses pada Dashboard Admin PulseCare. Setelah berhasil login, sistem menampilkan ringkasan akun dan aktivitas akun terbaru. Selanjutnya, Admin dapat memilih untuk mengelola akun pengguna. Jika memilih tidak, Admin dapat keluar melalui fitur logout. Jika memilih ya, sistem akan mengarahkan Admin ke menu Kelola Akun User untuk melakukan pengelolaan akun pengguna.
</details>

<details>
<summary>3. Flowchart Dashboard Petugas</summary>

<img width="1966" height="365" alt="Dashboard Petugas drawio" src="https://github.com/user-attachments/assets/aa55985b-78cd-4d90-8186-a58f061798ea" />
Pada flowchart ini menggambarkan proses kerja Petugas pada Dashboard PulseCare. Setelah login, sistem menampilkan ringkasan kunjungan dan antrean pasien hari ini. Petugas dapat mengelola data pasien, mendaftarkan kunjungan, memperbarui status kunjungan, serta melihat riwayat kunjungan pasien. Setiap fitur dapat dipilih sesuai kebutuhan pelayanan. Jika tidak ingin menggunakan fitur lainnya, Petugas dapat mengakhiri aktivitas dengan memilih menu Logout.
</details>

<details>
<summary>4. Flowchart Dashboard Dokter</summary>

<img width="1605" height="365" alt="Dashboard Dokter drawio" src="https://github.com/user-attachments/assets/b3fbffd5-620e-455c-b095-4751d91680c6" />
Pada flowchart ini menggambarkan proses kerja Dokter pada Dashboard PulseCare. Setelah login, sistem menampilkan informasi pasien berikutnya dan daftar antrean yang harus diperiksa. Dokter dapat melihat antrean pasien, memperbarui status kunjungan sesuai proses pemeriksaan, serta melihat riwayat kunjungan pasien. Setiap fitur dapat dipilih sesuai kebutuhan pelayanan. Jika seluruh aktivitas telah selesai, Dokter dapat keluar dari sistem melalui menu Logout.
</details>

<details>
<summary>5. Flowchart (Admin) Kelola Akun User</summary>

<img width="2753" height="2685" alt="(Admin) Kelola Akun User drawio" src="https://github.com/user-attachments/assets/e73bd7c3-1bd3-47c0-9548-efd9aa5fa123" />
Pada flowchart ini menggambarkan proses pengelolaan akun pengguna oleh Admin pada sistem PulseCare. Sistem terlebih dahulu menampilkan daftar akun yang tersimpan di database, kemudian Admin dapat menambahkan akun baru, mencari akun berdasarkan kata kunci, mengubah data akun, atau menonaktifkan akun pengguna. Saat menambahkan akun, Admin harus mengisi nama, username, password, dan role serta menetapkan hak akses sesuai peran pengguna. Sistem akan memvalidasi data sebelum menyimpannya ke database. Jika proses berhasil, sistem menampilkan notifikasi dan memperbarui daftar akun. Jika Admin tidak memilih tindakan lainnya, proses akan kembali ke Dashboard Admin.
</details>

<details>
<summary>6. Flowchart (Petugas 1) Kelola Data Pasien</summary>

<img width="2687" height="2410" alt="(Petugas 1) Kelola Data Pasien drawio" src="https://github.com/user-attachments/assets/94387ab2-5394-43fe-914c-36ba076ccb48" />
Pada flowchart ini menggambarkan proses pengelolaan data pasien oleh Petugas pada sistem PulseCare. Sistem menampilkan daftar pasien beserta fitur tambah, ubah, hapus, dan pencarian data. Petugas dapat menambahkan pasien baru, memperbarui data pasien dengan mengisi informasi seperti nama, NIK, tanggal lahir, jenis kelamin, alamat, nomor HP, dan status BPJS, kemudian sistem melakukan validasi sebelum menyimpan perubahan ke database. Petugas juga dapat menghapus data pasien, tetapi pasien yang masih memiliki kunjungan aktif tidak dapat dihapus. Selain itu, tersedia fitur pencarian pasien berdasarkan nama, NIK, atau ID pasien agar data lebih mudah ditemukan.
</details>

<details>
<summary>7. Flowchart (Petugas) Tambah Pasien Baru</summary>

<img width="2026" height="1045" alt="(Petugas) Tambah Pasien Baru  drawio" src="https://github.com/user-attachments/assets/b727ef01-7745-4057-9a9e-e7cc99563630" />
Pada flowchart ini i menggambarkan proses penambahan pasien baru pada sistem PulseCare. Petugas mengisi formulir yang berisi nama, NIK, tanggal lahir, jenis kelamin, alamat, nomor HP, dan status BPJS. Sistem kemudian memvalidasi nomor HP yang harus terdiri dari 10–13 digit dan NIK sebanyak 16 digit serta memastikan NIK belum terdaftar. Jika data valid, sistem membuat ID pasien dan menyimpan data ke database. Setelah berhasil disimpan, sistem menampilkan notifikasi bahwa data pasien berhasil ditambahkan dan Petugas dapat memilih untuk melanjutkan ke pendaftaran kunjungan atau kembali ke menu Kelola Data Pasien. Jika data tidak valid atau gagal disimpan, sistem akan menampilkan pesan kesalahan.
</details>

<details>
<summary>8. Flowchart (Petugas2) Daftarkan Kujungan</summary>

<img width="1745" height="1175" alt="(Petugas 2) Daftarkan Kunjungan drawio" src="https://github.com/user-attachments/assets/8ee1e9c7-b67a-4fa7-bf25-d8c8736beafc" />
Pada flowchart ini menggambarkan proses pendaftaran kunjungan pasien pada sistem PulseCare. Petugas terlebih dahulu mencari pasien berdasarkan nama, NIK, atau ID pasien. Sistem akan memeriksa data pasien melalui database. Jika kata kunci kosong, sistem meminta Petugas mengisinya terlebih dahulu. Jika pasien ditemukan dan terdaftar, Petugas dapat memilih pasien lalu melanjutkan proses pendaftaran kunjungan. Namun, jika pasien belum terdaftar, sistem memberikan pilihan untuk menambahkan pasien baru atau kembali ke menu sebelumnya.
</details>

<details>
<summary>9. Flowchart Daftarkan Kujungan2</summary>

<img width="1968" height="1325" alt="Daftarkan Kunjungan (2) drawio" src="https://github.com/user-attachments/assets/03def17e-4d46-4c89-a364-b4e835304610" />
Pada flowchart ini menggambarkan proses pendaftaran kunjungan pasien pada sistem PulseCare. Petugas memilih poli tujuan, kemudian sistem memvalidasi kelengkapan data dan memeriksa apakah pasien sudah memiliki kunjungan aktif pada poli dan tanggal yang sama. Jika tidak ditemukan kunjungan ganda, Petugas melakukan konfirmasi data pasien dan kunjungan. Selanjutnya, sistem menyimpan data ke database, membuat nomor antrean berdasarkan tanggal dan urutan pendaftaran, serta menetapkan status kunjungan menjadi menunggu. Jika pendaftaran berhasil, sistem menyimpan data secara permanen dan menampilkan tiket nomor antrean. Petugas juga dapat melanjutkan pendaftaran pasien lain atau kembali ke Dashboard Petugas. Jika proses gagal, sistem membatalkan pendaftaran dan menampilkan notifikasi kesalahan.
</details>

<details>
<summary>10. Flowchart Petugas dan Dokter Lihat Riwayat kunjungan </summary>

<img width="1082" height="1320" alt="(Petugas dan Dokter) Lihat Riwayat Kunjungan drawio" src="https://github.com/user-attachments/assets/2c8bad01-1a44-4f90-aa32-38f6d98eab81" />
Pada flowchart ini menggambarkan proses melihat riwayat kunjungan pasien pada sistem PulseCare. Petugas memasukkan waktu daftar pada kolom pencarian, kemudian sistem memeriksa data di database. Jika data kosong, sistem menampilkan informasi belum ada riwayat kunjungan. Jika tersedia, sistem menampilkan detail riwayat berupa tanggal daftar, poli, dokter, nomor antrean, dan status. Petugas kemudian dapat tetap berada di halaman atau kembali ke Dashboard Petugas maupun Dashboard Dokter sesuai dengan role pengguna.
</details>

<details>
<summary>11. Flowchart (Petugas dan Dokter) Perbarui Status Kunjungan. </summary>

<img width="2709" height="1447" alt="Petugas dan Dokter) Perbarui Status Kunjungan drawio" src="https://github.com/user-attachments/assets/a9b6b5a0-df0e-43b5-933d-d477687ef49e" />
Pada flowchart ini menggambarkan proses memperbarui status kunjungan pasien pada sistem PulseCare. Sistem menampilkan daftar kunjungan hari ini dari database. Petugas memilih data kunjungan dan menentukan status baru, yaitu Menunggu, Sedang Diperiksa, atau Selesai. Setelah disimpan, sistem memvalidasi perubahan status dan memeriksa apakah data telah diubah oleh petugas lain. Jika berhasil, sistem menyimpan status baru dan menampilkan notifikasi bahwa status kunjungan berhasil diperbarui. Jika perubahan tidak diperbolehkan, sistem menampilkan peringatan.
</details>

<details>
<summary>12. Flowchart (Dokter 1) Antrean Dokter </summary>
  
<img width="2105" height="1131" alt="(Dokter 1) Antrean Dokter drawio" src="https://github.com/user-attachments/assets/1bae8d65-bf86-4ca5-9438-2ef02ccab93d" />
Pada flowchart ini menggambarkan proses dokter melihat antrean pasien pada sistem PulseCare. Sistem menampilkan daftar antrean dengan status Menunggu dari database. Jika tidak ada antrean, sistem menampilkan informasi bahwa tidak ada antrean. Jika tersedia, sistem menampilkan tabel berisi nomor antrean, pasien, keluhan, dan status. Dokter kemudian dapat kembali ke Dashboard Dokter atau memilih antrean untuk diperiksa. Sistem memeriksa apakah kunjungan sedang dibuka oleh dokter lain. Jika iya, sistem menampilkan peringatan. Jika tidak, sistem mengunci kunjungan untuk dokter tersebut, mengubah status menjadi Sedang Diperiksa, lalu mengarahkan dokter ke halaman Form Pemeriksaan.
</details>

<details>
<summary>13. Flowchart (Dokter) Form Pemeriksaan </summary>
  
<img width="1434" height="1830" alt="(Dokter) Form Pemeriksaan drawio" src="https://github.com/user-attachments/assets/1cf4d14b-1bbf-4b2e-ae96-1d9a741cdf92" />
Pada flowchart ini menggambarkan proses pemeriksaan pasien pada sistem PulseCare. Dokter melihat data pasien dan riwayat singkat, kemudian mengisi hasil pemeriksaan, diagnosis, serta resep obat jika diperlukan. Dokter juga dapat menambahkan catatan tindak lanjut berupa rekomendasi dan saran pemeriksaan. Setelah selesai, sistem memvalidasi kelengkapan hasil pemeriksaan dan diagnosis. Jika sudah lengkap, sistem menyimpan rekam medis, resep, dan tindak lanjut ke database, kemudian mengubah status kunjungan menjadi Selesai serta menampilkan notifikasi bahwa pemeriksaan berhasil diselesaikan.
</details>
