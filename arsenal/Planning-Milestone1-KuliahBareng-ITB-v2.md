   # Planning Milestone 1 (v2) — IF3151 Interaksi Manusia Komputer
## "KuliahBareng" — Info Matkul & Dosen, Forum Tanya, Kalkulator IPK, dan Simulasi Rencana Studi untuk Mahasiswa ITB

| Item | Keterangan |
|---|---|
| Deadline | **Minggu, 20 September 2026 pukul 20.00** (target internal submit: **18.00**) |
| Sisa waktu (dihitung dari Rabu, 16 Sept malam) | ± 4 hari efektif |
| Output | 1 file `.pptx` → `MS1-Requirement-<no kelas>-<no kelompok>-KuliahBareng` |
| Tempat submit | `s.hmif.dev/PengumpulanMilestoneIMK` |
| Metode data | Wawancara langsung semi-terstruktur + observasi artefak (tanpa Google Form) |
| Status dokumen | Versi 2 — menggantikan v1. Semua isi bertanda **[HIPOTESIS]** wajib divalidasi dengan data wawancara. |

---

## Daftar Isi

0. Baca Ini Dulu (wajib, 10 menit)
1. Struktur Tim & Pembagian Tugas
2. Timeline Rabu–Minggu & Titik Sinkronisasi
3. Infrastruktur Kerja (Drive, Registry Sheet, Konvensi Kode, Glosarium)
4. Deskripsi Topik & SDG
5. Pendekatan Riset
6. Panduan Wawancara v2
7. Template Ringkasan Wawancara
8. Sesi Sintesis (Jumat malam)
9. Masalah & Opportunity
10. User Goals (User Story)
11. User Process Flow (Swimlane)
12. User Persona
13. Scenario
14. User Tasks
15. Fungsionalitas Sistem (Essential Use Case)
16. Usability Goals & UX Goals
17. Lampiran (Penggunaan AI & Evidence)
18. Outline PPT Final (urutan sesuai spesifikasi) + Owner per Slide
19. Review, QA, & Checklist Submit
20. Risiko & Mitigasi
21. Kartu Tugas per Anggota (ringkasan to-do harian)

---

## 0. Baca Ini Dulu

### 0.1 Apa saja yang diperbaiki dari v1

| # | Masalah di v1 | Dampak | Perbaikan di v2 |
|---|---|---|---|
| 1 | Fitur dan user story sudah "dikunci" sebelum wawancara | Milestone 1 menilai **problem space**; asisten bisa menilai kelompok *solution-first* dan data terkesan dicocok-cocokkan | Semua M, UG, P, persona diberi label **[HIPOTESIS]**, ada **aturan keputusan** di sesi sintesis untuk mempertahankan/mengubah/menggugurkan (Bagian 8) |
| 2 | Urutan outline PPT tidak mengikuti sistematika spesifikasi (persona sebelum flow, Masalah ditaruh di slide 29 setelah fungsionalitas) | Berisiko dianggap tidak sesuai format | Outline disusun ulang persis mengikuti urutan 1a → 5b spesifikasi (Bagian 18) |
| 3 | Swimlane v1 hanya rantai linear 7 kotak, tanpa keputusan (decision), dan **tidak mencakup proses hitung IPK/rencana studi** | UG5/UG6 tidak punya kode Proses → tabel User Task v1 menulis "M5" di kolom Proses (salah kolom) | Swimlane baru 4 lane, 13 proses, 3 decision, mencakup siklus satu semester penuh sehingga semua UG punya P (Bagian 11) |
| 4 | PIC User Task tersebar lintas User Goal (UG1 dipegang PIC-1 & PIC-2, dst.) | Banyak koordinasi antar-anggota → tidak paralel | Model **domain ownership**: tiap anggota memegang 1 domain end-to-end (segmen wawancara → UG → UT → F → baris usability goal) (Bagian 1) |
| 5 | Segmen wawancara tidak selaras dengan UG (mis. UG4 "mahasiswa pindahan/exchange" tidak pernah diwawancara) | UG4 tidak punya data pendukung | Segmen informan dipetakan 1:1 ke domain; UG4 di-reframe ke "mahasiswa yang menyusun FRS/matkul pilihan" |
| 6 | Panduan wawancara 23 pertanyaan untuk 20–30 menit, beberapa pertanyaan *leading* & hipotetis (mis. "fitur apa yang kamu butuhkan", "seberapa kepikiran pakai fitur X") | Data bias, waktu tidak cukup, jawaban hipotetis tidak valid | Dipecah jadi **Modul Inti** (semua informan) + **Modul Deep-Dive** (per domain), fokus pada perilaku masa lalu, ditambah **observasi artefak** (Bagian 6) |
| 7 | Tidak ada pertanyaan soal kebiasaan device/aplikasi | Spesifikasi 2d secara eksplisit meminta "kebiasaan menggunakan aplikasi, device" di persona | Ditambahkan di Modul Inti bagian Profil Digital |
| 8 | Spesifikasi menyebut metode riset "Kuesioner, Interview, Observasi"; v1 hanya wawancara | Pendekatan riset terlihat tipis | Ditambah **observasi artefak** (informan menunjukkan spreadsheet IPK, pencarian di grup chat, halaman FRS) — tanpa biaya waktu tambahan |
| 9 | Persona 1 (TPB semester 2 memilih "matkul pilihan") dan skenario "seminggu sebelum FRS" tidak konsisten dengan kalender & kurikulum TPB yang sebagian besar sudah ditentukan | Tidak realistis → persona terlihat dikarang | Persona & skenario disusun ulang dengan kalender yang konsisten; TPB diarahkan ke kebutuhan IP untuk penjurusan (verifikasi di wawancara) |
| 10 | Hanya 2 persona, dan tidak ada persona yang merepresentasikan kebutuhan IPK/rencana studi; skenario tidak menyentuh UG5/UG6 | Spesifikasi: scenario disusun dari **kumpulan** user story | 3 kerangka persona (berbasis perilaku) + 2 skenario yang bersama-sama mencakup UG1–UG6 |
| 11 | Tabel Fungsionalitas bukan format **Essential Use Case** (User Intention ↔ System Responsibility) dan hubungannya 1 UT : 1 F | Tidak sesuai contoh spesifikasi | Format EUC per UG, 1 UT boleh beberapa F, penomoran F per UG, 1 contoh lengkap sebagai standar kualitas (Bagian 15) |
| 12 | Usability goals: "Effective" dipakai 2 kali, tidak ada *safety* & *memorability*, UX goals memakai istilah di luar buku (Empowering, Trustworthy) tanpa justifikasi | Justifikasi lemah; padahal goals ini dipakai lagi di MS3 & MS5 | Enam usability goals (Rogers, Sharp & Preece) masing-masing dipakai tepat 1 kali + kriteria terukur untuk evaluasi nanti (Bagian 16) |
| 13 | Tipe interaksi kurang tepat (mis. "Instructing/Responding" untuk membalas forum) | Poin 2f dinilai | Pemetaan tipe interaksi dikoreksi + alasannya (Bagian 14.3) |
| 14 | Tidak ada analisis solusi existing | Tujuan umum tugas: produk harus inovatif atau menyelesaikan masalah software existing "sehingga pengguna beralih" | Ditambah slide *existing solutions & gap* dan positioning pembeda dari TemanKuliah (Bagian 4.3) |
| 15 | Tidak ada timeline, protokol sintesis, template catatan, konvensi kode, atau mekanisme review | Rawan bentrok kode, inkonsistensi, dan telat | Bagian 2, 3, 7, 8, 19 |
| 16 | Tips "satu pewawancara, satu pencatat" bertentangan dengan kerja paralel 5 orang × 2 informan | Jadwal saling tunggu | Wawancara solo + rekaman audio + template catatan; berpasangan hanya jika kebetulan jadwal cocok |

### 0.2 Lima prinsip kerja (disepakati semua anggota)

1. **Data dulu, klaim belakangan.** Setiap M, persona, dan kutipan di slide harus bisa ditunjuk sumbernya (kode informan I1–I10). Kalau tidak ada datanya, jangan ditulis.
2. **Satu sumber kebenaran untuk kode.** Semua kode (I, M, UG, P, UT, F, UsG, UxG) hanya dibuat/diubah di **Registry Sheet** (Bagian 3.2). Slide mengutip Registry, bukan sebaliknya.
3. **Kerjakan domainmu sendiri end-to-end.** Anggota tidak menunggu anggota lain kecuali di 3 titik sinkronisasi yang sudah dijadwalkan (Bagian 2).
4. **Istilah seragam.** Pakai istilah dari Glosarium (Bagian 3.4). Contoh: selalu "matkul", bukan campur "mata kuliah/course/MK".
5. **Aturan AI dari spesifikasi:** AI hanya boleh untuk **eksplorasi masalah & pendalaman konsep desain interaksi**. Persona, kutipan, temuan, M, dan skenario **ditulis kelompok dari data wawancara**, bukan digenerate. Setiap penggunaan AI dicatat di tab `AI_Log` (termasuk penggunaan AI untuk menyusun dokumen planning ini).

### 0.3 Keputusan yang WAJIB dikunci malam ini (Rabu, 16 Sept, maks. 22.00)

| # | Keputusan | Default yang disarankan | Siapa memutuskan |
|---|---|---|---|
| K1 | SDG final (cek `s.hmif.dev/KelompokIMK` **sekarang**, isi secepatnya karena satu kelas tidak boleh sama) | SDG 4; cadangan SDG 10 (lihat 4.2) | Semua, dieksekusi A |
| K2 | Siapa Anggota A–E | Lihat 1.2 — cocokkan dengan jaringan informan tiap orang | Semua |
| K3 | Tools kolaborasi | Google Drive + Google Sheets (Registry) + FigJam/Miro (sintesis) + draw.io/FigJam (swimlane) + Google Slides (lalu export .pptx) **atau** PowerPoint Online | Semua |
| K4 | Nama produk final | "KuliahBareng" (boleh ganti, tapi kunci malam ini supaya tidak ubah 40 slide) | Semua |
| K5 | No. kelas & no. kelompok untuk nama file | — | A |

---

## 1. Struktur Tim & Pembagian Tugas

### 1.1 Model pembagian: *Domain Owner* + *Integrator*

Setiap anggota punya **dua peran**:

- **Domain Owner** — memegang satu area masalah secara vertikal: mewawancarai 2 informan dari segmen domain itu → menulis User Goal domainnya → 2 User Task → Fungsionalitas (EUC) → 1 baris Usability Goal + 1 baris UX Goal. Karena tiap domain berdiri sendiri, kelima anggota bisa bekerja **bersamaan tanpa saling tunggu**. Ini sekaligus memenuhi syarat spesifikasi "setiap anggota wajib menjadi PIC untuk User Task yang berbeda".
- **Integrator** — memegang satu artefak lintas-domain (topik, swimlane, persona, masalah+skenario, PPT). Integrator **menerima input** dari semua domain owner lewat template, lalu menyatukannya.

### 1.2 Tabel pembagian anggota

> Isi nama & NIM di Registry tab `Tim`. Pilih siapa jadi A–E berdasarkan **siapa punya akses termudah ke segmen informannya**, bukan berdasarkan fitur favorit.

| Anggota | Domain (Owner) | User Goal | User Task (PIC) | Informan | Segmen informan | Peran Integrator |
|---|---|---|---|---|---|---|
| **A** `[Nama – NIM]` | Info Matkul & Dosen | UG1 | UT1.1, UT1.2 | I1, I2 | **Pencari info**: angkatan 2025 (semester 3) yang baru pertama kali FRS di prodi | **Topik & Riset** (slide judul, 1a, 1b), **fasilitator sesi sintesis**, **Lampiran** (AI & Evidence), koordinator umum |
| **B** `[Nama – NIM]` | Jelajah & Bandingkan Matkul (penyusunan FRS) | UG4 | UT4.1, UT4.2 | I3, I4 | **Perencana FRS lintas prodi**: angkatan 2023–2024 yang pernah ambil matkul pilihan di luar prodi / minor | **Swimlane** (2c: diagram + deskripsi P) |
| **C** `[Nama – NIM]` | Forum Tanya Matkul | UG2 | UT2.1, UT2.2 | I5, I6 | **Penanya tugas**: semester 3–5 yang sedang ambil matkul dengan tugas berat dan aktif di grup kelas | **Persona** (2d) |
| **D** `[Nama – NIM]` | Kontribusi Kating | UG3 | UT3.1, UT3.2 | I7, I8 | **Kating kontributor**: angkatan 2022–2023, sering ditanya adik tingkat (mentor/asisten/pengurus himpunan) | **Masalah & Opportunity** (2a) + **Scenario** (2e) |
| **E** `[Nama – NIM]` | Perencanaan Akademik | UG5, UG6 | UT5.1, UT6.1 | I9, I10 | **Perencana akademik**: I9 = angkatan 2025 yang menghitung IP saat TPB (terkait penjurusan); I10 = angkatan 2022–2023 yang menyusun sisa SKS sampai lulus | **PPT Owner** (template, konsolidasi tabel UT/F/Usability, perakitan akhir, export, submit) |

