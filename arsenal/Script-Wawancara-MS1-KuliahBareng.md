# Script Wawancara — Milestone 1 IF3151 Interaksi Manusia Komputer
## Riset Pengalaman Mahasiswa ITB dalam Keputusan Akademik & Perkuliahan

| Item | Keterangan |
|---|---|
| Dipakai oleh | Anggota A–E (sesuai Planning v2) |
| Jumlah informan | 10 (I1–I10), 2 per anggota |
| Durasi target | 30 menit (maks. 35 menit; lihat catatan di Bagian 9) |
| Struktur | Pembuka → Modul Wawancara Gabungan (Q1–Q10, semua informan, semua pewawancara) → Penutup |
| Output setelah sesi | Template Ringkasan Wawancara (Planning v2, Bagian 7) diisi ≤ 3 jam setelah sesi |
| Status metode | **v3 (final)** — modul Inti + 5 Modul Deep-Dive per domain digabung jadi satu set 10 pertanyaan yang sama untuk semua informan; observasi artefak dihapus dari implementasi. Rekrutmen tetap tersegmentasi per domain (Planning v2 Bagian 5.4). Sumber keputusan: `Panduan-Wawancara-Final-v3.md`. |

---

## Daftar Isi

1. Cara Membaca Script Ini
2. Persiapan Sebelum Wawancara
3. Script Rekrutmen & Screening
4. Pembuka (3 menit)
5. Modul Wawancara Gabungan — Semua Informan (Q1–Q10)
6. Penutup (3 menit)
7. Bank Pertanyaan Probing
8. Menangani Situasi Sulit
9. Lembar Catatan Cepat (untuk dicetak/dibuka saat sesi)

---

## 1. Cara Membaca Script Ini

### 1.1 Simbol

| Simbol | Arti |
|---|---|
| 🗣️ | Kalimat yang **diucapkan** pewawancara (boleh disesuaikan gaya bicara, maknanya jangan diubah) |
| 🔍 | Pertanyaan **probing**, dipakai jika jawaban belum cukup dalam |
| 👂 | Apa yang perlu **didengarkan/dicatat** dari jawaban (tidak diucapkan) |
| ⭐ | Pertanyaan **prioritas**; wajib ditanyakan walau waktu mepet |
| ⏭️ | Pertanyaan **opsional**; lewati jika waktu kurang |
| ➡️ | Kalimat **transisi** antar-bagian |
| ⏱️ | Anggaran waktu |

### 1.2 Tujuan tiap bagian (untuk diingat pewawancara)

| Bagian | Menghasilkan data untuk |
|---|---|
| Q1 — Profil digital | Persona: device, aplikasi, kebiasaan |
| Q2 — War dan matkul cadangan | Swimlane (proses P, potensi decision node), M2, Scenario |
| Q3 — Kredibilitas informasi | M1 (utama), UG1 |
| Q4 — Kandidat matkul pilihan | UT4.1/UT4.2, M1/M2/M6, UG4 |
| Q5 — Kesulitan tugas/materi | UG2, M3, swimlane P10–P13 |
| Q6 — Posisi sebaliknya (ditanya orang lain) | UG3, M3/M4 |
| Q7 — Nilai keluar | UG5, M5, swimlane P1–P2 |
| Q8 — Prediksi nilai pasca-UTS | UG5, F5.4/F5.5, UsG3 |
| Q9 — Beban matkul dalam rencana studi | UG6, M6 |
| Q10 — Prioritas keluhan | Lintas M, prioritas untuk sesi sintesis |

### 1.3 Aturan emas (baca sebelum sesi pertama)

