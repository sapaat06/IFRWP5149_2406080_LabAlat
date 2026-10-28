### Situasi A — Mahasiswa melihat kalender akademik tanpa hubungan langsung dengan use case

Berdasarkan diagram, situasi ini diperbolehkan. Mahasiswa tetap dapat menjalankan SIA-UC07 meskipun tidak memiliki garis asosiasi langsung dengan use case tersebut.

Hal ini karena Mahasiswa merupakan turunan dari aktor Civitas Akademika melalui relasi generalisasi. Mengacu pada UML 2.5.1 dari OMG, aktor khusus dapat mewarisi kemampuan interaksi aktor umum. Dengan demikian, Mahasiswa mewarisi akses ke SIA-UC07 melalui Civitas Akademika tanpa perlu menggambar ulang garis asosiasi untuk Mahasiswa maupun Dosen.

### Situasi B — Dosen yang bukan pengampu mencoba menginput nilai

Sistem harus menolak permintaan tersebut. Pada langkah kedua alur utama SIA-UC08, sistem memeriksa apakah dosen merupakan pengampu mata kuliah yang dipilih. Jika syarat tidak terpenuhi, alur alternatif A1 dijalankan. Sistem menampilkan pesan penolakan, tidak membuka formulir input nilai, dan tidak menyimpan nilai apa pun.

Aturan ini didasarkan pada prasyarat SIA-UC08, kebutuhan SIA-R08 mengenai penginputan nilai untuk mata kuliah yang diampu, serta batasan dalam dokumen kebutuhan. Asosiasi Dosen dengan SIA-UC08 menunjukkan bahwa dosen dapat menggunakan fitur input nilai, sedangkan hak input untuk mata kuliah tertentu ditentukan oleh alur use case.

### Situasi C — Admin Akademik menghapus data siswa yang masih memiliki data akademik aktif

Sistem harus menolak penghapusan data siswa tersebut. Alur alternatif SIA-UC13 dijalankan dengan menampilkan alasan bahwa siswa masih memiliki data akademik aktif. Data siswa tetap tersimpan dan tidak mengalami perubahan.

Ketentuan ini mengacu pada SIA-UC13, yang membatasi penghapusan data hanya untuk siswa yang tidak memiliki data akademik aktif, serta aturan dalam dokumen kebutuhan. Admin Akademik tetap memiliki hak untuk menjalankan SIA-UC13 melalui asosiasi dengan use case umum SIA-UC10. Namun, pelaksanaan penghapusan ditolak karena kondisi data tidak memenuhi persyaratan.