Estimasi beban per orang ± 14–17 jam dalam 4 hari; beban integrator diseimbangkan dengan waktunya (A berat di Kamis & Minggu, B–D berat di Sabtu, E berat di Kamis & Minggu).

### 1.3 Matriks tanggung jawab per deliverable

R = mengerjakan, A = memastikan selesai & final, I = memberi input, V = reviewer

| Deliverable (spesifikasi) | A | B | C | D | E |
|---|---|---|---|---|---|
| Slide Judul + identitas | R/A | | | | V |
| 1a Deskripsi topik & SDG | R/A | | | | V |
| 1b Pendekatan riset | R/A | I | I | I | I |
| Wawancara & ringkasan (2 informan) | R | R | R | R | R |
| Sesi sintesis (affinity map) | A (fasilitator) | R | R | R | R |
| 2a Masalah & Opportunity | I | I | I | R/A | V |
| 2b User Goals | R (UG1) | R (UG4) | R (UG2) | R (UG3) | R (UG5, UG6) + A (konsolidasi) |
| 2c Swimlane + deskripsi P | I | R/A | I | I | V |
| 2d Persona | I | I | R/A | V | I |
| 2e Scenario | V | I | I | R/A | I |
| 2f Tabel UT + deskripsi UT | R | R | R | R | R + A (tabel gabungan) |
| 3 Fungsionalitas (EUC) | R | R | R | R | R + A (konsistensi format) |
| 4 Usability & UX Goals | R (baris domain) | R | R | R | R + A (tabel gabungan) |
| 5a Lampiran AI | R/A | I | I | I | I |
| 5b Evidence | A | I | I | I | I |
| Perakitan, export, submit | V | | | | R/A |

---

## 2. Timeline Rabu–Minggu & Titik Sinkronisasi

Hanya ada **3 sinkronisasi wajib** (SYNC). Di luar itu kerja paralel + update async di grup chat.

### Rabu, 16 Sept (malam) — Kickoff
| Waktu | Aktivitas | Siapa |
|---|---|---|
| 19.30–20.30 | **SYNC-1 Kickoff (online, 60 menit)**: kunci K1–K5, baca Bagian 0–3 bersama, sepakati pembagian A–E, uji coba 1 pertanyaan wawancara | Semua |
| 20.30–22.00 | Hubungi calon informan (target 2 utama + **1 cadangan** per orang), buat jadwal wawancara Kamis–Jumat pagi | Semua |
| 20.30–22.00 | Buat folder Drive, Registry Sheet (tab lengkap), template ringkasan wawancara, board FigJam kosong | A (Drive & Registry), E (template PPT mulai) |
| 22.00 | Setiap orang post di grup: nama inisial informan + jadwal | Semua |

### Kamis, 17 Sept — Hari Wawancara + Pekerjaan yang Tidak Butuh Data
| Waktu | Aktivitas | Siapa |
|---|---|---|
| Sepanjang hari | Wawancara I1–I10 (target **minimal 6 dari 10 selesai hari ini**) | Semua |
| ≤ 3 jam setelah tiap wawancara | Isi Template Ringkasan (Bagian 7) selagi ingatan segar + upload rekaman | Pewawancara |
| Siang | Draft slide Judul, 1a (topik & SDG), 1b (pendekatan riset) — tidak bergantung data | A |
| Siang | Master template PPT: warna, font, layout judul/divider/tabel/persona/EUC, slide kosong sesuai outline Bagian 18 | E |
| Sore | Draft kerangka lane swimlane dari hipotesis P (Bagian 11) di draw.io — nanti divalidasi | B |
| Sore | Siapkan layout persona kosong 3 buah di template E | C |
| Sore | Riset existing solutions (lihat 4.3) — kumpulkan dari jawaban wawancara yang sudah masuk | D |
| 21.00 | Update async: "wawancara selesai x/2, ringkasan x/2, blocker: ..." | Semua |

### Jumat, 18 Sept — Selesaikan Data + Sintesis
| Waktu | Aktivitas | Siapa |
|---|---|---|
| ≤ 13.00 | **Semua 10 wawancara selesai** (pakai cadangan bila ada yang batal) | Semua |
| ≤ 17.00 | Semua 10 ringkasan terisi + sticky notes (10–20 per informan) sudah ditempel di FigJam area masing-masing | Semua |
| 17.00–19.00 | Baca sticky notes informan domain lain (wajib, supaya sintesis cepat) | Semua |
| 19.00–21.30 | **SYNC-2 Sesi Sintesis (online, 150 menit)** — protokol Bagian 8. Output: M final, UG final, keputusan persona, daftar P final, kode dikunci di Registry | Semua, fasilitator A |
| 21.30–22.30 | A merapikan Registry; D menulis draf kalimat M; B mulai menggambar swimlane final | A, B, D |

### Sabtu, 19 Sept — Produksi Paralel
| Waktu | Aktivitas | Siapa |
|---|---|---|
| ≤ 10.00 | **Swimlane final + kode P1–Pn dikunci di Registry** (domain owner butuh P untuk tabel UT) | B |
| ≤ 12.00 | Slide 2a Masalah & Opportunity + slide temuan wawancara | D |
| ≤ 12.00 | UG domain final + baris tabel UT (UG–P–UT–PIC) di Registry | A, B, C, D, E |
| ≤ 14.00 | Draf 3 persona | C |
| ≤ 16.00 | Deskripsi UT (2 slide per orang) + EUC & deskripsi F domain | A, B, C, D, E |
| ≤ 17.00 | Baris Usability Goal + UX Goal domain beserta justifikasi | A, B, C, D, E |
| 14.00–18.00 | Scenario S1 & S2 (butuh persona C + P dari B) | D |
| ≤ 18.00 | Lampiran AI & Evidence (kumpulkan dari AI_Log & folder evidence) | A |
| ≤ 20.00 | **Semua konten sudah masuk file PPT** di slide masing-masing | Semua |
| 20.00–21.00 | **SYNC-3 Walkthrough (online, 60 menit)**: E menampilkan PPT dari awal sampai akhir, semua mencatat ketidakkonsistenan | Semua |
| 21.00–23.00 | Konsolidasi tabel gabungan UT, F, Usability/UX; perbaikan hasil SYNC-3 | E (tabel), semua (slide sendiri) |

### Minggu, 20 Sept — Review, QA, Submit
| Waktu | Aktivitas | Siapa |
|---|---|---|
| 08.00–11.00 | **Cross-review** berpasangan (Bagian 19.1) — reviewer menulis komentar di slide, tidak mengedit langsung | Semua |
| 11.00–14.00 | Perbaikan dari komentar | Pemilik slide |
| 14.00–15.00 | **Traceability check** penuh (Bagian 19.2) | A + E |
| 15.00–17.00 | Polish visual, cek font/tabel/diagram, nomor slide | E |
| 17.00 | **Content freeze** — tidak ada perubahan isi setelah ini kecuali typo | Semua |
| 17.00–18.00 | Export .pptx, buka ulang di PowerPoint/Keynote/Google Slides untuk cek layout, cek ukuran file, rename sesuai format | E |
| **18.00** | **Submit** + screenshot bukti submit ke grup | E |
| 18.00–20.00 | Buffer darurat (jangan dipakai kecuali terpaksa) | — |

### Aturan jika terlambat
- Jika seseorang tidak bisa menyelesaikan item di jam targetnya, **wajib post di grup paling lambat 2 jam sebelum target** dengan: apa yang belum, perkiraan selesai, butuh bantuan apa.
- Koordinator (A) boleh memindahkan pekerjaan ke anggota yang paling longgar di hari itu.
- Jika wawancara ke-10 tidak didapat sampai Jumat 13.00: ambil informan cadangan siapa pun yang memenuhi segmen **terdekat**; jika tetap tidak ada, lanjut dengan 9 dan tulis jujur di slide pendekatan riset.

---

## 3. Infrastruktur Kerja

### 3.1 Struktur folder Google Drive
```
IMK-MS1-KuliahBareng/
├── 00_Admin/                  → Registry Sheet, dokumen planning ini, spesifikasi
├── 01_Rekaman/  (akses terbatas anggota saja)
│   ├── I01_A_<inisial>/       → audio/video + foto sesi
│   └── ... I10_E_<inisial>/
├── 02_Ringkasan_Wawancara/    → I01.docx ... I10.docx (template Bagian 7)
├── 03_Sintesis/               → link FigJam + export PNG affinity map
├── 04_Diagram/                → swimlane (.drawio + .png), EUC
├── 05_PPT/                    → file kerja + export final
├── 06_Evidence_Terpilih/      → foto/screenshot yang sudah disamarkan untuk lampiran
└── 07_AI_Log/                 → screenshot percakapan AI
```

### 3.2 Registry Sheet (Google Sheets) — tab yang wajib ada

| Tab | Kolom | Pemilik edit |
|---|---|---|
| `Tim` | Kode anggota (A–E), Nama, NIM, Domain, Peran integrator, No. HP | A |
| `Informan` | Kode (I1–I10), Pewawancara, Inisial, Angkatan, Prodi, Fakultas, Segmen, Tanggal, Mode (tatap muka/online), Durasi, Consent rekam (Y/N), Consent foto (Y/N), Link rekaman, Link ringkasan | Pewawancara masing-masing |
| `Masalah` | Kode M, Deskripsi, Tipe (Masalah/Opportunity), Informan pendukung (I..), Jumlah (x/10), Kutipan terpilih + kode informan | D (setelah sintesis) |
| `UserGoal` | Kode UG, Role, Goal, Reason, Menjawab M.., Owner | Domain owner (baris sendiri) |
| `Proses` | Kode P, Lane, Deskripsi, Masuk dari, Keluar ke, Terkait UG | B |
| `UserTask` | Kode UT, UG, P, Nama task, User, Tipe interaksi, Metafora, PIC (NIM) | Domain owner (baris sendiri) |
| `Fungsional` | Kode F, UT, User intention, System responsibility, PIC | Domain owner (baris sendiri) |
| `UsabilityUX` | Kode (UsG1../UxG1..), Nama goal, Justifikasi, M, UG, F, Kriteria terukur, Owner | Domain owner (baris sendiri), dirapikan E |
| `Traceability` | Matriks cek otomatis M ↔ UG ↔ P ↔ UT ↔ F (Bagian 19.2) | A |
| `Glosarium` | Istilah baku, definisi, istilah yang dilarang | A |
| `AI_Log` | Tanggal, Anggota, Tools, Tujuan, Prompt ringkas, Bagaimana hasilnya dipakai/diubah, Link screenshot | Semua |
| `Status` | Item, Owner, Target jam, Status (Belum/Proses/Review/Selesai), Catatan | Semua |

### 3.3 Konvensi kode (tidak boleh dilanggar)

| Kode | Format | Contoh | Aturan |
|---|---|---|---|
| Informan | `I1`–`I10` | I3 | I1–I2 = A, I3–I4 = B, I5–I6 = C, I7–I8 = D, I9–I10 = E. Cadangan: `I11+` |
| Masalah/Opportunity | `M1`, `M2`, … | M4 | Tulis "(Opportunity)" di belakang jika opportunity |
| User Goal | `UG1`–`UG6` | UG4 | Nomor UG **tetap mengikuti domain** walau urutan tampil di slide berbeda |
| Proses | `P1`, `P2`, … | P11 | Diberi nomor berurutan mengikuti alur waktu di swimlane; hanya B yang memberi nomor |
| Decision | `D1`, `D2`, … | D2 | Belah ketupat di swimlane |
| User Task | `UT<UG>.<n>` | UT4.2 | Maksimal 2 per domain (E: UT5.1 & UT6.1) |
| Fungsional | `F<UG>.<n>` | F4.3 | Nomor per UG, **tidak terikat nomor UT** (satu UT boleh punya F4.1–F4.3) — sehingga tidak mungkin bentrok antar-anggota |
| Usability goal | `UsG1`–`UsG6` | UsG5 | Satu per jenis usability goal |
| UX goal | `UxG1`–`UxG6` | UxG2 | Satu per domain |
| Persona | `PR1`–`PR3` | PR2 | |
| Scenario | `S1`, `S2` | S1 | |

