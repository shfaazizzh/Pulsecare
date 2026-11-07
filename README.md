# PULSECARE: SISTEM INFORMASI MANAJEMEN PASIEN RAWAT JALAN 
PulseCare merupakan sistem informasi pelayanan pasien rawat jalan yang dirancang untuk mempermudah proses administrasi dan pelayanan kesehatan. Sistem ini mencakup pengelolaan data pasien, pendaftaran kunjungan, antrean, pemeriksaan dokter, pencatatan rekam medis, diagnosis, serta resep obat sehingga proses pelayanan pasien dapat berjalan lebih teratur dan terstruktur.

# Fitur Utama Program
- Login dan Logout - Pegawai masuk dan keluar sesuai hak akses.
- Pengelolaan Akun Pegawai - Admin mengelola akun dan menetapkan role.
- Pengelolaan Data Pasien - Pegawai menambah dan mengelola data pasien.
- Pendaftaran Kunjungan - Pegawai mendaftarkan kunjungan pasien.
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
| NetBeans | IDE yang digunakan untuk menulis, menjalankan, dan mengembangkan program Java. |
| Laragon | Digunakan sebagai lingkungan lokal untuk menjalankan dan mengelola database. |
| Canva | Digunakan untuk membuat desain dan kebutuhan visual proyek. |
| Figma | Digunakan untuk merancang tampilan antarmuka dan desain UI/UX. |
| Microsoft Word | Digunakan untuk menyusun laporan dokumentasi proyek. |
| Data Modeler | Digunakan untuk merancang dan memvisualisasikan model database. |

# Perancangan Sistem
## Use Case 
<details>
<summary>Use Case </summary>
 <img width="1023" height="1353" alt="usecase drawio" src="https://github.com/user-attachments/assets/66031506-4b23-498e-ae3c-616d231c4eda" />
Sistem PulseCare memiliki tiga pengguna, yaitu Admin, Petugas, dan Dokter yang wajib melakukan login sebelum menggunakan sistem. Admin bertugas mengelola akun dan menetapkan role pengguna, Petugas mengelola data pasien serta pendaftaran kunjungan, sedangkan Dokter melakukan pemeriksaan dan mencatat hasil pemeriksaan serta diagnosis. Selain itu, Dokter dapat membuat resep obat dan catatan tindak lanjut jika diperlukan. Petugas dan Dokter juga dapat melihat riwayat serta memperbarui status kunjungan pasien agar proses pelayanan dapat dipantau dengan baik.
</details>



## Flowchart
<details>
<summary>1. Flowchart Login</summary>

<img width="1683" height="1515" alt="Usecase dan Flowchart-Menu Utama drawio" src="https://github.com/user-attachments/assets/a56831da-64b2-425a-b42e-c7c6b56778d1" />

Proses PulseCare dimulai dari Menu Utama, tempat pengguna dapat memilih Login atau Keluar. Pengguna yang login harus memasukkan username dan password yang akan divalidasi oleh sistem melalui database. Jika gagal, sistem memberikan maksimal tiga kali percobaan sebelum akun dikunci sementara selama 10 detik. Jika berhasil, pengguna diarahkan ke dashboard sesuai role, yaitu Admin untuk mengelola akun, Petugas untuk mengelola data dan kunjungan pasien, serta Dokter untuk mengelola antrean, melihat riwayat, dan mencatat hasil pemeriksaan. Setiap pengguna dapat melakukan logout untuk mengakhiri sesi dan kembali ke Menu Utama.
</details>

<details>
<summary>2. Flowchart Dashboard admin</summary>
<img width="1040" height="348" alt="Usecase dan Flowchart-Dashboard Admin drawio" src="https://github.com/user-attachments/assets/a8567bf9-d8c7-4201-9eda-f799d117c1e4" />

flowchart untuk dashboard admin. Proses dimulai saat Admin Sistem memasuki Dashboard Admin. Sistem menampilkan ringkasan akun dan aktivitas akun terbaru. Admin Sistem kemudian dapat memilih menu Kelola Akun User untuk mengelola akun pengguna. Jika memilih Ya, sistem akan mengarahkan Admin Sistem ke halaman Kelola Akun User. Jika memilih Tidak, Admin Sistem dapat melakukan logout untuk mengakhiri sesi login.
</details>

