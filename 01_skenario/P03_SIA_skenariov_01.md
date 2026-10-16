Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan. Admin Mengelola Jadwal Kuliah. 

| ID      | Kebutuhan tugas                                                           |
| ------- | ------------------------------------------------------------------------- |
| SIA-R01 | Admin akademik dapat mengelola jadwal kuliah                              |
| SIA-R02 | Mahasiswa dapat mengajukan KRS                                            |
| SIA-R03 | Sistem memvalidasi KRS sebagai bagian pengajuan                           |
| SIA-R04 | Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
| SIA-R05 | Dosen wali dapat memproses persetujuan atau penolakan KRS                 |

Batas dan asumsi: 
• Pengguna telah terautentikasi. 
• Data mata kuliah, prasyarat, dan jadwal tersedia. 
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan. 
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan. 
• KRS tersimpan belum berarti disetujui. 
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas. 

| Aktor          | Tujuan terhadap sistem                                    |
| -------------- | --------------------------------------------------------- |
| Mahasiswa      | Mengajukan KRS dan mengunduh bukti pengajuan              |
| Dosen Wali     | Menyetujui atau menolak KRS dan memberi catatan keputusan |
| Admin Akademik | Mengelola Jadwal kuliah                                   |

| ID       | Nama use case             | Peran dalam model                                                  |
| -------- | ------------------------- | ------------------------------------------------------------------ |
| SIA-UC01 | Ajukan KRS                | Fungsi utama mahasiswa                                             |
| SIA-UC02 | Validasi KRS              | Perilaku yang disertakan UC01                                      |
| SIA-UC03 | Unduh bukti pengajuan KRS | Tambahan bersyarat pada UC01                                       |
| SIA-UC04 | Proses keputusan KRS      | kFungsi utama dosen wali                                           |
| SIA-UC05 | Kelola jadwal kuliah      | Fungsi utama admin akademik; berdiri sendiri, tanpa include/extend |


Relasi include
SIA-UC01 «include» SIA-UC02
Sumber: Ajukan KRS.
Tujuan: Validasi KRS.
Arah panah: dari Ajukan KRS ke Validasi KRS, garis putus-putus berkepala terbuka, label <<include>>.
Alasan: skenario menyatakan setiap pengajuan menjalankan validasi (SIA-R04), jadi validasi adalah bagian pelaksanaan pengajuan. Validasi dapat berhasil atau gagal; gagal tidak berarti opsional. Autentikasi tidak dibuat include, tetapi dicatat sebagai prasyarat.

Relasi extend
SIA-UC03 «extend» SIA-UC01
Use case dasar: Ajukan KRS (SIA-UC01).
Use case tambahan: Unduh bukti pengajuan KRS (SIA-UC03).
Arah panah: dari Unduh bukti ke Ajukan KRS, garis putus-putus berkepala terbuka, label <<extend>>.
Extension point: Bukti pengajuan tersedia, pada langkah 6 SIA-UC01 (saat konfirmasi pengajuan tampil).
Kondisi: [mahasiswa memilih unduh].
Alasan: pengajuan tetap berhasil tersimpan tanpa unduh bukti (SIA-R05). Ajukan KRS tetap bermakna tanpa perilaku tambahan ini.