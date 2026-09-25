# 📚 Library Loan Management System

Selamat datang di repositori kode sumber (*source code*) untuk aplikasi manajemen peminjaman buku! Website ini dirancang dengan standar modern untuk mengelola data peminjaman buku secara efisien dan interaktif.

Proyek ini dibangun menggunakan arsitektur full-stack dengan pemisahan folder yang terstruktur agar kode tetap bersih, mudah dipelihara, dan dikembangkan di masa mendatang.

---

## 🛠️ Tech Stack (Teknologi yang Digunakan)

Website ini dibangun menggunakan kombinasi teknologi modern web development berikut:

* **Frontend:** ReactJS (Vite), React Router DOM
* **Styling & UI:** Tailwind CSS v4, DaisyUI
* **Backend:** Node.js, Express.js
* **Database & ORM:** MySQL (`library_loan`), Sequelize ORM
* **Bahasa Pemrograman:** JavaScript (ES6+)

---

## 📁 Struktur Project yang Diharapkan

Berikut adalah peta direktori berkas utama dari proyek ini:

```text
library-loan/
├── backend/
│   ├── config/database.js
│   ├── controllers/loanController.js
│   ├── models/loanModel.js
│   ├── routes/loanRoute.js
│   ├── request.rest
│   ├── index.js
│   └── package.json
└── frontend/
    ├── src/
    │   ├── components/LoanTable.jsx
    │   ├── pages/Home.jsx
    │   ├── pages/CreateLoan.jsx
    │   ├── pages/EditLoan.jsx
    │   ├── services/loanService.js
    │   ├── App.jsx
    │   ├── main.jsx
    │   └── index.css
    └── package.json
```

---
## 🚀 Cara Menjalankan Proyek
Ikuti langkah-langkah berikut untuk menjalankan aplikasi di komputer lokal Anda:

### Prasyarat
Pastikan komputer Anda sudah menginstal:
* [Node.js](https://nodejs.org/) (versi LTS direkomendasikan)
* Git (untuk mengunduh repositori)

### Langkah-langkah Instalasi:
Clone repositori ini ke komputer Anda
1. **Clone repositori ini ke komputer Anda**
   ```bash
   git clone https://github.com/gyenisasyofiaa/portofolio.git
   ```

2. **Masuk ke direktori proyek**
   ```bash
   cd fullstackv4-peminjaman
   ```
   
3. **Install semua *dependencies* yang diperlukan**
   ```bash
   npm install
   ```
   *(Atau Anda bisa menggunakan `yarn install` / `pnpm install`)*
   
4. **Konfigurasi Database**
Di jendela utama Laragon, klik tombol "Start All".Tombol ini akan mengaktifkan Apache/Nginx dan MySQL secara bersamaan. Pastikan status layanan berubah menjadi Running.
Buat database baru melalui phpMyAdmin dengan nama library_loan.

---
5. **Jalankan server lokal(development mode)**

   
   **Backend**
   ```bash
   cd backend
   ```

   ```bash
   nodemon index
   ```
   
   **Frontend**
   ```bash
   cd frontend
   ```

   ```bash
   npm run dev
   ```



6. **Buka di Browser**
   Buka browser Anda dan akses tautan berikut:
   `http://localhost:5173/`

---

## 🔗 Endpoint API (Backend Integration)
Method HTTP,        Endpoint URL,        Deskripsi Fungsi
GET,                /peminjaman,        Mengambil seluruh data daftar peminjaman buku

GET,                /peminjaman/:id,        Mengambil detail data berdasarkan ID untuk form edit

POST,                /peminjaman,        Menambahkan data peminjaman buku baru

PUT / PATCH,        /peminjaman/:id,        Memperbarui data peminjaman berdasarkan ID

DELETE,            /peminjaman/:id,        Menghapus data peminjaman berdasarkan ID

---

## ⚠️ Kendala dan Solusi Teknis
## Format Tanggal pada Form Edit:

Kendala: Backend mengirimkan data tanggal berformat ISO string lengkap dengan waktu, sedangkan elemen <input type="date"> di HTML hanya membaca format YYYY-MM-DD.
Solusi: Menerapkan metode pemotongan string .split("T")[0] pada fungsi pengambilan data di dalam useEffect.

## Potensi White Screen Saat Data Kosong:
Kendala: Aplikasi sempat mengalami crash ketika mencoba membaca properti array sebelum data dari server berhasil dimuat.
Solusi: Memberikan nilai default berupa array kosong serta menerapkan pengaman optional chaining (loan?.id) pada komponen tabel.

---

## 🤝 Kontribusi & Kontak

Jika Anda memiliki pertanyaan, saran, atau ingin berkolaborasi, silakan hubungi saya melalui:
* **Email:** gyenisasyofiaa@gmail.com
* **LinkedIn:** https://linkedin/in/gyenisa-syofia
* **WhatsApp:** 082286764277
    
