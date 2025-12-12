# **NIK Generator & Validator**

**NIK Generator & Validator** adalah aplikasi desktop Windows yang digunakan untuk melakukan *generating* dan *validasi* NIK (Nomor Induk Kependudukan) secara otomatis berdasarkan format resmi Indonesia.
Aplikasi ini dibuat untuk keperluan **pengujian**, **simulasi**, dan **support pemrosesan file** seperti `*.nik`,`*.sql`, `*.json`, `*.csv`, `*.tsv`, `*.xml`, `*.parquet`, `*.db`, `*.bin`, `*.ibd`, `*.frm`, `*.orc`, `*.bson`, `*.sqlite3`.

> **Catatan penting:**
> Aplikasi ini **tidak** mengambil, menyimpan, atau memproses data NIK asli. Seluruh data bersifat simulasi dengan referensi dasar dari struktur administratif Indonesia.

---

## 🎯 **Fitur Utama**

### **1. NIK Generator**

* Menghasilkan NIK secara otomatis berdasarkan pola resmi Indonesia.
* Mendukung:

  * Kode Provinsi
  * Kode Kabupaten/Kota
  * Kode Kecamatan
  * Tanggal lahir (L/P format resmi)
  * Nomor urut 0001–9999
* Sistem *multithreading* untuk performa cepat.
* Output hasil generator akan tersimpan otomatis di folder:

  ```
  /logs/
  ```

### **2. NIK Validator**

* Memeriksa apakah sebuah NIK sesuai struktur dan format baku.
* Menampilkan rincian:

  * Provinsi
  * Kabupaten/Kota
  * Kecamatan
  * Jenis Kelamin
  * Tanggal Lahir

---

## 📌 **Sumber Data**

Data utama wilayah administratif diambil dari Wikipedia:

**[https://id.wikipedia.org/wiki/Provinsi_di_Indonesia](https://id.wikipedia.org/wiki/Provinsi_di_Indonesia)**

Saat ini database bawaan aplikasi hanya mencakup:

✔ **Provinsi Jawa Barat (ID: 32)**
Termasuk seluruh Kabupaten/Kota dan Kecamatan di Jawa Barat.

---

## 📂 **Struktur Folder**

```
📁 NIK-Generator-Validator/
│
├── assets/images/         # Ikon, gambar UI, screenshot aplikasi
├── database/
│   └── jawa_barat.nik/    # Database wilayah (saat ini hanya Jawa Barat)
├── logs/                  # Hasil output NIK Generator
│
└── README.md              # Dokumentasi proyek
```

---

## 🖼️ **Tangkapan Layar**

<div align="center">
  <img src="./assets/images/NIK Generator & Validator.jpg" alt="NIK Generator & Validator">
</div>

---

## ⚙️ **Cara Menggunakan**

### **1. Generate NIK**

1. Buka tab **NIK Generator**.
2. Tentukan:

   * `Max Threads`
   * `Max Data` (jumlah NIK yang ingin dihasilkan)
3. Klik **Generate NIK**.
4. Hasil akan muncul pada list dan otomatis tersimpan di `logs/`.

### **2. Validasi NIK**

1. Masuk ke tab **NIK Validator**.
2. Masukkan nomor NIK.
3. Aplikasi akan menampilkan data administratif terkait.

---

## 📦 **Requirements**

* Windows 10/11
* .NET Framework / .NET Runtime

---

## 🚀 **Roadmap**

* [ ] Penambahan database untuk seluruh provinsi di Indonesia
* [ ] Ekspor ke HTML/JSON
* [ ] API lokal untuk integrasi sistem lain
* [ ] Mode *bulk validation*

---

## 📄 **Lisensi**

Proyek ini dirilis menggunakan lisensi bebas (MIT).

---
