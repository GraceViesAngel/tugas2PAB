# 📋 Form Registrasi Event Kampus

## Identitas

**NAMA :** Grace Vies Angel  
**NIM :** 2409116005  
**KELAS :** A'2024  

---

## Deskripsi Aplikasi

Pada project ini saya membuat sebuah aplikasi Flutter sederhana yang berfungsi sebagai **form registrasi peserta event kampus**. Aplikasi ini memberikan pengguna untuk mengisi data pendaftaran melalui beberapa input form seperti nama, email, password, jenis kelamin, program studi, dan tanggal lahir.

Setelah pengguna mengisi form dan menekan tombol daftar, data peserta akan disimpan sementara di dalam aplikasi menggunakan **Provider sebagai state management**. Data yang sudah tersimpan kemudian dapat dilihat pada halaman **daftar peserta**.

Selain itu, aplikasi ini juga menyediakan **halaman detail peserta** yang menampilkan informasi lengkap dari setiap pendaftar. Jika diperlukan, pengguna juga dapat menghapus data peserta dari daftar yang ada.

Melalui project ini saya belajar bagaimana cara membuat form input di Flutter, melakukan validasi data, serta mengelola data menggunakan state management Provider.

---

## ✨ Fitur Aplikasi

Beberapa fitur yang terdapat pada aplikasi ini antara lain:

- ✅ Multi-field form (nama, email, password, dll)
- ✅ Real-time validation
- ✅ Berbagai input widgets (TextFormField, Radio, Dropdown, DatePicker, Checkbox)
- ✅ Provider untuk menyimpan daftar pendaftar
- ✅ Halaman list pendaftar
- ✅ Halaman detail pendaftar

### App Structure

```text
+------------------------+        +------------------------+        +------------------------+
|  Registration          |        |  Registrant            |        |  Registrant            |
|  Form Page             |        |  List Page             |        |  Detail Page           |
|                        |        |                        |        |                        |
| • Name                 |        | • ListView             |        | • Full info            |
| • Email                |        | • Badge count          |        | • All fields           |
| • Password             |        | • Delete action        |        |                        |
| • Gender (Radio)       |        |                        |        |                        |
| • Prodi (Drop)         |        |                        |        |                        |
| • DoB (Date)           |        |                        |        |                        |
| • Agree (Check)        |        |                        |        |                        |
+------------------------+        +------------------------+        +------------------------+

        ↑                          ↑                           ↑
        └──────────── Provider (RegistrationProvider) ────────────┘

              Shared state: List<Registrant>

```

Diagram di atas menunjukkan struktur halaman pada aplikasi yang saya buat.
Aplikasi terdiri dari tiga halaman utama yaitu Registration Form Page, Registrant List Page, dan Registrant Detail Page yang semuanya terhubung melalui Provider sebagai pengelola data.

---

## 📁 Struktur Folder Project

Struktur folder utama yang saya gunakan pada project ini sebagai berikut:

```
lib/
│
├── models/
│   └── registrant_model.dart
│
├── providers/
│   └── registration_provider.dart
│
├── pages/
│   ├── registration_page.dart
│   ├── registrant_list_page.dart
│   └── registrant_detail_page.dart
│
└── main.dart
```

### Penjelasan Folder

**models** 

<img width="208" height="62" alt="image" src="https://github.com/user-attachments/assets/c1249902-74c4-4bd6-87ca-74b240a47f24" />

Folder `models` saya gunakan untuk menyimpan struktur data yang dipakai di dalam aplikasi. Di dalam folder ini terdapat file `registrant_model.dart` yang berisi model atau bentuk data dari peserta yang melakukan registrasi.

Model ini menyimpan beberapa informasi penting seperti nama, email, jenis kelamin, program studi, tanggal lahir, serta waktu saat peserta melakukan pendaftaran. Dengan adanya model ini, data peserta bisa disimpan dan diolah dengan lebih rapi di dalam aplikasi.


**providers**  

<img width="244" height="56" alt="image" src="https://github.com/user-attachments/assets/5f02aead-cd16-460d-8807-2ae0af029b37" />

Folder `providers` saya gunakan untuk mengatur dan mengelola data peserta menggunakan **Provider sebagai state management**.

