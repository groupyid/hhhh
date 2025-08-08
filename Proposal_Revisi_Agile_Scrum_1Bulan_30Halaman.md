# Proposal Pengembangan Web App (Maks 30 Halaman)

## Ringkasan Eksekutif
- **Durasi**: 1 bulan (4 sprint mingguan)
- **Metodologi**: Agile Scrum (iteratif, inkremental)
- **Cakupan**: Pengembangan web app hingga **maksimal 30 halaman unik** (route-level)
- **Hasil Akhir**: Aplikasi siap rilis (MVP), dokumentasi, source code, pipeline CI/CD, dan materi serah terima

## Tujuan
Membangun web app fungsional dengan kualitas produksi dalam 1 bulan, melalui iterasi mingguan yang memungkinkan umpan balik cepat dan prioritas yang adaptif.

## Ruang Lingkup (Maks 30 Halaman)
- **Definisi halaman**: Satu halaman = satu route unik (mis. `/login`, `/dashboard`, `/users/[id]`). Variasi modal/komponen pada halaman yang sama tidak dihitung terpisah.
- **Contoh alokasi** (dapat disesuaikan saat Sprint Planning):
  - Auth: Login, Register, Lupa Password (3)
  - Dashboard utama (1)
  - Manajemen Pengguna: List, Detail, Tambah/Edit (3)
  - Modul Inti A: List, Detail, Tambah/Edit (3-4)
  - Modul Inti B: List, Detail, Tambah/Edit (3-4)
  - Laporan/Analitik: 2-4 halaman
  - Pengaturan: Profil, Preferensi, Hak Akses (2-3)
  - Halaman pendukung: Beranda publik, 404, 500 (2-3)
- **Out of scope** (opsional untuk fase lanjut): Fitur realtime kompleks, integrasi pihak ketiga besar, mobile app native.
- **Perubahan scope**: Perubahan prioritas dimungkinkan per sprint; total halaman tetap ≤ 30.

## Metodologi: Agile Scrum
- **Peran**:
  - Product Owner (PO) – perwakilan stakeholder, memprioritaskan backlog
  - Scrum Master – fasilitasi proses, hilangkan hambatan
  - Development Team – engineer, QA, UI/UX, DevOps
- **Event**:
  - Sprint Planning (2 jam/minggu)
  - Daily Scrum (maks 15 menit/hari)
  - Sprint Review (1 jam/minggu) – demo inkrement
  - Sprint Retrospective (45 menit/minggu)
- **Artefak**: Product Backlog, Sprint Backlog, Increment, Burndown
- **Definition of Ready (DoR)**: User story jelas, acceptance criteria, desain/wireframe siap, dependensi teridentifikasi
- **Definition of Done (DoD)**: Kode lulus review, unit test ≥ 60% area kritis, e2e happy path, lulus QA, terdokumentasi, ter-deploy ke staging

## Rencana Iterasi (4 Sprint, 1 Bulan)
- **Sprint 1 (Minggu 1)** – Fondasi & Kerangka
  - Setup repo, arsitektur, desain sistem, komponen UI dasar
  - Auth (Login/Logout), skema basis data inti, pipeline CI/CD, deployment staging
- **Sprint 2 (Minggu 2)** – Modul Inti I
  - CRUD modul prioritas tertinggi, Dashboard awal, tabel & filter dasar
  - Unit test prioritas, validasi form, notifikasi dasar
- **Sprint 3 (Minggu 3)** – Modul Inti II + Laporan
  - CRUD modul kedua, laporan/ekspor awal, peran & izin dasar
  - Optimalisasi performa awal, penguatan QA (e2e utama)
- **Sprint 4 (Minggu 4)** – Hardening & Go‑Live
  - Penyempurnaan UX, perbaikan bug, security pass, dokumentasi akhir
  - UAT, persiapan rilis, handover, pelatihan singkat

## Timeline (Mingguan)
- Minggu 1: Inisiasi, arsitektur, Auth, staging siap
- Minggu 2: Modul Inti I, Dashboard, QA awal
- Minggu 3: Modul Inti II, Laporan, Role/Permission
- Minggu 4: Stabilitas, UAT, Go‑Live

## Deliverables
- Source code (backend, frontend), infrastruktur sebagai kode (jika relevan)
- Desain UI (wireframe/prototype) dan design system komponen
- Dokumen: arsitektur ringkas, panduan deploy, panduan pengguna
- Pipeline CI/CD, environment staging; rilis produksi (jika disepakati)

## Kualitas & Pengujian
- Unit test modul kritis; target cakupan proporsional terhadap risiko
- E2E untuk alur utama (auth, CRUD, laporan)
- Static analysis & lint, PR review wajib, keamanan dasar (OWASP Top 10 tingkat dasar)

## Teknologi (Contoh)
- Frontend: React/Next.js atau Vue/Nuxt
- Backend: Node.js (NestJS/Express) atau alternatif sesuai kebutuhan
- Database: PostgreSQL/MySQL
- Infrastruktur: Docker, CI/CD (GitHub Actions/GitLab CI), hosting cloud

## Manajemen Perubahan
- Perubahan prioritas melalui Product Backlog Refinement
- Penambahan di luar 30 halaman dinegosiasikan sebagai fase lanjutan

## Risiko & Mitigasi
- Ketidakjelasan kebutuhan → Refinement mingguan, prototipe cepat
- Waktu terbatas → Fokus MVP, potong ruang lingkup rendah nilai
- Integrasi eksternal → Mock/adapter, fallback manual sementara

## Peran & Komunikasi
- Channel utama: ruang chat/tiket proyek
- Cadence: Daily Scrum ringkas, Review & Retro tiap akhir minggu
- Keputusan prioritas oleh PO; transparansi via board Kanban/Scrum

## Kriteria Penerimaan (Contoh)
- Semua user story MVP lulus UAT di staging
- Tidak ada bug blocker/critical terbuka menjelang rilis
- Dokumentasi pengguna dan operasional tersedia

## Dukungan Pasca Rilis
- Garansi perbaikan bug kritis: 2 minggu setelah rilis
- Knowledge transfer/handover tim internal

---
Catatan: Rincian modul/halaman disesuaikan bersama PO saat Sprint Planning pertama; total halaman tetap maksimal 30 dalam rentang 1 bulan.