1. **Tanyakan kejadian nyata terakhir**, bukan kebiasaan umum. "Ceritakan terakhir kali…" lebih baik dari "Biasanya kamu…".
2. **Jangan sebut ide aplikasi kita** sebelum penutup. Kalau informan bertanya "ini buat bikin aplikasi ya?", jawab: *"Kami masih di tahap memahami masalah dulu, belum ada solusi. Makanya pengalamanmu penting banget."*
3. **Jangan pernah bertanya** "fitur apa yang kamu mau?" atau "kamu bakal pakai aplikasi X nggak?".
4. **Jangan menyimpulkan untuk informan.** ❌ "Berarti kamu kesel ya?" ✅ "Gimana rasanya waktu itu?"
5. **Jangan membela atau mengoreksi** pendapat informan, termasuk soal dosen atau jurusan tertentu.
6. **Diam 3 detik** setelah informan selesai bicara. Sering muncul cerita tambahan.
7. **Catat timestamp** untuk kutipan bagus, format `[mm:ss]`.
8. **Nama dosen yang disebut informan tidak dicatat** di ringkasan. Tulis "Dosen X matkul Y".

---

## 2. Persiapan Sebelum Wawancara

### 2.1 H-1 (sehari sebelum)
- [ ] Jadwal & lokasi/tautan meeting sudah dikonfirmasi ke informan
- [ ] Baca ulang script Bagian 5 (Modul Wawancara Gabungan) minimal sekali dengan suara pelan — sama untuk semua pewawancara, tidak ada modul khusus per domain lagi
- [ ] Siapkan file ringkasan kosong `I0x_<inisial>.docx` di `02_Ringkasan_Wawancara`
- [ ] Isi baris informan di Registry tab `Informan` (kode, segmen, jadwal)

### 2.2 H-0 (30 menit sebelum)
- [ ] Baterai HP ≥ 50%, memori kosong ≥ 1 GB
- [ ] Uji rekaman 10 detik (tatap muka: aplikasi perekam suara; online: fitur rekam Zoom/Meet/Discord **dan** perekam HP sebagai cadangan)
- [ ] Mode "Jangan Ganggu" aktif
- [ ] Lembar Catatan Cepat (Bagian 9) terbuka/tercetak
- [ ] Siapkan minuman/snack kecil untuk informan (opsional, tatap muka)

### 2.3 Lokasi
- **Tatap muka:** tempat yang cukup tenang agar rekaman jelas (hindari kantin saat jam makan siang). Duduk bersebelahan/menyerong, bukan berhadapan seperti interogasi.
- **Online:** minta informan bergabung lewat panggilan suara/video seperti biasa; tidak ada kebutuhan *share screen* khusus karena sesi ini tidak lagi memakai observasi artefak.

---

## 3. Script Rekrutmen & Screening

### 3.1 Pesan ajakan (chat)

> Halo `[nama]`! Aku `[namamu]`, `[prodi/angkatan]`. Aku lagi ngerjain tugas besar matkul Interaksi Manusia Komputer, dan butuh ngobrol sekitar **30 menit** sama mahasiswa ITB soal **pengalaman ngurus FRS, cari info matkul, ngerjain tugas, dan ngatur rencana studi**. Nggak ada jawaban benar/salah, murni cerita pengalaman. Bisa tatap muka atau online.
>
> Kalau berkenan, boleh aku tanya satu hal dulu buat mastiin kamu cocok sama kriteria kami? 🙏

### 3.2 Pertanyaan screening (kirim setelah dibalas)

| Kode | Pewawancara | Pertanyaan screening (harus dijawab "ya") | Data tambahan yang ditanyakan |
|---|---|---|---|
| I1, I2 | A | "Semester ini kamu baru pertama kali FRS di prodi, dan sempat cari info soal matkul/dosen sebelum FRS?" | Angkatan, prodi |
| I3, I4 | B | "Kamu pernah atau sedang ambil matkul pilihan di luar prodi, atau minor?" | Angkatan, prodi, matkul luar prodi apa |
| I5, I6 | C | "Semester ini atau kemarin, kamu cukup sering nanya soal tugas/materi ke grup atau teman?" | Angkatan, prodi |
| I7, I8 | D | "Kamu cukup sering ditanya adik tingkat soal matkul atau tugas?" | Angkatan, prodi, peran (asisten/mentor/pengurus) |
| I9 | E | "Waktu TPB, kamu memantau atau menghitung IP sendiri, misalnya buat persiapan penjurusan?" | Angkatan, prodi |
| I10 | E | "Kamu sedang atau baru saja menghitung sisa SKS atau menyusun matkul supaya bisa lulus tepat waktu?" | Angkatan, prodi |

