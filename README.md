![alt text](image/coverbpf.png?raw=true)

## BAB I Pendahuluan


## 1.1 Tujuan

Dokumen Software Requirement Specification (SRS) merupakan dokumen spesifikasi perangkat lunak untuk membangun “Sistem Informasi Ayam Geprek Qiana”. Dokumen ini dibangun untuk memudahkan pengelola Ayam Geprek Qiana dalam memberikan informasi, promosi, dan layanan kepada pelanggan. Sehingga dokumen ini dapat dijadikan acuan teknis untuk membangun perangkat lunak “SISTEM INFORMASI AYAM GEPREK QIANA”.


## 1.2 Lingkup
Sistem Informasi Ayam Geprek Qiana merupakan website yang kami bangun untuk mempermudah pengelola Ayam Geprek Qiana dalam memberikan informasi kepada pelanggan seputar menu makanan, promosi, lokasi restoran, layanan pesan antar, dan berbagai informasi terkait lainnya.

## 1.3 Akronim, singkatan, definisi
| Istilah | Definisi |
| ------ | ------ |
|   SRS     |    Software Requirement Specification    |
|    Login    | Digunakan untuk mengakses aplikasi       |
|   Software Requirement Specification     | perangkat lunak yang akan dibuat dan sebagai penyembatani komunikasi pembuat dengan pengguna       |
|    Use Case    | situasi dimana sistem anda digunakan untuk memenuhi satu atau lebih kebutuhan pemakaian anda       |

## 1.4 Referensi
Referensi yang digunakan dalam pengembangan perangkat lunak ini adalah :

- https://fore.coffee/
- https://chatime.co.id/
- https://www.makobakery.com/product



## 1.5 Overview
Bab selanjutnya yaitu menjelaskan sistem yang di terapkan pada website. Menjelaskan gambaran umum dari website, 


## BAB II GAMBARAN UMUM  
**Ayam Geprek Qiana** adalah bisnis kuliner yang menawarkan berbagai varian menu ayam geprek dengan cita rasa khas dan pilihan tingkat kepedasan sesuai selera pelanggan. Pada era globalisasi ini, perkembangan teknologi dapat dimanfaatkan untuk meningkatkan promosi dan memberikan informasi yang mudah diakses oleh pelanggan. Dalam proyek ini, kami merancang sebuah **Sistem Informasi Ayam Geprek Qiana** sebagai platform informasi yang berfungsi untuk mendukung pengelola dalam menyampaikan informasi mengenai bisnis Ayam Geprek Qiana secara efektif.  

Sistem informasi ini dirancang untuk memberikan kemudahan kepada pelanggan dalam mengakses informasi seperti menu, lokasi, dan promosi. Selain itu, sistem ini juga membantu pengelola dalam mengelola informasi bisnis mereka dengan lebih terstruktur dan efisien. Berikut adalah fungsi utama yang dirancang untuk sistem informasi ini:  

### **Fungsi untuk Pengunjung/Pelanggan:**
- Melihat menu Ayam Geprek Qiana beserta harga.
- Melihat informasi tentang promosi atau diskon.
- Melihat lokasi dan jam operasional Ayam Geprek Qiana.
- Melihat testimoni pelanggan Ayam Geprek Qiana.
- Mengakses informasi kontak untuk pemesanan atau pertanyaan.

### **Fungsi untuk Admin/Pengelola:**
- Input data menu baru.
- Mengelola promosi atau diskon.
- Mengelola informasi lokasi dan kontak.
- Update, edit, atau hapus data yang sudah ada.

## 2.1 Perspektif produk
Sistem Ayam Geprek Qiana adalah sebuah sistem informasi berbasis website. Terdapat 2 jenis aktor yaitu admin dan pengunjung. Pengolahan data dilakukan oleh admin pada website dan pengunjung hanya melihat informasi pada website.

**2.1.1 Antarmuka Sistem**
![alt text](image/antarmukasistem.png?raw=true)

Sistem Informasi Parenting memiliki 2 pengunjung yaitu admin dan pengunjung. Admin mempunyai fungsi mengelola data informasi dan Pengunjung bisa melihat informasi serta memberikan komentar.

**2.1.2 Antarmuka Pengguna**

