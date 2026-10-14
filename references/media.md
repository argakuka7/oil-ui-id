# Aset

Dari mana gambar berasal, memikul apa, dan bagaimana menyatunya dengan halaman. Untuk karakter, properti, koleksi, dan sprite sheet yang dibutuhkan produk game, koleksi, dan petualangan, lihat “Aset set”.

## Navigasi isi

- [Tentukan dulu apa yang dipikul gambar](#tentukan-dulu-apa-yang-dipikul-gambar)
- [Pakai ulang, hasilkan, atau serahkan ke kode](#pakai-ulang-hasilkan-atau-serahkan-ke-kode)
- [Biarkan gambar memikul makna](#biarkan-gambar-memikul-makna)
- [Menulis prompt](#menulis-prompt)
- [Setelah dihasilkan, dinilai di dalam halaman](#setelah-dihasilkan-dinilai-di-dalam-halaman)
- [Menyatukan gambar dengan halaman](#menyatukan-gambar-dengan-halaman)
- [Satu lukisan sebagai panggung](#satu-lukisan-sebagai-panggung)
- [Unifikasi monokrom aset heterogen](#unifikasi-monokrom-aset-heterogen)
- [Penurunan visual utama untuk teknologi abstrak](#penurunan-visual-utama-untuk-teknologi-abstrak)
- [Aset set: karakter, properti, dan sprite sheet](#aset-set-karakter-properti-dan-sprite-sheet)
- [3D real-time](#3d-real-time)
- [Jalur opsional video hasil generate](#jalur-opsional-video-hasil-generate)
- [File dan keterangan](#file-dan-keterangan)

## Tentukan dulu apa yang dipikul gambar

Aset adalah titik awal desain, bukan dekorasi yang diisi setelah layout selesai. Tanyakan dulu: bila hanya boleh menyisakan satu gambar, satu judul, dan satu aksi, gambar mana yang layak menempati posisi itu? Baru setelah itu putuskan apakah perlu modul tambahan.

- **Bedakan dari mana gap berasal.** Apakah persoalannya informasi dan komposisi, atau memang kekurangan satu gambar yang mampu mengekspresikan produk dan brand-nya. Jangan menutupi masalah hierarki dengan lebih banyak gambar, efek cahaya, dan animasi; juga jangan mengganti gambar yang wajib ada dengan gradasi generik dan bentuk geometris hanya karena lebih mudah dikodekan.
- **Berikan satu kalimat tugas untuk tiap gambar.** Ia memamerkan objek, menjelaskan hubungan, atau membangun brand dan emosi; apa yang harus langsung dipahami orang dari situ. Bila tidak bisa dijawab, tunda mencari gambar dan jangan meng-generate. Yang sudah dijelaskan gambar, tidak diulang oleh teks.
- **Panel admin dan alat juga perlu penilaian ini.** Thumbnail objek membantu pengenalan, sampul konten mendukung penjelajahan, peta atau gambar ruang membantu orientasi, dan diagram menjelaskan hubungan; semuanya bisa jadi bagian antarmuka yang paling bernilai. Bila tugasnya memang murni data dan tidak terbantu, pertahankan penyajian data yang jelas tanpa memaksakan gambar suasana.
- **Gambar mengikuti North Star, lalu halaman menyambut gambar.** Subjek, sudut pandang, skala, cahaya, warna, material, dan ruang kosong ditentukan North Star desain; font, latar, perlakuan tepi, dan gerak halaman membangun keterhubungan dari gambar ini, dan boleh memakai satu kontras terkendali untuk menonjolkan aksi utama. Gambar-gambar dalam satu kelompok menyatukan skala subjek, sudut pandang, cahaya, dan tekstur tepi — bukan menyamakan semua gambar dengan satu filter.
- **Gambar adalah struktur, bukan ilustrasi yang dikurung kotak.** Biarkan ia melintasi batas bidang, memenuhi layar pertama, atau bertumpuk dengan teks; caranya lihat “Menyatukan gambar dengan halaman”.
- **Masukkan dulu ke halaman nyata untuk ditinjau satu putaran, baru kembangkan ke area lain.** Bila aset belum tersedia, review estetika versi placeholder tidak dihitung lolos akhir.

## Pakai ulang, hasilkan, atau serahkan ke kode

- **Bila ada yang cocok, pakai ulang.** Lihat dulu gambarnya secara nyata baru mengutip karakteristiknya; bila sudah ada aset yang bagus, desain di sekelilingnya — jangan meng-generate ulang sekadar untuk membuktikan memakai alat.
- **Bila tidak ada, buat.** Bila tidak ada aset yang cocok dan host mampu menghasilkan gambar, buat aset kuncinya secara proaktif; jangan melewati langkah ini hanya karena sedang menulis kode frontend. Ikuti aturan input dan edit milik alat generate host masing-masing.
- **Teks dan antarmuka diserahkan ke kode.** Teks, tombol, form, label data, dan layout reguler seluruhnya ditata dengan HTML/CSS nyata; jangan digambar oleh model gambar, dan jangan menjadikan screenshot utuh sebagai produk interaktif: gambar yang berisi teks mudah salah, tak bisa diubah, tak bisa diseleksi, dan tak terbaca screen reader. Gambar hanya bertugas untuk benda, material, serta cahaya-bayangan.
- **Bila tak mampu, tinggalkan brief.** Bila tidak ada kemampuan generate atau gambarnya memang belum ada, sisakan wadah yang ukurannya tepat dan tulis brief aset yang bisa dieksekusi: mau mengekspresikan apa, subjeknya apa, diletakkan di mana, bagaimana crop di layar lebar-sempit, di mana area penampung teks, dan detail apa yang tidak boleh hilang. Jangan memasang alat sendiri, berpindah ke layanan berbayar, atau meminta pengguna menempelkan API key ke dalam percakapan.
- Objek yang perlu diputar, punya fisika, atau berubah mengikuti sudut pandang lihat “3D real-time”; perubahan kontinu yang sudah tertentu sebelumnya lihat “Jalur opsional video hasil generate”.

## Biarkan gambar memikul makna

Kegagalan paling umum pada gambar hasil generate bukan gambar yang jelek, melainkan gambar yang terlalu penuh: makin kaya detail makin mirip foto stok, dan setelah masuk layout tak ada lagi titik fokusnya — pun tak berhubungan dengan halaman.

“Pemandangan cantik” yang tak berhubungan dengan produk justru mencuri perhatian begitu masuk layout; setiap tempat penuh detail berarti tidak ada yang jadi fokus. Saat menggambar benda nyata atau adegan nyata, kerjakan tekstur dan cahaya subjeknya sampai tuntas, dan biarkan latar serta area penampung teks tetap bersih; saat menggambar fungsi abstrak atau perubahan before-after, bidang luas boleh dipipihkan menjadi monokrom, model polos, atau out of focus, dan hanya beberapa titik kunci itu yang dibiarkan memancarkan warna, cahaya, atau detail.

Pilih subjek yang bisa “tersambung” dengan halaman:

- Satu benda tunggal yang bisa melintasi batas dua bidang warna.
- Benda memanjang yang bisa menjulur keluar dari bingkai.
- Ruang yang bisa diberi anotasi: model, peta, potongan, denah.

Subjek seperti ini kelak bisa menyatu dengan garis, anotasi, dan section milik halaman; foto lanskap yang berdiri sendiri tidak mampu melakukannya.

## Menulis prompt

Tulis dengan urutan tetap, tiap bagian satu-dua kalimat:

1. **Subjek dan bentuk ekspresi**: benda apa, disajikan dalam genre apa (foto, ilustrasi, model, atau diagram); genre diturunkan dari arah halaman.
2. **Komposisi dan ruang kosong**: posisi dan porsi subjek di dalam bingkai, serta bidang mana yang dikosongkan untuk teks. Tuliskan area dan porsi subjek sesuai kerangka layar pertama yang sudah dipilih, dan pastikan bidang untuk teks benar-benar bersih. Area ruang kosong jangan berisi highlight, pantulan, atau tekstur berantakan agar teksnya jelas terbaca.
3. **Jarak aman**: subjek, alas, dan bayangan jangan menempel ke tepi teks; sisakan sekitar 10% celah agar teks tidak menindih benda saat layar menyempit.
4. **Latar**: tuliskan langsung nilai hex yang benar-benar dipakai halaman, atau minta latar transparan murni. Bila nilai warnanya sama, tepi gambar menyatu natural ke halaman tanpa perlu CSS mask tambahan.
5. **Material dan cahaya**: arah cahaya utama, cahaya bantu, tekstur. Beberapa gambar dalam satu halaman memakai arah cahaya yang sama. Pantulan lantai meredup natural ke arah ruang kosong, tidak menyapu ke area teks.
6. **Exclusion**: jangan ada teks, logo, pseudo-code, screenshot antarmuka, atau benda melayang berlebih; untuk ikon kecil atau gambar transparan, tuliskan “tanpa bayangan jatuh di lantai” — bayangan luar diserahkan ke CSS `filter: drop-shadow(...)` di frontend.

## Setelah dihasilkan, dinilai di dalam halaman

Lihat di halaman nyata dengan ukuran nyata, bukan dinilai di image viewer. Gambar yang bagus ketika dilihat sendiri, setelah masuk layout sering kali subjeknya terlalu penuh, arah hadapnya salah, atau ruang kosongnya ada di posisi yang keliru.

Bila kurang pas, perbaiki prompt dan generate ulang dengan tertulis apa yang harus diubah, misalnya “geser subjek ke kanan, sisakan setengah ruang di kiri” atau “hilangkan pantulan lantai, ganti latar dengan warna hex halaman”. Jangan memutar layout mengikuti satu gambar yang tidak cocok. Dari satu batch, pilih yang paling mudah ditata, bukan yang paling banyak detailnya.

## Menyatukan gambar dengan halaman

**Melebur ke latar.** Visual utama dan gambar besar yang harus melebur ke latar tidak diberi bingkai dan tidak dikurung kartu membulat: ambil warna nyata dari keempat sudut gambar, samakan nilai latar halaman dengannya, atau gunakan CSS mask dan export fade untuk memudarkan keempat sisinya ke warna latar. Saat latarnya warna solid, menyamakan warna dasar di prompt dengan halaman membuat tepinya menyambung natural.

**Gambar transparan.** Letakkan dulu di latar final untuk memeriksa tepi, white fringe, dan sisa pola kotak-kotak; memeriksa alpha channel harus melihat piksel, bukan melihat ekstensi file. Bayangan jangan dipanggang ke dalam gambar; tambahkan drop shadow dari halaman sesuai latar yang sebenarnya, sehingga tetap benar bila latar berganti.

**Melintasi struktur.** Letakkan benda transparan tepat di garis batas dua blok warna atau dua section, sehingga ia milik kedua sisi sekaligus.

**Gambar dan kode bertitipan.** Gambar hasil generate mengerjakan material dan cahaya yang tak mampu dibuat kode — logam, kaca, model, cahaya-bayangan. Kode mengerjakan bagian yang butuh presisi, bisa diedit, dan harus berlanjut: garis, path, dan anotasi yang menjulur keluar dari gambar. Bila ada bagian di gambar yang seharusnya berlanjut ke halaman, potong bagian itu dan lanjutkan dengan vektor. Dengan begitu ia menembus layout secara presisi, membawa teks nyata, dan bisa menata ulang jalurnya pada lebar berbeda.

**Anotasi.** Anotasi di atas gambar memakai garis penunjuk tipis plus teks, bukan kartu gelembung berlatar dan berbayangan. Ujung garis penunjuk harus tepat pada posisi nyata di dalam gambar: gambar memakai ukuran dan posisi tetap di layout, dan koordinat dikonversi dari piksel gambar. Sembunyikan anotasi di layar sempit atau ubah menjadi daftar di bawah gambar; jangan biarkan mereka melayang ke posisi yang salah.

**Crop layar sempit.** Jangan mengecilkan satu gambar adegan luas secara proporsional hingga tak terbaca. Crop area fokus dari gambar aslinya dan simpan sebagai versi layar sempit, atau gunakan object-position untuk mengunci fokus. Dua versi crop, desktop dan ponsel, sama-sama harus menyelamatkan bagian yang memikul informasi.

**Satu gambar dipakai berkali-kali.** Bagian penutup atau section lain boleh memakai close-up dari bagian gambar yang sama — lebih menyatu daripada meng-generate gambar baru yang cahaya dan gayanya tidak cocok.

## Satu lukisan sebagai panggung

Pemakaian lain justru kebalikannya: gambar tidak membawa informasi, hanya memberi suasana; antarmuka tetap hitam-putih yang restraint, dan seluruh halaman hanya memakai satu lukisan bergaya sapuan kuas sebagai satu-satunya sumber warna.

- **Lukisan sebagai panggung, antarmuka berdemonstrasi di atasnya.** Letakkan versi sederhana antarmuka nyata di atas lukisan, dan biarkan lukisan tersingkap dari sekelilingnya. Saat scroll, lukisan tetap diam; yang berganti hanya isi antarmuka di depannya — menyambung dengan “narasi scroll”.
- **Berani memotong.** Sisakan hanya satu sudut atau satu bagian lukisan, mendekati abstrak, tidak berebut perhatian dengan antarmuka. Temanya tak harus berhubungan harfiah dengan produk, tetapi karakternya harus nyambung.
- **Longgar dan rapat saling menonjolkan.** Makin longgar lukisannya, makin presisi dan bersih antarmukanya harus; keduanya hadir bersama, keduanya makin indah.
- **Dipakai hemat.** Satu lukisan menembus seluruh halaman, atau hanya muncul di dua-tiga tempat — misalnya puncak kartu harga dan footer; jangan memberi satu lukisan untuk setiap section. Lukisan di satu halaman menyatukan jenis dan sapuan kuasnya.
- **Demonstrasi memakai antarmuka nyata yang sudah disederhanakan.** Konten sekunder diburamkan atau diganti skeleton; hanya satu hal yang sedang dibahas dibuat jelas. Perbandingan angka digambar langsung dengan elemen antarmuka — misalnya dua progress bar berbeda panjang — bukan membuat chart terpisah.

## Unifikasi monokrom aset heterogen

Saat memasukkan lukisan historis, patung potret, atau foto eksternal, bitmap berwarna mudah bentrok dengan warna tema antarmuka. Satukan aset dari berbagai sumber ke dalam arah saat ini lewat perlakuan monokrom yang seragam:

- **Pemetaan monokrom**: ubah aset menjadi hitam-putih berkontras tinggi, lalu petakan area gelap dan terang ke warna utama dan warna dasar halaman.
- **Halftone dan dithering titik**: terapkan halftone atau scanline halus pada foto realistis untuk meluruhkan kesan fotografisnya, sehingga ia bisa hidup berdampingan dengan tipografi dan grid.

## Penurunan visual utama untuk teknologi abstrak

Bila tidak ada screenshot produk, jangan mundur ke bola bercahaya warna-warni generik atau gradasi besar. Cari satu objek berwujud dari hal yang diproses produk: seperti apa bentuk data yang ia baca-tulis, alat atau proses apa yang ia gantikan, apa yang ada di tangan penggunanya. Bentuk ekspresinya harus memenuhi dua syarat: gradasi warna bidang luasnya stabil dan tahan ditindih teks; serta garis dan garis skala di dalam gambar bisa dilanjutkan oleh SVG/CSS. Bila tidak menemukan objek berwujud, serahkan visual utama kepada tipografi itu sendiri.

## Aset set: karakter, properti, dan sprite sheet

Produk game, koleksi, dan petualangan tidak butuh satu gambar pendukung, melainkan satu set aset yang akan dipasang, dibalik, dan dibandingkan berulang-ulang.

- **Tulis dulu style guide-nya.** Satu kalimat untuk gaya gambar, sudut pandang, arah cahaya, material, proporsi, dan palet; seluruh prompt dalam satu batch ditulis mengikuti itu.
- **Seri yang sama dibedakan lewat siluet.** Satukan proporsi dan arah cahaya, bedakan individu lewat ciri siluet seperti telinga, properti, dan aksesori — bukan hanya mengganti warna. Saat diperkecil ke ukuran tampil nyata, masih harus terbedakan sekali lihat.
- **Multi-status diturunkan dari satu gambar yang sama.** Tahap pertumbuhan, sisi depan-belakang, sebelum-sesudah cangkang terbuka, berbagai aksi: edit variannya dengan gambar pertama sebagai referensi agar tetap karakter yang sama; titik pijak tiap status disejajarkan ke satu baseline yang sama.
- **Sprite sheet transparan dipotong mengikuti siluet.** Sisakan jarak transparan antar sel, potong mengikuti kontur nyata, bukan membagi rata per sel — kalau tidak, tajuk pohon bisa terpotong dan serpihan sel sebelah bisa terbawa. Periksa piksel alpha, bukan warna latar di preview, lalu letakkan di latar final untuk memeriksa tepinya.
- **Menempel di benda harus sah dari dua sisi.** Aset yang akan dibalik, jatuh, atau berputar ke samping wajib punya sisi depan dan belakang, dengan tepi tertutup mengikuti kontur. Pencahayaan diserahkan ke scene; jangan memanggang cahaya-bayangan yang berlawanan arah dengan scene ke dalam gambar.

## 3D real-time

Tiga kondisi yang memakai 3D real-time: objek yang harus bisa diputar dan diperiksa pengguna; fisika seperti menumpuk, bertabrakan, mendorong, dan berayun; serta material yang berubah mengikuti sudut pandang seperti kaca, logam, dan plastik transparan. Bila satu gambar hasil generate sudah cukup mengekspresikannya, atau pemakaiannya hanya demi kesan premium, jangan pakai.

- Pakai engine matang seperti three.js, dan tambahkan satu library rigid body bila butuh fisika. Gambar hasil generate dipakai sebagai texture, sprite, atau sumber environment light; kode mengerjakan ruang, gerak, dan gaya.
- Acceptance melihat gambar, bukan mencatat pemakaian library: still frame harus memperlihatkan volume, perspektif, contact shadow, dan pembedaan material; di rekaman layar gerakannya kontinu dan gaya sampai ke benda yang didorong.
- Mockup baru mengunduh library ke `vendor/` di direktori tugas beserta lisensinya, tanpa merujuk CDN; proyek existing mengikuti cara dependensi yang sudah dipakai proyek. Halaman dan texture yang diimpor sebagai module harus dibuka lewat local server; bila dibutuhkan bisa dibuka dengan dobel-klik, bundel menjadi satu script biasa dengan texture di-inline atau diletakkan di direktori yang sama.
- Batas device pixel ratio diambil 2; hentikan render saat halaman tersembunyi atau keluar viewport; tampilkan gambar statis scene yang sama bila WebGL tak tersedia; saat efek gerak dikurangi, hasil tetap dihitung seperti biasa dan hanya guncangan kamera serta pertunjukan dekoratif yang dimatikan.
- Sebelum screenshot, pastikan canvas benar-benar sudah menggambar isinya, lihat [Alat](tools.md).

## Jalur opsional video hasil generate

Bila butuh satu potongan materi yang berulang terus di atas halaman, periksa dulu tiga hal: apakah akhir dan awalnya menyambung, apakah tepi subjeknya bersih, dan bagaimana perlakuan latarnya. Generate di latar monokrom lalu chroma-key hanyalah salah satu cara yang bisa dicoba: benda transparan dan reflektif bisa kehilangan tepi atau membawa warna latar setelah di-key — harus dilihat di atas latar final halaman.

Bila beberapa potongan video disambung menjadi satu narasi, gunakan frame terakhir potongan sebelumnya sebagai frame pertama potongan berikutnya, atau rencanakan keyframe semua potongan secara seragam sejak awal. Bila progresnya dikendalikan scroll atau gesture, periksa lompatan ke frame mana pun, pemutaran mundur, kecepatan loading, dan pemakaian memori; jangan mengasumsikan seluruh video didekode menjadi gambar-gambar besar.

Benda yang butuh refraksi atau transmisi cahaya seperti kaca dan kristal: generate dulu gambarnya di atas warna latar final halaman sehingga refraksi dan bayangannya terpanggang ke dalam materi, lalu hilangkan latarnya dengan model video matting. Generate di green screen lalu key akan membawa warna hijau ke dalam refraksinya. Refraksi dan pencahayaan pra-render hanya berlaku untuk latar saat generate, dan tidak boleh menjanjikan efek fisika real-time yang mengikuti isi halaman apa pun.

Video berlatar transparan sama seperti gambar, boleh dikendaikan di atas batas dua section; caranya lihat “Melintasi struktur” di atas.

## File dan keterangan

- Export pada 2× ukuran tampil, jangan langsung menempel gambar asli yang besar. Yang tak transparan memakai JPEG atau WebP, yang transparan memakai WebP atau PNG; satu gambar dijaga di bawah ratusan KB. Setelah di-inline menjadi data URL, ukurannya bertambah sekitar sepertiga lagi.
- Simpan prompt, gambar asli, dan versi yang sudah diproses; tuliskan dengan jelas sumber, kegunaan, dan cara memproses tiap gambar, serta bedakan pakai ulang, crop, generate, dan pasca-proses.
- Gambar hasil generate dan aset pengganti tidak boleh menyamar sebagai screenshot produk nyata, tempat nyata, orang nyata, atau bukti produk.