Di dalam folder ini terdapat file `registration_provider.dart` yang berfungsi untuk menyimpan daftar peserta yang sudah melakukan registrasi. Selain itu, provider ini juga digunakan untuk menambahkan data peserta baru, mengambil data peserta berdasarkan id, serta menghapus data peserta dari daftar.

Dengan menggunakan Provider, data peserta bisa diakses oleh beberapa halaman sekaligus tanpa harus mengirim data secara manual antar halaman.

**pages** 

<img width="231" height="111" alt="image" src="https://github.com/user-attachments/assets/b07737ab-8da9-4f4c-9443-50b7b8b7db94" />

Folder `pages` berisi semua halaman yang ada di dalam aplikasi. Setiap halaman dipisahkan ke dalam file yang berbeda supaya struktur project lebih rapi dan mudah dipahami.

Berikut adalah file yang terdapat dalam folder ini:

- `registration_page.dart` → halaman form registrasi tempat pengguna mengisi data pendaftaran.
- `registrant_list_page.dart` → halaman yang menampilkan daftar peserta yang sudah mendaftar.
- `registrant_detail_page.dart` → halaman yang menampilkan informasi lengkap dari peserta yang dipilih.


**main.dart** 

<img width="146" height="36" alt="image" src="https://github.com/user-attachments/assets/4eba06d8-3a6d-462e-bf39-af53f102b6a2" />

File `main.dart` merupakan file utama yang digunakan untuk menjalankan aplikasi Flutter.

---

## Tampilan Aplikasi

Aplikasi ini memiliki tiga halaman utama yang saling terhubung. Setiap halaman memiliki peran masing-masing dalam proses registrasi peserta, mulai dari pengisian data, melihat daftar peserta, sampai melihat detail informasi dari peserta yang dipilih.

---

### 1️⃣ Registration Form Page

Halaman pertama yang muncul saat aplikasi dijalankan adalah halaman **form registrasi**. Pada halaman ini pengguna diminta untuk mengisi beberapa data yang dibutuhkan untuk melakukan pendaftaran event.

Field yang harus diisi antara lain:

- Nama
- Email
- Password
- Jenis Kelamin
- Program Studi
- Tanggal Lahir
- Persetujuan Syarat dan Ketentuan

Setiap field memiliki validasi sehingga pengguna tidak bisa langsung mendaftar jika data belum diisi dengan benar. Setelah semua data lengkap, pengguna dapat menekan tombol **Daftar Sekarang** untuk menyimpan data peserta ke dalam aplikasi.

📸 **Tampilan Halaman Registrasi**

<img width="1919" height="912" alt="Screenshot 2026-03-10 182859" src="https://github.com/user-attachments/assets/aae89bcd-fa07-4502-87ce-64726e8bf7c5" />

---

### 2️⃣ Registrant List Page

Setelah pengguna berhasil melakukan registrasi, data peserta akan muncul pada halaman **daftar peserta**. Halaman ini berfungsi untuk menampilkan semua peserta yang sudah terdaftar di dalam aplikasi.

Pada halaman ini pengguna dapat melihat:

- daftar peserta yang sudah melakukan registrasi
- jumlah peserta yang sudah terdaftar
- tombol untuk menghapus data peserta jika diperlukan

Selain itu, pengguna juga dapat menekan salah satu peserta pada daftar tersebut untuk melihat informasi yang lebih lengkap pada halaman detail.

📸 **Tampilan Halaman Daftar Peserta**

<img width="1919" height="913" alt="Screenshot 2026-03-10 183056" src="https://github.com/user-attachments/assets/61f05fec-11c2-4112-b71e-e8ced6bfd72c" />

---

### 3️⃣ Registrant Detail Page

Halaman ini digunakan untuk menampilkan **informasi lengkap dari peserta yang dipilih**. Data yang ditampilkan pada halaman ini merupakan data yang sebelumnya diisi oleh peserta saat melakukan registrasi.

Beberapa informasi yang ditampilkan pada halaman ini antara lain:

- Nama peserta
- Email
- Gender
- Program Studi
- Tanggal lahir
- Umur peserta

Dengan adanya halaman ini, pengguna dapat melihat detail data peserta dengan lebih jelas dan lengkap.

📸 **Tampilan Halaman Detail Peserta**

