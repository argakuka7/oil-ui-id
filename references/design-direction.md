# Arah Desain

## Navigasi isi

- [Kenali kategori, bongkar tolok ukur](#kenali-kategori-bongkar-tolok-ukur)
- [Tetapkan tone dulu, baru cari perbedaan](#tetapkan-tone-dulu-baru-cari-perbedaan) (termasuk [Kata samar wajib diterjemahkan](#kata-samar-wajib-diterjemahkan))
- [Bangun arah dari mesin generatif](#bangun-arah-dari-mesin-generatif)
- [Tetapkan warna](#tetapkan-warna)
- [Tetapkan kerangka layar pertama](#tetapkan-kerangka-layar-pertama-dan-workspace) ([Kerangka persuasif](direction-persuasion.md))
- [Kartu arah](#kartu-arah)
- [Uji pembeda](#uji-pembeda)
- [North Star dan keterhubungan](#north-star-dan-keterhubungan)
- [Momen yang membekas](#momen-yang-membekas)
- [Cara referensi menjadi keputusan desain](#cara-referensi-menjadi-keputusan-desain)
- [Mockup, pilihan, dan selera](#mockup-pilihan-dan-selera)

Target arah adalah “tim terbaik di kategori ini akan mengerjakannya seperti ini, dan hasilnya tetap berwajah produk ini sendiri”; sekadar “berbeda dari default model” belum cukup. Kesan premium lahir dari kelengkapan dan detail satu bahasa desain, bukan dari tema yang jarang dipakai.

Tema, material, skenario, font, dan palet warna dalam sebuah arah selalu diturunkan dari konten, audiens, dan konteks pemakaian produk saat ini; bila arah yang terpikir bertabrakan dengan “gaya viral” yang umum, harus bisa disebutkan alasannya dari produk ini, jika tidak, pilih ulang.

## Kenali kategori, bongkar tolok ukur

Sebelum mulai, kenali dulu ini produk kategori apa, lalu lihat bagaimana produk terbaik di kategori itu mengerjakannya. Langkah ini memberi lantai dasar: struktur yang sudah diharapkan pengguna, dan tingkat penyelesaian produk kelas satu. Tone dan mesin generatif setelahnya mencari kekhasan produk ini di atas lantai dasar itu.

Kerjakan dalam tiga langkah, dan tuliskan setiap langkah:

1. **Sebutkan kategori dan tolok ukurnya.** Ini produk kategori apa, misalnya “aplikasi belajar bahasa”, “situs component library”, “alat manajemen proyek”, “galeri karya”. Siapa dua-tiga yang bergaya paling menonjol di kategori ini. Pilih yang gayanya paling menonjol — belum tentu yang paling terkenal.
2. **Dapatkan tampilan nyata, lalu bongkar salah satunya.** Pakai browser atau pencarian milik host untuk mengambil tampilan nyata layar pertama dan satu kontrol kunci dari dua-tiga tolok ukur itu; simpan ke direktori tugas dan bongkar sambil melihat gambar, jangan menulis dari ingatan: produk dalam ingatan sering kali adalah wujudnya bertahun-tahun lalu. Bila halaman salah satunya tidak bisa dibuka atau 404, coba sekali lagi dengan alamat lain; bila tetap gagal, ganti ke yang lain. Dua tampilan nyata sudah cukup; halaman yang tak terbuka tidak dihitung sebagai referensi. Bongkar menjadi 6–10 elemen yang terlihat, dan tiap butir menuliskan dua hal: seperti apa wujudnya, dan mengapa ia dibuat begitu. Bongkar menurut lapisan-lapisan ini: bentuk dan feel kontrol, font, warna, ikon dan ilustrasi, status dan feedback, animasi, nada copy, serta apa saja yang diletakkan di layar pertama. Bongkar sampai tingkat yang bisa ditiru: tuliskan bentuk, hubungan ukuran, cara status berubah, dan konteks pemakaian yang dilayaninya. Bila hasil bongkaran hanya “bersih, ruang kosong, satu warna aksen”, berarti bongkarannya belum sampai; ganti ke yang lain dan bongkar ulang. Bila benar-benar tak bisa mendapatkan tampilan, tuliskan di awal baris “tolok ukur dan trade-off” kartu arah: “belum melihat gambar, dari ingatan”, lalu tandai tiga kolom — font, warna, visual utama — sebagai perlu verifikasi: tiga kolom inilah yang paling mudah tertulis sebagai default model karena disarikan dari ingatan.
3. **Putuskan apa yang dipertahankan dan apa yang diganti.** Cocokkan satu per satu dengan audiens, konten, dan konteks pemakaian produk ini: yang alasannya tetap berlaku dipertahankan, yang alasannya tidak berlaku diganti, dan bagian yang diganti diberi pengganti oleh mesin generatif setelahnya. Hasilnya ditulis ke bagian “tolok ukur dan trade-off” kartu arah.

Saat membongkar, bedakan tiga hal ini:

- **Baseline**: struktur yang sudah diharapkan pengguna, misalnya karya tampil duluan di galeri dan filter di bagian atas, atau keranjang di pojok kanan atas pada toko. Ikuti saja, pengguna tidak perlu belajar ulang.
- **Formula bawaan**: layout default yang dipakai semua orang di kategori ini. Minimal satu arah dalam satu ronde harus memecahkannya, lihat “uji pembeda”.
- **Tampak kembar**: font, palet, visual utama, dan ikon semuanya sama dengan suatu tolok ukur, hanya namanya yang diganti. Tidak diizinkan pada arah mana pun.

## Tetapkan tone dulu, baru cari perbedaan

Turunkan tone dari tema produk, audiens, nada brand, dan konteks pemakaiannya. Gambarkan dengan lima skala, dan tuliskan dasarnya untuk tiap skala:

| Skala | Dua ujung | Yang dilihat di layar |
| --- | --- | --- |
| Energi | Tenang ↔ Riuh | Saturasi, kontras, apakah elemen saling bertabrakan |
| Tingkat penyelesaian | Kasar ↔ Halus | Perlakuan tepi, grain dan noise, seberapa ketat perataannya |
| Kepadatan | Renggang ↔ Padat | Skala ruang kosong, lapisan bertumpuk, disiplin grid |
| Bobot | Ringan ↔ Berat | Weight font, luas blok warna, kekerasan bayangan |
| Keseriusan | Ceria ↔ Khidmat | Radius sudut, bahasa ilustrasi, amplitudo animasi |

Tulis nilai sebagai “produk ini apa → ujung mana yang dipilih tiap skala”, dengan dasar dari audiens, konten, dan konteks pemakaiannya. Kombinasi apa pun di kedua ujung skala bisa sepenuhnya sah; yang gagal adalah default tanpa dasar:

- Bukti menunjuk ke riuh dan kasar, tetapi yang diserahkan justru kartu krem, bayangan lembut, dan ruang kosong luas. Ini kegagalan paling umum: desain tergiling kembali ke “tenang premium” default model.
- Sebaliknya, demi terlihat menarik, memaksakan grain, tepi kertas sobek, dan border tebal pada produk yang seharusnya tenang.

Saat bukti sudah mengunci tone, semua kandidat tinggal di dalam tone itu, dan perbedaan dijauhkan pada komposisi, identitas warna, dan visual utama. Jangan menyelipkan satu opsi aman minimalis-tenang demi “keseimbangan”. Hanya bila bukti memang ambigu, kandidat boleh tersebar di beberapa tone.

### Kata samar wajib diterjemahkan

“Premium, halus, restraint, epik, terasa literer, minimalis” tidak boleh dipakai sebagai alasan desain. Saat pengguna — atau dirimu sendiri — mengucapkan kata-kata seperti itu, terjemahkan dulu menjadi keputusan yang bisa diamati:

| Kata samar | Diterjemahkan menjadi apa |
| --- | --- |
| Premium | Perjelas dulu premium yang mana, baru putuskan kontras font, cara pemisahan, skala jarak, dan jumlah hue. Kata “premium” saja tidak memutuskan apa pun |
| Halus (refined) | Toleransi: bagaimana letter-spacing disetel, grid berapa piksel untuk perataan, maksimal berapa tingkat bayangan, maksimal berapa jenis hue |
| Restraint | Anggaran saturasi, misalnya warna aksen tidak melebihi 10% layar; batas amplitudo animasi; batas jumlah hue |
| Epik | Skala: seberapa besar huruf display, seberapa luas gambar utama, seberapa kuat kontras terang-gelap |
| Terasa literer | Karakter font family, panjang baris, line-height, dan palet — nilai mana yang dipilih masing-masing |
| Kasar (raw) | Sarana apa yang dipakai dan seberapa jauh, misalnya bergeser berapa piksel, diputar berapa derajat |
| Minimalis | Tingkat kepadatan, serta apa yang dihapus dan mengapa. Minimalis adalah hasil, bukan instruksi |

Kata yang tidak bisa diterjemahkan menjadi keputusan yang teramati, hapus dari alasan.

Kata samar pada animasi dan interaksi juga wajib diterjemahkan menjadi pola konkret:

| Kata samar animasi | Diterjemahkan menjadi apa |
| --- | --- |
| “Bergerak saat di-scroll” | Bedakan dulu scroll-triggered atau scroll-driven, lihat “Dua mode interaksi scroll” di [Narasi Scroll](scroll-narrative.md); bila tidak disebutkan, perlakukan sebagai satu arah sekali jalan |
| “Pindah halaman lebih mulus” | Pilih pola transisi: curtain, overlapping, atau shared element; trade-off dan durasinya lihat “Trade-off stabilitas transisi satu halaman penuh” di [Animasi](motion.md) |
| “Latar terasa tiga dimensi” | **Paralaks berlapis**: beda kecepatan latar depan-belakang dan lapisan mana yang tidak diberi paralaks, ikuti “Paralaks dan one-shot” di [Narasi Scroll](scroll-narrative.md) |
| “Layar pertama harus berdampak” | Tetapkan satu protagonis tunggal layar pertama (tipografi besar, satu benda nyata, 3D inti, atau video) tanpa menumpuk ornamen sekunder; durasi masuk lihat “Durasi dan amplitudo” di [Animasi](motion.md) |

## Bangun arah dari mesin generatif

Setiap arah berangkat dari satu mesin yang konkret, bukan dari kata sifat, dan arah-arah yang berbeda sebaiknya memakai mesin yang berbeda. Isi mesin berasal dari bukti produk ini: audiens, konten, konteks pemakaian, dan aset brand yang sudah ada.

- **Material × lingkungan**: satu material diletakkan di satu lingkungan konkret. Dari sana diturunkan pencahayaan, kedalaman, perlakuan tepi, dan damping animasi.
- **Satu skenario konkret**: satu adegan dengan waktu, tempat, dan cahaya. Tekstur dan kecepatan animasi diturunkan dari cahaya, suara, material, dan ritme di dalam skenario. Cocok untuk alat yang berbasis emosi.
- **Arketipe karakter**: beri produk satu karakter konkret, dan biarkan karakter itu menentukan font serta gerakannya.
- **Satu gerakan desain atau tata bahasa budaya**: pilih satu gerakan desain atau tradisi visual yang punya hubungan nyata dengan tema, audiens, atau wilayah produk, lalu pinjam tata bahasanya — bukan menempel motifnya.
- **Seluruh bahasa rupa dari bidang lain**: pinjam cara berekspresi dari media atau benda di bidang lain. Pinjam hanya satu-dua tekniknya yang paling khas; halaman tetap ber-genre aslinya. Jangan memindahkan komponen media itu satu per satu — itu menjadi tumpukan properti.
- **Sengaja memecah konvensi**: layout asimetris yang radikal, palet dan font yang disonan, ruang kosong yang membuat gelisah — tetapi keseluruhannya tetap indah dan fungsinya utuh.

Mesin menentukan struktur, feel, tekstur, dan animasi; warna ditetapkan terpisah di bagian berikutnya.

## Tetapkan warna

Aset brand produk sendiri, benda fisiknya, dan gambar kontennya adalah sumber warna pertama; bila visual utamanya adalah produk fisik itu sendiri, warna utama bisa langsung diambil darinya. Bila belum ada warna utama, jangan langsung menjadikan warna bawaan material atau skenario di mesin generatif sebagai warna utama — begitu metafora mendarat di kuningan, serat kayu, atau darkroom, produk-produk yang berbeda pada akhirnya akan menabrak set warna yang sama. Tetapkan dalam tiga langkah:

1. Tulis dulu dua baris yang dipakai bersama semua arah: apa palet default yang paling lazim di kategori ini, sebutkan warna dasar dan warna aksennya; serta hue dan terang-gelap apa yang ditempati masing-masing tolok ukur yang sudah dibongkar.
2. Tiap arah menetapkan set hue dan terang-gelap yang berbeda, atau hitam-putih yang tegas, dengan satu kalimat tentang dari mana asalnya dalam produk ini: konten, audiens, atau aset brand. Hindari palet tolok ukur yang baru saja dibongkar; minimal satu arah keluar dari palet default kategori ini.
3. Tuliskan minimal tiga lapis: warna dasar, warna aksen utama, serta turunannya — latar terpilih, stroke, dan status disabled.

Hitam-putih-abu plus satu warna aksen, bahkan tanpa warna sama sekali, juga merupakan identitas warna yang utuh; saat itu warna diserahkan ke konten: screenshot produk, foto pengguna, sebuah lukisan. Antar-arah tidak dibedakan lewat terang-gelap: kegagalan nomor satu adalah “satu terang, satu gelap, satu hangat”; tiap arah harus punya keluarga hue atau tekstur materialnya sendiri, dan terang-gelap hanyalah hasil akhirnya.

## Tetapkan kerangka layar pertama dan workspace

Tetapkan kerangka sebelum menulis copy, dan biarkan copy menyesuaikan kerangka. Jawab dulu satu pertanyaan: **pengguna datang ke layar pertama untuk melihat apa dan melakukan apa?**

- **Halaman untuk mendengar satu kalimat, melihat satu gambar, atau diyakinkan** (landing page, halaman brand, halaman peluncuran produk, halaman pameran): pilih dari 8 kerangka layar pertama, keluar dari template default dua kolom kiri-kanan. Selengkapnya lihat [Kerangka layar pertama halaman persuasif](direction-persuasion.md).
- **Halaman untuk melihat konten, memilih barang, atau memproses objek** (galeri, toko, feed, dokumen, portofolio, alat, dan panel admin): layar pertama adalah baris konten pertama itu sendiri atau workspace. Navigasi, judul, dan filter digabung tidak lebih dari satu-dua baris, dan baris konten pertama harus tampak utuh di layar pertama. Jangan menaruh slogan layar pertama, juga tidak perlu paragraf yang menjelaskan halaman ini untuk apa. Atur konten mengikuti aksi yang paling sering dilakukan pengguna: untuk menjelajah, biarkan konten memenuhi layar; untuk memproses, dekatkan objek saat ini dengan aksinya.
- **Bila keduanya ada** (misalnya banner kampanye di atas beranda toko): ikuti yang paling sering dilakukan pengguna; banner boleh tetap ada, tetapi tidak boleh mendorong baris konten pertama keluar dari layar pertama.

## Kartu arah

Tiap arah menulis satu kartu arah, tiap isian berupa keputusan konkret, bukan kata sifat. Pada ronde yang menghasilkan tiga layar pertama, tone serta tolok ukur dan trade-off dipakai bersama oleh beberapa arah (bila kandidat tersebar di beberapa tone, tone diisi masing-masing), dan tiap arah hanya mengisi North Star, mesin generatif, kerangka layar pertama, font, warna, visual utama, ikon, dan tata bahasa kontrol; kolom lainnya dilengkapi setelah arah terpilih, sebelum halaman lengkap dikerjakan. Saat menurunkan layout, tiap varian layout hanya menulis ulang tiga kolom: kerangka layar pertama, struktur halaman, dan visual utama:

| Kolom | Tingkat detail yang harus dicapai |
| --- | --- |
| North Star | Satu kalimat niat yang bisa memandu trade-off: kesan pertama apa yang diberikan, dan di sekeliling apa seluruh halaman berputar |
| Tone | Nilai kelima skala beserta dasarnya |
| Tolok ukur dan trade-off | Kategorinya apa, siapa yang dibongkar, terhadap tampilan nyata mana bongkaran dilakukan (tulis path penyimpanannya; bila belum melihat gambar, tulis “belum melihat gambar, dari ingatan”); butir mana yang diikuti, mana yang diganti, dan alasan masing-masing |
| Mesin generatif | Yang mana yang dipakai, apa secara konkret, dan bukti apa dari produk ini |
| Kerangka layar pertama | Tulis dulu apa yang dilihat pengguna di layar pertama. Halaman konten: berapa objek terlihat di layar pertama dan berapa baris header; halaman persuasif: kerangka mana yang dipilih dari tabel, disertai wireframe layar pertama 3–5 kotak: tiap blok berisi apa, seberapa luas, dan di mana pembacaan dimulai |
| Struktur halaman | Bagaimana organisasi di bawah layar pertama, misalnya satu kolom scroll imersif, atau tiga kolom navigasi-konten-detail |
| Bentuk tiap section | Tiap section utama di bawah layar pertama (contoh nyata produk, fitur, harga, privasi, penutup, dll.) berubah menjadi apa di arah ini. Bentuknya diturunkan dari mesin generatif, bukan modul yang sama yang sekadar diganti warna |
| Font | Font family, weight, dan hubungan skala yang konkret: display, body, dan angka masing-masing memakai apa, dan bedanya seberapa besar |
| Warna | Tulis sesuai “Tetapkan warna”: nilai hex dan kegunaannya, minimal tiga lapis, plus satu kalimat dari mana asalnya dalam produk ini |
| Visual utama | Gambar atau bentuk mana yang memikul emosi dan identitas, dan asalnya: pakai ulang, hasil generate, atau tipografi itu sendiri |
| Ikon | Set mana yang dipakai, seberapa tebal stroke dan bagaimana bentuk ujungnya; atau tanpa ikon, memakai karakter dan penomoran |
| Tata bahasa kontrol | Satu set bentuk dan feel yang dipakai bersama oleh tombol, input, selection, label, status, dan animasi; tulis dalam satu kalimat, misalnya radius sudut berapa, seberapa tebal stroke, dan bagaimana berubah saat ditekan |
| Animasi | Feel ditulis dengan “satu onomatope + satu gerakan benda nyata”, dan bendanya dicari dari dunia produk ini; bagaimana masing-masing dari tiga animasi dasar bergerak dan bagaimana mereka saling menyambung; halaman tipe landing page ditambah storyboard scroll (kemunculan section, teknik narasi scroll-driven mana yang dipilih), lihat [Narasi Scroll](scroll-narrative.md). Lihat juga [Animasi](motion.md) |
| Terobosan struktural | Satu penyimpangan dari konvensi yang mengubah struktur layar pertama, dan bagaimana ia memperbesar North Star. Detail lokal seperti anotasi tulisan tangan, tombol bertekstur, atau garis coretan tidak dihitung |
| Titik yang membekas | Satu-dua tempat di mana tenaga difokuskan: pada momen atau posisi mana, dengan material, gerakan, atau gaya gambar apa, lihat “Momen yang membekas” |
| Apa yang ditinggalkan | Praktik umum yang sengaja tidak diambil oleh arah ini |

North Star, font, palet, dan karakteristik ditulis langsung ke manifest halaman perbandingan, ditampilkan bersama tampilannya.

## Uji pembeda

Setelah kartu arah selesai, sebelum layar pertama dibuat, periksa butir demi butir. Bila layout diturunkan dari arah yang sudah terpilih, atau pengguna sudah memberi pedoman brand, font dan palet dipakai bersama: beberapa butir tentang font dan warna di bawah tidak berlaku, tetapi kerangka, visual utama, dan struktur halaman tetap wajib berbeda satu sama lain:

- **Bandingkan wireframe, bukan deskripsi**: letakkan wireframe layar pertama tiap arah berdampingan dan bandingkan. Deskripsi tiap arah boleh berbeda-beda, tetapi wireframe-nya bisa saja semuanya “judul besar di kiri, blok kecil di kanan”. Wireframe yang mirip berarti kerangka yang sama; pilih ulang kerangkanya.
- **Dari empat hal, maksimal satu yang sama**: dari kerangka layar pertama, font, warna, dan visual utama, dua arah apa pun boleh paling banyak memiliki satu kesamaan; jika tidak, keduanya varian dari arah yang sama — ganti mesin generatif dan tulis ulang salah satunya.
- **Arah tidak dibedakan lewat terang-gelap**: tiap arah punya keluarga hue atau hitam-putihnya sendiri, lihat “Tetapkan warna”.
- **Struktur juga harus berbeda**: beberapa kandidat yang mengisi “struktur halaman” (varian layout, atau arah yang semuanya akan dibuat sebagai halaman penuh) tidak boleh punya organisasi halaman yang persis sama dengan hanya mengganti warna dan tekstur. Kandidat cukup berbagi konten inti dan tugas utama.
- **Minimal satu berani ekstrem**: dalam rentang tone yang diizinkan bukti, minimal satu arah mengambil pilihan yang tegas pada komposisi, warna, dan visual utama tanpa berkompromi; arah yang berkompromi paling banyak satu.
- **Minimal satu memecah formula kategori**: dalam tone yang sama, minimal satu arah tidak memakai layout default kategori ini. Memecah formula bukan berarti membuang baseline. Formula yang umum:
  - Panel admin: sidebar kiri, topbar, plus grid kartu.
  - E-commerce: banner besar, grid produk, plus footer.
  - Sosial: tab bar bawah, feed, plus tombol mengambang.
  - Landing page: visual utama, fitur, testimoni, lalu satu tombol aksi terakhir.
  - Chat: kontak di kiri, pesan di kanan.
  - Alat AI dan developer: latar hitam, lingkaran cahaya ungu-biru yang menyebar, partikel melayang, dan tombol pill yang itu-itu saja.
- **Tidak tampak kembar**: lihat tiap arah berdampingan dengan tolok ukur yang dibongkarnya; bila tampak kembar, kerjakan ulang (definisi lihat “Kenali kategori, bongkar tolok ukur”). Mengikuti baseline tidak dihitung tampak kembar.
- **Uji buta**: tutupi nama dan deskripsinya, lihat hanya gambarnya, dan tetap harus bisa menyebutkan kesan berbeda yang diberikan tiap arah.

Setelah layar pertama jadi, bandingkan sekali lagi tampilan nyatanya: lihat layar pertama berdampingan di halaman perbandingan, sipitkan mata dan lihat hanya bidang terang-gelapnya. Bila distribusi bidangnya mirip — misalnya sama-sama blok besar di kiri dan blok kecil di kanan — meski font dan warnanya berbeda, kembali ke tabel kerangka dan kerjakan ulang; jangan menambalnya dengan mengganti dekorasi.

## North Star dan keterhubungan

Setelah North Star terpilih, terjemahkan menjadi hubungan yang konsisten di seluruh halaman: siapa protagonis tiap layar, bagaimana informasi sekunder mundur, tipografi atau bentuk apa yang berulang di seluruh halaman membentuk ritme, dan di titik mana kontras dipakai untuk menonjolkan aksi utama.

Terobosan struktural harus menyentuh struktur — misalnya kerangka layar pertama, proporsi, atau urutan baca — bukan sekadar menambah satu ornamen; ia memperkuat tema atau mengarahkan orang ke aksi kunci. Saat memoles, jangan menghaluskan pilihan yang justru membuatnya khas. Elemen baru yang tidak memperkuat niat yang sama, jangan ditambahkan.

## Momen yang membekas

Tiap arah memilih satu-dua tempat untuk memusatkan tenaga, sisanya tetap tenang. Titik yang membekas biasanya berupa satu aksi dari satu komponen: hasil, material, cahaya-bayangan, feel, dan ritmenya dikerjakan sampai tuntas.

Di mana mencarinya:

- **Aksi yang akan dilakukan pengguna.** Tap, drag, beralih, submit — lebih mudah menjadi momen yang membekas dibanding scroll.
- **Momen kunci.** Pembayaran sukses, menyelesaikan tugas pertama kali, upgrade, hapus, upload, menunggu hasil. Emosi di momen-momen ini paling kuat, dan satu animasi kecil memberi imbal hasil paling tinggi.
- **Halaman pinggiran.** 404, empty state, loading, footer. Tidak diharapkan siapa pun dan risikonya rendah — paling mudah bersinar.
- **Saat AI sedang bekerja.** Buat prosesnya terlihat; beda antara sedang berjalan dan selesai langsung tampak pada gambar dan perubahan konten, bukan hanya animasi berputar.

Cara memikirkannya:

- **Biar hasilnya terjadi di tempat.** Pergantian status bukan sekadar mengganti ikon, tetapi membuat hal yang terdampak berubah saat itu juga. Yang dilihat pengguna adalah hasilnya, bukan kontrol yang sedang pentas.
- **Gambar angka sebagai kuantitas yang terlihat.** Persentase, durasi, saldo — tanyakan dulu apakah bisa digambar sebagai luas, panjang, atau jumlah. Angka hanya label; kuantitas itulah gambarnya.
- **Pinjam benda nyata di dunia ini untuk menyerahkan hasil.** Lihat dulu apa yang ada di tangan dan di mata pengguna saat melakukan hal ini — misalnya track audio, layer kanvas, paket, atau tagihan — lalu pinjam wujud dan gerakannya untuk menyerahkan status. Properti retro seperti struk, printer, kaset, dan konsol game lama sudah terlalu sering dipakai; bila tidak berhubungan dengan produk, jangan dipakai.
- **Beri kontrol fisika dan karakter.** Drag punya elastisitas dan bobot, penekanan mengubah cahaya-bayangan, dan bila ditarik terlalu jauh ia memantul kembali dengan enggan.
- **Gaya gambar harus bisa disebut asalnya.** Gaya seperti pola titik, seni karakter, piksel, partikel, atau material realistis hanya dipilih bila bisa dijelaskan berasal dari apa yang dikerjakan produk ini. Tidak bisa menjelaskan asal, jangan dipilih; sudah dipilih, pakai konsisten dari visual utama sampai loading, ikon, dan empty state.

## Cara referensi menjadi keputusan desain

Perjelas dulu referensi ini dipakai untuk apa: meminjam hubungan visualnya, menjadikannya garis dasar kualitas, atau merekonstruksi secara presisi sesuai gambarnya. Lihat gambarnya dulu, baru deskripsikan wujudnya. Saat meminjam, yang diambil adalah hubungannya — misalnya “judul paling berat, gambar bertugas membawa emosi, informasi pendukung ditekan sangat tipis” — lalu disusun ulang dengan konten saat ini; jangan menyalin modul bisnis, identitas, dan copy dari referensi. Metafora pinjaman harus mendarat menjadi keputusan antarmuka yang konkret, bukan dibuat menjadi kulit simulasi yang menghambat operasi.

Hal yang tidak ada di referensi juga merupakan keputusan. Bila layar pertama referensi tidak punya area judul dan paragraf penjelas, jangan menambahkannya untuk referensi itu; ornamen yang tidak dipakai referensi, jangan ditambahkan kembali.

## Mockup, pilihan, dan selera

Arah hanya dibuat sampai layar pertama, tidak langsung beberapa set produk lengkap; ronde dan jumlahnya lihat langkah 1 di SKILL.md.

Pilih halaman yang bisa memperlihatkan kekuatan dan kelemahan arah sebagai layar pertama: produk dengan form kompleks tidak bisa hanya membuat sampul.

Halaman yang memperkenalkan produk harus membuat pengguna melihat apa yang benar-benar diserahkan produknya: satu laporan yang sudah jadi, satu kontrak yang sudah diekspor, satu potongan data nyata yang sudah diproses — bukan sekadar janji tertulis “bisa melakukan apa”. Contoh nyata ini biasanya lebih meyakinkan daripada daftar fitur, dan paling mudah menjadi protagonis salah satu segmen di bawah layar pertama.

Alasan rekomendasi ditimbang dari kesesuaian tugas, kekhasan, kapasitas konten, keterbacaan, dan biaya implementasi. Saat meminta pengguna melengkapi selera, tanyakan: kesan apa yang diinginkan, apa yang tidak diinginkan dan mengapa, serta bagian mana yang harus dipertahankan. Bila pengguna hanya berkata “buat lebih premium”, gunakan tabel penerjemahan di atas untuk bertanya lanjut, atau sajikan dua mockup untuk dibandingkan pengguna.

Tuliskan arah terpilih dan selera ke catatan desain, sebagai baseline penilaian selanjutnya. Saat review mengusulkan gaya baru, nilai dulu apakah ia menyelesaikan tujuan awal; eksplorasi ulang hanya bila arah saat ini memang tidak cocok, atau pengguna mengubah tujuannya.