**Halaman Admin**
|  |  |
|--|--|
| ![alt text](image/login.png?raw=true) Halaman login admin diminta untuk mengisi username dan password.| ![alt text](image/dashboard.png?raw=true) Setelah login admin akan masuk ke tampilan Dashboard admin.
|  |  |
| ![alt text](image/testimoni.png?raw=true) Pada halaman testimoni, selain menambahkan dan mengedit, admin juga dapat menghapus data testimoni yang mana ketika button hapus di klik akan muncul pop up untuk memastikan admin benar-benar ingin menghapus atau tidak.| ![alt text](image/aboutus.png?raw=true) Pada halaman about us, admin juga dapat mengedit data about us, begitu juga dengan pengelolaan data di kolom tersedia.
|  |  |


## 2.2 Spesifikasi kebutuhan fungsional
![alt text](image/2.2_UseCase.drawio.png?raw=true)
**2.2.1 Admin Login**

Use Case: Login

Diagram:
![alt text](image/adminLogin.png?raw=true)

Deskripsi Singkat:  
Admin melakukan login terlebih dahulu sebelum masuk ke tampilan dashboard admin. Jika login gagal, akan muncul pesan alert "error login".

Deskripsi Langkah-Langkah: 
1. Admin melakukan login dengan username dan password pada form login.
2. Sistem melakukan validasi login.
3. Jika valid, admin akan diarahkan ke dashboard utama (home admin).
4. Jika tidak valid, sistem akan menampilkan pesan peringatan "error login".

Xref: Bagian 3.2.1, Login Admin

**2.2.2 Admin Register**

Use Case: Register

Diagram:

![alt text](image/adminRegister.drawio.png?raw=true)

Deskripsi Singkat: 
Terdapat form registrasi untuk menambahkan admin baru, yang hanya dapat diakses oleh admin dengan hak akses tertentu.

Deskripsi Langkah-langkah:
1. Admin dengan hak akses tertentu (Super Admin) dapat mengakses form untuk menambahkan admin baru.
2. Super Admin mengisi data pada form registrasi.
3. Sistem akan menyimpan data ke database.

Xref: Bagian 3.2.2, Register Admin

**2.2.3 Admin Input Tampilan Dashboard**

Use Case: Input Tampilan Dashboard

Diagram:

![alt text](image/2.2.3.png?raw=true)

Deskripsi Singkat: 
Admin dapat menginputkan tampilan dashboard setelah berhasil login. Dan terdapat gambar dan ucapan singkat saat memasuki dashboard.

Deskripsi Langkah-langkah:
1. Sistem menampilkan tampilan dashboard.
2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload image dan informasi atau ucapan singkat.
3. Sistem akan menyimpan ke database.
4. sudah disimpan sistem akan menampilkan pemberitahuan.

Xref: Bagian 3.2.3, Input Tampilan Dashboard

**2.2.4 Admin Input Data Menu**

Use Case: Input Data Menu

Diagram:
![alt text](image/Menu.png?raw=true)

Deskripsi Singkat: 
Sistem dapat menampilkan halaman input data tentang menu dan Admin dapat menginput data tentang menu-menu yang ada pada Ayam Geprek Qiana.

Deskripsi Langkah-langkah:
1. Sistem akan menampilkan tampilan Menu yang ada pada ayam geprek qiana.
2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload image dan informasi yang terdapat di menu.
3. Sistem akan menyimpan ke database.
4. sudah disimpan sistem akan menampilkan pemberitahuan.

Xref: Bagian 3.2.4, Input Data Menu

**2.2.5 Admin Input Data About Us**

Use Case: Input Data About Us

Diagram:![alt text](image/2.2.5.png?raw=true)


Deskripsi Singkat: 
Sistem dapat menampilkan halaman input About Us tentang Ayam Geprek Qiana dan Admin dapat menginput data tentang Ayam Geprek Qiana.

Deskripsi Langkah-langkah:
1. Sistem akan menampilkan tampilan data tentang About Us.
2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload image dan deskripsi tentang ayam geprek qiana.
3. Sistem akan menyimpan ke database.
4. sudah disimpan sistem akan menampilkan peringatan.

Xref: Bagian 3.2.5, Data About us Ayam Geprek Qiana

**2.2.6 Admin Input Data Promo**

Use Case: Input Data Promo

Diagram:![alt text](image/2.2.6.png?raw=true)