<details>
<summary>3. Flowchart Dashboard Petugas</summary>

<img width="1966" height="365" alt="Dashboard Petugas drawio" src="https://github.com/user-attachments/assets/aa55985b-78cd-4d90-8186-a58f061798ea" />
Dashboard Petugas menampilkan ringkasan kunjungan dan antrean pasien hari ini. Petugas dapat mengelola data pasien, mendaftarkan kunjungan ke poliklinik, memperbarui status kunjungan, serta melihat riwayat kunjungan pasien. Jika seluruh aktivitas selesai, Petugas dapat melakukan logout untuk mengakhiri sesi.
</details>

<details>
<summary>4. Flowchart Dashboard Dokter</summary>

<img width="1605" height="365" alt="Dashboard Dokter drawio" src="https://github.com/user-attachments/assets/b3fbffd5-620e-455c-b095-4751d91680c6" />
Dashboard Dokter menampilkan informasi pasien berikutnya dan daftar antrean sesuai poliklinik tempat dokter bertugas. Dokter dapat melihat dan memeriksa pasien melalui menu Antrean Dokter, memperbarui status kunjungan, serta melihat riwayat kunjungan pasien. Setelah selesai, Dokter dapat melakukan logout untuk mengakhiri sesi.
</details>

<details>
<summary>5. Flowchart (Admin) Kelola Akun User</summary>

<img width="2753" height="2685" alt="(Admin) Kelola Akun User drawio" src="https://github.com/user-attachments/assets/e73bd7c3-1bd3-47c0-9548-efd9aa5fa123" />
Proses pengelolaan akun dimulai saat Admin membuka halaman Kelola Akun User. Sistem menampilkan daftar akun beserta fitur pencarian, tambah, ubah, dan nonaktifkan akun. Saat menambahkan akun, Admin mengisi nama, username, password, dan role, kemudian sistem memvalidasi kelengkapan serta keunikan username. Jika data valid, sistem menetapkan hak akses sesuai role, menyimpan akun ke database, dan menampilkan notifikasi keberhasilan.
</details>

<details>
<summary>6. Flowchart (Petugas 1) Kelola Data Pasien</summary>

<img width="2687" height="2410" alt="(Petugas 1) Kelola Data Pasien drawio" src="https://github.com/user-attachments/assets/94387ab2-5394-43fe-914c-36ba076ccb48" />
Proses pengelolaan data pasien dimulai saat Petugas membuka halaman Kelola Data Pasien. Sistem menampilkan daftar pasien beserta fitur pencarian, tambah, ubah, dan hapus data. Petugas dapat menambahkan pasien baru, memperbarui data pasien melalui formulir yang akan divalidasi sebelum disimpan ke database, serta menghapus data pasien jika tidak memiliki kunjungan aktif. Petugas juga dapat mencari data berdasarkan nama, NIK, atau ID pasien. Jika data ditemukan, sistem menampilkannya pada tabel, sedangkan jika tidak, sistem memberikan pemberitahuan bahwa pasien tidak ditemukan. Setelah selesai, Petugas dapat kembali ke Dashboard Petugas.
</details>

<details>
<summary>7. Flowchart (Petugas) Tambah Pasien Baru</summary>

<img width="2026" height="1045" alt="(Petugas) Tambah Pasien Baru  drawio" src="https://github.com/user-attachments/assets/b727ef01-7745-4057-9a9e-e7cc99563630" />
tambah pasien dimulai saat Petugas memilih menu Tambah Pasien Baru dan mengisi formulir data pasien. Sistem kemudian memvalidasi nomor telepon agar terdiri dari 10–13 digit dan NIK sebanyak 16 digit serta belum terdaftar. Jika seluruh data valid, sistem membuat ID pasien dan menyimpan data ke database. Setelah berhasil disimpan, sistem menampilkan notifikasi dan memberikan pilihan untuk melanjutkan ke pendaftaran kunjungan atau kembali ke halaman Kelola Data Pasien. Jika penyimpanan gagal, sistem menampilkan pesan kegagalan dan mengarahkan Petugas kembali ke halaman Kelola Data Pasien.
</details>