### 3.4 Glosarium awal (lengkapi di Registry)

| Pakai | Jangan pakai | Arti |
|---|---|---|
| matkul | mata kuliah / MK / course (campur-campur) | Mata kuliah |
| kating | senior / kakak tingkat (campur-campur) | Mahasiswa angkatan di atas |
| FRS | KRS / pengisian jadwal | Formulir Rencana Studi di SIX |
| dosen wali | doswal / PA | Dosen yang menyetujui FRS |
| ulasan | review / testimoni | Tulisan pengalaman terstruktur tentang matkul/dosen |
| pertanyaan & jawaban | thread / post / QnA (campur-campur) | Konten forum |
| rencana studi | study plan / roadmap | Susunan matkul per semester sampai lulus |
| beban matkul | workload | Estimasi jam & jumlah tugas per minggu |
| informan | responden / narasumber (campur-campur) | Orang yang diwawancarai |

> Istilah khas ITB (FRS, SIX, dosen wali, TPB, penjurusan, SKS maksimum, prasyarat) **wajib dicek ulang** dengan pengalaman informan dan Peraturan Akademik ITB, jangan diasumsikan.

---

## 4. Deskripsi Topik & SDG (Owner: A)

### 4.1 Latar belakang (draf untuk slide — rapikan setelah sintesis)

Keputusan akademik mahasiswa ITB — matkul pilihan/lintas prodi apa yang diambil, kelas mana, berapa SKS, apakah rencana studinya cukup untuk lulus tepat waktu — sebagian besar masih bergantung pada **informasi informal**: cerita kating, grup chat angkatan/himpunan, dan akun menfess. Informasi ini tersebar, sulit dicari ulang, sering bertentangan, dan aksesnya bergantung pada **seberapa luas jaringan sosial** seseorang. Di saat yang sama, pemantauan IPK dan penyusunan rencana studi banyak dilakukan manual (spreadsheet pribadi, catatan, perkiraan), terpisah dari informasi tentang beban matkul itu sendiri. **[HIPOTESIS — ganti klaim umum dengan angka "x dari 10 informan" setelah sintesis]**

### 4.2 Relevansi SDG

**Pilihan utama: SDG 4 — Pendidikan Berkualitas**, Target 4.3 (akses setara terhadap pendidikan tinggi yang berkualitas).
Argumen yang dipakai: yang tidak setara bukan hanya akses masuk kuliah, tetapi **akses terhadap informasi yang dibutuhkan untuk menjalani kuliah dengan baik**; mahasiswa dengan jaringan kating luas mendapat keuntungan informasi dibanding mahasiswa pendatang, introvert, atau lintas prodi.

**Cadangan jika SDG 4 sudah diambil kelompok lain: SDG 10 — Berkurangnya Kesenjangan**, Target 10.2 (inklusi sosial, ekonomi, politik bagi semua). Argumen: kesenjangan informasi akademik akibat perbedaan modal sosial (kenal kating/tidak, anggota himpunan aktif/tidak, perantau/lokal). Isi slide cukup ganti bingkai, masalah & fitur tetap.

> A wajib: (1) cek slot SDG di `s.hmif.dev/KelompokIMK` malam ini, (2) salin kutipan resmi target dari sdgs.un.org dengan sitasi di slide, (3) buat tabel "aspek masalah ↔ poin target SDG" maksimal 4 baris.

### 4.3 Solusi existing & gap (Owner: D, dimasukkan di slide 2a)

Tujuan umum tugas meminta produk yang inovatif atau menyelesaikan masalah software existing **sehingga pengguna beralih**. Maka slide 2a wajib punya tabel pendek:

| Solusi yang dipakai sekarang (isi dari wawancara) | Dipakai untuk | Kelebihan menurut informan | Kekurangan/pain menurut informan | Informan |
|---|---|---|---|---|
| Grup chat angkatan/himpunan | `[...]` | `[...]` | `[...]` | `[I..]` |
| Japri kating | | | | |
| Akun menfess / media sosial | | | | |
| Spreadsheet/catatan IPK pribadi | | | | |
| SIX (FRS & nilai) | | | | |
| Aplikasi/website lain yang disebut informan | | | | |
| TemanKuliah (RISTEK UI) sebagai referensi luar ITB | Ulasan matkul, tanya teman, kalkulator nilai | — | Tidak untuk ITB; `[isi gap yang ingin kita jawab]` | Desk research |

**Hipotesis pembeda (positioning) untuk dibuktikan data:** fitur-fitur di aplikasi sejenis berdiri sendiri-sendiri. Peluang KuliahBareng adalah **menghubungkan informasi beban matkul dari ulasan dengan perencanaan studi** — misalnya simulasi rencana studi yang memperlihatkan perkiraan beban tiap semester, bukan hanya jumlah SKS. Pertahankan pembeda ini **hanya jika** sintesis menunjukkan informan memang merasakan keterputusan antara "info matkul" dan "rencana studi".

### 4.4 Hipotesis fitur (dipertahankan dari v1, diberi status)

| Fitur | Status | Domain | Syarat dipertahankan setelah sintesis |
|---|---|---|---|
| Ulasan matkul & dosen | HIPOTESIS | A (UG1), D (UG3) | Ada M terkait info tersebar/tidak kredibel |
| Jelajah & bandingkan matkul | HIPOTESIS | B (UG4) | Informan benar-benar punya pilihan matkul/kelas (lihat catatan 5.5) |
| Forum tanya per matkul | HIPOTESIS | C (UG2), D (UG3) | Ada M terkait diskusi tugas sulit dicari ulang/pertanyaan berulang |
| Kalkulator IPK & proyeksi | HIPOTESIS | E (UG5) | Ada M terkait hitung manual/salah hitung/kebutuhan target |
| Simulasi rencana studi | HIPOTESIS | E (UG6) | Ada M terkait salah rencana SKS/prasyarat/lulus |
| Testimoni individual | DROP (tetap) | — | — |
| Integrasi SIX real-time | DROP (tetap) | — | Sebut sebagai batasan di slide |

---

## 5. Pendekatan Riset (Owner slide: A; semua mengeksekusi)

### 5.1 Target pengguna
Mahasiswa aktif S1 ITB (semua angkatan & fakultas) yang (a) mengambil keputusan tentang matkul/kelas/rencana studi, (b) membutuhkan bantuan saat perkuliahan berjalan, atau (c) sering menjadi sumber informasi bagi mahasiswa lain.

### 5.2 Metode
| Metode | Deskripsi | Mengapa dipilih |
|---|---|---|
| **Wawancara semi-terstruktur** (utama) | 25–35 menit per informan, 10 informan, Modul Inti + Modul Deep-Dive | Topik menyangkut pengalaman personal & kebiasaan (salah ambil matkul, cara bertanya, cara menghitung IPK) yang butuh probing "kenapa" dan cerita konkret; kuesioner tertutup tidak bisa menangkap urutan proses & emosi yang dibutuhkan untuk swimlane dan persona |
| **Observasi artefak** (pendukung, dilakukan di dalam sesi wawancara) | Informan diminta *menunjukkan* (bukan menceritakan) artefak nyata: spreadsheet IPK, pencarian di grup chat, halaman FRS di SIX, catatan rencana studi, chat pertanyaan dari adik tingkat | Mengurangi bias ingatan (orang sering melaporkan kebiasaan secara tidak akurat); menghasilkan evidence visual; menangkap langkah kerja nyata untuk P dan UT |
| Desk research (pelengkap) | Referensi TemanKuliah, target SDG, Peraturan Akademik/kurikulum untuk verifikasi istilah | Konteks & validasi fakta, bukan sumber pain point |

Alasan tidak memakai kuesioner ditulis positif di slide ("kedalaman > jumlah untuk tahap eksplorasi problem space"), jangan terkesan menghindari kerja.

### 5.3 Tujuan riset (sesuai poin spesifikasi) → pertanyaan yang menjawabnya

| Tujuan riset (spesifikasi) | Apa yang ingin diketahui | Sumber di panduan wawancara |
|---|---|---|
| User Goal untuk menyusun Scenario & Business Process Flow | Apa yang ingin dicapai mahasiswa di tiap momen semester; urutan langkah yang benar-benar dilakukan | Inti-2, Inti-4, Inti-5, seluruh Deep-Dive |
| User Task yang merinci user goal | Langkah & tindakan konkret, tools, titik keputusan | Observasi artefak, probing "lalu apa yang kamu lakukan?" |
| Karakteristik user untuk Persona | Demografi, device, aplikasi harian, gaya belajar, sikap terhadap bertanya/berbagi, motivasi | Inti-1 (Profil Digital), Deep-Dive |
| Masalah/tantangan desain interaksi | Pain point, workaround, konsekuensi, emosi, alasan tidak memakai solusi existing | Inti-3, Inti-6, Deep-Dive |

### 5.4 Kriteria & sebaran informan

Aturan sebaran untuk ke-10 informan (dicek di tab `Informan`):
- Minimal **4 fakultas/sekolah berbeda**; maksimal **3 informan dari STEI** (hindari bias lingkaran anggota kelompok).
- Minimal **3 angkatan berbeda** (2022/2023, 2024, 2025).
- Dua informan milik satu anggota **wajib beda prodi**, sebisa mungkin beda angkatan.
- **Bukan** anggota kelompok, **bukan** teman satu kelompok tugas besar IMK kelas yang sama.
- Minimal 1 informan non-perantau dan 1 perantau (relevan untuk argumen jaringan sosial) — tanyakan, jangan diasumsikan.

Segmen per domain (screening question saat mengajak):

| Informan | Owner | Segmen | Pertanyaan screening (harus "ya") |
|---|---|---|---|
| I1, I2 | A | Pencari info | "Semester ini kamu baru pertama kali FRS di prodi, dan sempat cari info soal matkul/dosen sebelum FRS?" |
| I3, I4 | B | Perencana FRS lintas prodi | "Kamu pernah/sedang ambil matkul pilihan di luar prodi atau minor?" |
| I5, I6 | C | Penanya tugas | "Semester ini/lalu kamu sering nanya soal tugas/materi ke grup atau teman?" |
| I7, I8 | D | Kating kontributor | "Kamu cukup sering ditanya adik tingkat soal matkul/tugas?" |
| I9 | E | Perencana akademik (TPB) | "Waktu TPB kamu memantau/menghitung IP sendiri, misalnya untuk penjurusan?" |
| I10 | E | Perencana akademik (tingkat akhir) | "Kamu sedang/baru saja menghitung sisa SKS atau menyusun matkul supaya lulus tepat waktu?" |

### 5.5 Hal yang wajib divalidasi di wawancara (jangan diasumsikan di slide)
1. Seberapa bebas mahasiswa **memilih kelas/dosen** saat FRS di prodinya? Jika ternyata jarang bisa memilih dosen, UG1 & UG4 di-reframe dari "memilih" menjadi "mempersiapkan diri & menentukan matkul pilihan".
2. Apakah **IP TPB** memang dipakai dalam penjurusan di fakultas informan? (relevansi UG5 untuk mahasiswa baru)
3. Bagaimana alur **persetujuan FRS oleh dosen wali** dan apa yang biasanya membuat FRS direvisi?
4. Kanal apa saja yang **benar-benar** dipakai (WA/Line/Discord/Telegram/menfess X/Instagram) — jangan tulis kanal yang tidak disebut informan.

### 5.6 Etika, consent, dan privasi
- Minta izin rekam **sebelum** mulai dan ulangi konfirmasi di akhir. Catat di tab `Informan`.
- Foto evidence: minta izin terpisah; tawarkan wajah diblur/ambil dari belakang.
- Di slide: pakai **kode informan + deskripsi singkat** (mis. "I3, angkatan 2023, FTI"), **tanpa nama asli**. Screenshot artefak **diblur** untuk nama, NIM, nilai, dan isi chat pribadi orang lain.
- Rekaman hanya di folder berakses terbatas; hapus setelah nilai tugas besar keluar (sampaikan ini ke informan).

---

## 6. Panduan Wawancara v2 (dipakai semua anggota)

### 6.1 Struktur sesi (target 30 menit, maks. 35)

| Blok | Menit | Isi |
|---|---|---|
| Pembuka | 3 | Perkenalan, tujuan, consent |
| Modul Inti | 12 | 6 pertanyaan yang **sama untuk semua informan** (supaya data 10 orang bisa dibandingkan) |
| Modul Deep-Dive | 12 | Sesuai domain pewawancara, **termasuk observasi artefak** |
| Penutup | 3 | Pertanyaan terbuka, konfirmasi consent, foto evidence |