Deskripsi Singkat: 
Sistem dapat menampilkan halaman Input data promo dan Admin mengInput data promo ayam geprek qiana.

Deskripsi Langkah-langkah:
1. Sistem akan menampilkan tampilan data promo ayam geprek qiana.
2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload image, deskripsi, diskon, serta tanggal berlaku dan berakhirnya promo ayam geprek qiana.
3. Sistem akan menyimpan ke database.
4. sudah disimpan sistem akan menampilkan pemberitahuan.

Xref: Bagian 3.2.6, Data Promo

**2.2.7 Admin Input Data Contact Us**

Use Case: Input Data Contact Us

Diagram:![alt text](image/contactUs.png?raw=true)


Deskripsi Singkat: 
Sistem dapat menampilkan halaman Input data contact us seperti maps dan contact yang dapat dihubungi dan Admin mengInput data contact us.

Deskripsi Langkah-langkah:
1. Sistem akan menampilkan tampilan data contact us.
2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload maps, dan kontak yang dapat dihubungi dari ayam geprek qiana.
3. Sistem akan menyimpan ke database.
4. sudah disimpan sistem akan menampilkan pemberitahuan.

Xref: Bagian 3.2.7, Data Contact Us

**2.2.8 Admin Input Data Testimoni**

Use Case: Input Data Testimoni

Diagram:![alt text](image/testimoni.png?raw=true)


Deskripsi Singkat: 
Sistem dapat menampilkan halaman input data testimoni dan Admin mengInput data testimoni.

Deskripsi Langkah-langkah:
1. Sistem akan menampilkan tampilan data testimmoni.
2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload gambar dan deskripsi ayam geprek qiana.
3. Sistem akan menyimpan ke database.
4. sudah disimpan sistem akan menampilkan pemberitahuan.

Xref: Bagian 3.2.8, Data Testimoni

**2.2.9 Customer Mengunjungi website**

Use Case: Mengunjungi website

Diagram:
![alt text](image/2.2.9.png?raw=true)

Deskripsi Singkat: 
Customer mengunjungi website dan langsung masuk ke halaman Dashboard sebagai tampilan utama, kemudian melanjutkan ke berbagai fitur seperti Menu untuk mencari atau melihat daftar menu yang tersedia, About Us untuk mengetahui informasi tentang ayam geprek qiana, dan Contact Us untuk melihat kontak serta peta lokasi, Promo untuk melihat informasi promosi, dan Testimoni untuk melihat/membaca review dari pelanggan/customer ayam geprek qiana.

Deskripsi Langkah-Langkah: 
1. Sistem akan menampilkan halaman dashboard.
2. Customer dapat memilih fitur yang tersedia di navbar dashboard sesuai keinginan seperti fitur Menu, About Us, Contact Us, Promo, dan Testimoni.
3. Apabila memilih fitur Menu maka customer akan dapat melihat atau mecari daftar menu, harga, dll yang tersedia.
4. Apabila memilih fitur About Us maka customer akan dapat melihat Informasi lebih detail mengenai ayam geprek qiana.
5. Apabila memilih fitur Contact Us maka customer akan dapat melihat lokasi ayam geprek qiana dengan maps dan kontak dari ayam gerek qiana yang bisa dihubungi.
6. Apabila memilih fitur Promo maka customer akan dapat melihat promo yang tersedia.
7. Apabila memilih fitur Testimoni maka customer akan dapat melihat atau membaca review dari customer atau pelanggan setia ayam geprek qiana.
8. Customer dapat mengklik navbar dashboard kembali jika ingin keluar pada halaman konten yang telah dilihat.

Xref: Bagian 3.2.9, Customer

## 2.3 Spesifikasi kebutuhan non-fungsional
- tabel kebutuhan non-fungsional

| no | deskripsi |
| ------ | ------ |
|     1   |   Semua interface dan fungsi menggunakan Bahasa Indonesia     |
|     2   |   Perangkat Lunak dapat dipakai di semua platofrm OS ( Super Admin, Admin, Customer )     |

## 2.4 Karakteristik Pengguna
Karakteristik pengguna dari perangkat lunak ini adalah pengguna langsung berinteraksi dengan sistem dan dihubungkan dengan hak akses atau level autentikasi.

## 2.5 Batasan-batasan
tidak ada

## 2.6 Asumsi-asumsi
tidak ada

