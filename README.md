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
---