### 6.2 Aturan bertanya (baca sebelum wawancara pertama)
1. **Tanyakan kejadian nyata terakhir, bukan kebiasaan umum.** ✅ "Ceritakan terakhir kali kamu…" ❌ "Biasanya kamu…?" (boleh sebagai lanjutan).
2. **Jangan sebut ide aplikasi kita** sampai penutup. Menyebut solusi membuat informan menjawab untuk menyenangkan pewawancara.
3. **Jangan tanya "fitur apa yang kamu mau"** atau "kamu mau pakai aplikasi X nggak?". Tanyakan masalah, konsekuensi, dan workaround.
4. **Probing standar** (pakai berulang): "Kenapa?", "Lalu apa yang kamu lakukan?", "Bisa kasih contoh?", "Gimana rasanya waktu itu?", "Kalau diurutkan langkahnya bagaimana?", "Ada cara lain yang kamu coba?"
5. **Diam 3 detik** setelah informan selesai bicara — sering muncul cerita tambahan.
6. Catat **timestamp** rekaman untuk kutipan bagus (mis. `[12:40]`) supaya mudah dicari saat bikin slide.
7. Jika waktu mepet, **Deep-Dive didahulukan** atas pertanyaan Inti bertanda (opsional).

### 6.3 Pembuka (script)
> "Halo, makasih sudah mau ngobrol. Aku `[nama]` dari kelompok tugas besar Interaksi Manusia Komputer. Kami lagi riset tentang **pengalaman mahasiswa ITB dalam mengambil keputusan akademik dan menjalani perkuliahan** — nggak ada jawaban benar atau salah, yang kami butuh justru pengalaman jujurmu, termasuk yang menyebalkan. Ngobrolnya sekitar 30 menit. Boleh aku rekam audionya? Rekaman cuma dipakai kelompok kami untuk tugas, namamu nggak akan muncul di presentasi, dan akan dihapus setelah nilai keluar. Kamu juga boleh skip pertanyaan apa pun."

Catat: inisial, angkatan, prodi/fakultas, semester sekarang, asal daerah (perantau/tidak, **opsional**).

### 6.4 Modul Inti (semua informan)

**Inti-1 — Profil Digital & Keseharian (±2 menit)**
- "Device apa yang paling sering kamu pakai untuk urusan kuliah — HP, laptop, tablet? Untuk apa masing-masing?"
- "Aplikasi apa saja yang kamu buka hampir setiap hari untuk urusan kuliah?" *(probing: berapa grup chat kuliah yang kamu ikuti kira-kira? mana yang paling aktif?)*

**Inti-2 — FRS terakhir (±3 menit)** — *sumber utama swimlane*
- "Coba ceritakan FRS semester ini dari awal sampai disetujui. Mulai dari kapan kamu mulai mikirin, lalu langkahnya apa saja?"
  - Probing: dari mana tahu matkul apa yang harus/bisa diambil? ada momen ragu? tanya siapa? ada revisi dari dosen wali? kenapa?

**Inti-3 — Kredibilitas informasi (±2 menit)**
- "Terakhir kali kamu dapat info soal suatu matkul atau dosen (dari kating, grup, menfess), infonya ternyata sesuai kenyataan nggak? Ceritakan."
  - Probing: gimana cara kamu memutuskan info mana yang dipercaya?

**Inti-4 — Kesulitan saat perkuliahan (±2 menit)**
- "Ceritakan terakhir kali kamu bingung soal tugas atau materi. Apa yang kamu lakukan dari awal sampai dapat jawaban (atau nggak dapat)?"
  - Probing: sempat cari di chat lama? berapa lama sampai dapat jawaban?

**Inti-5 — Pemantauan nilai & rencana (±2 menit)**
- "Setelah nilai semester keluar, apa yang kamu lakukan dengan nilai itu? Kamu menghitung atau mencatat sesuatu?"
  - Probing: pakai apa? pernah salah hitung atau kaget dengan IPK/SKS?

**Inti-6 — Berbagi informasi (±1 menit, opsional jika waktu mepet)**
- "Pernah nggak kamu yang ditanya atau membagikan info soal matkul ke orang lain? Ceritakan satu kejadian."

### 6.5 Modul Deep-Dive per Domain

#### Deep-Dive A — Pencari Info Matkul & Dosen (I1, I2)
1. "Untuk matkul yang paling bikin kamu ragu semester ini, info apa saja yang kamu cari sebelum FRS? Urutkan dari yang paling penting."
2. "Dari mana saja kamu dapat info itu? Berapa lama total waktu yang kamu habiskan?"
3. "Info apa yang **tidak** berhasil kamu dapatkan tapi sebenarnya kamu butuhkan?"
4. "Kalau dua sumber bilang hal yang bertentangan soal matkul/dosen, apa yang kamu lakukan?"
5. "Sekarang setelah kuliah berjalan, apa yang berbeda dari ekspektasimu? Apa dampaknya buatmu?"
6. **Observasi:** "Boleh tunjukkan chat/postingan yang kamu pakai waktu cari info matkul itu?" → screenshot (blur).

#### Deep-Dive B — Jelajah & Bandingkan Matkul untuk FRS (I3, I4)
1. "Ceritakan waktu kamu memilih matkul di luar prodi. Ada berapa kandidat awalnya, dan bagaimana kamu mengerucutkannya?"
2. "Apa saja yang kamu bandingkan antar-kandidat? (probing: SKS, jadwal, beban, dosen, relevansi, prasyarat, peluang nilai)"
3. "Di mana kamu menaruh/mencatat perbandingan itu? Di kepala, catatan, spreadsheet?"
4. "Seberapa bebas sebenarnya kamu memilih kelas atau dosen di SIX? Apa yang membatasi?"
5. "Pernah ada matkul pilihan yang kamu sesali atau yang kamu lewatkan karena kurang info? Ceritakan."
6. **Observasi:** "Boleh tunjukkan daftar/catatan kandidat matkul atau halaman FRS-mu (nama & nilai diblur)?"

#### Deep-Dive C — Bertanya Soal Tugas/Materi (I5, I6)
1. "Ceritakan pertanyaan tugas terakhir yang kamu kirim ke grup/teman. Kenapa kamu pilih bertanya ke sana?"
2. "Sebelum bertanya, kamu mencoba cari jawabannya di mana dulu? Bagaimana hasilnya?"
3. "Pernah menunda atau batal bertanya? Kenapa? (probing: malu, takut dianggap bodoh, bingung harus tanya siapa)"
4. "Kalau jawabannya datang dari beberapa orang/grup berbeda, bagaimana kamu menyatukannya?"
5. "Jawaban yang pernah kamu dapat, apakah kamu simpan? Pernah butuh lagi di kemudian hari?"
6. **Observasi:** "Boleh coba cari di grup kelasmu diskusi soal tugas minggu lalu? Aku perhatikan caranya ya." → catat berapa langkah/waktu, kesulitan, screenshot (blur).

#### Deep-Dive D — Kating Kontributor (I7, I8)
1. "Dalam satu semester, kira-kira seberapa sering kamu ditanya adik tingkat soal matkul/tugas? Lewat kanal apa?"
2. "Pertanyaan apa yang paling sering berulang? Ceritakan contoh terbaru."
3. "Bagaimana kamu biasanya menjawab? Berapa lama waktumu tersita? Pernah memilih tidak menjawab? Kenapa?"
4. "Pernah membuat catatan/dokumen/rangkuman tips untuk adik tingkat? Apa yang terjadi dengan dokumen itu?"
5. "Apa yang membuatmu mau (atau malas) berbagi pengalaman matkul? (probing: waktu, takut salah info, takut menyinggung dosen, anonimitas, pengakuan)"
6. **Observasi:** "Boleh tunjukkan contoh chat pertanyaan yang pernah kamu terima (nama pengirim diblur)?"

#### Deep-Dive E — Perencanaan Akademik (I9, I10)
1. (I9) "Waktu TPB, kenapa kamu memantau IP? Apa target yang ingin kamu capai dan dari mana kamu tahu target itu?"
   (I10) "Ceritakan bagaimana kamu menghitung sisa matkul/SKS sampai lulus. Kapan terakhir melakukannya?"
2. "Langkah menghitungnya seperti apa? Data diambil dari mana?"
3. "Pernah salah hitung atau telat sadar (SKS kurang/lebih, prasyarat, matkul wajib terlewat, bentrok)? Apa dampaknya?"
4. "Kalau nilai semester depan bisa diprediksi, apa yang akan kamu lakukan dengan informasi itu?" *(boleh — ini tentang keputusan, bukan fitur)*
5. "Saat menyusun rencana beberapa semester ke depan, apakah kamu mempertimbangkan beratnya matkul, bukan hanya SKS? Bagaimana caranya?"
6. **Observasi:** "Boleh tunjukkan spreadsheet/catatan IPK atau rencana studimu? Coba perlihatkan cara kamu memperbaruinya setelah nilai keluar." → catat rumus/langkah, screenshot (nilai diblur).

### 6.6 Penutup (semua informan)
1. "Dari semua yang kita obrolin, mana yang paling mengganggu buatmu?"
2. "Kalau kamu bisa mengubah satu hal dari cara mahasiswa ITB mencari info akademik atau merencanakan studi, apa?"
3. "Ada yang belum aku tanya tapi menurutmu penting?"
4. Konfirmasi ulang izin memakai rekaman & foto sebagai lampiran (samaran). Ambil 1 foto sesi.
5. "Kalau nanti kami punya rancangan awal, boleh kami hubungi lagi untuk dicoba?" → sangat berguna untuk **MS3 (evaluasi low-fi)**. Catat di Registry.

### 6.7 Checklist pewawancara
- [ ] Baterai & memori HP cukup, mode pesawat/jangan ganggu aktif (kecuali untuk rekaman online)
- [ ] Template ringkasan dibuka / siap diisi
- [ ] Consent rekam & foto tercatat
- [ ] Minimal 1 observasi artefak + screenshot
- [ ] Minimal 3 kutipan bertimestamp
- [ ] Ringkasan diisi ≤ 3 jam setelah sesi, sticky notes ditempel di FigJam

---

## 7. Template Ringkasan Wawancara (1 file per informan)

```
KODE INFORMAN: I_   | PEWAWANCARA: _ | TANGGAL: __ | DURASI: __ menit | MODE: tatap muka/online
Consent rekam: Y/N  | Consent foto: Y/N | Link rekaman: __

1. PROFIL
   Angkatan: __ | Prodi/Fakultas: __ | Semester: __ | Perantau: Y/N/tidak disebut
   Device utama untuk kuliah: __ | Aplikasi harian untuk kuliah: __ | Jumlah grup chat kuliah (perkiraan): __
   Karakter yang terlihat (dari cerita, bukan tebakan): __

2. ALUR YANG BENAR-BENAR DILAKUKAN (langkah demi langkah, beri tanda siapa pelakunya)
   a. FRS terakhir:   1) __ 2) __ 3) __ ... (tandai titik keputusan: [KEPUTUSAN] ...)
   b. Saat bingung tugas: 1) __ 2) __ ...
   c. Setelah nilai keluar / rencana studi: 1) __ 2) __ ...

3. PAIN POINTS (satu baris per pain)
   | Pain | Konsekuensi nyata | Emosi | Seberapa sering | Timestamp |

4. WORKAROUND & TOOLS YANG DIPAKAI SEKARANG
   | Tools/cara | Untuk apa | Kenapa dipakai | Kekurangan |

5. GOALS / YANG INGIN DICAPAI (kata-kata informan, bukan fitur)
   - __

6. KUTIPAN TERPILIH (maks. 5, verbatim, ada timestamp)
   - "__" [mm:ss]

7. OBSERVASI ARTEFAK
   Apa yang ditunjukkan: __ | Langkah yang terlihat: __ | Kesulitan yang terlihat: __ | Link screenshot (blur): __

8. KEJUTAN / HAL YANG BERTENTANGAN DENGAN HIPOTESIS KITA
   - __

9. STICKY NOTES UNTUK SINTESIS (10–20 baris, 1 ide per baris, format "I_: ...")
   - I_: ...
```

---

## 8. Sesi Sintesis — SYNC-2, Jumat 19.00–21.30 (Fasilitator: A)

### 8.1 Persiapan (sebelum 17.00)
- Board FigJam dengan 10 kolom (I1–I10). Setiap pewawancara menempel sticky notes dari bagian 9 template, **warna berbeda per segmen**.
- Area kosong: "Cluster", "Kandidat M", "Alur (P)", "Perilaku untuk Persona", "Parkir (menarik tapi di luar scope)".