<details>
<summary>8. Flowchart (Petugas2) Daftarkan Kujungan</summary>

<img width="1745" height="1175" alt="(Petugas 2) Daftarkan Kunjungan drawio" src="https://github.com/user-attachments/assets/8ee1e9c7-b67a-4fa7-bf25-d8c8736beafc" />
pendaftaran kunjungan dimulai saat Petugas membuka menu Daftarkan Kunjungan dan mencari data pasien berdasarkan nama, NIK, atau ID pasien. Jika pasien ditemukan, Petugas memilih pasien dan menentukan poliklinik yang dituju. Sistem kemudian memeriksa kemungkinan kunjungan aktif untuk mencegah pendaftaran ganda. Jika tidak ditemukan kunjungan ganda, Petugas memeriksa dan mengonfirmasi data pendaftaran. Selanjutnya, sistem menyimpan kunjungan, membuat nomor antrean secara berurutan untuk seluruh poliklinik, dan menetapkan status Menunggu. Jika pendaftaran berhasil, sistem menampilkan tiket antrean dan memberikan pilihan untuk mendaftarkan pasien berikutnya atau kembali ke Dashboard Petugas.
</details>

<details>
<summary>9. Flowchart Daftarkan Kujungan2</summary>

<img width="1968" height="1325" alt="Daftarkan Kunjungan (2) drawio" src="https://github.com/user-attachments/assets/03def17e-4d46-4c89-a364-b4e835304610" />
pendaftaran kunjungan dimulai saat Petugas membuka menu Daftarkan Kunjungan dan mencari data pasien berdasarkan nama, NIK, atau ID pasien. Jika pasien ditemukan, Petugas memilih pasien dan menentukan poliklinik yang dituju. Sistem kemudian memeriksa kemungkinan kunjungan aktif untuk mencegah pendaftaran ganda. Jika tidak ditemukan kunjungan ganda, Petugas memeriksa dan mengonfirmasi data pendaftaran. Selanjutnya, sistem menyimpan kunjungan, membuat nomor antrean secara berurutan untuk seluruh poliklinik, dan menetapkan status Menunggu. Jika pendaftaran berhasil, sistem menampilkan tiket antrean dan memberikan pilihan untuk mendaftarkan pasien berikutnya atau kembali ke Dashboard Petugas.
</details>

<details>
<summary>10. Flowchart Petugas dan Dokter Lihat Riwayat kunjungan </summary>

<img width="1082" height="1320" alt="(Petugas dan Dokter) Lihat Riwayat Kunjungan drawio" src="https://github.com/user-attachments/assets/2c8bad01-1a44-4f90-aa32-38f6d98eab81" />
Lihat Riwayat Kunjungan dimulai saat Petugas atau Dokter membuka menu Lihat Riwayat Kunjungan. Sistem menampilkan kolom pencarian dan filter berdasarkan waktu pendaftaran untuk mencari data kunjungan. Jika waktu pendaftaran diisi, sistem menampilkan riwayat kunjungan yang berisi tanggal pendaftaran, poliklinik, dokter, nomor antrean, dan status kunjungan. Jika pencarian tidak diisi, sistem memberikan pesan bahwa belum ada riwayat kunjungan. Setelah selesai melihat data, pengguna dapat kembali ke dashboard sesuai dengan perannya, yaitu Dashboard Petugas atau Dashboard Dokter.
</details>

<details>
<summary>11. Flowchart (Petugas dan Dokter) Perbarui Status Kunjungan. </summary>

<img width="2709" height="1447" alt="Petugas dan Dokter) Perbarui Status Kunjungan drawio" src="https://github.com/user-attachments/assets/a9b6b5a0-df0e-43b5-933d-d477687ef49e" />
Perbarui Status Kunjungan dimulai saat Petugas atau Dokter membuka menu Perbarui Status Kunjungan. Sistem menampilkan daftar kunjungan pasien hari ini yang berisi nomor antrean, nama pasien, dokter, dan status kunjungan. Pengguna dapat memilih kunjungan dan mengubah status menjadi Menunggu, Sedang Diperiksa, atau Selesai. Sebelum disimpan, sistem memvalidasi status dan memeriksa apakah data telah diubah oleh pengguna lain. Jika tidak ada kendala, sistem menyimpan perubahan ke database dan menampilkan notifikasi keberhasilan.
</details>