## 2.7 Kebutuhan Penyeimbang
tidak ada

## BAB III Requirement Specification


## 3.1 Persyaratan Antarmuka Eksternal
Salah satu cara mengakses website ini yaitu customer membuka website nya terlebih dahulu dan masuk ke tampilan dashboard lalu memilih fitur yang tersedia di navbar sehingga dapat melihat konten yang ada di website tersebut.

## 3.2 Functional Requirement
**3.2.1 Login Admin**

| Nama Fungsi         | Login                                  |
| ------------------- | -------------------------------------- |
| Xref                | Bagian 2.2.1, Admin Login               |
| Trigger             | Admin Membuka Website Sistem Ayam Geprek Qiana |
| Precondition        | Halaman login                          |
| Basic Path          | 1. Admin melakukan login dengan username dan password.
|        |         2. Sistem melakukan validasi login. |
|        | 3. Bila sukses, sistem akan mengarahkan ke home admin.  |
|        | 4. Bila gagal, sistem akan menampilkan peringatan. |
|     Alternative       |                   Tidak Ada                   |
| Post Condition     |                  admin dapat login dan mengakses webiste sistem Ayam Geprek Qiana                   |
|         Exception Push          |                  Username dan password salah                   |


**3.2.2 Register Admin**

| Nama Fungsi         | Register                                |
| ------------------- | -------------------------------------- |
| Xref                | Xref: Bagian 2.2.2, Admin Register               |
| Trigger             | Admin Membuka Website Sistem Ayam Geprek Qiana |
| Precondition        | Halaman Register                         |
| Basic Path          | 1. 1. Admin dengan hak akses tertentu (Super Admin) dapat mengakses form untuk menambahkan admin baru.
|        |         2. Super Admin mengisi data pada form registrasi. |
|        | 3. Jika valid, data admin baru disimpan ke database. |
|        | 4. Sistem akan menyimpan ke database. |
|     Alternative       |                   Tidak Ada                   |
| Post Condition     |                  Setelah registrasi admin dapat login dan mengakses webiste sistem Ayam Geprek Qiana                   |
|         Exception Push          |                  Tidak ada koneksi                |


**3.2.3 Admin Input Tampilan Dashboard**
| Nama Fungsi | Input Tampilan Dashboard |
| ------ | ------ |
| Xref       | Bagian 2.2.3, Admin Input Tampilan Dashboard      |
| Triger       | Membuka website sistem informasi Ayam Geprek Qiana        |
| Precondition | Menginput data tampilan dashboard |
| Basic Path | 1. Sistem menampilkan tampilan dashboard. |
|            | 2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload image dan informasi singkat. |
|            | 3. Sistem akan menyimpan data ke database. |
| Alternative | Tidak ada |     
| Post Condition | Admin mengelola dashboard
| Exception Push | Tidak ada koneksi |


**3.2.4 Input Data Menu**

| Nama Fungsi        | Input Data Menu                              |
| ------------------- | ---------------------------------- |
| Xref               | Bagian 2.2.4, Admin Input Data Menu                     |
| Trigger            | admin dapat menginputkan data Menu |
| Precondition       | Admin menginputkan Data Daftar Menu yang tersedia di Ayam Geprek Qiana |
| Basic Path         | 1. Sistem akan menampilkan tampilan Menu yang ada pada ayam geprek qiana. |
|                    | 2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload image dan informasi yang terdapat di menu.   |
|                    | 3. Sistem akan menyimpan ke database.   |
|                    | 4. Jika sudah disimpan sistem akan menampilkan pemberitahuan.   |
| Alternative        |  Tidak Ada                                 |
| Post Condition     |  Admin Dapat menginputkan data daftar menu seperti gambar, deskripsi, dan harga.        |
| Exception Push     | Tidak Ada        |

**3.2.5 Input Data About Us**

| Nama Fungsi        | Input About Us Ayam Geprek Qiana                              |
| ------------------- | ---------------------------------- |
| Xref               | Bagian 2.2.5, Admin Input Data About Us                     |
| Trigger            | admin dapat menginputkan data About Us Ayam Geprek Qiana |
| Precondition       | Admin menginputkan data informasi lebih detail tentang Ayam Geprek Qiana ke website |
| Basic Path         | 1. Sistem akan menampilkan tampilan data tentang About Us. |
|                    | 2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload image dan deskripsi tentang ayam geprek qiana.   |
|                    | 3. Sistem akan menyimpan ke database.   |
|                    | 4. Jika sudah disimpan sistem akan menampilkan pemberitahuan.   |
| Alternative        |  Tidak Ada                                 |
| Post Condition     |  Admin Dapat menginputkan data About Us seperti visi & misi, latar belakang, dll.        |
| Exception Push     | Tidak Ada        |