### 8.2 Agenda
| Menit | Langkah | Output |
|---|---|---|
| 0–10 | A membacakan aturan & tujuan; tiap orang 1 menit: "1 temuan paling mengejutkan dari informanku" | Semua sudah tahu konteks |
| 10–35 | **Silent clustering**: semua memindahkan sticky notes ke kelompok berdasarkan kemiripan masalah/perilaku (bukan berdasarkan informan atau fitur) | 6–12 cluster |
| 35–55 | Beri nama tiap cluster dalam bentuk **kalimat masalah dari sudut pandang user** ("Aku nggak bisa tahu … sebelum …") | Kandidat M |
| 55–70 | Hitung bukti tiap cluster: berapa informan (x/10), dari berapa segmen, ada konsekuensi nyata? | Kolom bukti |
| 70–90 | Terapkan **aturan keputusan 8.3** → M final (4–6 buah), UG dipertahankan/diubah/gugur | M & UG terkunci |
| 90–110 | Susun **alur P bersama** di FigJam dari bagian 2 template (FRS → perkuliahan → akhir semester), beri lane; B memimpin | Daftar P final untuk digambar B |
| 110–135 | **Persona**: kelompokkan informan berdasarkan perilaku (mis. "mencari aktif vs pasif", "pemberi vs penerima info", "perencana vs spontan") → tentukan 2–3 persona & informan pendukung tiap persona; C memimpin | Keputusan PR1–PR3 |
| 135–150 | Kunci semua kode di Registry; konfirmasi tugas Sabtu & jam target; catat perubahan domain jika ada | Registry terkunci |

### 8.3 Aturan keputusan
1. **M diterima** jika: didukung **≥ 3 informan dari ≥ 2 segmen**, **atau** didukung ≥ 2 informan dengan konsekuensi nyata yang signifikan (mis. mengulang matkul, telat lulus, revisi FRS berkali-kali).
2. **Opportunity** boleh diterima dengan 2 informan jika jelas potensinya (mis. kating mau berbagi asal ada kondisi tertentu).
3. **UG dipertahankan** hanya jika menjawab ≥ 1 M yang diterima.
4. **Jika UG sebuah domain gugur**: domain owner **tetap memegang 2 User Task**, tetapi pindah ke cluster kuat yang belum tertangani UG mana pun (pilih bersama di sesi). Jumlah UT per orang tetap 2 → syarat PIC tetap terpenuhi.
5. **Data yang bertentangan dengan hipotesis tidak dibuang** — tulis di slide temuan sebagai insight ("Berbeda dari dugaan awal, …"). Ini menaikkan kredibilitas.
6. Hal menarik di luar scope → area "Parkir", bisa disebut sebagai "Peluang pengembangan lanjutan".

---

## 9. Masalah & Opportunity — Slide 2a (Owner: D)

### 9.1 Draf M **[HIPOTESIS — timpa dengan hasil sintesis]**

| Kode | Masalah/Opportunity (draf) | Domain terkait | Bukti (isi setelah sintesis) |
|---|---|---|---|
| M1 | Informasi tentang matkul & dosen tersebar di banyak kanal informal dan sulit dinilai kredibilitasnya | A, B, D | `x/10 informan; kutipan I_` |
| M2 | Mahasiswa sulit memperkirakan beban & tingkat kesulitan matkul sebelum mengambilnya, sehingga keputusan FRS sering meleset dari ekspektasi | A, B, E | |
| M3 | Diskusi dan jawaban soal tugas/materi tercecer di banyak grup dan sulit ditemukan kembali, sehingga pertanyaan yang sama diajukan berulang | C, D | |
| M4 (Opportunity) | Kating memiliki pengalaman & tips matkul yang berharga, tetapi berbaginya lewat japri satu per satu melelahkan dan pengetahuannya hilang saat kating lulus | D | |
| M5 | Pemantauan IPK dan penyusunan rencana studi dilakukan manual sehingga rawan salah hitung SKS, prasyarat, atau target nilai | E | |
| M6 (Opportunity) | Informasi beban matkul dan perencanaan studi tidak saling terhubung; mahasiswa menyusun rencana hanya berdasarkan SKS | B, E | |

### 9.2 Format slide 2a (maks. 3 slide)
1. **Slide temuan wawancara**: 4–6 insight kunci, masing-masing dengan angka "x/10 informan" + 1 kutipan pendek + kode informan.
2. **Slide M1–Mn**: format spesifikasi "M1: …", tiap M satu kalimat masalah + satu kalimat dampak.
3. **Slide solusi existing & gap** (tabel 4.3) + 1 kalimat positioning.

**Definition of Done 2a:** tiap M punya ≥ 1 kutipan & jumlah informan; tidak ada M yang menyebut fitur/solusi ("tidak ada aplikasi ulasan" ❌ → "tidak ada tempat terpusat yang bisa dinilai kredibilitasnya" ✅).

---

## 10. User Goals — Slide 2b (Owner: tiap domain; konsolidasi E)

### 10.1 Aturan penulisan
- Format wajib: **As a [role], I want [goal], so that [reason/value].** Boleh Bahasa Indonesia penuh ("Sebagai …, saya ingin …, sehingga …") — pilih satu dan konsisten di semua UG (disarankan Bahasa Indonesia agar selaras dengan slide lain).
- **Role** spesifik perilaku (bukan "user"/"mahasiswa" saja).
- **Goal** adalah tujuan user, **bukan fitur/antarmuka** (❌ "saya ingin klik tombol bandingkan"; ✅ "saya ingin membandingkan kandidat matkul").
- **Reason** menjelaskan nilai/manfaat yang terlihat di data.
- Setiap UG diakhiri "→ menjawab M.., M..".

### 10.2 Draf UG **[HIPOTESIS]**

| Kode | Owner | User Story (draf) | Menjawab |
|---|---|---|---|
| UG1 | A | Sebagai **mahasiswa yang akan menentukan matkul semester depan**, saya ingin **mengetahui gambaran realistis suatu matkul dan dosen pengampunya (beban, gaya mengajar, tingkat kesulitan) dari sumber yang kredibilitasnya bisa saya nilai**, sehingga **keputusan saya tidak lagi bergantung pada rumor dari satu-dua orang**. | M1, M2 |
| UG2 | C | Sebagai **mahasiswa yang sedang kesulitan dengan tugas atau materi**, saya ingin **menemukan diskusi yang sudah ada atau bertanya kepada orang yang pernah mengambil matkul yang sama**, sehingga **saya mendapat jawaban relevan dengan cepat tanpa menyebar pertanyaan ke banyak grup**. | M3 |
| UG3 | D | Sebagai **kating yang pernah menyelesaikan suatu matkul**, saya ingin **membagikan pengalaman dan tips saya sekali dan dapat dibaca banyak orang**, sehingga **adik tingkat terbantu dan saya tidak menjawab pertanyaan yang sama berulang kali**. | M3, M4 |
| UG4 | B | Sebagai **mahasiswa yang menyusun FRS dengan beberapa kandidat matkul pilihan/lintas prodi**, saya ingin **menjelajahi matkul yang bisa saya ambil dan membandingkan kandidatnya secara berdampingan**, sehingga **saya dapat memilih kombinasi matkul yang sesuai minat, jadwal, dan kemampuan saya**. | M1, M2, M6 |
| UG5 | E | Sebagai **mahasiswa yang memantau capaian akademiknya**, saya ingin **mengetahui IPK saat ini dan nilai yang perlu saya capai untuk target tertentu**, sehingga **saya bisa mengatur prioritas belajar tanpa menghitung manual setiap semester**. | M5 |
| UG6 | E | Sebagai **mahasiswa yang merencanakan studi sampai lulus**, saya ingin **menyusun rencana matkul per semester dan mengetahui apakah rencana itu memenuhi syarat kelulusan serta seimbang bebannya**, sehingga **saya terhindar dari salah rencana yang membuat studi saya molor**. | M5, M6 |

**Slide 2b**: 2 slide, tiap UG satu kartu (role/goal/reason dipisah visual) + label M.

---

## 11. User Process Flow (Swimlane) — Slide 2c (Owner: B)

### 11.1 Aturan dari spesifikasi yang sering terlewat
- Menggambarkan **alur kerja natural/existing** (tanpa aplikasi KuliahBareng). Tidak boleh ada kotak berbunyi "membuka aplikasi".
- **Setiap kotak proses punya kode P** dan setiap P punya deskripsi singkat.
- Diagram harus menunjukkan **keterkaitan antar user story** → gunakan satu siklus semester yang menyambungkan semua UG.

### 11.2 Lane
| Lane | Pelaku |
|---|---|
| L1 | Mahasiswa |
| L2 | Kating / Teman |
| L3 | Dosen Wali |
| L4 | SIX & Dokumen Akademik (sistem/dokumen existing) |

> Jika data menunjukkan menfess/media sosial adalah pelaku aktif (misalnya admin menfess menyaring pertanyaan), boleh tambah lane L5.

### 11.3 Draf proses **[HIPOTESIS — validasi di sintesis bagian "Alur (P)"]**

| Kode | Lane | Proses | Masuk dari | Keluar ke | Terkait UG |
|---|---|---|---|---|---|
| P1 | L4 | Nilai dan IP semester diterbitkan di SIX | Start (akhir semester) | P2 | UG5 |
| P2 | L1 | Menyalin nilai ke catatan/spreadsheet pribadi dan menghitung IPK atau target nilai secara manual | P1 | P3 | UG5 |
| P3 | L1 (+ L4 dokumen kurikulum) | Mengecek kurikulum, sisa SKS, matkul wajib, dan prasyarat | P2 | P4 | UG4, UG6 |
| P4 | L1 | Menyusun daftar kandidat matkul/kelas semester depan | P3, D2 (ditolak) | D1 | UG4, UG6 |
| D1 | L1 | Keputusan: informasi tentang kandidat matkul/dosen sudah cukup? | P4 | Ya → P8; Tidak → P5 | UG1 |
| P5 | L1 | Bertanya di grup angkatan/himpunan atau japri kating | D1 | P6 | UG1 |
| P6 | L2 | Menjawab berdasarkan ingatan/pengalaman pribadi, satu per satu | P5 | P7 | UG1, UG3 |
| P7 | L1 | Mencari informasi tambahan di menfess/media sosial dan membandingkan jawaban yang berbeda | P6 | P8 | UG1, UG4 |
| P8 | L1 + L4 | Memutuskan dan mengisi FRS di SIX | D1, P7 | P9 | UG4 |
| P9 | L3 | Meninjau FRS mahasiswa | P8 | D2 | UG6 |
| D2 | L3 | Keputusan: FRS disetujui? | P9 | Ya → P10; Tidak → P4 | UG6 |
| P10 | L1 | Menjalani perkuliahan dan menemui kesulitan tugas/materi | D2 | P11 | UG2 |
| P11 | L1 | Menelusuri chat lama/arsip grup untuk mencari diskusi serupa | P10 | D3 | UG2 |
| D3 | L1 | Keputusan: jawaban ditemukan? | P11 | Ya → End (kembali ke P1 di akhir semester); Tidak → P12 | UG2 |
| P12 | L1 | Mengirim pertanyaan ke beberapa grup dan/atau japri kating/teman | D3 | P13 | UG2 |
| P13 | L2 | Menjawab pertanyaan (sering pertanyaan yang sama dari orang berbeda) | P12 | End | UG2, UG3 |

### 11.4 Instruksi menggambar
1. Tools: draw.io (template "Cross-Functional Flowchart") atau FigJam swimlane. Orientasi **horizontal** (lane bertumpuk ke bawah) agar muat 16:9.
2. Bentuk: oval = start/end, persegi panjang = proses (kode P di baris pertama, tebal), belah ketupat = decision (kode D).
3. Beri **3 zona waktu** tipis di atas diagram: "Akhir semester" (P1–P2), "Masa FRS" (P3–P9), "Perkuliahan" (P10–P13).
4. Opsional tapi disarankan: tanda ⚠ kecil di proses yang menjadi titik pain (P2, P6, P7, P11, P12) dengan referensi M.
5. Jika diagram tidak terbaca dalam 1 slide: slide 1 = diagram penuh, slide 2 = deskripsi P1–P13 & D1–D3 dalam tabel 2 kolom.
6. Export PNG resolusi tinggi (≥ 2x) dan simpan file sumber di `04_Diagram`.

**Definition of Done 2c:** semua UG1–UG6 muncul di kolom "Terkait UG" minimal sekali; tidak ada proses bernuansa solusi; semua P di diagram = semua P di tabel = semua P di Registry.

---

## 12. User Persona — Slide 2d (Owner: C)