Setelah "ya": cek aturan sebaran di Registry (≥ 4 fakultas, ≥ 3 angkatan, maks. 3 dari STEI, dua informanmu beda prodi). Jika tidak memenuhi, cari kandidat lain dengan sopan: *"Makasih banyak! Kebetulan kuota prodi itu sudah terisi, nanti kalau butuh aku kabarin lagi ya."*

> Catatan: pertanyaan screening di atas hanya menentukan **siapa yang diwawancarai** (segmen A–E tetap sesuai Planning v2 Bagian 5.4). Pertanyaan wawancara yang sesungguhnya (Bagian 5) sama untuk semua segmen.

### 3.3 Pesan konfirmasi jadwal

> Makasih banyak, `[nama]`! Kita ngobrol **`[hari, tanggal]` jam `[jam]`** di **`[lokasi/link]`** ya. Kalau boleh, obrolannya nanti aku rekam audionya buat catatan tugas saja, nama kamu nggak akan muncul di presentasi. Kalau ada perubahan jadwal kabarin aja 🙌

---

## 4. Pembuka

⏱️ **3 menit**

### 4.1 Salam & tujuan

🗣️ *"Halo `[nama]`, makasih banyak udah mau ngeluangin waktu. Aku `[namamu]` dari `[prodi/angkatan]`."*

🗣️ *"Jadi kelompok kami lagi ngerjain tugas besar Interaksi Manusia Komputer. Kami lagi riset tentang **gimana pengalaman mahasiswa ITB waktu ngambil keputusan akademik dan ngejalanin perkuliahan**, misalnya waktu FRS, nyari info matkul, ngerjain tugas, sampai ngatur rencana studi."*

🗣️ *"Nggak ada jawaban benar atau salah. Justru yang paling kami butuhin itu cerita jujur, termasuk hal-hal yang nyebelin atau ribet. Kamu juga nggak lagi dinilai kok, yang kami pelajari itu pengalamannya, bukan orangnya."*

### 4.2 Consent

🗣️ *"Ngobrolnya sekitar 30 menit. Boleh aku **rekam audionya**? Rekamannya cuma dipakai kelompok kami buat nyatet, **nama kamu nggak akan muncul** di presentasi, dan rekamannya bakal dihapus setelah nilai tugasnya keluar."*

👂 Tunggu jawaban eksplisit "boleh". Jika menolak: *"Oke, nggak masalah, aku catat manual aja ya."* → catat lebih detail, tulis "Consent rekam: N".

🗣️ (setelah rekaman mulai) *"Oke, rekaman udah jalan. Buat catatan, sekarang `[hari, tanggal]`, dan kamu setuju obrolan ini direkam ya?"*

👂 Informan menjawab "setuju" di rekaman → ini bukti consent.

🗣️ *"Kalau ada pertanyaan yang nggak nyaman, bilang aja skip ya. Kamu juga boleh berhenti kapan aja."*

### 4.3 Data diri singkat

🗣️ *"Sebelum mulai, boleh sebutin angkatan, prodi, sama sekarang semester berapa?"*

🗣️ ⏭️ *"Kamu asli Bandung atau merantau?"* (opsional, jangan dipaksa)

👂 Catat: angkatan, prodi/fakultas, semester, perantau (Y/N/tidak disebut).

➡️ *"Oke, aku mulai dari hal yang ringan dulu ya."*

---

## 5. Modul Wawancara Gabungan — Semua Informan (Q1–Q10)

⏱️ **Target 28–32 menit.** Berlaku untuk **semua informan I1–I10**, dibawakan oleh **pewawancara mana pun (A–E)** — tidak ada lagi pembagian Modul Inti vs Modul Deep-Dive per domain. Rekrutmen & segmen informan tetap sesuai Planning v2 Bagian 5.4 (I1/I2 = segmen A, I3/I4 = segmen B, dst.); yang disatukan hanya pertanyaannya.

Setiap pertanyaan punya dua versi kalimat — **Informal** dan **Formal** — pilih sesuai kenyamanan informan, maknanya harus sama. Probing tambahan ditulis di dalam tanda kurung `(...)`, tanyakan hanya jika jawaban awal belum cukup dalam.