<details>
<summary>12. Flowchart (Dokter 1) Antrean Dokter </summary>
  
<img width="2105" height="1131" alt="(Dokter 1) Antrean Dokter drawio" src="https://github.com/user-attachments/assets/1bae8d65-bf86-4ca5-9438-2ef02ccab93d" />
Antrean Dokter dimulai saat Dokter membuka menu Antrean Dokter untuk melihat daftar pasien dengan status Menunggu. Sistem menampilkan informasi nomor antrean, nama pasien, keluhan, dan status kunjungan. Dokter kemudian memilih pasien yang akan diperiksa. Sistem akan memeriksa apakah kunjungan tersebut sedang dibuka oleh dokter lain. Jika belum, sistem mengunci kunjungan untuk dokter yang sedang login dan mengubah statusnya menjadi Sedang Diperiksa. Selanjutnya, Dokter diarahkan ke Form Pemeriksaan untuk mencatat keluhan, hasil pemeriksaan, diagnosis, resep obat, serta catatan tindak lanjut jika diperlukan.
</details>

<details>
<summary>13. Flowchart (Dokter) Form Pemeriksaan </summary>
  
<img width="1434" height="1830" alt="(Dokter) Form Pemeriksaan drawio" src="https://github.com/user-attachments/assets/1cf4d14b-1bbf-4b2e-ae96-1d9a741cdf92" />
Form Pemeriksaan dimulai setelah Dokter memilih pasien dari halaman Antrean Dokter. Sistem menampilkan data pasien dan riwayat singkat sebagai referensi pemeriksaan. Dokter kemudian mengisi hasil pemeriksaan dan diagnosis, serta menambahkan resep obat dan catatan tindak lanjut jika diperlukan. Sebelum pemeriksaan diselesaikan, sistem memvalidasi kelengkapan hasil pemeriksaan dan diagnosis. Jika data sudah lengkap, sistem menyimpan seluruh hasil pemeriksaan ke database dan mengubah status kunjungan menjadi Selesai. Setelah itu, Dokter diarahkan kembali ke halaman Antrean Dokter untuk melayani pasien berikutnya.
</details>

## ERD
<details>
<summary>1. Logical </summary>
  <img width="2760" height="1486" alt="Logical_pulse" src="https://github.com/user-attachments/assets/4a16c888-ad42-4a80-95a9-a439865d49db" />
Diagram logical database pada sistem PulseCare menggambarkan hubungan antarentitas, yaitu pegawai, admin, petugas, dokter, shift, pasien, poliklinik, riwayat_kunjungan, dan hasil_kunjungan. Pegawai memiliki beberapa peran, yaitu admin, petugas, dan dokter. Petugas memiliki shift dan menangani pendaftaran kunjungan pasien. Setiap pasien dapat memiliki beberapa riwayat kunjungan yang terhubung dengan poliklinik. Kunjungan tersebut juga dapat ditangani oleh dokter dan menghasilkan data pemeriksaan berupa keluhan, diagnosis, resep obat, serta catatan tindak lanjut. Hubungan antarentitas ini membantu menggambarkan alur pengelolaan data pasien dan pelayanan kesehatan secara terstruktur dalam sistem PulseCare.
</details>