### 12.1 Aturan
- Persona dibangun dari **pola perilaku** hasil sintesis, **bukan** salinan satu informan dan **bukan** dikarang. Tiap persona mencantumkan "Dibangun dari: I_, I_, I_" (kecil, di pojok slide).
- Nama & foto fiktif (pakai ilustrasi/avatar/stok gratis) — **dilarang** memakai foto informan.
- Semua field di bawah wajib (sesuai 2d spesifikasi: nama, karakteristik, tujuan, latar belakang, kebiasaan aplikasi, device, langkah kerja, masalah).
- Kalender harus konsisten: September 2026 → angkatan 2026 = semester 1, 2025 = semester 3, 2024 = semester 5, 2023 = semester 7.

### 12.2 Template persona (1 slide per persona)
```
[Foto/ilustrasi]  NAMA — Label arketipe (mis. "Si Pencari Kepastian")
Umur | Angkatan & semester | Prodi/Fakultas | Perantau/tidak (jika relevan)
Kutipan khas (parafrase dari data): "…"
Bio (3–4 kalimat): latar belakang yang relevan dengan keputusan akademik
Goals: 3 poin (terkait UG)
Kebiasaan digital: device utama, aplikasi harian, jumlah grup chat, pola pakai (mis. buka HP di sela kelas)
Langkah kerja saat ini: 3–5 langkah (merujuk P)
Pain points: 3–4 poin (merujuk M)
Motivasi & kekhawatiran: 2 poin
Skala perilaku (slider visual): Aktif mencari ↔ Pasif menunggu | Penerima info ↔ Pemberi info | Perencana ↔ Spontan | Nyaman bertanya ↔ Sungkan bertanya
Dibangun dari: I_, I_, I_
```

### 12.3 Kerangka persona **[HIPOTESIS — finalkan di sintesis]**

| Persona | Arketipe | Dominan di UG | Kemungkinan informan pendukung | Catatan perbaikan dari v1 |
|---|---|---|---|---|
| PR1 | **Adik tingkat pencari kepastian** — angkatan 2025, semester 3, baru pertama kali FRS di prodi, jaringan kating terbatas, sungkan bertanya | UG1, UG2, UG4 | I1, I2, I5, I6 (+I3 bila cocok) | Menggantikan "Kirana TPB semester 2" yang tidak konsisten dengan kalender & kurikulum TPB |
| PR2 | **Kating yang jadi "tempat bertanya"** — angkatan 2022/2023, pernah jadi mentor/asisten, mau berbagi tapi lelah dijapri berulang | UG3 (+ UG4 sebagai pengambil matkul lintas prodi) | I7, I8 (+I4) | Dipisahkan dari kebutuhan hitung IPK agar fokus |
| PR3 | **Perencana studi** — angkatan 2023, semester 7, mengejar lulus tepat waktu, mengelola spreadsheet sendiri; atau varian angkatan 2025 yang mengejar target IP | UG5, UG6 | I9, I10 (+ informan lain yang menunjukkan perilaku serupa) | Persona baru — v1 tidak punya persona untuk UG5/UG6 |

Jika sintesis hanya menemukan 2 pola perilaku yang jelas, gabungkan PR3 ke PR1 atau PR2 — **jangan memaksakan 3**.

**Definition of Done 2d:** setiap pain point persona bisa ditunjuk ke M; setiap goal persona bisa ditunjuk ke UG; ada field kebiasaan device/aplikasi.

---

## 13. Scenario — Slide 2e (Owner: D)

### 13.1 Aturan dari spesifikasi
- Disusun dari **kumpulan user story**, menggambarkan **aktivitas sehari-hari tanpa aplikasi** (bukan fungsi aplikasi).
- Menghidupkan process flow dengan karakteristik persona → sebut kode **(P_)** di kalimat yang sesuai dan **(UG_)** di akhir paragraf.
- Deskripsikan konteks: latar tempat, waktu, suasana, kondisi sosial.

### 13.2 Rencana skenario
| Skenario | Judul kerja | Persona | Rentang waktu | Mencakup UG | Mencakup P |
|---|---|---|---|---|---|
| S1 | "Nilai Keluar, FRS Menanti" | PR3 (pembuka) → PR1 (inti) → PR2 (menjawab) | Akhir semester genap sampai FRS disetujui (± Juli–Agustus) | UG5, UG6, UG4, UG1, UG3 | P1–P9, D1–D2 |
| S2 | "Tugas Pertama yang Membingungkan" | PR1 → PR2 | Minggu ke-3 perkuliahan semester ganjil (± September) | UG2, UG3 | P10–P13, D3 |

### 13.3 Kerangka alur S1 (tulis sebagai narasi 3–4 paragraf, 250–350 kata)
1. **Konteks & P1–P2:** malam hari nilai terbit di SIX, PR3 di kos membuka spreadsheet lamanya, memperbarui nilai, rumus salah karena ada matkul mengulang → rasa panik singkat. *(UG5)*
2. **P3–P4:** PR3 (atau PR1, pilih yang lebih kuat datanya) membuka dokumen kurikulum, menghitung sisa SKS, menyusun kandidat matkul; ragu antara dua matkul pilihan lintas prodi. *(UG6, UG4)*
3. **D1–P7:** PR1 bertanya di grup angkatan; PR2 menjawab dari ingatan sambil mengerjakan hal lain; jawaban lain di grup bertentangan; PR1 mencari di menfess dan menemukan info usang. *(UG1, UG3)*
4. **P8–D2:** PR1 memilih dengan info seadanya, FRS dikembalikan dosen wali karena kombinasi SKS/prasyarat → kembali ke P4. *(UG6)*

Isi detail (tempat, emosi, kalimat chat) **wajib diambil dari cerita informan**, disamarkan.

### 13.4 Kerangka alur S2 (2–3 paragraf, 200–300 kata)
1. **P10:** PR1 menemui instruksi tugas yang ambigu, deadline dua hari lagi, di sela kelas.
2. **P11–D3:** mencoba mencari di grup kelas & chat angkatan tahun lalu, hasil pencarian tenggelam oleh stiker/pengumuman. *(UG2)*
3. **P12–P13:** mengirim pertanyaan ke tiga grup, menunggu; PR2 menerima pertanyaan serupa dari tiga orang berbeda minggu itu, menjawab singkat karena lelah. *(UG2, UG3)*

**Definition of Done 2e:** UG1–UG6 semuanya muncul di S1 ∪ S2; semua P disebut minimal sekali; tidak ada kata "aplikasi KuliahBareng".

---

## 14. User Tasks — Slide 2f (Owner: tiap domain; tabel gabungan: E)

### 14.1 Tabel ringkas (format mengikuti contoh spesifikasi) **[HIPOTESIS]**

| User Goal | Proses | User Task | PIC (NIM) |
|---|---|---|---|
| UG1 — mengetahui gambaran realistis matkul & dosen | P5, P7 | UT1.1 Menemukan informasi tentang matkul/dosen tertentu | A `135xxxxx` |
| | P6, P7 | UT1.2 Menilai isi & kredibilitas pengalaman mahasiswa lain tentang matkul/dosen | A `135xxxxx` |
| UG2 — menemukan jawaban soal tugas/materi | P11, D3 | UT2.1 Mencari diskusi atau jawaban yang sudah ada untuk suatu matkul | C `135xxxxx` |
| | P12 | UT2.2 Mengajukan pertanyaan kepada mahasiswa yang pernah/sedang mengambil matkul yang sama | C `135xxxxx` |
| UG3 — membagikan pengalaman sekali untuk banyak orang | P6 | UT3.1 Menuliskan pengalaman & tips tentang matkul yang pernah diambil | D `135xxxxx` |
| | P13 | UT3.2 Menjawab pertanyaan adik tingkat yang relevan dengan pengalamannya | D `135xxxxx` |
| UG4 — menjelajah & membandingkan kandidat matkul | P3 | UT4.1 Menjelajahi daftar matkul yang dapat diambil | B `135xxxxx` |
| | P4, P8 | UT4.2 Membandingkan beberapa kandidat matkul secara berdampingan | B `135xxxxx` |
| UG5 — mengetahui IPK & target nilai | P1, P2 | UT5.1 Mencatat nilai dan melihat IPK beserta nilai yang dibutuhkan untuk target | E `135xxxxx` |
| UG6 — menyusun & memvalidasi rencana studi | P3, P4, D2 | UT6.1 Menyusun rencana matkul per semester dan memeriksa kelayakannya | E `135xxxxx` |

Nama UT ditulis sebagai **tindakan user dengan kata kerja**, bebas teknologi (tanpa "klik", "tombol", "halaman").

### 14.2 Template deskripsi UT (2 slide per PIC, format mengikuti contoh spesifikasi)

```
PIC: <NIM> — <Nama>
User Task <kode> — <nama task>
• User/pengguna: <persona/segmen yang melakukan task + konteks kapan>
• Deskripsi: <narasi 2–4 kalimat: pemicu → langkah yang dilakukan user → hasil yang diharapkan>
• Tipe interaksi: <instructing | conversing | manipulating | exploring | responding> — <1 kalimat alasan>
• Model konseptual:
    - Objek: <mis. Matkul, Dosen, Ulasan>
    - Aksi: <mis. mencari, memfilter, membaca>
    - Relasi: <mis. satu Matkul punya banyak Ulasan; Ulasan ditulis oleh mahasiswa yang pernah mengambil>
• Metafora: <metafora + 1 kalimat mengapa familiar bagi persona (didukung data kebiasaan aplikasi)>
```

### 14.3 Saran tipe interaksi & metafora (PIC boleh mengubah dengan justifikasi)

Pengingat definisi (Rogers, Sharp & Preece): **instructing** = user memberi perintah (mengetik, memilih perintah, mengisi form); **conversing** = user berdialog dengan sistem seolah percakapan; **manipulating** = user memanipulasi objek secara langsung (drag, geser, ubah nilai dan melihat hasil seketika); **exploring** = user bergerak menjelajahi ruang informasi; **responding** = sistem yang memulai interaksi (notifikasi/peringatan) lalu user merespons.

| UT | Tipe interaksi utama | Alasan | Metafora kandidat | Catatan koreksi dari v1 |
|---|---|---|---|---|
| UT1.1 | Instructing | User memasukkan kata kunci/filter | Katalog perpustakaan / mesin pencari | Tetap |
| UT1.2 | Exploring | User menelusuri ringkasan lalu masuk ke detail pengalaman | Ulasan produk di marketplace dengan label "pernah mengambil" (setara "pembeli terverifikasi") | Tambahkan aspek kredibilitas |
| UT2.1 | Instructing + Exploring | Mencari lalu menelusuri hasil | Fitur "pertanyaan serupa" di forum Q&A | Tetap |
| UT2.2 | Instructing | User menyusun & mengirim pertanyaan | Papan pengumuman kelas / thread forum | v1 menyebut "Reddit/Kaskus" — pakai hanya jika informan memang familiar |
| UT3.1 | Instructing | Mengisi struktur ulasan | Menulis ulasan setelah belanja | Tetap |
| UT3.2 | Responding → Instructing | Sistem memberi tahu ada pertanyaan tentang matkul yang pernah diambil kating; kating merespons | Kotak masuk pertanyaan / "mention" | v1 "Instructing/Responding" tanpa alasan → kini jelas siapa yang memulai |
| UT4.1 | Exploring | Menjelajah daftar per prodi/kategori | Katalog kursus online | Tetap |
| UT4.2 | Manipulating + Exploring | Memasukkan/mengeluarkan kandidat ke area perbandingan dan melihat perbedaan langsung | Tabel perbandingan spesifikasi HP | v1 "Exploring" saja |
| UT5.1 | Instructing + Manipulating | Memasukkan nilai, lalu mengubah asumsi nilai target dan melihat proyeksi berubah seketika | Kalkulator simulasi cicilan/target tabungan | v1 "Instructing" saja; proyeksi "what-if" adalah manipulating |
| UT6.1 | Manipulating + Responding | Menyusun matkul ke kolom semester; sistem memperingatkan pelanggaran prasyarat/batas SKS | Papan kanban / menyusun itinerary perjalanan | v1 menyebut peringatan tapi tidak memasukkannya ke tipe interaksi |

**Definition of Done 2f:** 10 UT, 5 PIC, tiap PIC tepat 2 UT (E: UT5.1 & UT6.1); setiap UT merujuk ≥ 1 P yang ada di swimlane; alasan tipe interaksi & metafora tertulis.

---

## 15. Fungsionalitas Sistem — Essential Use Case (Owner: tiap domain; konsistensi format: E)

