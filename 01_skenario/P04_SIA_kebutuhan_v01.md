
Skenario (ditetapkan jobsheet, fiktif)
Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin Akademik mengelola data mahasiswa: menambah data mahasiswa baru, mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh collaboration yang bersesuaian.

Kebutuhan baru Pertemuan 4
| ID | Kebutuhan tugas |
|---|---|
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa |
| SIA-R11 | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data mahasiswa |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS |

SIA-R01 dan SIA-R02 (Pertemuan 2) serta SIA-R03 sampai SIA-R06 (Pertemuan 3) tetap berlaku, tidak berubah arti, dan tidak disalin ulang; rujuk berkas P02 dan P03.

Batas dan asumsi yang sudah ditetapkan
- Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 sampai SIA-R06 tetap mempunyai identitas berbeda.
- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
- Kalender akademik adalah agenda resmi institusi (awal semester, batas KRS, masa ujian, dan sejenisnya), bukan jadwal kuliah Pertemuan 2.
- Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. Nilai yang diinput belum terpublikasi; KHS hanya menampilkan nilai yang sudah dipublikasikan.
- Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data akademik aktif (ketentuan fiktif untuk latihan).
- Pengajuan KRS tetap digambar sebagai bagian diagram kumulatif dari Pertemuan 3.
- Pembayaran dan perancangan basis data berada di luar tugas.

Pertanyaan belum terjawab (tidak diputuskan sendiri)
1. Rentang nilai yang sah pada Input Nilai Mata Kuliah belum ditetapkan skenario.
2. Siapa dan melalui fungsi apa nilai dinyatakan resmi (dipublikasikan) belum dimodelkan.
3. Apa yang dimaksud "data akademik aktif" pada Hapus Data Mahasiswa belum dirinci.
4. Dosen Wali dan Dosen dimodelkan sebagai aktor terpisah; apakah Dosen Wali bentuk khusus dari Dosen tidak ditetapkan jobsheet, sehingga tidak digambar sebagai generalization.

Metadata tambahan P04
- Generalization yang digunakan: aktor (Mahasiswa → Civitas Akademika, Dosen → Civitas Akademika); use case (SIA-UC11, UC12, UC13 → SIA-UC10).
- Collaboration yang digunakan: SIA-CO01 Input Nilai Mata Kuliah (merealisasikan SIA-UC08), SIA-CO02 Lihat KHS (merealisasikan SIA-UC09).
- Sumber kebutuhan baru: SIA-R07 sampai SIA-R12.

Uji konsistensi (Langkah 8)
Situasi A — Mahasiswa melihat kalender akademik tanpa asosiasi langsung.**
Tetap benar: Mahasiswa adalah bentuk khusus dari Civitas Akademika, dan asosiasi Civitas Akademika ke SIA-UC07 Lihat Kalender Akademik digambar satu kali dari aktor umum. Mahasiswa mewarisinya (demikian pula Dosen), sehingga garis tidak digambar ulang.

Situasi B — Dosen bukan pengampu mencoba menginput nilai.**
Menurut deskripsi SIA-UC08, alur alternatif A1 berlaku: sistem menolak, tidak ada nilai yang tersimpan, pascakondisi gagal berlaku.

Situasi C — Admin Akademik menghapus data mahasiswa yang masih memiliki data akademik aktif.**
Menurut aturan tugas, SIA-UC13 hanya berlaku untuk mahasiswa tanpa data akademik aktif. Penghapusan tidak dilakukan, data mahasiswa tetap ada, dan hasilnya adalah pascakondisi gagal pada use case khusus tersebut.

Diagram dan deskripsi konsisten untuk ketiga situasi.