> **Catatan lokal (khusus Q2):** mekanisme "dosen otomatis ditempatkan per kelas" berlaku di prodi penyusun panduan ini. Pewawancara dari prodi lain wajib memvalidasi apakah mekanisme yang sama berlaku di prodi informan, dan menyesuaikan probing bagian dosen di Q2 bila berbeda.

### Q1 — Profil digital
🗣️ **Informal:** *"Buka HP, aplikasi apa yang paling sering kepencet buat urusan kuliah? Buat apa masing-masing?"*
🗣️ **Formal:** *"Aplikasi apa yang paling sering Anda gunakan untuk keperluan perkuliahan? Untuk apa masing-masing biasanya digunakan?"*
👂 **Mengisi:** 2d Persona (kebiasaan device/aplikasi)

### Q2 — War dan matkul cadangan
🗣️ **Informal:** *"Semester ini ada matkul yang pas war kamu sampai gagal dapet kelasnya? Kalau ada, coba runut dari awal, gimana taunya bakal rebutan, abis gagal ngapain, udah nyiapin cadangan dari awal atau baru nyari pas itu juga? (Kalau nggak pernah gagal: berarti emang udah mikirin strategi dari awal? Ceritain gimana caranya milih matkul yang aman.) (Probing: Walau tau kelasnya udah include dosen tertentu, ada nggak momen kamu sengaja milih kelas jam tertentu karena pengen dapet atau ngehindarin dosen tertentu? Atau udah pasrah aja mana yang keambil?)"*
🗣️ **Formal:** *"Apakah pada semester ini ada mata kuliah yang gagal Anda dapatkan kelasnya karena rebutan slot (war)? Jika ada, dapatkah Anda menceritakan prosesnya, mulai dari bagaimana Anda mengetahui akan terjadi rebutan, hingga langkah yang Anda ambil setelah gagal? Apakah Anda sudah menyiapkan mata kuliah cadangan sejak awal, atau baru mencari setelahnya? (Jika tidak pernah gagal: berarti Anda sudah memiliki strategi tertentu? Dapatkah Anda menjelaskan bagaimana Anda memilih mata kuliah yang aman?) (Lanjutan: Meskipun kelas sudah terikat dengan dosen tertentu, apakah pernah ada momen Anda sengaja memilih jadwal kelas tertentu karena ingin mendapatkan atau menghindari dosen tertentu? Atau Anda cenderung menerima kelas mana pun yang berhasil didapatkan?)"*
👂 **Mengisi:** 2c Swimlane (proses P baru, potensi decision node), 2a M2, 2e Scenario

### Q3 — Kredibilitas informasi
🗣️ **Informal:** *"Coba inget info soal matkul atau dosen yang terakhir kamu denger dari kating atau grup. Itu bener kejadiannya kayak gitu atau meleset? Runut dari kamu denger sampai kamu percaya atau enggak."*
🗣️ **Formal:** *"Dapatkah Anda menceritakan informasi terakhir mengenai suatu mata kuliah atau dosen yang Anda peroleh dari kating atau grup? Apakah informasi tersebut sesuai dengan kenyataan atau ternyata meleset? Mohon diceritakan prosesnya, mulai dari Anda menerima informasi tersebut hingga Anda memutuskan untuk mempercayainya atau tidak."*
👂 **Mengisi:** 2a M1 (utama), 2b UG1

### Q4 — Kandidat matkul pilihan
🗣️ **Informal:** *"Kalau ambil matkul pilihan atau lintas prodi, ada berapa kandidat di awal, dan apa yang paling nentuin kamu milih satu? (Probing: Info soal kandidat-kandidat itu kamu tau dari mana? Ada yang ternyata infonya nggak lengkap atau salah pas udah dijalanin?)"*
🗣️ **Formal:** *"Ketika Anda mengambil mata kuliah pilihan atau lintas program studi, berapa jumlah kandidat mata kuliah pada awalnya, dan faktor apa yang paling menentukan pilihan akhir Anda? (Lanjutan: Informasi mengenai kandidat-kandidat tersebut Anda peroleh dari mana? Apakah ada yang ternyata informasinya tidak lengkap atau keliru setelah dijalani?)"*
👂 **Mengisi:** 2f UT4.1/UT4.2, 2a M1/M2/M6, 2b UG4