<details>
<summary>2. Relational </summary>
  <img width="2556" height="1490" alt="Relational_pulse" src="https://github.com/user-attachments/assets/bbfba53a-775a-4105-95e1-5c22f2562700" />
  Relational database pada sistem PulseCare menggambarkan hubungan antara 9 tabel utama, yaitu pegawai, dokter, admin, petugas, pasien, poliklinik, shift, riwayat_kunjungan, dan hasil_kunjungan. Tabel pegawai menjadi data utama yang terhubung dengan dokter, admin, dan petugas. Tabel pasien menyimpan identitas pasien, sedangkan poliklinik dan shift menyimpan data layanan serta jadwal kerja. Selanjutnya, tabel riwayat_kunjungan mencatat data pendaftaran, nomor antrean, dan status kunjungan pasien. Sementara itu, tabel hasil_kunjungan menyimpan keluhan, hasil pemeriksaan, diagnosis, resep obat, dan catatan tindak lanjut dokter. Seluruh tabel saling terhubung menggunakan Primary Key (PK) dan Foreign Key (FK) sehingga pengelolaan data dalam sistem PulseCare menjadi lebih terstruktur dan terintegrasi.
</details>

# Struktur Folder/Package
```text
PulseCare/
│
├── lib/
│   └── unknown/
│       └── binary/
│           └── AbsoluteLayout/
│               └── SNAPSHOT/
│                   └── AbsoluteLayout-SNAPSHOT.jar
│
├── src/
│   └── main/
│       ├── java/
│       │   ├── config/
│       │   │   ├── KoneksiDB.java
│       │   │   └── TestKoneksiDB.java
│       │   │
│       │   ├── controller/
│       │   │   ├── AdminController.java
│       │   │   ├── KunjunganController.java
│       │   │   ├── LoginController.java
│       │   │   ├── PasienController.java
│       │   │   ├── PemeriksaanController.java
│       │   │   └── RiwayatKunjunganController.java
│       │   │
│       │   ├── main/
│       │   │   └── Main.java
│       │   │
│       │   ├── model/
│       │   │   ├── Admin.java
│       │   │   ├── Akun.java
│       │   │   ├── Dokter.java
│       │   │   ├── HasilKunjungan.java
│       │   │   ├── Pasien.java
│       │   │   ├── Petugas.java
│       │   │   ├── Poliklinik.java
│       │   │   ├── RiwayatKunjungan.java
│       │   │   ├── Shift.java
│       │   │   │
│       │   │   └── dao/
│       │   │       ├── AdminDAO.java
│       │   │       ├── AntreanDokterDAO.java
│       │   │       ├── HasilKunjunganDAO.java
│       │   │       ├── KunjunganDAO.java
│       │   │       ├── LoginDAO.java
│       │   │       ├── PasienDAO.java
│       │   │       ├── ReferensiDAO.java
│       │   │       └── RiwayatKunjunganDAO.java
│       │   │
│       │   └── view/
│       │       ├── AntreanDokter.java
│       │       ├── AntreanDokter.form
│       │       ├── DaftarkanKunjungan.java
│       │       ├── DaftarkanKunjungan.form
│       │       ├── DashboardAdmin.java
│       │       ├── DashboardAdmin.form
│       │       ├── DashboardDokter.java
│       │       ├── DashboardDokter.form
│       │       ├── DashboardPetugas.java
│       │       ├── DashboardPetugas.form
│       │       ├── FormAkun.java
│       │       ├── FormAkun.form
│       │       ├── FormPasien.java
│       │       ├── FormPasien.form
│       │       ├── FormPemeriksaan.java
│       │       ├── FormPemeriksaan.form
│       │       ├── KelolaAkun.java
│       │       ├── KelolaAkun.form
│       │       ├── KelolaPasien.java
│       │       ├── KelolaPasien.form
│       │       ├── Login.java
│       │       ├── Login.form
│       │       ├── MainFrame.java
│       │       ├── MainFrame.form
│       │       ├── MenuUtama.java
│       │       ├── MenuUtama.form
│       │       ├── PerbaruiStatus.java
│       │       ├── PerbaruiStatus.form
│       │       ├── RiwayatKunjungan.java
│       │       └── RiwayatKunjungan.form
│       │
│       └── resources/
│           ├── Admin 70x70.png
│           ├── Dokter 50x50.png
│           ├── Dokter 70x70.png
│           ├── Dokter_40x40.png
│           ├── Hapus akun.jpg.jpeg
│           ├── Logo PulseCare 256x256.png
│           ├── Logo PulseCare sedang tanpa tulisan.png
│           ├── Logo PulseCare sedang.png
│           ├── Modern Hospital Entrance and Wayfinding.png
│           ├── bg form.png
│           ├── hapus akun besar.png
│           ├── orang navy baru.jpg
│           ├── orang pulsecare yg bener.png
│           ├── petugas_40x40.png
│           ├── pulsecare_profile_icon_50.png
│           ├── tambah akun.png
│           └── ubah akun.png
│
└── pom.xml
```