**3.2.6 Input Data Promo**

| Nama Fungsi        | Input Informasi Promo                             |
| ------------------- | ---------------------------------- |
| Xref               | Bagian 2.2.6, Admin Input Data Promo                      |
| Trigger            | admin dapat menginputkan data promo |
| Precondition       | Admin menginputkan data promo ke website |
| Basic Path         | 1. Sistem akan menampilkan tampilan data promo ayam geprek qiana |
|                    | 2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload image, deskripsi, diskon, serta tanggal berlaku dan berakhirnya promo ayam geprek qiana.   |
|                    | 3. Sistem akan menyimpan ke database.   |
|                    | 4. Jika sudah disimpan sistem akan menampilkan pemberitahuan.   |
| Alternative        |  Tidak Ada                                 |
| Post Condition     |  Admin Dapat menginputkan data promo seperti nama promo, deskripsi promo, diskon, tanggal berlaku dan berakhirnya promo.        |
| Exception Push     | Tidak Ada        |

**3.2.7 Input Data Contact Us**

| Nama Fungsi        | Input Informasi contact person dan lokasi                              |
| ------------------- | ---------------------------------- |
| Xref               | Bagian 2.2.7, Admin Input Data Contact Us                     |
| Trigger            | admin dapat menginputkan data contact us|
| Precondition       | Admin menginputkan data contact us ke website |
| Basic Path         | 1. Sistem akan menampilkan tampilan data contact us. |
|                    | 2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload maps, dan kontak yang dapat dihubungi dari ayam geprek qiana.   |
|                    | 3. Sistem akan menyimpan ke database.   |
|                    | 4. Jika sudah disimpan sistem akan menampilkan pemberitahuan.   |
| Alternative        |  Tidak Ada                                 |
| Post Condition     |  Admin Dapat menginputkan data contact us seputar website seperti lokasi(maps), dan contact person.        |
| Exception Push     | Tidak Ada        |

**3.2.8 Input Data Testimoni**

| Nama Fungsi        | Input Informasi Testimoni                             |
| ------------------- | ---------------------------------- |
| Xref               | Bagian 2.2.8, Admin Input Data Testimoni                      |
| Trigger            | admin dapat menginputkan data testimoni |
| Precondition       | Admin menginputkan data testimoni ke website |
| Basic Path         | 1. Sistem akan menampilkan tampilan data testimmoni. |
|                    | 2. Admin dapat melihat, menambahkan, mengedit, menghapus dan mengupload gambar dan deskripsi ayam geprek qiana.   |
|                    | 3. Sistem akan menyimpan ke database.   |
|                    | 4. Jika sudah disimpan sistem akan menampilkan pemberitahuan.   |
| Alternative        |  Tidak Ada                                 |
| Post Condition     |  Admin Dapat menginputkan data testimoni seperti gambar dan deskripsi.        |
| Exception Push     | Tidak Ada        |

**3.2.9 Mengunjungi website**