### Q5 — Kesulitan tugas/materi
🗣️ **Informal:** *"Terakhir kali bingung soal tugas, coba certain dari mulai bingung sampai dapet jawaban. Dari mana dan butuh berapa lama?"*
🗣️ **Formal:** *"Dapatkah Anda menceritakan pengalaman terakhir Anda mengalami kebingungan terkait tugas atau materi perkuliahan? Mohon diceritakan mulai dari saat Anda mengalami kebingungan hingga memperoleh jawaban, termasuk dari mana jawaban tersebut Anda dapatkan dan berapa lama waktu yang diperlukan."*
👂 **Mengisi:** 2b UG2, 2a M3, 2c swimlane P10–P13

### Q6 — Posisi sebaliknya (ditanya orang lain)
🗣️ **Informal:** *"Pernah kebalik posisinya, kamu yang ditanya adik tingkat atau temen soal matkul? Ceritain kejadiannya."*
🗣️ **Formal:** *"Apakah Anda pernah berada di posisi sebaliknya, yaitu ditanya oleh adik tingkat atau teman mengenai suatu mata kuliah? Dapatkah Anda menceritakan kejadian tersebut?"*
👂 **Mengisi:** 2b UG3, 2a M3/M4

### Q7 — Nilai keluar
🗣️ **Informal:** *"Abis nilai keluar, coba certain apa yang kamu lakuin sama nilai itu. Dihitung, dicatat, atau dibiarin aja? (Probing: Dari situ, pernah nggak hasilnya beda dari yang kamu kira? Misal SKS kurang, prasyarat kelewat, atau IPK meleset dari dugaan?)"*
🗣️ **Formal:** *"Setelah nilai semester diumumkan, dapatkah Anda menceritakan apa yang biasanya Anda lakukan dengan nilai tersebut? (Lanjutan: Dari situ, apakah pernah hasilnya berbeda dari yang Anda perkirakan? Misalnya SKS kurang, prasyarat terlewat, atau IPK meleset dari dugaan?)"*
👂 **Mengisi:** 2b UG5, 2a M5, 2c swimlane P1–P2

### Q8 — Prediksi nilai pasca-UTS
🗣️ **Informal:** *"Abis UTS, coba certain cara kamu mikirin nilai UAS yang dibutuhkan biar dapet target tertentu. Itungannya pake spreadsheet, dicatat manual, atau kira-kira di kepala aja? Kalau mau bikin spreadsheet buat itungan kayak gitu, susah nggak menurut kamu?"*
🗣️ **Formal:** *"Setelah UTS, dapatkah Anda menceritakan bagaimana Anda memperkirakan nilai UAS yang dibutuhkan untuk mencapai target tertentu? Apakah Anda menghitungnya menggunakan spreadsheet, mencatatnya secara manual, atau hanya memperkirakan dalam pikiran? Jika Anda mencoba menyusun spreadsheet untuk perhitungan tersebut, menurut Anda apakah hal itu sulit dilakukan?"*
👂 **Mengisi:** 2b UG5, 3 F5.4/F5.5, 4 UsG3

### Q9 — Beban matkul dalam rencana studi
🗣️ **Informal:** *"Pas nyusun rencana matkul ke depan, coba certain gimana kamu mikirin beratnya matkul, bukan cuma SKS-nya."*
🗣️ **Formal:** *"Ketika menyusun rencana pengambilan mata kuliah untuk semester berikutnya, dapatkah Anda menjelaskan bagaimana Anda mempertimbangkan beban mata kuliah, tidak hanya jumlah SKS-nya?"*
👂 **Mengisi:** 2b UG6, 2a M6

