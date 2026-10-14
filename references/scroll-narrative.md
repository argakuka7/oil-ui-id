# Narasi Scroll

## Animasi scroll landing page

Untuk landing page, halaman brand, halaman peluncuran produk, dan halaman pameran, animasi scroll diverifikasi bersama tiga animasi dasar dari [Animasi](motion.md); dokumen, artikel, alat, dan panel admin tidak memakai. Implementasinya dengan library animasi matang, lihat “Library animasi” di bawah.

**Wajib ada dua**: section di bawah layar pertama muncul sesuai kontennya; dan sedikitnya satu segmen narasi scroll-driven yang membuat protagonis berubah secara mencolok di dalam scroll. **Teknik dipilih sesuai halaman**: kedalaman layar pertama, wordmark menyusut ke navigasi, one-shot tanpa potongan, shot transisi antar-bab, latar berganti warna mengikuti bab, manifesto menyala kata demi kata — pilih yang paling cocok dari visual utama dan isi halaman, tuliskan ke storyboard beserta alasannya; jangan mengunci layar pertama untuk efek zoom di setiap halaman secara default.

### Kedalaman layar pertama (cocok untuk layar pertama dengan lapisan depan-belakang yang jelas)

Layar pertama adalah panggung yang dipatok diam, scroll langsung menggerakkan perubahan lapisan-lapisannya, scroll mundur memutar balik:

- Layar pertama mematok jarak scroll 100–200vh; layar sempit bisa dipangkas ke 80–120vh.
- Minimal dua lapisan berubah dengan kecepatan atau arah berbeda — misalnya latar depan mendekat dan latar belakang bergeser lambat, atau visual utama dan judul besar dibuka jarak skala-nya; lapisan latar bergerak paling lambat, lapisan depan paling cepat.
- Amplitudonya harus besar sampai terlihat sekali lihat di rekaman layar: skala lapisan utama tidak kurang dari 15%, atau perpindahan tidak kurang dari 15vh. Di bawah amplitudo itu, terlihat seperti halaman biasa yang sedang scroll.
- Judul besar adalah lapisan grafis: boleh di-zoom dan diberi paralaks; body text, tombol, dan form tidak di-zoom dan tidak diberi paralaks, tetap terbaca dan bisa diklik setelah dipatok.
- Status akhir harus menyerahkan kepada section berikutnya: visual utama menyusut ke posisi section berikutnya, judul mundur menjadi tekstur latar, atau gambar memberi jalan bagi protagonis section berikutnya. Jangan biarkan setelah dipatok selesai seluruh bidang langsung terdorong pergi.

Bila layar pertama adalah wordmark brand satu layar penuh, pakai “Wordmark menyusut ke navigasi” di bawah. Bila layar pertama berisi teks satu layar penuh jenis lain, antarmuka produk, atau tipografi murni, kedalaman belum tentu cocok; narasi scroll-driven bisa diletakkan di belakang.

### Wordmark menyusut ke navigasi (cocok untuk layar pertama berupa wordmark brand satu layar penuh)

Layar pertama adalah nama brand itu sendiri; saat scroll ia menyusut menjadi logo di dalam navbar. Satu elemen menyelesaikan sekaligus kerangka teks satu layar penuh dan satu segmen narasi scroll-driven; cocok untuk studio, brand, dan portofolio dengan nama brand pendek dan bentuk huruf berkarakter:

- Layar pertama hanya berisi wordmark itu, memenuhi lebar bidang konten, dan di layar sempit tetap satu baris penuh; di dalam navigasi tidak diletakkan logo kedua.
- Scroll-driven, melewati 60–100vh; wordmark menyusut menyusuri satu path ke posisi dan ukuran logo di navigasi, dan membesar kembali saat scroll mundur. Status akhirnya adalah logo di dalam navigasi; posisi dan ukurannya diukur dari navigasi yang sebenarnya, dan serah terimanya tanpa lompatan.
- Skala memakai transform elemen yang sama, bukan menganimasikan font-size; wordmark memakai SVG, atau font-size yang dihitung dari lebar wadah.
- Saat wordmark menyerahkan layar pertama, isi section berikutnya sudah masuk ke dalam gambar; jangan menyisakan satu layar kosong.
- Wordmark menyusut dari satu layar penuh menjadi logo navigasi adalah penyusutan protagonis yang mencolok plus satu serah terima, dan dihitung satu segmen narasi scroll-driven; halaman yang sama tidak lagi membuat kedalaman layar pertama.
- Saat reduce motion, wordmark tetap di layar pertama tanpa zoom, dan navigasi menampilkan logo sejak awal.

### Section muncul sesuai konten (wajib, scroll-triggered)

Setiap section di bawah layar pertama, begitu scroll mencapai posisinya muncul satu kali; scroll mundur tidak memutar ulang. Cara kemunculannya diturunkan dari isi dan material section itu, dan mengikuti intuisi fisika: yang berat jatuh lalu overshoot sebelum tenang, yang ringan punya hambatan udara, yang mekanis klik sampai tempatnya.

