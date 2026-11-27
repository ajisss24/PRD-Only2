# Prototipe Tokopedia: Fitur Ulasan Relevan (Eksperimen A - Baseline: PRD Only)

> **Mata Kuliah:** Rekayasa Interaksi (UX) – Kelas C  
> **Tugas:** Worksheet 12 – Wireframe and Prototype (Merancang Tampilan dan Prototipe)  
> **Metode Pengembangan:** Eksperimen A (Baseline: PRD Only)  
> **Repository:** [https://github.com/ajisss24/PRD-Only2.git](https://github.com/ajisss24/PRD-Only2.git)  
> **Live Demo:** [https://ajisss24.github.io/PRD-Only2/](https://ajisss24.github.io/PRD-Only2/)  

---

## 📋 Deskripsi Proyek
Proyek ini merupakan implementasi **Eksperimen A (Baseline: PRD Only)** dalam rangka praktikum Rekayasa Interaksi. Prototipe ini dirancang dan dikembangkan secara langsung menggunakan acuan spesifikasi tunggal yaitu **Product Requirements Document (PRD) v1.0: Fitur Ulasan Relevan – Tokopedia**.

Fitur **Ulasan Relevan** dirancang untuk mempermudah calon pembeli Tokopedia dalam mengevaluasi pengalaman pembeli terdahulu secara lebih cepat, terstruktur, dan objektif tanpa perlu membaca ratusan ulasan satu per satu.

---

## 📱 Alur Interaksi & Keterhubungan Layar (Minimal 5 Layar/State)
Prototipe ini menyediakan minimal 5 tampilan/layar interaktif yang saling terhubung dalam satu user flow terpadu:

1. **Layar 1 – Product Detail Page (PDP) Tokopedia**
   - Header aplikasi e-commerce Tokopedia (Search, Cart, Notifikasi, Info Lokasi).
   - Tampilan produk utama (*SoundPulse ANC Pro Wireless Earbuds*).
   - Info harga, varian, toko Official Store, dan rating produk (4.8 / 5.0 dari 1.250 ulasan).
   - Section ulasan pembeli dengan Banner Fitur Baru "Ulasan Relevan".
   - CTA interaktif untuk membuka evaluasi ulasan lengkap.

2. **Layar 2 – Evaluasi Ulasan Penuh & Ringkasan Kelebihan/Kekurangan (FR-03)**
   - Header navigasi kembali ke detail produk.
   - Ringkasan Kelebihan (Pros): Suara jernih, baterai tahan 8 jam, build kokoh, pengiriman aman.
   - Ringkasan Kekurangan (Cons): ANC kurang maksimal di tempat sangat bising, kabel charger pendek.
   - Baris tab aspek (Semua, Kualitas, Fungsi, Kesesuaian, Pengiriman) dan tombol filter foto.
   - Daftar ulasan asli pembeli dengan rating, nama, tanggal, badge verifikasi pembelian.

3. **Layar 3 – Filter Aspek Ulasan Aktif (FR-01, FR-02)**
   - Pengguna memilih aspek tertentu (misal: "Kualitas" atau "Fungsi").
   - Sistem menyaring ulasan sesuai aspek yang dipilih.
   - Indikator active chip, jumlah ulasan yang relevan, serta tombol Reset/Hapus Filter.

4. **Layar 4 – Filter Ulasan Berfoto & Media Viewer (FR-05)**
   - Pengguna mengaktifkan toggle/filter "Dengan Foto".
   - Tampilan hanya menyajikan ulasan yang melampirkan foto barang asli.
   - Klik pada foto ulasan akan membuka **Modal Lightbox Foto** untuk melihat kondisi fisik produk yang diterima pembeli beserta ulasan aslinya.

5. **Layar 5 – Identifikasi Keluhan Umum & Penanganan Empty State (FR-04, AC-08)**
   - Tab "Keluhan Sering Muncul": menampilkan rangkuman topik masalah yang berulang (misal: "Kabel charger pendek - 14 pembeli", "Eartips ukuran S agak longgar - 8 pembeli") dan ulasan pembeli terkait.
   - Tombol simulasi "Uji Filter Kosong" untuk menampilkan **Empty State** (AC-08: "Ulasan tidak ditemukan") beserta tombol reset filter.

---

## 🛠️ Panduan Menjalankan Secara Lokal

```bash
# 1. Clone repository
git clone https://github.com/ajisss24/PRD-Only2.git

# 2. Masuk ke direktori
cd PRD-Only2

# 3. Install dependensi
npm install

# 4. Jalankan server lokal
npm run dev
```

Aplikasi dapat diakses melalui browser di `http://localhost:5173`.

---

## 📄 Dokumen PRD
Dokumentasi lengkap PRD v1.0 tersedia pada file terpisah: [PRD.md](./PRD.md).

---
*Proyek ini disusun untuk pemenuhan Tugas Praktikum Individu Worksheet 12 - Rekayasa Interaksi C.*