### Q10 — Prioritas keluhan
🗣️ **Informal:** *"Dari semua yang tadi kamu certain, bagian mana yang paling bikin sebel? (Kalau kredibilitas info belum tersentuh di jawaban manapun: Dari sisi nyari info soal matkul/dosen sendiri, ada yang menurut kamu ganggu nggak?)"*
🗣️ **Formal:** *"Dari seluruh pengalaman yang telah Anda ceritakan, bagian mana yang menurut Anda paling merepotkan?"*
👂 **Mengisi:** Lintas 2a, prioritas untuk sesi sintesis

➡️ *"Makasih, ceritanya membantu banget. Sebelum kita tutup, satu pertanyaan lagi ya."*

🗣️ **Informal:** *"Kalau bisa benerin satu hal dari cara ngurus akademik di ITB, apa?"*
🗣️ **Formal:** *"Jika Anda dapat memperbaiki satu hal dari cara pengelolaan akademik di ITB, apa yang ingin Anda perbaiki?"*

➡️ Lanjut ke **Bagian 6 Penutup** (T1–T5 di bawah melengkapi, tidak perlu mengulang pertanyaan yang jawabannya sudah didapat dari Q10/pertanyaan di atas).

---

## 6. Penutup

⏱️ **3 menit**

> Catatan: T1 dan T2 di bawah mirip dengan Q10 dan pertanyaan penutup Bagian 5 — kalau sudah terjawab jelas di sana, cukup konfirmasi ulang singkat, tidak perlu bertanya dari nol.

**⭐ T1 — Paling mengganggu**
🗣️ *"Dari semua yang udah kita obrolin tadi, hal apa yang paling mengganggu atau paling bikin repot buat kamu?"*

👂 Prioritas pain point menurut informan sendiri. **Tandai sebagai kutipan kandidat.**

**⭐ T2 — Satu perubahan**
🗣️ *"Kalau kamu bisa ngubah satu hal dari cara mahasiswa ITB nyari info akademik atau ngerencanain studi, apa yang bakal kamu ubah? Kenapa?"*

👂 Jika informan menjawab dalam bentuk fitur/aplikasi, **tanyakan balik masalahnya**: *"Kalau itu ada, masalah apa yang jadi selesai buat kamu?"*

**T3 — Hal yang terlewat**
🗣️ *"Ada hal lain yang belum aku tanyain, tapi menurutmu penting soal topik ini?"*

**⭐ T4 — Konfirmasi consent & foto**
🗣️ *"Sekali lagi, kamu oke ya kalau rekaman tadi dipakai buat tugas kami, dengan nama dan data pribadi disamarkan?"*

🗣️ *"Boleh aku foto sesi ini buat bukti wawancara di lampiran? Kalau mau, wajahnya bisa diblur atau fotonya dari belakang."*

👂 Catat consent foto Y/N dan preferensi blur.

**⭐ T5 — Izin kontak lanjutan**
🗣️ *"Nanti kalau kami udah punya rancangan awal, boleh kami hubungi lagi buat nyobain dan kasih masukan?"*

👂 Catat Y/N di Registry (berguna untuk MS3 evaluasi low-fi).

**Terima kasih**
🗣️ *"Makasih banyak ya `[nama]`, ceritamu ngebantu banget buat riset kami. Kalau ada yang mau ditambahin nanti, chat aku aja."*

⏹️ Hentikan rekaman **setelah** informan selesai bicara (kadang cerita penting muncul di sini; jika muncul setelah rekaman berhenti, catat manual dengan tanda `[setelah rekaman]`).

### 6.1 Setelah informan pergi (5 menit, jangan ditunda)
- [ ] Simpan & beri nama rekaman: `I0x_<inisial>_<YYYYMMDD>.m4a`
- [ ] Tulis 3 kesan terkuat dalam 3 baris di Lembar Catatan Cepat
- [ ] Upload rekaman & foto ke `01_Rekaman/I0x_<pewawancara>_<inisial>/`
- [ ] Update Registry tab `Informan` (durasi, consent, link)
- [ ] Jadwalkan pengisian Template Ringkasan ≤ 3 jam dari sekarang

---

## 7. Bank Pertanyaan Probing

Pakai kapan saja jawaban informan masih dangkal.

