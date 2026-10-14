# Alat

Program bawaan direktori ini tidak perlu dibaca source-nya. Di sini hanya dituliskan kapan dipakai dan beberapa perintah yang paling sering; seluruh opsi, cara menulis aksi, dan file output lihat `--help` masing-masing, dan bila salah tulis, pesan errornya memberikan cara penulisan yang bisa langsung disalin.

Bila host punya alat browser sendiri, melihat halaman dan menelusuri alur tetap memakainya seperti biasa. Saat harus menyerahkan bukti, utamakan alat screenshot di sini: ia membuka browser sementara yang terpisah dan tidak menyentuh data browser milik pengguna. Bila mesin lokal tidak punya Node 22, atau tidak ada Chrome, Chromium, atau Edge, mundur ke alat host dan serahkan bukti yang sama. Bila tugas atau proyek sudah menetapkan alat screenshot, ikuti itu.

## Screenshot dan rekaman layar

### Kapan screenshot, berapa banyak

Screenshot ada dua kegunaan, jangan dicampur:

- **Sekali lihat**: setelah satu batch perubahan selesai, ingin melihat hasilnya. Screenshot layar yang terlihat saja, satu perintah. Kumpulkan dulu satu batch perubahan baru screenshot; bila halaman tidak berubah, jangan screenshot ulang.
- **Pengambilan bukti**: dengan `--evidence`, ambil sekaligus gambar status, gambar berdampingan, versi tanpa teks, gambar 2×, dan rekaman layar. Hanya pada dua saat: sebelum dikirim ke review, dan sebelum penyerahan. Ronde layar pertama arah: tiap arah cukup satu screenshot, tanpa pengambilan bukti.

Tiap ronde review hanya mengambil ulang bukti yang terdampak perubahan ronde itu. Status dan animasi yang tidak disentuh, lanjutkan file ronde sebelumnya dan catat mana yang diwarisi saat serah terima; bila tak yakin terdampak atau tidak — misalnya style bersama ikut berubah — ambil ulang butir itu.

### Perintah umum

```text
node <skill>/scripts/shoot.mjs <alamat halaman atau file HTML> [opsi]
```

| Butuh apa | Tambahkan |
| --- | --- |
| Sekali lihat tampilan desktop | `--size desktop`; tanpa opsi, default ponsel 390x844 |
| Beroperasi beberapa langkah baru screenshot | `--steps "click .open; wait 300"` |
| Ambil bukti sebelum review atau penyerahan | `--evidence --states idle,done --steps "send: click .send"` |
| Landing page, rekam scroll dari atas ke bawah | `--record --steps "scroll 600; scroll 600; scroll 600"`, tambahkan langkah sesuai panjang halaman |
| Rekonstruksi screenshot: bandingkan dengan referensi | `--compare referensi.png --size <ukuran logis referensi>` |
| Menunjukkan masalah ke pengguna: kotak dan nomor pada elemen | `--mark "1=.page-head .btn; 2=.toggle-row" --full` |

Status dimasuki lewat parameter alamat, jadi halaman harus bisa membuka tiap status lewat `?state=<nama>`. Sisa opsi, cara menulis selector dan aksi, file output, dan struktur `report.json`: jalankan `node <skill>/scripts/shoot.mjs --help`. Bila ragu dengan cara penulisannya, tambahkan `--dry-run` dulu untuk memeriksa tanpa membuka browser. Saat banyak tugas berjalan bersamaan dan screenshot timeout, tambahkan `--timeout-scale 2`.

### Membaca hasil

Sebelum diserahkan ke reviewer, lihat sendiri dulu: apakah status default sudah selesai dimuat, dan apakah versi tanpa teks ikut menutupi grafis. Bila buktinya salah, screenshot ulang dulu baru serahkan ke reviewer. Bila ringkasannya menandai rekaman layar dan screenshot tidak konsisten, status akhir statis mengikuti screenshot, lalu rekam ulang segmen itu untuk memeriksa transisinya. Screenshot WebGL yang kosong tidak boleh dijadikan bukti.

Tiap screenshot juga diperiksa terhadap satu set masalah yang bisa dinilai langsung dari style halaman, dan tampil sebagai “peringatan default practices” di output perintah:

- **Masalah keterbacaan yang wajib diubah**: kontras teks tidak memenuhi ambang, body text di bawah 13px, line-height body multi-baris terlalu rapat, konten yang tertahan pada status transparan di layar pertama.
- **Ubah atau tuliskan alasannya**: teks abu di atas latar berwarna, baris body terlalu panjang, serta default model: eyebrow label dan label nomor di atas judul, garis sisi warna tunggal, teks gradasi, kartu di dalam kartu, emoji sebagai ikon, label kapital Latin di antarmuka non-Latin, dan judul yang jaraknya ke paragraf atas lebih dekat daripada ke paragraf bawah. Butir yang dipertahankan, tuliskan di catatan penyerahan bagaimana ia melayani arah.

Pemeriksaan bisa false positive — misalnya nomor langkah yang nyata atau label yang memang perlu; false positive dicatat satu kalimat di catatan penyerahan. Ia hanya mengenali pola tulisan, tidak bisa menilai bagus-tidaknya: setelah peringatan nol, tetap harus melihat screenshot sendiri. Bila pemeriksaan melaporkan error 401/404 API dan semacamnya yang tak berhubungan dengan tampilan, catat satu baris di catatan penyerahan; jangan mengubah kode bisnis seperti login atau API demi lolos pemeriksaan.

## Menulis mockup interaktif

Layar pertama pada tahap eksplorasi arah tidak membuat interaksi, bagian ini tidak terpakai; gunakan setelah arah terpilih saat mengerjakan halaman lengkap. Proyek existing mengikuti tech stack proyeknya sendiri.

Satu komponen atau satu halaman hanya satu file, status diganti lewat parameter alamat; jangan menggandakan file untuk tiap status. Kunci dulu warna, ukuran font, jarak, dan radius ke belasan CSS variable, dan setelahnya selalu rujuk variable; jangan memasukkan alat yang butuh build. Status seperti form, toggle, dan expand ditulis dengan Alpine.js pada atribut HTML: salin `<skill>/assets/vendor/alpine.min.js` ke `vendor/` di direktori tugas lalu rujuk, kumpulkan status dalam satu `x-data`, dan status awal dibaca dari parameter alamat. Gesture ikut tangan, simulasi fisika, dan gambar Canvas/WebGL diletakkan di modul JS terpisah; data yang diperbarui tiap frame tidak dimasukkan ke status Alpine.
