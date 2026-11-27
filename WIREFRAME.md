# DOKUMENTASI WIREFRAME & STRUKTUR INFORMASI
## Fitur: Ulasan Relevan – Tokopedia
**Mata Kuliah:** Rekayasa Interaksi (UX)  
**Tugas:** Worksheet 12 – Wireframe and Prototype  
**Persona Pengguna:** Muhammad Alfarizi Hardiansyah (21 tahun, Mahasiswa)  

---

## 📌 Ringkasan 5 Layar Wireframe Terhubung

Rancangan wireframe ini menerjemahkan kebutuhan pengguna dan *User Flow* evaluasi produk menjadi antarmuka struktural (*low-fidelity*) yang menghubungkan minimal 5 layar:

```mermaid
flowchart LR
    L1["Layar 1: PDP Tokopedia (Entry Point)"] -->|Klik Banner Ulasan Relevan| L2["Layar 2: Evaluasi & Ringkasan Pros/Cons (FR-03)"]
    L2 -->|Pilih Chip Aspek| L3["Layar 3: Filter Aspek Aktif (FR-01, FR-02)"]
    L3 -->|Aktifkan Filter Foto| L4["Layar 4: Filter Foto & Modal Lightbox (FR-05)"]
    L4 -->|Pilih Tab Keluhan / Uji Filter| L5["Layar 5: Keluhan Umum (FR-04) & Empty State (AC-08)"]
    L5 -->|Reset / Kembali| L1
```

---

## 📐 Blueprint Struktur Informasi & Komponen Per Layar

### 1. LAYAR 1 – Product Detail Page (PDP) Tokopedia
*Tujuan Layar:* Memberikan informasi dasar produk dan menyediakan pintu masuk (*entry point*) yang jelas menuju fitur Ulasan Relevan.

```text
+-------------------------------------------------------+
| [<]  [ Search: TWS ANC Bluetooth... ]     [Bell] [Cart]|
+-------------------------------------------------------+
|  Dikirim ke: Kost Mahasiswa Alfarizi, Jakarta Selatan |
+-------------------------------------------------------+
|                                                       |
|              [  AREA FOTO PRODUK  ]                   |
|                   [ X - Box ]                         |
|                                                       |
|                                         1/3 Foto  [♥] |
+-------------------------------------------------------+
| [Official Store] Jakarta Pusat                        |
| SoundPulse ANC Pro Wireless Earbuds - Hi-Res Audio    |
| Rp 489.000  (Rp 750.000) [-35%]                       |
| ★ 4.8 | 2.890 Terjual | 98% Pembeli Puas              |
+-------------------------------------------------------+
| Varian Warna: [ Midnight Black ] [ Frost White ]      |
+-------------------------------------------------------+
| ===================================================== |
| [✦ FITUR BARU: ULASAN RELEVAN TOKOPEDIA]              |
| Evaluasi kualitas & fungsi produk lebih cepat!        |
| [✓ Ringkasan Kelebihan/Kekurangan] [✓ Filter Aspek]   |
| [ >>> TOMBOL CTA: Buka Ulasan Relevan & Rangkuman <<<]|
| ===================================================== |
+-------------------------------------------------------+
| Ulasan Pembeli (1.248)                   Lihat Semua >|
| [★ 4.8 / 5.0] [===== Progress Bar Rating =====]       |
+-------------------------------------------------------+
| [ + Keranjang ]                [ Beli Langsung ]      |
+-------------------------------------------------------+
```

**Komponen Utama:**
1. **Header Tokopedia:** Search input, ikon notifikasi, dan keranjang belanja.
2. **Media Showcase:** Foto produk dengan indikator jumlah gambar dan tombol favorit/share.
3. **Informasi Produk:** Badge toko, judul produk, harga diskon, dan rating kepuasan.
4. **Banner Prominen Ulasan Relevan (FR-01 s/d FR-05):** Menjelaskan manfaat fitur baru dan tombol CTA untuk masuk ke alur evaluasi.
5. **Sticky Bottom Bar:** Tombol tindakan langsung beli/tambah keranjang.

---

### 2. LAYAR 2 – Layar Evaluasi & Ringkasan Pros/Cons (FR-03)
*Tujuan Layar:* Menyajikan sintesis ringkasan kelebihan (*pros*) dan kekurangan (*cons*) secara transparan dari ribuan ulasan pembeli tanpa bias.