### 15.1 Aturan
- Format mengikuti contoh spesifikasi: nama use case (UpperCamelCase, kata kerja + objek), dua kolom **USER INTENTION (user task)** ↔ **SYSTEM RESPONSIBILITY (fungsional)**.
- Essential use case bersifat **abstrak & bebas teknologi**: ❌ "User menekan tombol Hitung" → ✅ "Menyatakan ingin mengetahui IPK".
- Satu UT boleh diturunkan ke beberapa F. Penomoran **F<UG>.<n>**.
- Setelah EUC, tiap PIC menulis **deskripsi setiap F** (format spesifikasi): kode & nama F, user/pengguna, deskripsi (apa yang disediakan sistem, input, output, aturan/validasi penting).
- Satu slide EUC + satu slide deskripsi F per domain (E boleh 2 + 2 karena 2 UG).

### 15.2 Contoh standar kualitas (domain E, UG5) — **[HIPOTESIS, E finalkan]**

**Essential Use Case: *PantauCapaianAkademik***

| USER INTENTION (user task) | SYSTEM RESPONSIBILITY (fungsional) |
|---|---|
| UT5.1 — Menyatakan ingin mengetahui capaian akademiknya | **F5.1** Meminta daftar matkul, SKS, dan nilai huruf per semester |
| Memberikan nilai & SKS yang dimiliki | **F5.2** Memvalidasi nilai terhadap skala nilai huruf yang berlaku dan menandai data yang tidak wajar (mis. SKS kosong, matkul ganda karena mengulang) |
| | **F5.3** Menghitung dan menampilkan IP per semester dan IPK kumulatif |
| Menyatakan target IPK yang ingin dicapai | **F5.4** Menghitung IP minimum yang dibutuhkan pada sisa SKS untuk mencapai target |
| Mencoba berbagai kemungkinan nilai | **F5.5** Memperbarui proyeksi seketika tanpa mengubah data nilai asli |

**Deskripsi fungsional (contoh satu butir):**
- **F5.2 Validasi data nilai**
  - User/pengguna: mahasiswa semua angkatan (PR3)
  - Deskripsi: sistem memeriksa setiap baris nilai terhadap skala nilai huruf dan bobot yang berlaku di ITB `[verifikasi skala resmi dari Peraturan Akademik]`, memastikan SKS berupa bilangan positif, dan mendeteksi matkul yang tercatat lebih dari sekali agar perhitungan mengulang matkul sesuai aturan `[verifikasi aturan nilai mengulang]`. Menjawab kesalahan hitung manual yang ditemukan pada M5.

### 15.3 Kerangka EUC domain lain (PIC melengkapi dengan kualitas setara 15.2)

| Domain | Nama use case kandidat | UT | F kandidat (sesuaikan dengan data) |
|---|---|---|---|
| A (UG1) | *KenaliMatkulDanDosen* | UT1.1, UT1.2 | F1.1 meminta kriteria pencarian (nama/kode matkul, dosen, prodi); F1.2 menampilkan matkul/dosen yang sesuai; F1.3 menyajikan ringkasan pengalaman (beban, kesulitan, gaya mengajar); F1.4 menampilkan detail tiap pengalaman beserta konteks kredibilitas (semester diambil, status pernah mengambil); F1.5 memungkinkan penyaringan pengalaman berdasarkan tahun ajaran/dosen |
| B (UG4) | *BandingkanKandidatMatkul* | UT4.1, UT4.2 | F4.1 menyajikan matkul yang dapat diambil per prodi/kategori; F4.2 menyaring berdasarkan SKS, jadwal, prasyarat; F4.3 menyimpan kandidat pilihan user; F4.4 menampilkan perbandingan kandidat pada atribut yang sama; F4.5 menyorot perbedaan penting (bentrok jadwal, prasyarat belum terpenuhi) |
| C (UG2) | *CariDanTanyakanMasalahMatkul* | UT2.1, UT2.2 | F2.1 meminta konteks matkul & kata kunci; F2.2 menampilkan diskusi serupa yang sudah terjawab; F2.3 menerima pertanyaan beserta konteks matkul; F2.4 menyediakan opsi identitas (anonim/bernama) `[hanya jika didukung data]`; F2.5 memberi tahu penanya ketika ada jawaban |
| D (UG3) | *BagikanPengalamanMatkul* | UT3.1, UT3.2 | F3.1 menyediakan struktur pengalaman (beban, kesulitan, tips, dosen, semester diambil); F3.2 memastikan penulis pernah mengambil matkul tersebut `[mekanisme ditentukan nanti, cukup tanggung jawab sistem]`; F3.3 menerbitkan pengalaman agar dapat dibaca banyak orang; F3.4 memberi tahu kating tentang pertanyaan pada matkul yang pernah diambil; F3.5 menerima jawaban dan mengaitkannya ke pertanyaan; F3.6 menunjukkan dampak kontribusi (jumlah pembaca/terbantu) `[jika data motivasi mendukung]` |
| E (UG6) | *RencanakanStudiSampaiLulus* | UT6.1 | F6.1 menyajikan syarat kelulusan & matkul wajib prodi; F6.2 menerima penempatan matkul ke tiap semester rencana; F6.3 memeriksa prasyarat, batas SKS per semester, dan kelengkapan matkul wajib; F6.4 memperingatkan pelanggaran beserta alasannya; F6.5 menampilkan total SKS & perkiraan beban per semester (menghubungkan data pengalaman dari UG1/UG3 — **pembeda M6**) |

**Definition of Done 3:** setiap UT punya ≥ 1 F; tidak ada kata antarmuka (klik/tombol/halaman/scroll); tiap F punya deskripsi; F yang ditandai `[jika data mendukung]` dihapus bila tidak didukung.

---

## 16. Usability Goals & UX Goals — Slide 4 (Owner baris: tiap domain; tabel gabungan & justifikasi akhir: E)

### 16.1 Aturan
- Gunakan enam **usability goals**: effectiveness, efficiency, safety, utility, learnability, memorability — **masing-masing tepat sekali** (dibagi ke domain yang paling relevan).
- Gunakan **UX goals** dari daftar aspek pengalaman yang diinginkan (mis. helpful, satisfying, rewarding, motivating, supportive of creativity, enjoyable, engaging). Jika memakai istilah di luar daftar buku (mis. *trustworthy*), wajib ada kalimat justifikasi mengapa istilah itu dipakai.
- Setiap baris: **goal → justifikasi (1–2 kalimat, merujuk data) → M → UG → F → kriteria terukur**. Kriteria terukur tidak diminta eksplisit di MS1, tetapi **akan dipakai sebagai acuan evaluasi di MS3 & MS5**, jadi sebaiknya disiapkan sekarang.

### 16.2 Draf tabel **[HIPOTESIS]**

| Kode | Usability Goal | Justifikasi (draf, ganti dengan data) | Masalah | User Goal | Fungsional | Kriteria terukur (untuk MS3/MS5) | Owner |
|---|---|---|---|---|---|---|---|
| UsG1 | **Effectiveness** | Inti M1–M2 adalah keputusan matkul yang meleset karena info tidak memadai; sistem harus benar-benar memungkinkan user mendapat gambaran matkul | M1, M2 | UG1 | F1.2, F1.3, F1.4 | ≥ 90% partisipan berhasil menemukan beban & gaya mengajar matkul target tanpa bantuan | A |
| UsG2 | **Efficiency** | Informan membandingkan kandidat di kepala/catatan terpisah dan butuh waktu lama | M1, M6 | UG4 | F4.3, F4.4 | Membandingkan 3 kandidat matkul selesai < 2 menit | B |
| UsG3 | **Utility** | Masalah bukan ketiadaan tempat bertanya, tetapi jawaban yang sudah ada tidak bisa ditemukan kembali; fungsi pencarian harus benar-benar berguna | M3 | UG2 | F2.1, F2.2 | ≥ 70% partisipan menemukan diskusi relevan sebelum membuat pertanyaan baru | C |
| UsG4 | **Learnability** | Kating hanya mau berbagi jika tidak merepotkan; kontribusi pertama harus langsung bisa dilakukan tanpa panduan | M4 | UG3 | F3.1, F3.5 | Partisipan kating menyelesaikan ulasan pertama tanpa bantuan < 5 menit | D |
| UsG5 | **Safety** | Kesalahan hitung/rencana berdampak besar (studi molor); sistem harus mencegah dan memulihkan kesalahan | M5 | UG5, UG6 | F5.2, F5.5, F6.3, F6.4 | 100% pelanggaran prasyarat/batas SKS pada skenario uji terdeteksi; data nilai asli tidak berubah saat simulasi | E |
| UsG6 | **Memorability** | Perencanaan FRS & pembaruan nilai hanya terjadi **sekali per semester**; user kembali setelah ± 5–6 bulan tanpa ingat caranya | M5, M6 | UG6, UG4 | F6.2, F4.3 | Partisipan yang sudah mencoba sekali menyelesaikan task yang sama seminggu kemudian tanpa kesalahan navigasi berarti | E (koordinasi dengan B) |

| Kode | UX Goal | Justifikasi (draf) | Masalah | User Goal | Fungsional | Indikator (untuk MS3/MS5) | Owner |
|---|---|---|---|---|---|---|---|
| UxG1 | **Helpful** | Mahasiswa dengan jaringan kating terbatas merasa sendirian saat memutuskan matkul | M1, M2 | UG1 | F1.3 | Skor rata-rata ≥ 4/5 pada pernyataan "membantu saya memutuskan" | A |
| UxG2 | **Satisfying** | Menyusun FRS saat ini melelahkan & penuh keraguan | M2, M6 | UG4 | F4.4, F4.5 | Partisipan menyatakan lebih yakin dengan pilihannya dibanding cara biasa | B |
| UxG3 | **Supportive / tidak mengintimidasi** *(justifikasi istilah: data menunjukkan rasa sungkan bertanya)* | Informan menunda bertanya karena takut dianggap tidak paham | M3 | UG2 | F2.3, F2.4 | Partisipan tidak ragu mengirim pertanyaan dalam uji | C |
| UxG4 | **Rewarding** | Kating mau berbagi jika kontribusinya terasa berdampak & dihargai | M4 | UG3 | F3.3, F3.6 | Partisipan kating menyatakan mau berkontribusi lagi | D |
| UxG5 | **Motivating** | Mengetahui target nilai yang realistis mendorong mengatur prioritas belajar | M5 | UG5 | F5.4 | Partisipan dapat menyebutkan target nilai konkret setelah memakai prototipe | E |
| UxG6 | **Trustworthy** *(justifikasi istilah wajib ditulis)* | Keraguan terhadap kebenaran info adalah pola kuat di M1 | M1 | UG1, UG3 | F1.4, F3.2 | Partisipan dapat menjelaskan mengapa sebuah ulasan layak/tidak layak dipercaya | D (koordinasi dengan A) |

---

## 17. Lampiran (Owner: A)

### 17.1 Slide Penggunaan AI (5a)
Isi slide:
1. Tabel dari tab `AI_Log`: tools, anggota, tujuan, bagaimana hasilnya diubah/diverifikasi.
2. Pernyataan: AI dipakai untuk **eksplorasi masalah dan pendalaman konsep desain interaksi** (mis. merapikan struktur planning, meninjau kelengkapan terhadap spesifikasi, menguji apakah pertanyaan wawancara bersifat leading, mendiskusikan definisi tipe interaksi). Data wawancara, temuan, M, persona, dan skenario disusun kelompok dari hasil wawancara.
3. 2–4 screenshot percakapan AI yang representatif (termasuk penggunaan AI untuk menyusun dokumen planning ini).

**Dilarang:** memakai AI untuk mengarang kutipan informan, persona, atau angka temuan.

### 17.2 Evidence User Gathering (5b)
- 1 slide kolase: 10 foto/screenshot sesi (wajah diblur jika diminta) dengan label kode informan, tanggal, mode.
- 1 slide tabel informan (kode, angkatan, fakultas, segmen, pewawancara, tanggal, durasi) — tanpa nama.
- 1 slide contoh observasi artefak (2–4 screenshot yang diblur).
- (Opsional) link folder rekaman berakses terbatas untuk asisten jika diminta, **hanya jika informan menyetujui**.

---

## 18. Outline PPT Final — urutan persis mengikuti sistematika spesifikasi

