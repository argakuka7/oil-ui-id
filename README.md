Bahasa Indonesia · [English (upstream)](https://github.com/oil-oil/oil-ui#readme) · [中文 (upstream)](https://github.com/oil-oil/oil-ui/blob/main/README.zh-CN.md)

> **Catatan:** ini adalah terjemahan bahasa Indonesia tidak resmi dari [oil-ui](https://github.com/oil-oil/oil-ui) karya oil-oil (lisensi MIT). Semua kredit desain dan metodologi milik penulis asli. Untuk versi asli (Inggris/中文), rilis resmi, dan pembaruan, kunjungi repositori upstream. Bug terjemahan dilaporkan di repositori ini.

<p align="center">
  <img src="./assets/readme/hero.en.webp" width="100%" alt="oil-ui: dorong kemampuan desain UI AI hingga batasnya. Seseorang menyematkan pin kuning di tengah salah satu dari tiga pratinjau bergaya berbeda">
</p>

<p align="center">
  <a href="https://ui.oiloil.org/en/?utm_source=github&utm_medium=referral&utm_campaign=readme-id"><img src="./assets/readme/showcase.en.webp" width="100%" alt="Sorotan galeri: aplikasi belajar bahasa Inggris, rekap tahunan musik, situs hardware dan component library, alat manajemen proyek, aplikasi ride-hailing, asisten suara, alur checkout, dan kamera film"></a>
</p>

Oil UI adalah Skill desain antarmuka untuk AI agent. Ia mengeksplorasi beberapa arah desain yang benar-benar berbeda secara berdampingan, membiarkanmu memilih satu, lalu memolesnya berdasarkan screenshot nyata. Berlaku untuk website, aplikasi, dashboard, dan komponen. Lihat lebih banyak contoh hasil di [ui.oiloil.org](https://ui.oiloil.org/en/?utm_source=github&utm_medium=referral&utm_campaign=readme-id).

## Cara ia mendesain

1. **Pahami dulu ini produk apa.** Sebelum menggambar apa pun, ia menyebutkan kategori produknya, mencari dua-tiga pembanding terbaik dengan gaya paling khas, dan menelaah apa yang mereka lakukan serta mengapa. Setelah itu ia memutuskan apa yang diikuti dan apa yang diganti.
2. **Menerjemahkan “premium” dan “bersih” menjadi keputusan konkret.** Semua orang memakai kata-kata itu, tetapi kata-kata itu tidak mengatakan apa yang harus diletakkan di layar. Ia menetapkan tone lebih dulu dari subjek, audiens, dan suara brand — misalnya meriah atau tenang, kilauan atau kasar, padat atau lapang — lalu menerjemahkan tone itu menjadi pilihan yang terlihat: font apa, berapa banyak ruang kosong, dan seberapa luas halaman yang diberi warna.
3. **Tiap arah berangkat dari sesuatu yang konkret.** Bisa berupa satu material dalam lingkungannya, satu adegan, satu karakter, atau bahasa visual bidang lain. Idenya lahir dari produk itu sendiri, bukan dari kata sifat seperti “minimalis” atau “berani”.
4. **Putuskan untuk siapa layar pertama dibuat.** Pada halaman tempat orang menjelajah, berbelanja, atau bekerja, layar pertama adalah kontennya sendiri. Hanya halaman yang bertugas meyakinkan yang butuh tata letak pembuka yang dirancang — ditetapkan sebelum copy ditulis.
5. **Arah-arahnya harus benar-benar berbeda.** Dari layout, tipografi, warna, dan gambar kunci, dua arah apa pun boleh berbagi paling banyak satu kesamaan. Setelah pratinjau jadi, ia menyandingkannya dan menyipitkan mata melihat sebaran terang-gelap tiap layar pertama. Bila dua di antaranya terlihat mirip, layoutnya yang diubah — bukan sekadar bertukar warna.
6. **Menyisakan satu momen yang diingat orang.** Alih-alih mendorong semua bagian halaman, ia membuat satu-dua detail menjadi luar biasa — misalnya respons sebuah tap, momen pembayaran sukses, AI yang terlihat sedang bekerja, atau halaman 404. Sisanya tetap tenang.
7. **Kamu yang memutuskan mana yang terlihat benar.** Pratinjau diletakkan di satu halaman perbandingan. Kamu memilih satu dan menyebutkan apa yang disukai dan tidak, lalu ia menguncup desainnya mengikuti masukanmu sebelum lanjut.
8. **Percaya layar yang nyata.** Setelah halaman selesai, ia membukanya pada ukuran desktop dan ponsel lalu memeriksa screenshot-nya. Kamu juga bisa melibatkan reviewer yang belum melihat proses pembuatannya. Terakhir, satu ronde pengurangan: satu titik fokus per halaman, tanpa copy, garis, atau kotak yang tidak membantu pemahaman.

Untuk antarmuka yang lebih fungsional, redesain proyek existing, atau efek seperti jejak cahaya dan pola titik, lihat [Oil UI Pro](https://ui.oiloil.org/en/pro/?utm_source=github&utm_medium=referral&utm_campaign=readme-id). Perbedaannya didaftarkan [di bawah](#open-source-dan-pro).

## Instalasi

Kirim ini ke agent yang bisa memasang Skill:

```text
Pasang Skill ini untuk saya: https://github.com/argakuka7/oil-ui-id
```

Atau jalankan di terminal:

```bash
npx skills add argakuka7/oil-ui-id
```

Langsung bisa dipakai setelah terpasang, tanpa konfigurasi apa pun. Bila versi upstream terbit rilis baru, pembaruan terjemahan mengikuti repositori ini — lihat bagian [Pemeriksaan versi](#pemeriksaan-versi). Bila kamu sudah punya Oil UI Pro, versi open source ini tidak perlu dipasang; memasang keduanya membuat keduanya berebut permintaan yang sama.

## Pemakaian

Sampaikan kebutuhanmu langsung ke agent, misalnya:

- “Pakai oil-ui untuk mengeksplorasi beberapa arah desain produk booking kursus ini, lalu buat halaman yang bisa saya pratinjau.”
- “Buat tiga desain dengan tipografi, warna, dan komposisi berbeda. Taruh di satu halaman perbandingan supaya saya bisa memilih.”
- “Poles halaman ini mengikuti pedoman desain yang sudah ada di proyek.”
- “Review saja homepage ini, jelaskan apa yang harus diubah dan bagaimana. Jangan sentuh file-nya.”
- “Rekonstruksi halaman ini dari screenshot, dan tambahkan juga layout ponselnya.”

Sertakan aset brand, screenshot, atau proyek existing kalau ada. Ia bisa mulai tanpa referensi dan hanya bertanya saat deliverable-nya belum jelas.

## Halaman perbandingan gaya bawaan

<p align="center">
  <img src="./assets/readme/proof-mona-lisa.webp" width="100%" alt="Halaman perbandingan gaya: tiga arah untuk halaman pameran Mona Lisa yang sama, berjudul Thirty Centimeters, Extra! 1911, dan Sfumato">
</p>

Saat kamu ingin membandingkan desain, ia menyandingkannya berdampingan di satu halaman. Yang disandingkan bisa file HTML, gambar, atau halaman dev yang sedang berjalan, dan versi saat ini bisa diletakkan lebih dulu sebagai baseline. Kamu bisa berganti ukuran desktop/ponsel, membuka tiap kandidat pada ukuran asli, dan menjelajah dengan tombol panah. Tekan “Pilih” pada yang kamu sukai, tempel kalimat yang tersalin ke agent, dan ia melanjutkan dari situ.

## Open source dan Pro

<p align="center">
  <img src="./assets/readme/proof-van-gogh.webp" width="100%" alt="Halaman perbandingan gaya versi lengkap: tiga arah untuk halaman pameran Van Gogh, berjudul To Theo, Brushstrokes, dan East Window">
</p>

Versi open source membawa halaman baru dari nol sampai menjadi desain yang bagus. Pro dibangun di atasnya: membuat antarmuka lebih mudah dipakai, memperbaiki proyek existing, dan menaikkan standar kualitas lewat review serta polesan yang lebih ketat.

| | Oil UI (open source) | Oil UI Pro |
| --- | :---: | :---: |
| Arah desain: kategori produk, tone, arah yang berbeda, halaman perbandingan | ✓ | ✓ |
| Visual: hierarki, tipografi, warna, jarak, gambar, dan animasi | ✓ | ✓ |
| Momen yang membekas dan narasi scroll (paralaks, one-shot) | ✓ | ✓ |
| Rekonstruksi dari screenshot | ✓ | ✓ |
| Ritme pertunjukan, feel, aset hasil generate, dan 3D real-time untuk mini-game | ✓ | ✓ |
| Review independen | Berskor, dengan daftar masalah | Review dan revisi berulang menargetkan 9/10; memeriksa tumpang tindih antar arah; menguji halaman dengan tugas nyata |
| Polesan: pemeriksaan default estetika AI, checklist detail, cara melakukan pengurangan | | ✓ |
| Kegunaan: interaksi dan status, form, dialog dan popover, layout desktop dan ponsel | | ✓ |
| Dashboard dan alat: layout workspace yang dipilih untuk produknya, dengan satu gaya menyeluruh | | ✓ |
| Proyek existing: pendekatan terpisah untuk refresh UI, perbaikan alur, dan fitur baru | Memberitahumu yang mana yang dibutuhkan | ✓ |
| Memoles satu komponen sampai tuntas | | ✓ |
| 19 prototipe kartu dengan kode dan wadah ruang yang bisa melipat-membentang | | ✓ |
| Efek seperti jejak cahaya, pola titik, dan gradasi mengalir | | ✓ |
| Layout scene, visual, dan pemeriksaan status untuk mini-game | | ✓ |

Oil UI Pro seharga $9.99: sekali beli, pembaruan seumur hidup. Beli di [ui.oiloil.org/pro](https://ui.oiloil.org/en/pro/?utm_source=github&utm_medium=referral&utm_campaign=readme-id).

## Pemeriksaan versi

Setiap kali dipakai, Skill memeriksa versi lebih baru, paling sering sekali tiap 10 menit sekali online. Ia hanya membaca daftar versi publik di ui.oiloil.org dan tidak mengunggah apa pun dari proyekmu. Perlu dicatat: Skill ini adalah terjemahan, dan mekanisme pembaruan bawaan akan mengganti Skill dengan **versi asli upstream (bukan terjemahan)** — jangan jalankan perintah pembaruan bila kamu ingin mempertahankan versi Indonesia. Untuk memperbarui terjemahan, ambil rilis terbaru dari repositori ini. Hasil pemeriksaan di-cache di `~/.local/state/oil/` (atau `XDG_STATE_HOME` bila diset; `%LOCALAPPDATA%\oil\` di Windows). Butuh Python 3. Set `OIL_NO_UPDATE_CHECK=1` untuk mematikannya.

## Dipakai bersama

- [oil-motion](https://github.com/oil-oil/oil-motion): mengubah video hasil generate atau rangkaian frame menjadi animasi web yang dikendalikan scroll atau drag, misalnya bongkar produk atau terowongan kamera. Pakai untuk animasi pembuka yang kuat.
- [oil-tone](https://github.com/oil-oil/oil-tone): menulis ulang judul, deskripsi, dan copy pengantar agar terbaca natural dan jelas. Pakai saat copy terasa tulisan mesin atau janggal.

## Lisensi

[MIT](LICENSE) — © oil-oil. Terjemahan bahasa Indonesia disediakan dengan lisensi yang sama.