```text
+-------------------------------------------------------+
| [< Kembali]  Detail Produk / Ulasan Relevan           |
+-------------------------------------------------------+
| [Daftar Ulasan]  [*Ringkasan Pros/Cons]  [Keluhan]    |
+-------------------------------------------------------+
| [✦] RINGKASAN CERDAS ULASAN (FR-03)                   |
| Otomatis dirangkum dari 1.248 ulasan terverifikasi    |
|                                                       |
| +---------------------------------------------------+ |
| | [✓] KELEBIHAN UTAMA PRODUK                        | |
| | - Suara Jernih & Bass Solid  [92% Puas]           | |
| |   Aspek: Kualitas  | [Lihat ulasan sumber >]      | |
| | - Baterai Awet 7+ Jam        [88% Puas]           | |
| |   Aspek: Fungsi    | [Lihat ulasan sumber >]      | |
| +---------------------------------------------------+ |
|                                                       |
| +---------------------------------------------------+ |
| | [!] PERLU DIPERTIMBANGKAN (KEKURANGAN)            | |
| | - ANC Kurang Kedap di Keramaian  [17% ulasan]     | |
| |   Aspek: Fungsi    | [Lihat ulasan sumber >]      | |
| | - Kabel Charger Bawaan Pendek    [14% ulasan]     | |
| |   Aspek: Kesesuaian| [Lihat ulasan sumber >]      | |
| +---------------------------------------------------+ |
+-------------------------------------------------------+
| Filter: [ Semua ] [ Kualitas ] [ Fungsi ] ...         |
| [ ( ) Hanya Ulasan dengan Foto ]                      |
+-------------------------------------------------------+
| [Daftar Ulasan Asli Pembeli...]                       |
+-------------------------------------------------------+
```

**Komponen Utama:**
1. **Sub-Navigasi Tab:** Membagi tampilan ke tab *Daftar Ulasan*, *Ringkasan*, dan *Keluhan*.
2. **Kartu Kelebihan (Pros Card):** Menampilkan daftar poin positif beserta persentase kepuasan dan tautan ke ulasan sumber.
3. **Kartu Kekurangan (Cons Card):** Menampilkan hal yang perlu diwaspadai pembeli sebelum checkout.

---

### 3. LAYAR 3 – Filter Aspek Ulasan Aktif (FR-01, FR-02)
*Tujuan Layar:* Mempersempit ulasan hanya pada dimensi produk yang ingin dievaluasi pengguna (misal: hanya ingin mengecek kualitas suara dan fisik).

```text
+-------------------------------------------------------+
| Filter Aspek Produk (FR-01):          [Reset Filter ↺]|
+-------------------------------------------------------+
| [Semua] [ *KUALITAS (742)* ] [Fungsi] [Kesesuaian] ...|
+-------------------------------------------------------+
| [ ( ) Hanya Ulasan dengan Foto ]  Menampilkan: 742 uls|
+-------------------------------------------------------+
| +---------------------------------------------------+ |
| | [Avatar] Budi Santoso [✓ Terverifikasi]    ★★★★★  | |
| | 12 Nov 2026 • Varian: Midnight Black              | |
| | [Aspek: Kualitas] [Aspek: Fungsi]                 | |
| | "Sangat puas dengan suaranya! Bass-nya empuk dan  | |
| | vokal sangat detail. Desainnya elegan & kokoh..." | |
| | [👍 Membantu (42)]                    [ Laporkan ]| |
| +---------------------------------------------------+ |
| +---------------------------------------------------+ |
| | [Avatar] Alfarizi [✓ Terverifikasi]        ★★★★☆  | |
| | 08 Nov 2026 • Varian: Midnight Black              | |
| | [Aspek: Kualitas]                                 | |
| | "Build quality juara untuk harga 400 ribuan..."   | |
| +---------------------------------------------------+ |
+-------------------------------------------------------+
```

**Komponen Utama:**
1. **Horizontal Chip Selector:** Chip pilihan aspek (*Kualitas, Fungsi, Kesesuaian, Pengiriman*) dengan *active state* yang jelas.
2. **Counter Hasil Filter:** Menampilkan jumlah ulasan yang relevan.
3. **Ulasan Terkategori:** Kartu ulasan asli yang dilabeli badge aspek yang sesuai.