| Tujuan | Pertanyaan |
|---|---|
| Minta cerita konkret | "Bisa kasih contoh kejadian yang paling kamu ingat?" |
| Urutan langkah | "Terus habis itu kamu ngapain?" · "Kalau diurutin langkahnya, dari awal gimana?" |
| Alasan | "Kenapa gitu?" · "Apa yang bikin kamu milih cara itu?" |
| Emosi | "Gimana rasanya waktu itu?" |
| Konsekuensi | "Dampaknya ke kamu apa?" · "Kalau itu nggak terjadi, bedanya apa?" |
| Frekuensi | "Itu sering kejadian atau cuma sekali?" |
| Workaround | "Ada cara lain yang pernah kamu coba?" · "Gimana kamu ngakalinnya?" |
| Klarifikasi istilah | "Maksudnya `[istilah]` itu gimana?" |
| Mengulang untuk validasi | "Jadi kalau aku nggak salah tangkap, kamu `[parafrase]`. Bener?" |
| Menggali pengecualian | "Ada kondisi di mana itu nggak berlaku?" |
| Keluar dari opini umum | "Itu pengalaman kamu sendiri atau cerita orang?" |

### 7.1 Pertanyaan yang **dilarang** & penggantinya

| ❌ Jangan | Kenapa | ✅ Ganti dengan |
|---|---|---|
| "Kamu setuju nggak kalau info matkul itu susah dicari?" | Leading | "Gimana pengalamanmu nyari info matkul?" |
| "Fitur apa yang kamu butuhin?" | User bukan desainer; jawaban hipotetis | "Apa yang paling bikin repot waktu …?" |
| "Kamu bakal pakai aplikasi kayak gitu nggak?" | Jawaban cenderung sopan, tidak prediktif | "Aplikasi kuliah apa yang pernah kamu coba lalu berhenti? Kenapa?" |
| "Biasanya kamu …?" (sebagai pertanyaan pertama) | Jawaban generalisasi | "Ceritain terakhir kali kamu …" |
| "Pasti ribet banget ya?" | Menanamkan emosi | "Gimana rasanya?" |
| "Kenapa kamu nggak nanya aja ke kating?" | Menghakimi | "Waktu itu apa yang kamu pertimbangin sebelum nanya?" |
| Dua pertanyaan sekaligus ("dari mana dan kenapa?") | Informan menjawab salah satu | Tanya satu per satu |

---

## 8. Menangani Situasi Sulit

| Situasi | Yang dilakukan |
|---|---|
| **Informan menjawab sangat singkat** | Pakai "Bisa kasih contoh kejadian terakhirnya?" Beri jeda diam. Jangan beralih ke pertanyaan berikut terlalu cepat. |
| **Informan terlalu panjang / keluar topik** | Tunggu jeda, lalu: *"Menarik banget. Aku balik sedikit ke `[topik]` ya, tadi kamu sempat bilang `[kata kunci]`…"* |
| **Waktu tersisa 10 menit tapi Q1–Q10 belum selesai** | Persingkat probing (🔍) dan durasi cerita per pertanyaan, tetap ajukan seluruh Q1–Q10 secara ringkas, lalu langsung ke Penutup: T1, T4, T5. |
| **Informan menjelekkan dosen/orang tertentu** | Jangan menanggapi penilaiannya. Arahkan ke pengalaman: *"Dampaknya ke cara kamu belajar gimana?"* Jangan catat nama dosen. |
| **Informan terlihat tidak nyaman/emosional** (mis. cerita nilai buruk, mengulang matkul) | *"Makasih udah mau cerita. Kalau mau skip bagian ini, nggak apa-apa banget."* Beri pilihan, jangan menggali lebih jauh. |
| **Informan balik bertanya pendapatmu** | *"Aku penasaran sama pendapatmu dulu. Nanti di akhir kita bisa ngobrol."* |
| **Informan menebak "ini buat bikin aplikasi ya?"** | *"Kami masih tahap memahami masalah, belum ke solusi. Makanya ceritamu penting."* |
| **Rekaman gagal di tengah sesi** | Jangan panik. Beri tahu informan, lanjutkan dengan catatan manual lebih detail, segera tulis ringkasan setelah sesi. |
| **Online: koneksi putus** | Hubungi lewat chat, lanjutkan dari pertanyaan terakhir. Jika tidak bisa lanjut dan data < 60%, jadwalkan ulang 15 menit atau pakai informan cadangan. |
| **Informan ternyata tidak cocok segmen** (baru ketahuan di tengah) | Selesaikan Q1–Q10 dengan sopan (datanya tetap berguna). Catat sebagai `I11+`, cari informan pengganti untuk segmen tersebut. |
| **Jawaban informan bertentangan dengan hipotesis kelompok** | **Bagus.** Gali lebih dalam: "Kenapa menurutmu itu nggak jadi masalah?" Catat di bagian "Kejutan" template ringkasan. |