| Isi section | Cara kemunculan |
| --- | --- |
| Kartu, benda nyata, plang harga | Jatuh dengan bobot lalu tenang; amplitudo overshoot lihat “Feel” di [Animasi](motion.md); kartu berikutnya terseret keluar oleh yang sebelumnya |
| Daftar, timeline, langkah | Membuka satu per satu searah baca; garis penghubung digambar dulu, node menyusul jatuh ke tempatnya |
| Angka, metrik | Menggulir ke nilai target; digit tinggi berhenti dulu, digit akhir menyusul; yang tidak mulai dari 0 menggulir dari nilai aslinya |
| Garis, chart, path | Tergambar menyusuri arah data atau proses; saat ujungnya mendarat, zoom kecil sekali |
| Gambar, foto | Mask tersingkap dari arah subjek gambar; gambar bersamaan menyusut dari 1.08 ke 1 |
| Kertas, kain, label | Cepat lalu lambat, sedikit berputar sebelum lurus, seperti diletakkan ke atas meja |
| Logam, mesin, hardware | Sampai tempatnya dengan pendek, tanpa pantulan lunak; boleh disertai satu getaran kecil |
| Judul besar, slogan | Naik dari balik mask per kata atau per baris; letter-spacing menguncup dari sedikit renggang |

Aturan:
- Kemunculan tiap section dituliskan ke storyboard: section penting dirancang kemunculannya sendiri sesuai isinya; section biasa memakai ritme seragam yang restraint — jangan seluruh halaman dari atas ke bawah memakai satu fade-in naik.
- Kurva memakai spring atau inersia; parameter diambil dari tabel “Feel” di [Animasi](motion.md) sesuai material, bukan memakai ease default.
- Protagonis tiba dulu, sisanya terseret keluar dengan jeda 40–80ms; total durasi kemunculan satu section tidak lebih dari 900ms.

### Narasi scroll-driven (wajib sedikitnya satu segmen)

Bisa berupa kedalaman layar pertama, wordmark menyusut ke navigasi, atau satu segmen one-shot di pertengahan halaman; aturannya lihat bagian berikutnya. Protagonis wajib berubah secara mencolok di dalam scroll: zoom, bongkar, metamorfosis, menembus, atau bertitipan bentuk. Satu titik kecil bergerak menyusuri garis atau node menyala satu per satu hanya dihitung detail di dalam narasi utama, tidak bisa berdiri sebagai narasi utama.

### Storyboard

Sebelum mulai, tuliskan storyboard scroll di kolom “Animasi” kartu arah: teknik mana saja yang dipilih dan mengapa; tiap segmen memakan jarak scroll berapa, protagonisnya siapa, apa isi gambar tiap shot, apa yang bergerak, ke arah mana, dan kapan teks muncul. Bongkar dulu ritme scroll dua landing page top di kategori yang sama sebagai pembanding, tuliskan jelas apa yang bergerak di tiap segmen mereka, baru menulis milikmu sendiri.

## Paralaks dan one-shot