| Nama Fungsi        |    Customer  Mengunjungi website             |
| ------------------- | ---------------------------------- |
| Xref               | Bagian 2.2.9 Customer Mengunjungi website             |
| Trigger            |Customer mengunjungi website dan langsung masuk ke halaman Dashboard sebagai tampilan utama, kemudian melanjutkan ke berbagai fitur seperti Menu untuk mencari atau melihat daftar menu yang tersedia, About Us untuk mengetahui informasi tentang ayam geprek qiana, dan Contact Us untuk melihat kontak serta peta lokasi, Promo untuk melihat informasi promosi, dan Testimoni untuk melihat/membaca review dari pelanggan/customer ayam geprek qiana |
| Precondition       |Customer Mengunjungi website |
| Basic Path         | 1. Sistem akan menampilkan halaman dashboard. |
|                    | 2. Customer dapat memilih fitur yang tersedia di navbar dashboard sesuai keinginan seperti fitur Menu, About Us, Contact Us, Promo, dan Testimoni.    |
|                    | 3. Apabila memilih fitur Menu maka customer akan dapat melihat atau mecari daftar menu, harga, dll yang tersedia.    |
|                    | 4. Apabila memilih fitur About Us maka customer akan dapat melihat Informasi lebih detail mengenai ayam geprek qiana.    |
|                    | 5. Apabila memilih fitur Contact Us maka customer akan dapat melihat lokasi ayam geprek qiana dengan maps dan kontak dari ayam gerek qiana yang bisa dihubungi.    |
|                    | 6. Apabila memilih fitur Promo maka customer akan dapat melihat promo yang tersedia.    |
|                    | 7. Apabila memilih fitur Testimoni maka customer akan dapat melihat atau membaca review dari customer atau pelanggan setia ayam geprek qiana.    |
|                    | 8. Customer dapat mengklik navbar dashboard kembali jika ingin keluar pada halaman konten yang telah dilihat.    |
| Alternative        |   Halaman Konten    |
| Post Condition     |   customer mengunjungi website dan melihat informasi yang ada pada website     |
| Exception Push     |    Jika ada kesalahan server atau gangguan teknis, sistem akan menampilkan pesan kesalahan kepada pengguna. Pengguna dapat mencoba kembali atau menghubungi dukungan teknis.    |

## 3.3 Struktur Detail Kebutuhan Non-Fungsional
![alt text](Image/3.3.png?raw=true)
**3.3.1 Logika Struktur Data**
Struktur data logika pada sistem informasi parenting terdapat struktur Database yang dijelaskan menggunakan ERD.

**Tabel Admin**
|Data Item|Tipe Data|Deskripsi|
|--|--|--|
|Id_Admin|int|Auto-increment dari Id_Admin|
|username|varchar|Berisi username admin untuk mengakses sistem|
|Password|varchar|Berisi password admin untuk mengakses sistem|
|level|varchar|untuk membedakan level saat login antara admin dan pengunjung|

**Tabel Artikel**
|Data Item|Tipe Data|Deskripsi|
|--|--|--|
|id_Artikel|int|Auto-increment dari Id_artikel|
|gambar|varchar|Berisi gambar didalam artikel sistem|
|deskripsi|text|Berisi deskripsi artikel sistem|
|judul|varchar|Berisi judul pada artikel sistem|
|kategori|varchar|Berisi kategori pada artikel sistem|

**Tabel Kegiatan**
|Data Item|Tipe Data|Deskripsi|
|--|--|--|
|id_kegiatan|int|Auto-increment dari Id_kegiatan|
|gambar|varchar|Berisi gambar didalam kegiatan sistem|
|deskripsi|text|Berisi deskripsi kegiatan sistem|
|judul|varchar|Berisi judul pada kegiatan sistem|
|tanggal|varchar|Berisi tanggal pada kegiatan sistem|

**Tabel about**
|Data Item|Tipe Data|Deskripsi|
|--|--|--|
|id_about|int|Auto-increment dari id_about|
|gambar|varchar|Berisi gambar didalam about sistem|
|deskripsi|text|Berisi deskripsi about sistem|

**Tabel contact**
|Data Item|Tipe Data|Deskripsi|
|--|--|--|
|id_contact|int|Auto-increment dari id_contact|
|judul|varchar|Berisi judul pada contact sistem|
|isi|text|Berisi isi contact sistem|

**Tabel team**
|Data Item|Tipe Data|Deskripsi|
|--|--|--|
|id_team|int|Auto-increment dari Id_team|
|gambar|varchar|Berisi gambar didalam team sistem|
|nama|text|Berisi nama team sistem|
|jabatan|varchar|Berisi jabatan pada team sistem|



## Pembagian tugas
BAB 1 ->Nindy

BAB 2 
2.1
  
  2.1.1 -> Nindy
  
  2.1.2 -> Nindy
  
  2.1.3 -> Ariyan
  
  2.1.4 -> Ariyan
 
  2.1.5 -> Ariyan
  
  2.1.6 -> Raditya
  
  2.1.7 -> Raditya
  
  2.1.8 -> Raditya

2.2 semua poin-poin (nindy)

BAB 3 

3.1 nindy

3.2 nindy

3.3 Nindy