---

## 9. Lembar Catatan Cepat

Salin blok di bawah untuk setiap informan. Isi selama sesi dengan singkat; detail dilengkapi dari rekaman saat mengisi Template Ringkasan.

```
═══════════════════════════════════════════════════════════════════
KODE: I__   PEWAWANCARA: __   TANGGAL: __/09/2026   MULAI: __:__   SELESAI: __:__
MODE: [ ] tatap muka  [ ] online     REKAM: [ ] Y [ ] N     FOTO: [ ] Y [ ] N   BLUR: [ ] Y [ ] N
Kontak lanjutan MS3: [ ] Y [ ] N
───────────────────────────────────────────────────────────────────
PROFIL   Angkatan: ____  Prodi/Fak: __________  Smt: __  Perantau: Y/N/-
         Device utama: __________  Apps harian: ______________________
         Jml grup chat kuliah: ___  App kuliah yang ditinggalkan & alasan: __________

CATATAN Q1–Q10 (ringkas saja, detail dilengkapi dari rekaman)
 Q1 (profil digital): ____________________________________________
 Q2 (war & matkul cadangan): _____________________________________
 Q3 (kredibilitas info): _________________________________________
 Q4 (kandidat matkul pilihan): ___________________________________
 Q5 (kesulitan tugas/materi): ____________________________________
 Q6 (posisi sebaliknya/ditanya orang lain): ______________________
 Q7 (nilai keluar): ______________________________________________
 Q8 (prediksi nilai pasca-UTS): __________________________________
 Q9 (beban matkul dlm rencana studi): ____________________________
 Q10 (prioritas keluhan): ________________________________________

 Pain points (+ konsekuensi):
  • _____________________________________________________________
  • _____________________________________________________________
  • _____________________________________________________________
 Workaround/tools: _______________________________________________

KUTIPAN KANDIDAT (verbatim + timestamp)
 [__:__] "________________________________________________________"
 [__:__] "________________________________________________________"
 [__:__] "________________________________________________________"

PENUTUP  Paling mengganggu: ______________________________________
         Satu perubahan: ______________________________________
KEJUTAN / BERTENTANGAN DGN HIPOTESIS: ____________________________

3 KESAN TERKUAT (tulis setelah informan pergi)
 1) ______________________________________________________________
 2) ______________________________________________________________
 3) ______________________________________________________________
═══════════════════════════════════════════════════════════════════
```

---

## Ringkasan Alokasi Waktu per Sesi

| Bagian | Menit | Kumulatif |
|---|---|---|
| Pembuka & consent | 3 | 3 |
| Modul Wawancara Gabungan (Q1–Q10 + pertanyaan penutup modul) | 28–32 | 31–35 |
| Penutup sesi (T1–T5, consent foto, izin kontak lanjutan) | 3 | 34–38 |

> Total ~34–38 menit — sedikit di atas target 30–35 menit di Planning v2 Bagian 5.2/6.1 karena modul kini satu sesi tunggal tanpa observasi artefak (yang dulu memangkas waktu cerita). Persingkat probing (🔍) di Bagian 5 bila sesi berjalan mendekati batas 35 menit.

*Script ini adalah panduan, bukan kuesioner lisan. Urutan boleh berubah mengikuti alur cerita informan, selama Q1–Q10 tercakup dan tidak ada pertanyaan yang menggiring.*
