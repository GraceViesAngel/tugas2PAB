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

Folder `providers` saya gunakan untuk mengatur dan mengelola data peserta menggunakan **Provider sebagai state management**. Di dalam folder ini terdapat file `registration_provider.dart` yang berfungsi untuk menyimpan daftar peserta yang sudah melakukan registrasi. Selain itu, provider ini juga digunakan untuk menambahkan data peserta baru, mengambil data peserta berdasarkan id, serta menghapus data peserta dari daftar. Dengan menggunakan Provider, data peserta bisa diakses oleh beberapa halaman sekaligus tanpa harus mengirim data secara manual antar halaman.

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









