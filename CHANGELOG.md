# Changelog – Eksperimen A: PRD Only (Baseline)

Semua perubahan dan tahapan pengembangan pada repositori [PRD-Only2](https://github.com/ajisss24/PRD-Only2.git) dicatat di file ini.

---

## [1.0.0] - 2026-11-27
### Added
- Inisialisasi repositori Git dan struktur proyek web prototipe `PRD-Only2`.
- Penambahan file dokumentasi utama:
  - `PRD.md`: Berisi Product Requirements Document v1.0 Fitur Ulasan Relevan Tokopedia.
  - `WIREFRAME.md`: Berisi spesifikasi struktur informasi, komponen utama, dan blueprint UI 5 layar low-fidelity untuk kebutuhan laporan Worksheet 12.
  - `README.md`: Berisi pengantar proyek, alur 5 layar interaktif, link live demo, dan panduan instalasi.
  - `CHANGELOG.md`: Riwayat pencatatan pengembangan baseline.
- Implementasi source code prototipe interaktif (React + Tailwind CSS + Lucide Icons):
  - **Fitur Switcher Mode:** Menambahkan toggle `✨ Prototipe Hi-Fi` vs `📐 Wireframe Lo-Fi (Blueprint Struktural)` langsung di aplikasi.
  - **Layar 1 (Product Detail Page)**: Menampilkan header Tokopedia, showcase produk TWS ANC, ringkasan rating 4.8/5.0, dan widget teaser ulasan relevan.
  - **Layar 2 (Halaman Ulasan Penuh & Ringkasan Sentimen)**: Komponen ringkasan kelebihan (pros) & kekurangan (cons) otomatis (FR-03).
  - **Layar 3 (Filter Aspek Ulasan)**: Fitur filter interaktif aspek kualitas, fungsi, kesesuaian deskripsi, dan pengiriman (FR-01, FR-02).
  - **Layar 4 (Filter Foto & Modal Lightbox)**: Filter khusus ulasan yang memiliki foto serta tampilan zoom foto produk asli pembeli (FR-05).
  - **Layar 5 (Keluhan Umum & Empty State)**: Komponen identifikasi masalah yang berulang (FR-04) dan penanganan kondisi filter kosong (AC-08).
- Konfigurasi build Vite dan GitHub Pages deployment workflow untuk akses live demo publik.