- **One-shot tanpa potongan.** Seluruh segmen adalah satu shot tanpa pemotongan. Satu protagonis berjalan dari awal sampai akhir — bisa produknya, satu garis, satu bentuk, atau satu huruf — di tiap langkah tumbuh, berubah, atau menyerahkan gambar berikutnya: mendekat untuk melihat detail, menjauh untuk melihat keseluruhan, berputar untuk melihat sisi belakang, menembus untuk memasuki scene berikutnya.
- **Protagonis dicari dari produk.** Protagonis adalah benda yang diproses produk ini, dan di dalam scroll ia menyelesaikan prosesnya sendiri. Bila tak menemukan protagonis yang hanya dimiliki produk ini, mundur ke teknik transisi di bawah; jangan memakai geometri melayang generik.
- **Berhenti dulu, baru bicara.** Tiap shot menyisakan satu jeda diam, dan teks muncul saat diam; membaca sambil bergerak itu melelahkan.
- **Paralaks butuh depan-belakang yang nyata.** Hanya dipakai bila gambar memang punya lapisan jauh-dekat: objek latar depan, latar tengah, latar belakang yang jauh; makin dekat makin banyak bergerak, dan bedanya kecil. Body text, tombol, dan form tidak diberi paralaks; judul besar sebagai lapisan grafis diperlakukan sesuai “Kedalaman layar pertama” di atas.
- **Transisi juga adalah shot.** Satu lingkaran mengembang dari satu titik membawa keluar section berikutnya; mendorong masuk ke satu gambar dan menembusnya menuju section berikutnya; warna latar berubah pelan mengikuti bacaan antar-bab; satu kalimat manifesto menyala kata demi kata mengikuti scroll. Tiap teknik hanya dipakai satu kali per halaman.
- **Sah juga saat scroll mundur.** Setiap frame hanya ditentukan oleh posisi scroll; mundur otomatis memutar balik, refresh atau lompat ke tengah pun langsung menampilkan gambar yang benar. Jangan mengambil alih scroll pengguna.
- **Sisakan pintu keluar.** Sebelum paragraf panjang, berikan pintu lewati; saat reduce motion, susun tiap frame diam menjadi section biasa berurutan.
- **Yang tak mampu dibuat kode, serahkan ke video.** Bila pengguna ingin animasi layar pertama yang kuat dan efeknya hanya bisa dicapai lewat video hasil generate atau frame sequence — misalnya karakter berbalik, produk dibongkar, kamera menembus scene — boleh menyarankan pengguna memakai [oil-motion](https://github.com/oil-oil/oil-motion). Yang bisa diselesaikan CSS, SVG, dan shader tetap dikerjakan sendiri; hanya disebut sekali per percakapan.

## Dua mode interaksi scroll

Perubahan yang dibawa scroll terbagi dua mode:

- **Scroll-driven.** Progres animasi terpetakan 1:1 dengan jarak scroll (scrub). Pengguna berhenti, animasi berhenti; scroll mundur, diputar balik. Kedalaman layar pertama, one-shot, pergantian sudut pandang 3D, dan dekonstruksi model hanya memakai scroll-driven; kecuali kedalaman layar pertama, one-shot paling banyak satu segmen per halaman.
- **Scroll-triggered.** Begitu elemen masuk threshold viewport, satu animasi independen dipicu dengan durasinya sendiri (misalnya kartu masuk, angka naik). Kapan selesainya diputuskan kode, tidak mengikuti scrollbar.
  - **Default satu arah sekali jalan (once).** Setelah terpicu gayanya terkunci; scroll naik tidak memutar ulang dan tidak me-reset, tidak membiarkan konten terbang masuk atau berkedip berulang di tengah bacaan.
  - **Reset saat keluar (reset on leave).** Hanya halaman pamer murni berirama kuat yang boleh me-reset setelah sepenuhnya keluar viewport; tidak memicu berulang di titik kritis viewport.

## Smooth scroll dan pemecahan layar penuh

- **Smooth scroll hanya mengurus mulusnya scroll, tidak dihitung animasi.** Library seperti Lenis dipakai untuk menghilangkan lompatan roda mouse per detent, sehingga animasi scroll-driven dan paralaks berjalan merata. Panel admin, dashboard, form, dan dokumen panjang tidak mengaktifkan smooth scroll global; pertahankan respons instan scroll native.
- **Hemat-hati dengan snap scroll.** Menyembunyikan scrollbar dan mengganti seluruh layar per sekali geser hanya cocok untuk galeri layar penuh dan sampul karya yang khusus; bisnis reguler dan teks panjang tidak memakai.

## Library animasi

Animasi scroll landing page wajib memakai library animasi matang; jangan menulis scroll listener dan perhitungan per frame sendiri:

- **Halaman tanpa framework**: GSAP; scroll memakai ScrollTrigger (`scrub` untuk scroll-driven, `once` untuk scroll-triggered, `pin` mematok panggung), judul besar dipecah per huruf memakai SplitText, elemen pindah posisi memakai Flip. Smooth scroll memakai Lenis dan disambungkan ke jam GSAP: `lenis.on('scroll', ScrollTrigger.update)`, `gsap.ticker.add((t) => lenis.raf(t * 1000))`, `gsap.ticker.lagSmoothing(0)`. GSAP dan plugin-nya bisa dipakai gratis.
- **Proyek React, Vue, dsb.**: lanjutkan library animasi yang sudah dipakai proyek (Motion, GSAP, dll.); bila belum ada, tambahkan GSAP, jangan menulis satu set sendiri.
- **Karya yang harus bisa dibuka offline**: taruh file library versi tetap ke direktori karya dan rujuk secara lokal, tanpa bergantung pada CDN.
- **Reduce motion**: pakai `gsap.matchMedia()` untuk memisahkan dua set: saat aktif, tidak ada pin dan tidak ada zoom, semua section langsung di posisinya, dan narasi utama disusun sebagai frame diam berurutan.
- Hanya animasikan transform, opacity, dan filter. Tinggi luar panggung yang dipatok adalah jarak scroll segmen itu; animasi off-screen dipause otomatis oleh library. Layar sempit boleh memangkas jarak dan amplitudo, tetapi teknik yang dipilih semua tetap dipertahankan.

## Periksa

Scroll dari atas ke bawah, lalu scroll kembali, lihat keduanya masing-masing sekali: apakah mundur memutar balik, apakah refresh di tengah menampilkan gambar yang benar, apakah teks muncul saat diam, apakah di layar sempit semua teknik yang dipilih masih ada, dan setelah “reduce motion” aktif apakah semua konten langsung terbaca.