# Penjelasan Penerapan 4 Pilar OOP di dalam program

### 1. Encapsulation (Enkapsulasi)

Enkapsulasi pada project PulseCare diterapkan melalui class Pasien dengan menggunakan atribut bertipe private, seperti ID pasien, NIK, nama lengkap, tanggal lahir, jenis kelamin, dan status BPJS. Atribut tersebut tidak dapat diakses secara langsung dari luar class, sehingga penggunaannya harus melalui method getter untuk mengambil data dan setter untuk mengubah data. Penerapan ini bertujuan untuk melindungi data pasien agar lebih terkontrol, serta membuat pengelolaan data menjadi lebih terstruktur.

**Contoh implementasi:**

```java
public class Pasien {
    private String idPasien;
    private String nik;
    private String namaLengkap;
    private LocalDate tanggalLahir;
    private String jenisKelamin;
    private String statusBpjs;

    public Pasien() {
    }

    public Pasien(String idPasien, String namaLengkap, String nik,
            LocalDate tanggalLahir, String jenisKelamin,
            String statusBpjs) {

        this.idPasien = idPasien;
        this.namaLengkap = namaLengkap;
        this.nik = nik;
        this.tanggalLahir = tanggalLahir;
        this.jenisKelamin = jenisKelamin;
        this.statusBpjs = statusBpjs;
    }

    public String getIdPasien() {
        return idPasien;
    }

    public void setIdPasien(String idPasien) {
        this.idPasien = idPasien;
    }

    public String getNik() {
        return nik;
    }

    public void setNik(String nik) {
        this.nik = nik;
    }

    public String getNamaLengkap() {
        return namaLengkap;
    }

    public void setNamaLengkap(String namaLengkap) {
        this.namaLengkap = namaLengkap;
    }

    public LocalDate getTanggalLahir() {
        return tanggalLahir;
    }

    public void setTanggalLahir(LocalDate tanggalLahir) {
        this.tanggalLahir = tanggalLahir;
    }

    public String getJenisKelamin() {
        return jenisKelamin;
    }

    public void setJenisKelamin(String jenisKelamin) {
        this.jenisKelamin = jenisKelamin;
    }

    public String getStatusBpjs() {
        return statusBpjs;
    }

    public void setStatusBpjs(String statusBpjs) {
        this.statusBpjs = statusBpjs;
    }
}

```
### 2. Inheritance (Pewarisan)
Konsep Inheritance (Pewarisan) pada sistem PulseCare diterapkan melalui class tampilan yang menggunakan keyword extends, seperti DashboardPetugas dan DashboardDokter. Class tersebut mewarisi atribut dan method dari class bawaan Java Swing, seperti JPanel, JDialog, dan JFrame, sehingga dapat menggunakan fungsi yang sudah tersedia tanpa harus membuatnya dari awal.

**Contoh implementasi:**

```java
public class DashboardPetugas extends javax.swing.JPanel

```
```java
public class DashboardDokter extends javax.swing.JPanel
```
### 3.Polymorphism (Polimorfisme)
Polymorphism merupakan konsep OOP yang memungkinkan suatu metode memiliki perilaku berbeda sesuai dengan objek yang menggunakannya. Konsep ini dapat diterapkan melalui overriding, yaitu menimpa metode dari class induk dengan implementasi yang berbeda, dan overloading, yaitu menggunakan nama metode yang sama dengan parameter berbeda.

Pada program PulseCare, konsep Polymorphism diterapkan melalui method overriding pada class DashboardPetugas.java. Program menimpa metode isCellEditable() dari class DefaultTableModel dengan mengembalikan nilai false. Tujuannya agar seluruh sel pada tabel tidak dapat diedit oleh pengguna. Dengan demikian, metode bawaan dari class induk memiliki perilaku khusus sesuai kebutuhan program.

