# UMGrow — Software Requirements Specification (SRS)

## UMGrow
**UMGrow** adalah sebuah platform kolaborasi digital yang dirancang khusus untuk UMKM (Usaha Mikro, Kecil, dan Menengah). Aplikasi ini bertujuan menjadi jembatan bagi para pelaku UMKM untuk saling terhubung, berkolaborasi, memasarkan produk, serta meningkatkan daya saing mereka di era digital.  

Dengan UMGrow, UMKM dapat membangun jejaring bisnis, membuat paket produk bersama, mencatat transaksi, hingga melakukan evaluasi terhadap hasil kolaborasi. Platform ini mengedepankan prinsip **kolaborasi dan saling menguatkan**, bukan hanya sekadar marketplace.

---

## Why UMGrow?
UMKM sering menghadapi tantangan seperti keterbatasan modal, kurangnya promosi, dan minimnya akses ke mitra usaha.  
UMGrow hadir sebagai solusi untuk:  
- Memperluas jaringan kolaborasi antar UMKM.  
- Menyediakan sarana promosi produk secara digital.  
- Membantu pencatatan transaksi dan evaluasi usaha.  
- Memberikan ruang untuk membuat produk bundling bersama mitra.  

---

## Use Cases

### 1. UMKM Owner
- Membuat profil usaha dan mengunggah produk.  
- Mengirim undangan kolaborasi ke UMKM lain.  
- Membuat paket bundling (produk tunggal atau kolaborasi).  
- Mencatat penjualan dan melihat laporan usaha.  

### 2. Collaborator / Partner
- Menerima atau menolak undangan kolaborasi.  
- Menyumbangkan produk untuk paket bundling.  
- Berbagi hasil evaluasi kolaborasi.  

### 3. Buyer / Customer
- Menjelajahi produk dan paket kolaborasi.  
- Menghubungi UMKM melalui kontak yang tersedia.  

### 4. Admin
- Memverifikasi akun UMKM.  
- Memoderasi konten dan menjaga keamanan platform.  
- Melihat statistik pertumbuhan UMKM di platform.  

---

## 🛠️ Technologies
- **Frontend:** HTML, CSS (Tailwind / Bootstrap), Blade Template Engine  
- **Backend:** Laravel (PHP Framework)  
- **Database:** MySQL  
- **Others (optional):**  
  - Livewire (untuk interaksi dinamis)  
  - PDF Generator (laporan)  
  - API WhatsApp/Email (notifikasi)  

---

## ✨ Main Features
1. **User Authentication & Profiles**  
   - Registrasi, login, dan manajemen profil UMKM.  

2. **Product Management**  
   - Tambah, edit, hapus produk.  
   - Atur stok, harga, dan kategori.  

3. **Collaboration Module**  
   - Kirim & terima undangan kolaborasi.  
   - Status kolaborasi (pending, aktif, selesai).  

4. **Bundling Products**  
   - Membuat paket gabungan dari produk sendiri atau dengan mitra.  
   - Paket kolaborasi tampil di katalog.  

5. **Transactions & Reports**  
   - Catat penjualan manual.  
   - Lihat dashboard penjualan harian/mingguan.  
   - Export laporan (PDF/CSV).  

6. **Evaluation & Rating**  
   - Memberikan rating/review setelah kolaborasi selesai.  

7. **Admin Panel**  
   - Verifikasi akun UMKM.  
   - Moderasi produk & konten.  

---

## Example Flow
1. Seorang UMKM mendaftar di UMGrow dan membuat profil usaha.  
2. UMKM menambahkan beberapa produk, lalu mencari mitra dengan kategori yang sesuai.  
3. UMKM mengirim undangan kolaborasi, mitra menerima, lalu keduanya membuat paket bundling.  
4. Penjualan dari bundling dicatat dalam sistem, dan hasilnya muncul di dashboard masing-masing UMKM.  
5. Setelah kolaborasi selesai, keduanya saling memberi rating sebagai evaluasi.  

---

## Conclusion
UMGrow bukan sekadar marketplace, melainkan sebuah **ekosistem digital untuk kolaborasi UMKM**. Dengan fitur kolaborasi, bundling produk, pencatatan transaksi, dan evaluasi usaha, platform ini diharapkan dapat memperkuat daya saing UMKM di era digital serta memberikan nilai tambah dibanding aplikasi jualan biasa.
