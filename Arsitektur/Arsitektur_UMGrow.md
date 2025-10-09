# Arsitektur Sistem UMGrow

## 1. Gambaran Umum
UMGrow merupakan **platform website berbasis kolaborasi UMKM**, dengan arsitektur yang menggabungkan *client-side dynamic rendering* dan *server-side data processing* menggunakan **Laravel (backend)**, **Tailwind CSS (frontend)**, dan **Livewire (interaksi real-time tanpa JavaScript murni)**.

Arsitektur ini menggunakan model **3-tier architecture**:
1. **Presentation Layer (Frontend/UI)**
2. **Application Layer (Logic/Controller)**
3. **Data Layer (Database Management)**

---

## 2. Arsitektur Umum Sistem

```
┌────────────────────────────────────────────────────────────┐
│                        CLIENT / USER                       │
│ (Browser: Chrome, Edge, Safari)                            │
│ └── Mengakses website UMGrow melalui URL utama             │
└────────────────────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│                 PRESENTATION LAYER (Frontend)              │
│ Framework: Tailwind CSS + Livewire                         │
│ - Tampilan Dashboard                                       │
│ - Daftar Produk & Kolaborasi                               │
│ - Form Login/Registrasi                                    │
│ - Form Ajakan Kolaborasi                                   │
│ - Komponen Dinamis (update data real-time)                 │
└────────────────────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│                APPLICATION LAYER (Backend/Logic)           │
│ Framework: Laravel (PHP)                                   │
│ - Authentication & Authorization                           │
│ - Pengelolaan Data Produk, Kolaborasi, Bundling            │
│ - Business Logic (pencarian mitra, evaluasi kolaborasi)    │
│ - Validasi Input & Proses CRUD                             │
│ - API internal Livewire untuk interaksi real-time          │
└────────────────────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│                    DATA LAYER (Database)                   │
│ Database: MySQL / MariaDB                                  │
│ - Tabel Users (akun pelaku UMKM)                           │
│ - Tabel ProfileUsaha (informasi UMKM)                      │
│ - Tabel Produk (data produk/jasa)                          │
│ - Tabel Kolaborasi (data ajakan dan status kolaborasi)     │
│ - Tabel Bundling (paket produk internal/kolaboratif)       │
│ - Tabel Penjualan (catatan transaksi dan statistik)        │
└────────────────────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│             EXTERNAL SERVICES & INTEGRATIONS               │
│ - WhatsApp API (komunikasi antar kolaborator)              │
│ - Email SMTP Server (notifikasi ajakan kolaborasi)         │
│ - Cloud Hosting / VPS (Laravel Deployment)                 │
└────────────────────────────────────────────────────────────┘
```

---

## 3. Komponen Utama dan Alur Data

1. **User mengakses website (Browser)** → menggunakan *interface* berbasis Tailwind CSS.  
2. **Livewire Component** → menangani event interaktif seperti “Ajak Kolaborasi”, “Tambah Produk”, “Update Dashboard” tanpa reload halaman.  
3. **Laravel Controller** → menerima request dari Livewire, memproses logika bisnis, dan berkomunikasi dengan database.  
4. **Database MySQL** → menyimpan data user, kolaborasi, penjualan, dan produk secara terstruktur.  
5. **External Integration** → saat kolaborasi diterima, sistem mengirim notifikasi lewat Email atau WhatsApp API.

---

## 4. Teknologi yang Digunakan

| Komponen | Teknologi | Fungsi |
|-----------|------------|--------|
| Frontend | Tailwind CSS | Desain responsif dan modern |
| Interaktivitas | Livewire | Real-time interaction tanpa JS manual |
| Backend | Laravel Framework | Logika aplikasi dan autentikasi |
| Database | MySQL / MariaDB | Penyimpanan data pengguna & transaksi |
| Hosting | VPS / Cloud (Render, Vercel, dsb) | Deploy aplikasi |
| Komunikasi | WhatsApp API & SMTP | Media komunikasi eksternal |

---

## 5. Diagram Arsitektur Sederhana

```
[User Browser]
      │
      ▼
[Frontend: Tailwind + Livewire]
      │
      ▼
[Laravel Controllers & Services]
      │
      ▼
[Database: MySQL]
      │
      └──> [External Services: Email, WhatsApp API]
```

---

## 6. Kelebihan Arsitektur

- **Efisien & interaktif:** Livewire memungkinkan UI dinamis tanpa JavaScript tambahan.  
- **Scalable:** Laravel modular, dapat diperluas untuk integrasi AI (seperti disebut di proposal).  
- **Secure:** Otentikasi Laravel + middleware melindungi data UMKM.  
- **Maintainable:** Pemisahan antara UI, logic, dan data memudahkan pengembangan.

---