| No | Bagian spesifikasi | Judul slide | Isi | Owner | Bergantung pada |
|---|---|---|---|---|---|
| 1 | Judul | KuliahBareng | Nama produk, tagline, SDG, no. kelas & kelompok, nama + NIM 5 anggota | A | K1, K4, K5 |
| 2 | — | Daftar Isi | 5 bagian utama | E | — |
| 3 | 1 (divider) | Deskripsi Topik | — | E | — |
| 4 | 1a | Latar Belakang | 4.1 | A | Sintesis (angka) |
| 5 | 1a | Relevansi SDG | 4.2 + tabel target | A | K1 |
| 6 | 1b | Target Pengguna & Segmen Informan | 5.1, 5.4 | A | Registry `Informan` |
| 7 | 1b | Metode Riset | 5.2 (wawancara + observasi artefak) | A | — |
| 8 | 1b | Tujuan Riset | 5.3 | A | — |
| 9 | 2 (divider) | User Gathering — Identifikasi Problem Space | — | E | — |
| 10 | 2a | Temuan Utama Wawancara | 9.2 butir 1 | D | Sintesis |
| 11 | 2a | Masalah & Opportunity (M1–Mn) | 9.2 butir 2 | D | Sintesis |
| 12 | 2a | Solusi Existing & Gap | 4.3 | D | Ringkasan wawancara |
| 13–14 | 2b | User Goals (UG1–UG6) | 10.2 | E konsolidasi; isi dari A–E | M final |
| 15 | 2c | Swimlane User Process Flow | 11 | B | P final |
| 16 | 2c | Deskripsi Proses P1–Pn & D1–Dn | 11.3 | B | P final |
| 17–19 | 2d | Persona PR1–PR3 | 12 | C | Sintesis |
| 20 | 2e | Scenario S1 | 13.3 | D | Persona, P |
| 21 | 2e | Scenario S2 | 13.4 | D | Persona, P |
| 22 | 2f | Tabel User Task (UG–P–UT–PIC) | 14.1 | E | Registry |
| 23–32 | 2f | Deskripsi User Task — 2 slide per PIC (A, B, C, D, E) | 14.2 | Masing-masing | UT final |
| 33 | 3 (divider) | Fungsionalitas Sistem | — | E | — |
| 34–45 | 3 | EUC + deskripsi F per PIC (± 2 slide per domain, E boleh 3–4) | 15 | Masing-masing | UT final |
| 46 | 4 (divider) | Usability & UX Goals | — | E | — |
| 47 | 4 | Tabel Usability Goals + justifikasi | 16.2 | E | Semua baris domain |
| 48 | 4 | Tabel UX Goals + justifikasi | 16.2 | E | Semua baris domain |
| 49 | 5 (divider) | Lampiran | — | E | — |
| 50 | 5a | Penggunaan AI | 17.1 | A | `AI_Log` |
| 51–53 | 5b | Evidence User Gathering | 17.2 | A | Folder evidence |
| 54 | — | Terima Kasih | — | E | — |

Aturan desain ringan (E menetapkan di template): satu font keluarga, maksimal 3 warna utama + 1 warna aksen per domain (dipakai konsisten di label UG/UT/F), ukuran teks isi ≥ 14 pt, tabel ≥ 12 pt, setiap slide punya nomor & label bagian spesifikasi di pojok (mis. "2f — User Task").

---

## 19. Review, QA, & Checklist Submit

### 19.1 Cross-review (Minggu 08.00–11.00)
| Reviewer | Mereview slide milik | Fokus |
|---|---|---|
| A | B (swimlane, UT4.x, F4.x) | Proses natural? semua P terdeskripsi? |
| B | C (persona, UT2.x, F2.x) | Persona berbasis data? field lengkap? |
| C | D (M, existing solutions, scenario, UT3.x, F3.x) | M bebas solusi? scenario tanpa aplikasi & mencakup semua UG? |
| D | E (tabel gabungan, UT5–6, F5–6, usability/UX) | Tiap goal punya justifikasi & rujukan? |
| E | A (judul, topik, riset, UT1.x, F1.x, lampiran) | Identitas lengkap? SDG benar? evidence aman privasi? |

Reviewer menulis komentar (fitur comment), **pemilik slide yang mengedit**.

### 19.2 Traceability check (Minggu 14.00–15.00, A + E) — semua harus "YA"
- [ ] Setiap **M** dijawab ≥ 1 UG
- [ ] Setiap **UG** menjawab ≥ 1 M, muncul di ≥ 1 P, punya ≥ 1 UT, muncul di scenario
- [ ] Setiap **P** di diagram ada di tabel deskripsi dan di Registry (dan sebaliknya)
- [ ] Setiap **UT** merujuk P yang ada, punya PIC, punya deskripsi lengkap (user, deskripsi, tipe interaksi, model konseptual/metafora)
- [ ] Setiap **UT** punya ≥ 1 **F**; setiap F punya deskripsi
- [ ] Setiap **usability/UX goal** merujuk M, UG, dan F yang ada
- [ ] Setiap pain point **persona** → M; setiap goal persona → UG
- [ ] Kode di slide = kode di Registry (cek acak minimal 15 kode)
- [ ] Istilah sesuai Glosarium (cari: "mata kuliah", "course", "review", "senior")

### 19.3 Definition of Done keseluruhan
- [ ] Semua bagian 1a–5b spesifikasi ada **dengan urutan yang sama**
- [ ] 10 informan (atau alasan tertulis jika kurang), sebaran sesuai 5.4
- [ ] Tidak ada nama asli informan / data pribadi tidak diblur
- [ ] Tidak ada placeholder `[...]`, `x/10`, `135xxxxx`, "[HIPOTESIS]" yang tertinggal (cari dengan Ctrl+F)
- [ ] Setiap anggota PIC untuk UT berbeda (5 PIC, 10 UT)

### 19.4 Checklist submit (E)
- [ ] Nama file: `MS1-Requirement-K<no kelas>-<no kelompok>-KuliahBareng.pptx`
- [ ] Format **.pptx** (bukan PDF/link Google Slides); dibuka ulang setelah export, cek font, tabel, dan diagram tidak bergeser
- [ ] Ukuran file wajar (kompres gambar jika > 50 MB)
- [ ] Hanya **satu** file dikumpulkan untuk kelompok
- [ ] Submit di `s.hmif.dev/PengumpulanMilestoneIMK` **≤ 18.00** (batas resmi 20.00)
- [ ] Screenshot bukti submit dikirim ke grup; file final disalin ke `05_PPT/FINAL/`

---

## 20. Risiko & Mitigasi

| Risiko | Kemungkinan | Dampak | Mitigasi | Pemilik |
|---|---|---|---|---|
| SDG 4 sudah diambil kelompok lain | Tinggi (SDG populer) | Tinggi | Cek & isi form malam ini; cadangan SDG 10 siap (4.2) | A |
| Informan batal/tidak membalas | Sedang | Tinggi | 1 cadangan per anggota; batas Jumat 13.00; boleh wawancara online 20 menit | Semua |
| Data tidak mendukung fitur tertentu (mis. forum) | Sedang | Sedang | Aturan keputusan 8.3; jumlah UT per orang tetap | A (fasilitator) |
| Informan terlalu homogen (mis. banyak dari STEI) | Tinggi | Sedang | Aturan sebaran 5.4, dicek di Registry Kamis malam | A |
| Kode bentrok/inkonsisten antar-slide | Tinggi tanpa Registry | Tinggi | Registry sebagai satu sumber, konvensi 3.3, traceability check | A, E |
| Swimlane telat sehingga tabel UT tertahan | Sedang | Sedang | Draf P hipotesis sudah ada; B mengunci P ≤ Sabtu 10.00; domain owner boleh mengisi UT dulu dan menambah P setelahnya | B |
| Konflik edit di file PPT | Sedang | Sedang | Tiap orang hanya mengedit slide miliknya (lihat 18); E satu-satunya yang mengubah template/urutan | E |
| Layout rusak saat export .pptx | Sedang | Sedang | Export uji coba Sabtu malam, bukan Minggu sore | E |
| Konten terkesan dibuat AI | Sedang | Tinggi | Prinsip 0.2 no. 5; kutipan & angka dari ringkasan; AI_Log jujur | Semua |
| Pelanggaran privasi di evidence | Rendah | Tinggi | Consent tercatat, blur, tanpa nama asli (5.6) | A |

---

## 21. Kartu Tugas per Anggota

### Anggota A — Info Matkul & Dosen (UG1) · Topik & Riset · Fasilitator · Lampiran · Koordinator
- **Rabu:** SYNC-1; cek & isi SDG; buat Drive + Registry + Glosarium + tab Status; rekrut I1, I2 (+cadangan).
- **Kamis:** wawancara I1–I2 (Inti + Deep-Dive A) + ringkasan; draf slide 1, 4–8; cek sebaran informan di Registry malam hari.
- **Jumat:** sticky notes siap ≤ 17.00; siapkan board FigJam; **fasilitasi SYNC-2**; rapikan Registry setelah sesi.
- **Sabtu:** UG1 final; UT1.1–UT1.2 (tabel + 2 slide deskripsi); EUC *KenaliMatkulDanDosen* + deskripsi F1.x; baris UsG1 & UxG1; slide 50–53 (AI & evidence); update angka di slide 4.
- **Minggu:** review slide E; perbaiki komentar; traceability check bersama E.

### Anggota B — Jelajah & Bandingkan Matkul (UG4) · Swimlane
- **Rabu:** SYNC-1; rekrut I3, I4 (+cadangan); pelajari template cross-functional flowchart.
- **Kamis:** wawancara I3–I4 (Inti + Deep-Dive B) + ringkasan; siapkan kerangka lane & draf P hipotesis di draw.io.
- **Jumat:** sticky notes ≤ 17.00; pimpin segmen "Alur (P)" di SYNC-2; mulai gambar swimlane final malam itu.
- **Sabtu:** **kunci P di Registry ≤ 10.00**; slide 15–16; UG4 final; UT4.1–UT4.2 (tabel + 2 slide); EUC *BandingkanKandidatMatkul* + deskripsi F4.x; baris UsG2 & UxG2; bantu E untuk UsG6.
- **Minggu:** review slide C; perbaiki komentar pada slide sendiri.

### Anggota C — Forum Tanya Matkul (UG2) · Persona
- **Rabu:** SYNC-1; rekrut I5, I6 (+cadangan).
- **Kamis:** wawancara I5–I6 (Inti + Deep-Dive C, termasuk observasi pencarian di grup) + ringkasan; siapkan layout 3 persona di template E.
- **Jumat:** sticky notes ≤ 17.00; pimpin segmen "Persona" di SYNC-2.
- **Sabtu:** draf PR1–PR3 ≤ 14.00 (kirim ke D untuk scenario); UG2 final; UT2.1–UT2.2 (tabel + 2 slide); EUC *CariDanTanyakanMasalahMatkul* + deskripsi F2.x; baris UsG3 & UxG3.
- **Minggu:** review slide D; perbaiki komentar pada slide sendiri.

### Anggota D — Kontribusi Kating (UG3) · Masalah & Opportunity · Scenario
- **Rabu:** SYNC-1; rekrut I7, I8 (+cadangan).
- **Kamis:** wawancara I7–I8 (Inti + Deep-Dive D) + ringkasan; mulai tabel solusi existing (4.3) dari ringkasan yang masuk.
- **Jumat:** sticky notes ≤ 17.00; ikut SYNC-2; tulis draf kalimat M malam itu.
- **Sabtu:** slide 10–12 ≤ 12.00; UG3 final; UT3.1–UT3.2 (tabel + 2 slide); EUC *BagikanPengalamanMatkul* + deskripsi F3.x; baris UsG4, UxG4, UxG6; scenario S1 & S2 (14.00–18.00).
- **Minggu:** review slide E; perbaiki komentar pada slide sendiri.

### Anggota E — Perencanaan Akademik (UG5, UG6) · PPT Owner
- **Rabu:** SYNC-1; rekrut I9, I10 (+cadangan); mulai master template PPT.
- **Kamis:** wawancara I9–I10 (Inti + Deep-Dive E, termasuk observasi spreadsheet) + ringkasan; selesaikan template + seluruh slide kosong berlabel sesuai outline 18; verifikasi skala nilai & aturan akademik yang dipakai F5.x/F6.x.
- **Jumat:** sticky notes ≤ 17.00; ikut SYNC-2.
- **Sabtu:** UG5 & UG6 final; UT5.1 & UT6.1 (tabel + 2 slide); EUC *PantauCapaianAkademik* & *RencanakanStudiSampaiLulus* + deskripsi F5.x, F6.x; baris UsG5, UsG6, UxG5; **pimpin SYNC-3**; konsolidasi slide 13–14, 22, 47–48; export uji coba .pptx.
- **Minggu:** review slide A; traceability check bersama A; polish visual; content freeze 17.00; export, cek, **submit ≤ 18.00**.

---

*Dokumen ini adalah rencana kerja. Semua isi bertanda [HIPOTESIS] adalah dugaan awal yang wajib diuji, diubah, atau digugurkan berdasarkan hasil wawancara. Perubahan kode hanya dilakukan di Registry Sheet.*