Contoh implementasi:
```java
DefaultTableModel model = new DefaultTableModel(kolom, 0) {
    @Override
    public boolean isCellEditable(int row, int column) {
        return false;
    }
};
```
### 4. Abstraction (Abstraksi)
Abstraction (Abstraksi) merupakan konsep OOP yang menyembunyikan detail proses atau implementasi dan hanya menampilkan bagian penting yang diperlukan. Konsep ini dapat diterapkan melalui abstract class dan abstract method, yaitu class dan metode yang menjadi dasar bagi class turunannya.

Pada program, konsep Abstraction diterapkan melalui class Pengguna.java yang menggunakan kata kunci abstract serta memiliki metode abstrak tampilkanPeran(). Metode tersebut tidak memiliki isi di class induk sehingga harus diimplementasikan oleh class turunannya sesuai dengan peran masing-masing.

Contoh implementasi Abstraction:
```java
public abstract class Pengguna {
    public abstract void tampilkanPeran();
}
```
# Cara Penggunaan Program
### 1. Menu Utama
<img width="599" height="391" alt="image" src="https://github.com/user-attachments/assets/9539061d-dce3-4d3c-8224-99c1dd429a5a" />

1. Jalankan aplikasi PulseCare.
   
2. unggu hingga halaman Menu Utama muncul.

3. Klik tombol Masuk untuk melanjutkan ke halaman Login.

4. Jika tidak ingin menggunakan aplikasi, klik tombol Keluar untuk menutup aplikasi.

### 2. Login
<img width="602" height="413" alt="Screenshot 2026-11-07 043741" src="https://github.com/user-attachments/assets/16877c52-0808-4cd4-b6a7-5103d1e7d8c5" />

1. Setelah menekan tombol Masuk, halaman Login akan ditampilkan

2. Masukkan Username/NIP pada kolom yang tersedia

3. Masukkan Password sesuai dengan akun yang terdaftar

4. klik tombol login


5. Sistem akan memeriksa kecocokan data akun yang terdaftar

6. Jika data benar, pengguna akan diarahkan ke dashboard sesuai role

7. jika data salah, sistem menampilkan pemberitahuan bahwa Username atau Password tidak sesuai

### 3. Dashboard Admin
<img width="605" height="422" alt="image" src="https://github.com/user-attachments/assets/12c66bb7-1c4f-45bf-88ea-ec774ddbf53d" />

1. Login menggunakan akun dengan role Admin

2. Sistem akan menampilkan Dashboard Admin

3. Pilih menu Kelola Akun untuk mengelola akun

4. Pilih menu Kelola Data Pasien untuk mengelola informasi pasien

### 4. Kelola Akun
<img width="604" height="416" alt="image" src="https://github.com/user-attachments/assets/4690c391-4853-4552-85fd-60805dda2f95" />

1. Buka menu Kelola Akun.

2. Sistem menampilkan daftar akun pengguna.

3. Pilih fungsi tambah atau ubah akun sesuai kebutuhan.

4. Isi informasi akun pada formulir.

5. Tentukan role pengguna, seperti Admin, Petugas, atau Dokter.

6. Simpan perubahan.

7. Sistem menyimpan data akun ke database.

### 5. Form Pasien
<img width="299" height="400" alt="image" src="https://github.com/user-attachments/assets/521c9759-446d-400c-9cc0-6b503517252c" />

1. Buka menu Kelola Pasien.

2. Sistem menampilkan daftar pasien.

3. Pilih pasien untuk melihat atau mengubah datanya.

4. Untuk menambahkan pasien, buka formulir pasien.

5. Isi identitas pasien sesuai informasi yang tersedia.

6. Simpan data pasien.

7. Sistem menyimpan perubahan ke database.
   
### 6. Dashboard Petugas 
<img width="604" height="413" alt="image" src="https://github.com/user-attachments/assets/1bc189c2-d7b5-48d7-a597-7256d9c75074" />

1. Login menggunakan akun dengan role Petugas.

2. Sistem menampilkan Dashboard Petugas.

3. Pilih menu Kelola Data Pasien atau Daftarkan Kunjungan sesuai kebutuhan.