---

### 4. LAYAR 4 – Filter Foto & Modal Lightbox (FR-05)
*Tujuan Layar:* Membantu pengguna membandingkan kondisi riil fisik barang kiriman dengan foto etalase toko.

```text
+-------------------------------------------------------+
| Filter: [Semua] [Kualitas] ...                        |
| [ [✓] HANYA ULASAN DENGAN FOTO (ACTIVE) ]             |
+-------------------------------------------------------+
| Galeri Foto Pembeli:                                  |
| [Foto 1: Box]  [Foto 2: Case]  [Foto 3: Unit]         |
+-------------------------------------------------------+
|                                                       |
|   =================================================   |
|   || MODAL LIGHTBOX FOTO PEMBELI (POP-UP ZOOM)   ||   |
|   ||---------------------------------------------||   |
|   || Foto Pembeli: Budi Santoso              [X] ||   |
|   ||                                             ||   |
|   ||           +---------------------+           ||   |
|   ||           |                     |           ||   |
|   ||           |  PREVIEW FOTO BESAR |           ||   |
|   ||           |                     |           ||   |
|   ||           +---------------------+           ||   |
|   ||                                             ||   |
|   || Keterangan: "Tampilan fisik boks & earbuds" ||   |
|   || "Sesuai banget sama deskripsi toko..."      ||   |
|   || [ >>> Tutup Foto <<< ]                      ||   |
|   =================================================   |
|                                                       |
+-------------------------------------------------------+
```

**Komponen Utama:**
1. **Toggle Filter Foto:** Kontrol satu klik untuk menyaring ulasan yang menyertakan lampiran foto.
2. **Grid Galeri Thumbnail:** Koleksi foto pembeli yang dapat diklik langsung.
3. **Modal Lightbox Foto (FR-05):** Tampilan gambar diperbesar dengan *backdrop overlay*, keterangan kondisi produk, dan nama ulasan sumber.

---

### 5. LAYAR 5 – Keluhan Umum (FR-04) & Penanganan Empty State (AC-08)
*Tujuan Layar:* Memetakan keluhan yang sering berulang agar calon pembeli dapat menilai toleransi risiko, serta memberikan panduan saat filter tidak menemukan hasil ulasan.

```text
+-------------------------------------------------------+
| [Daftar Ulasan]  [Ringkasan]  [*KELUHAN UMUM (3)*]    |
+-------------------------------------------------------+
| [!] IDENTIFIKASI KELUHAN BERULANG (FR-04)             |
|                                                       |
| +---------------------------------------------------+ |
| | [RINGAN]                                          | |
| | Kabel Charger Bawaan Terlalu Pendek  [18 Pembeli] | |
| | Dampak: Harus menaruh boks dekat sumber listrik.  | |
| | 💡 Solusi: Gunakan kabel Type-C ponsel standar.   | |
| | [Periksa ulasan asli pembeli terkait (BR-08) >]   | |
| +---------------------------------------------------+ |
|                                                       |
| +---------------------------------------------------+ |
| | [SEDANG]                                          | |
| | Kekedapan ANC Kurang Maksimal Outdoor[12 Pembeli] | |
| | 💡 Solusi: Ganti eartips silikon ukuran L di boks | |
| +---------------------------------------------------+ |
|                                                       |
| [ Tombol: Uji Kondisi Sistem Tanpa Hasil (AC-08) ]    |
|                                                       |
| ===================================================== |
| [ 🔍 KONDISI FILTER KOSONG (EMPTY STATE) ]            |
| "Ulasan Tidak Ditemukan"                              |
| Tidak ada ulasan yang cocok dengan kriteria filter.   |
| [ >>> Hapus Filter & Tampilkan Semua <<< ]            |
| ===================================================== |
+-------------------------------------------------------+
```

**Komponen Utama:**
1. **Daftar Keluhan Umum:** Pengelompokan topik masalah berulang lengkap dengan indikator keparahan dan saran solusi.
2. **Keterhubungan ke Ulasan Asli (BR-08):** Tautan untuk memverifikasi ulasan yang mendasari keluhan tersebut.
3. **Komponen Empty State (AC-08):** Penanganan kondisi ramah pengguna ketika kombinasi filter menghasilkan nol ulasan, disertai tombol pemulihan (*Reset Filter*).
