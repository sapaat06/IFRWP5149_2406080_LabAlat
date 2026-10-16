
## SIA-UC01 — Ajukan KRS

| Elemen | SIA-UC01 — Ajukan KRS |

| Tujuan | Menghasilkan pengajuan KRS yang tersimpan |
| Aktor utama | Mahasiswa |
| Sumber kebutuhan | SIA-R03 dan SIA-R05 |
| Pemicu | Mahasiswa memilih fungsi pengajuan KRS |
| Prasyarat | Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal tersedia |
| Pascakondisi berhasil | Pengajuan KRS tersimpan dengan status Menunggu persetujuan dosen wali |
| Pascakondisi gagal | Tidak ada pengajuan KRS baru yang berhasil tersimpan |
| Include | SIA-UC02 — Validasi KRS |
| Extension point | Bukti pengajuan tersedia, pada langkah 6 |
| Extend | SIA-UC03 jika [mahasiswa memilih unduh] |

## SIA-UC02 — Validasi KRS

| Elemen | SIA-UC02 — Validasi KRS |
|---|---|
| Tujuan | Menentukan apakah pilihan mata kuliah layak disimpan sebagai pengajuan |
| Aktor utama | Mahasiswa (melalui SIA-UC01) |
| Sumber kebutuhan | SIA-R04 |
| Pemicu | SIA-UC01 mencapai langkah 4 |
| Prasyarat | Pengajuan diterima; data mata kuliah, prasyarat, dan jadwal tersedia |
| Pascakondisi berhasil | Hasil validasi Berhasil, diserahkan ke SIA-UC01 |
| Pascakondisi gagal | Hasil validasi Gagal beserta daftar temuan; tidak ada data tersimpan |

## SIA-UC03 — Unduh bukti pengajuan KRS

| Elemen | SIA-UC03 — Unduh bukti pengajuan KRS |
|---|---|
| Tujuan | Mahasiswa memperoleh bukti pengajuan KRS yang dapat disimpan |
| Aktor utama | Mahasiswa |
| Sumber kebutuhan | SIA-R05 |
| Pemicu | Pada konfirmasi pengajuan, mahasiswa memilih unduh bukti |
| Prasyarat | SIA-UC01 telah menyimpan pengajuan dan mencapai extension point Bukti pengajuan tersedia |
| Pascakondisi berhasil | Mahasiswa memperoleh berkas bukti; pengajuan tetap tersimpan, status tidak berubah |
| Pascakondisi gagal | Tidak ada berkas bukti; pengajuan tetap tersimpan, status tidak berubah |
| Extend | Memperluas SIA-UC01 pada extension point Bukti pengajuan tersedia, jika [mahasiswa memilih unduh] |

## SIA-UC04 — Proses keputusan KRS

| Elemen | SIA-UC04 — Proses keputusan KRS |
|---|---|
| Tujuan | Menetapkan KRS yang diajukan menjadi disetujui atau ditolak, disertai catatan |
| Aktor utama | Dosen wali |
| Sumber kebutuhan | SIA-R06 |
| Pemicu | Dosen wali memilih memproses KRS yang menunggu keputusan |
| Prasyarat | Dosen wali telah terautentikasi dan berhak atas KRS tersebut; ada KRS berstatus Menunggu persetujuan dosen wali |
| Pascakondisi berhasil | KRS berstatus Disetujui atau Ditolak, dengan keputusan dan catatan tersimpan |
| Pascakondisi gagal | Status KRS tetap Menunggu persetujuan dosen wali; tidak ada keputusan tersimpan |

## SIA-UC05 — Kelola jadwal kuliah

| Elemen | SIA-UC05 — Kelola jadwal kuliah |
|---|---|
| Tujuan | Data jadwal kuliah tersedia dan terkini |
| Aktor utama | Admin akademik |
| Sumber kebutuhan | SIA-R02 |
| Pemicu | Admin akademik memilih fungsi kelola jadwal kuliah |
| Prasyarat | Admin akademik telah terautentikasi; data mata kuliah tersedia |
| Pascakondisi berhasil | Perubahan jadwal tersimpan |
| Pascakondisi gagal | Data jadwal tidak berubah |