### 7.Mendaftaran Kunjungan
<img width="581" height="394" alt="image" src="https://github.com/user-attachments/assets/03825d10-4ed3-4002-9ad1-29670e590cc6" />

1. Buka menu Daftarkan Kunjungan.

2. Masukkan identitas pasien pada kolom pencarian.

3. Klik tombol pencarian untuk menemukan data pasien.

4. Jika pasien sudah terdaftar, pilih data pasien tersebut.

5. Jika pasien belum terdaftar, tambahkan pasien melalui formulir FormPasien.java.

6. Pilih poliklinik tujuan sesuai kebutuhan kunjungan.

7. Lengkapi informasi pendaftaran.

8. Simpan pendaftaran kunjungan.

9. Sistem mencatat kunjungan dan memberikan nomor antrean kepada pasien.


### 8. Dashboard Dokter
<img width="604" height="412" alt="image" src="https://github.com/user-attachments/assets/e71100d5-51b6-46b7-b914-6ed6ddf68102" />

1. Login menggunakan akun dengan role Dokter.

2. Sistem menampilkan Dashboard Dokter.

3. Pilih menu Antrean Dokter untuk melihat pasien yang menunggu pemeriksaan.

### 9. Antrean Dokter
<img width="605" height="415" alt="image" src="https://github.com/user-attachments/assets/1073bd5c-faee-44ef-bd62-b371cd249945" />

1. Buka menu Antrean Dokter.

2. Sistem menampilkan daftar pasien yang memiliki kunjungan.

3. Perhatikan nomor antrean dan informasi pasien.

4. Pilih pasien yang akan diperiksa.

5. Sistem memeriksa apakah kunjungan sedang dibuka oleh dokter lain.

6. Jika tidak ada konflik, sistem membuka data kunjungan untuk proses pemeriksaan.

### 10. Pemeriksaan Ke Pasien
<img width="601" height="410" alt="image" src="https://github.com/user-attachments/assets/f7bfb6ad-a81d-4d28-bc33-db8e806ac0a0" />

1. Buka formulir pemeriksaan pasien yang dipilih.

2. Periksa informasi dan riwayat kunjungan pasien.

3. Masukkan keluhan pasien.

4. Catat hasil pemeriksaan.

5. Masukkan diagnosis berdasarkan hasil pemeriksaan.

6. Jika diperlukan, tambahkan resep obat.

7. Masukkan tindak lanjut apabila diperlukan.

8. Periksa kembali data yang telah diisi.

9. Klik tombol simpan untuk menyimpan hasil pemeriksaan.

10. Sistem menyimpan hasil pemeriksaan dan memperbarui status kunjungan menjadi Selesai.

### 11. Riwayat Kunjungan
<img width="604" height="416" alt="image" src="https://github.com/user-attachments/assets/accb5836-51ce-434a-b9aa-a65e5ffdf696" />

1. Buka menu Riwayat Kunjungan.

2. Masukkan informasi pencarian sesuai kolom yang tersedia.

3. Lakukan pencarian data kunjungan.

4. Sistem menampilkan riwayat kunjungan pasien jika data ditemukan.

5. Periksa tanggal kunjungan, poliklinik, dokter, nomor antrean, dan status kunjungan.

### 12. Perbarui Status
<img width="600" height="409" alt="image" src="https://github.com/user-attachments/assets/878f746b-b7cf-4d2a-9c8b-77288847f9ce" />

1. Buka menu Perbarui Status.

2. Sistem menampilkan daftar kunjungan pasien.

3. Pilih kunjungan yang ingin diperbarui.

4. Tentukan status kunjungan sesuai proses pelayanan.

5. Simpan perubahan status.

6. Sistem akan menampilkan pemberitahuan apabila perubahan berhasil.





# Nama Anggota
## Anggota Kelompok

| No. | Nama Anggota | NIM |
|:---:|---|:---:|
| 1 | Ghea Aisyah Windraswari | 2509116022 |
| 2 | Noor Hamsyah Pratama | 2509116046 |
| 3 | Condrado Alain Sharon | 2509116069 |
| 4 | Nurul Shafa Azizah | 2509116112 |