<img width="1919" height="903" alt="Screenshot 2026-03-10 183147" src="https://github.com/user-attachments/assets/6fd13896-1148-4400-9bc3-fd1cee0f69ce" />

---

## 🔄 Alur Penggunaan Aplikasi

Aplikasi ini digunakan untuk melakukan pendaftaran peserta event. Pengguna dapat mengisi data pendaftaran, melihat daftar peserta yang sudah terdaftar, serta melihat detail informasi dari setiap peserta.

---

### Mengisi Form Pendaftaran

Saat aplikasi dibuka, pengguna akan melihat halaman **Form Pendaftaran Event**. Pada halaman ini pengguna diminta untuk mengisi beberapa data seperti nama lengkap, email, password, jenis kelamin, program studi, dan tanggal lahir.

Selain itu pengguna juga harus mencentang **persetujuan syarat dan ketentuan** sebelum melakukan pendaftaran.

Setelah semua data diisi dengan benar, pengguna dapat menekan tombol **Daftar Sekarang** untuk menyimpan data pendaftaran.

📷 Tampilan Form Pendaftaran

<img width="1919" height="912" alt="Screenshot 2026-03-10 182859" src="https://github.com/user-attachments/assets/6ef5eb40-0d8b-4993-9e82-11b2d81ad3f2" />

<img width="1919" height="908" alt="Screenshot 2026-03-10 184347" src="https://github.com/user-attachments/assets/c95a47ef-0e94-4b23-bdaf-ad9f9a8558a9" />


---

### Proses Registrasi Berhasil

Jika semua data sudah diisi dengan benar, aplikasi akan menampilkan notifikasi bahwa proses registrasi berhasil dilakukan.

Pada notifikasi ini terdapat pilihan untuk **melakukan pendaftaran lagi** atau langsung **melihat daftar peserta** yang sudah terdaftar.

📷 Tampilan Registrasi Berhasil

<img width="1919" height="912" alt="Screenshot 2026-03-10 184428" src="https://github.com/user-attachments/assets/15f8a4ec-3b44-4f54-bda6-230545cb9d0d" />

---

### Melihat Daftar Peserta

Setelah proses registrasi selesai, data peserta akan tersimpan dan ditampilkan pada halaman **Daftar Peserta**.

Pada halaman ini pengguna dapat melihat daftar peserta yang sudah terdaftar. Setiap peserta ditampilkan dalam bentuk daftar yang berisi nama, program studi, dan email.

Selain itu terdapat **ikon hapus** di samping setiap data peserta yang dapat digunakan untuk menghapus peserta dari daftar.

📷 Tampilan Daftar Peserta

<img width="1919" height="913" alt="Screenshot 2026-03-10 183056" src="https://github.com/user-attachments/assets/96e29906-54d4-4f69-b7fb-d96f052aaf64" />


---

### Melihat Detail Peserta

Jika salah satu peserta pada daftar dipilih, aplikasi akan menampilkan halaman **Detail Peserta**.

Pada halaman ini ditampilkan informasi lengkap mengenai peserta seperti nama, email, jenis kelamin, program studi, tanggal lahir, serta umur peserta yang dihitung secara otomatis oleh sistem.

📷 Tampilan Detail Peserta

<img width="1919" height="903" alt="Screenshot 2026-03-10 183147" src="https://github.com/user-attachments/assets/168eb75f-1337-4fac-a91e-39273f483056" />

---

### Validasi Email yang Sudah Terdaftar

Aplikasi juga melakukan pengecekan pada email yang dimasukkan saat proses pendaftaran. Jika pengguna mencoba mendaftar menggunakan email yang sudah pernah digunakan sebelumnya, maka sistem akan menampilkan pesan peringatan **“Email sudah terdaftar!”**.

Pesan ini muncul di bagian bawah halaman dalam bentuk notifikasi sehingga pengguna mengetahui bahwa email tersebut tidak dapat digunakan kembali. Dengan adanya pengecekan ini, setiap peserta hanya dapat melakukan pendaftaran menggunakan email yang berbeda.

📷 Tampilan Peringatan Email Sudah Terdaftar

<img width="1919" height="908" alt="Screenshot 2026-03-10 184347" src="https://github.com/user-attachments/assets/5ea17956-8c00-4584-98c8-291333e6f786" />





