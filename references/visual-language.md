# Bahasa Visual

## Navigasi isi

- [Dari keseluruhan ke detail](#dari-keseluruhan-ke-detail)
- [Fokus dan ruang](#fokus-dan-ruang)
- [Font dan konten](#font-dan-konten) (termasuk [Keterbacaan adalah ambang penyerahan](#keterbacaan-adalah-ambang-penyerahan))
- [Warna dan permukaan](#warna-dan-permukaan)
- [Kontrol dan ikon](#kontrol-dan-ikon)

## Dari keseluruhan ke detail

Lihat dulu fokus informasi, komposisi, dan kepadatan konten, baru menyetel ruang, tipografi, warna, dan detail. Bila langkah sebelumnya sudah menyelesaikan masalahnya, jangan menambah gaya sekadar agar terlihat sungguh-sungguh.

Variabel visual, komponen, dan referensi yang sudah ada di proyek, pakai sebisa mungkin. Bila belum ada standar, definisikan hanya beberapa gaya teks, warna, dan jarak yang dibutuhkan saat ini; jangan mengarang satu sistem desain utuh dari nol.

Setiap perubahan harus bisa dijelaskan: elemen terlihat mana yang bermasalah, pada hubungannya dengan apa masalah itu muncul, bagaimana berniat menyetelnya, dan setelah disetel harus membaik di mana. Membaca source code bisa membuktikan gaya tidak konsisten, tetapi tidak bisa membuktikan tampilan menjadi lebih baik.

## Fokus dan ruang

- Setiap area harus membuat orang langsung mengenali satu informasi atau satu aksi yang paling penting; informasi lain mundur ke belakang lewat ukuran font yang lebih kecil, weight yang lebih ringan, kontras yang lebih rendah, atau posisi yang menjauh ke tepi. Jangan biarkan beberapa penekanan berebut perhatian bersamaan.
- Hubungan yang sama memakai jarak yang sama; di dalam satu kelompok lebih rapat, antar-kelompok lebih renggang. Bangun dulu strukturnya lewat perataan dan ruang kosong, baru pertimbangkan apakah perlu wadah atau garis pemisah.
- Ruang kosong dipakai untuk mengelompokkan, menonjolkan, dan mengendalikan ritme. Antarmuka alat tidak memangkas informasi yang perlu demi terlihat lapang, dan halaman brand juga tidak wajib menyempti layar pertama.
- Layout asimetris, grafis yang keluar dari batas, dan teks yang sangat besar semuanya boleh dipakai mengekspresikan arah yang dipilih, tetapi bagian lokalnya harus rata dan urutan bacanya jelas; asimetri yang disengaja tidak diperlakukan sebagai kesalahan yang harus diperbaiki.
- Cara area-area tersusun ditentukan oleh layout induk; komponen hanya mengatur ruang di dalam dirinya. Jarak yang sama jangan ditambahkan berulang oleh beberapa lapis gaya.
- Letakkan dulu konten langsung di kanvas, dan organisasikan lewat perataan, ukuran font, serta ruang kosong. Wadah baru ditambahkan hanya benar-benar perlu mengelompokkan, menandai selection, memisahkan kontras dengan latar, atau menandai area aksi; jangan melapis-lapiskan halaman, modul, butir, dan keterangan butir menjadi kartu di dalam kartu.
- Garis pemisah dan border jangan saling mengulang. Setiap garis hanya mengerjakan satu hal: pemisahan di lokasi yang sama tidak menumpuk dua garis, atau satu garis lalu ditambah satu kotak lagi; tempat yang sudah dipisahkan ruang kosong tidak ditambah garis; jangan menggambar ulang garis di setiap lapisan. Ketebalan garis berkorespondensi dengan lapisan — misalnya garis tebal memisahkan bidang halaman, garis tipis memisahkan kolom — dan konsisten di seluruh halaman. Bila garis itu sendiri bagian dari gaya, biarkan; hapus hanya yang berulang.

## Font dan konten

- Bagi teks menjadi beberapa peran — judul, body, informasi pendukung, label, dan data — kunci gaya tiap peran, dan pastikan pembeda antar lapisan cukup besar; apakah wrap atau berapa ruang yang disisakan, ditentukan oleh panjang konten yang nyata.
- Periksa bentuk huruf, weight, dan fallback font dengan bahasa yang benar-benar dipakai produk. Sampel Latin yang bagus belum tentu sah saat teks aslinya dirender; pada teks campuran (misalnya Latin dan CJK), periksa apakah baseline sejajar dan kedua aksara terlihat sama beratnya.
- Panjang baris dan line-height body text ditetukan dari kenyamanan membaca; tabel padat dibuat untuk dipindai dan dibandingkan, jangan meniru tata letak artikel. Angka yang perlu dibandingkan atas-bawah atau berubah saat scroll memakai angka tabular; angka besar yang berdiri sendiri dan input nominal yang di tengah dipilih berdasarkan keindahan bentuknya.
- Nama dan deskripsi yang penting tidak dipotong dengan tinggi tetap. Bila memang harus terpotong, sediakan pintu untuk melihat isi lengkapnya, dan jangan biarkan nama-nama yang mirip tak terbedakan setelah terpotong.
- Tulis dulu konten produk yang konkret, baru menyetel layout. Tombol menuliskan apa yang terjadi saat ditekan; saat menjelaskan keunggulan produk, tulis kegunaan nyatanya — jangan mengisi halaman dengan slogan kosong, endorsemen fiktif, atau bahasa Inggris tanpa makna.

### Keterbacaan adalah ambang penyerahan

Ukuran font dan line-height dinilai pada viewport nyata, font sebenarnya, dan ukuran baca 100%; thumbnail hanya dipakai menilai komposisi. Body text halaman berorientasi baca biasanya mulai dari 16–18px, body text antarmuka produk 14–16px, dan alat padat yang dipakai berjam-jam tiap hari bisa turun ke 13–14px; line-height body (unitless) 1.6–1.75; teks aksi biasanya 14–16px. Semua itu titik awal, bukan hukum mati antar-produk. Jangan membangun kesan “halus” dengan keterangan 9–12px, huruf tipis berkontras rendah, atau line-height yang dipadatkan. Bila informasinya terlalu banyak, hapus dulu yang berlebihan, setel ulang hierarki, atau susun ulang.

Judul multi-baris biasanya mulai dengan line-height 1.2–1.35 dan diperiksa dengan bentuk huruf yang sebenarnya. Jangan meniru line-height super rapat poster kapital berbahasa Latin, jangan mengunci tinggi judul satu baris, dan jangan memampatkan konten setelahnya dengan margin negatif. Bila huruf display memang perlu lebih rapat, hasil wrap nyata di setiap viewport yang didukung harus sudah dilihat dan dipastikan tidak ada huruf yang bertabrakan.

Kendalikan pemenggalan baris secara aktif: `text-wrap: pretty` atau `balance` hanya mengurangi kata yatim, tidak menghapusnya. Angka beserta satuannya (38 detik, 47 menit) dan istilah yang tidak boleh terpisah dibungkus tanpa wrap; paragraf pendek seperti penjelas layar pertama atau anotasi tepi dipenggal manual sesuai makna. Baris akhir yang hanya menyisakan satu-dua huruf, atau kata yang terpotong ke dua baris, sama-sama dihitung cacat.

**Huruf display sempit (Condensed / Compressed)**: hanya untuk judul display dan label nomor yang sangat pendek; ia mengorbankan keterbacaan horizontal, jadi body text dan bacaan panjang memakai font berlebar normal.

Saat acceptance, periksa judul panjang, body dua-tiga baris, teks campuran multi-aksara, angka bersatuan, dan fallback font; setelah layar sempit dan zoom membaca, periksa jarak antar baris, jarak antar blok, dan bagian dalam tombol. Teks saling menumpuk, informasi kunci terpotong, atau tertindih area tetangga dihitung belum selesai. Perbaiki dulu line-height, tinggi yang digerakkan konten, dan elastisitas wadah, baru pertimbangkan mengecilkan font.

### Data contoh harus terasa nyata

Data contoh membongkar kesan template, meski lapisan visualnya sudah bagus. Yang harus dihindari: metrik bulat sempurna (1.000 pengguna, +10%), nama generik dan perusahaan contoh, semua item bertanda “2 jam lalu”, placeholder bertulisk “judul”/“deskripsi”, serta “pelajari lebih lanjut” dan “mulai sekarang” yang berulang di halaman. Data nyata itu tidak rapi: 1.238 pengguna, +1,83%, waktu berbunyi “baru saja”, “kemarin 16.12”, “14 Maret”; nama ada yang panjang ada yang pendek — sekalian memverifikasi tata letak nama panjang. Tombol menyebutkan aksinya yang konkret, misalnya “Simpan draf” atau “Kirim hari Selasa”. Bila satu halaman memuat banyak demo (katalog komponen, library template, galeri fitur), biarkan semuanya berbagi satu skenario fiktif yang konkret: produk yang sama, orang-orang yang sama, file dan angka yang sama, dan demo-demo saling menyambung — jauh lebih kredibel daripada tiap demo mengarang “judul contoh” sendiri; jangan menjadikan nama library atau tech stack sebagai isi demo.

## Warna dan permukaan

Setiap warna punya kegunaan yang tetap: teks, latar, aksi, selection, atau status. Warna brand dan warna status boleh hidup berdampingan, tetapi status penting tidak boleh dibedakan hanya lewat warna.

Border, bayangan, material, dan gradasi harus searah dengan arah desain, dan benar-benar membantu: memisahkan lapisan, membawa suasana, atau membuat orang mengenali brand. Ungu, sudut membulat, dan gradasi bukan hal terlarang; yang bermasalah adalah pengulangan di mana-mana tanpa alasan, utamanya tak jelas, atau ketidakcocokan dengan tugas ini.

Jangan menghias setiap kartu biasa dengan warna aksen berbeda, border tebal, dan bayangan berat. Hal-hal yang satu lapisan terlihat sama beratnya; outline yang berada di dalam harus selaras dengan wadah di luarnya.

Lapisan permukaan bisa dibedakan lewat geseran suhu warna dan hue, bukan hanya terang-gelap. Cara memilih palet lihat “Tetapkan warna” di [Arah Desain](design-direction.md); bagian ini hanya mengatur cara warna dipakai.

Material/textur diambil sesuai tingkat penyelesaian tone, tanpa campur aduk:
- Ujung halus: toleransi kecil, lapisan rinci; sarana konkretnya dicari dari mesin generatif arah ini.
- Ujung kasar: jejak tangan dan cetak; juga dicari dari mesin generatif arah ini, bukan menempelkan satu set properti tetap.

**Sistem monokrom dan duotone**: selain abu netral berlapis plus satu warna aksen, seluruh halaman juga bisa hanya memakai satu warna utama dan satu warna dasar; informasi sekunder, border, dan status disabled semuanya diturunkan dari warna utama lewat transparansi atau campuran dengan warna dasar.

**Selang-seling blok terang-gelap**: section-section halaman panjang boleh berganti langsung antara latar gelap-teks terang dan latar terang-teks gelap dengan tepian keras tanpa transisi gradasi, membentuk jeda antar-bagian yang jelas.

Periksa sekali pada latar yang sebenarnya: apakah teks, tepi kontrol, focus, dan status selection masih terbaca — terutama saat latar berupa gambar, semi-transparan, atau bergerak. Bila proyek sudah punya requirement aksesibilitas, ikuti requirement itu; membaca konten dan melakukan operasi dasar tidak boleh mengandalkan terkaan.

## Kontrol dan ikon

Ikon dalam satu antarmuka memakai satu gaya gambar, terlihat sama besar, dan sejajar dengan teks di sebelahnya. Untuk ikon umum, utamakan library ikon yang matang; ilustrasi khusus brand digambar terpisah — jangan memaksakan satu ikon untuk tiap judul.

Hal yang bisa diklik harus terlihat bisa diklik, dan memberi feedback saat diklik. Default, pressed, focused, selected, disabled, dan processing adalah makna yang berbeda, wajibnya wujud yang berbeda; pintu yang hanya muncul saat hover harus tetap bisa dicapai lewat layar sentuh dan keyboard. Saat status berubah, area klik tidak membesar-mengecil dan tidak menggeser layout di sekitarnya.

Kontrol adalah satu tata bahasa: radius sudut, stroke, weight, bayangan, pergeseran saat ditekan, cara mengekspresikan selection, dan ikon status — semuanya memakai logika yang sama di tombol, input, label, switch, dan empty state. Arah tidak hanya menembus seluruh halaman, tetapi juga setiap kontrol. Bila tombol dan input masih berbentuk default library komponen, dan tak dikenali produk mana setelah diganti warna utamanya, berarti kontrol belum masuk ke dalam arah.

Ikon yang asing disertai teks yang terlihat; tombol ikon murni tetap butuh nama aksesibel. Simbol panah bermakna: ↗ berarti membuka halaman baru atau tautan eksternal, dan tidak dipakai untuk aksi di tempat seperti submit atau periksa. Label statis dan dekorasi jangan menyamar sebagai tombol, dan tombol inline jangan memicu aksi kartu luar secara tak sengaja.

### Library ikon juga bisa menyamarata

Default model adalah Lucide atau Heroicons: 24px, stroke 2px, ujung membulat. Library-nya sendiri tidak bermasalah; masalahnya setiap arah memakai set yang sama dengan penataan yang sama. Ikon sama seperti font adalah bagian dari arah: tuliskan di kartu arah set mana yang dipakai, seberapa tebal, dan bagaimana ujungnya — atau memang tanpa ikon.

| Karakter arah | Bisa dipertimbangkan | Ciri |
| --- | --- | --- |
| Halus, editorial, mewah | Phosphor Thin atau Light, Iconoir | Stroke tipis, dipadukan serif atau sans berweight ringan |
| Industrial, instrumen, alat korporat | Carbon, Material Symbols Sharp, Radix Icons | Ujung siku, grid ketat; Radix dirancang untuk antarmuka padat 15px |
| Ramah, membulat, konsumen | Phosphor Fill atau Duotone, MingCute | Ujung membulat, solid atau dua warna |
| Produk berbahasa CJK, butuh banyak ikon bisnis | IconPark, Remix Icon | Cakupan luas; IconPark bisa menyetel ketebalan stroke, ujung, dan tema |
| Butuh ketebalan dan fill yang bisa diatur kontinu | Material Symbols | Variable font; fill, weight, dan optical size bisa diatur kontinu |
| Piksel, game, retro | Pixelarticons | Grid piksel |
| Logo brand | Simple Icons | Bentuk vektor logo berbagai brand |

Dengan Iconify, SVG tunggal dari mayoritas library di atas bisa diambil langsung per nama.

- **Satu produk satu set.** Bila perlu melengkapi kekurangan, pilih yang stroke, ujung, dan radiusnya konsisten, lalu satukan ke canvas size dan ketebalan stroke yang sama.
- **Ketebalan mengikuti weight.** Stroke ikon mendekati ketebalan goresan body text pada ukuran yang sama: font ringan pasangan 1–1.5px, hitam tebal 2px ke atas atau solid. Ukuran ikon sekitar 1–1,25× ukuran font, disejajarkan dengan pusat visual, bukan dengan kotak luarnya.
- **Bisa tanpa ikon, ya tanpa ikon.** Arah editorial sering memakai karakter itu sendiri: → ↗ ※ §, penomoran, singkatan. Ikon hanya dipakai di tempat yang benar-benar mempercepat pengenalan.
- **Momen brand digambar tangan.** Di beberapa posisi seperti aksi inti dan empty state, boleh menggambar ikon garis atau ilustrasi kecil eksklusif dengan bahasa garis milik arah; aksi umum tetap memakai library. Visual utama seperti karakter, properti, dan skenario tidak andalkan SVG gambar tangan, lihat [Aset](media.md).
- **Mockup di-inline.** Mockup mandiri hanya meng-inline SVG yang dipakainya, tidak merujuk icon font atau CDN. Proyek existing mengikuti library yang sudah dipakai; mengganti library dihitung redesain.
- **Periksa lisensinya.** Mayoritas MIT, Apache, atau ISC; SF Symbols hanya boleh dipakai di antarmuka platform Apple, tidak untuk web; library yang mewajibkan atribusi, berikan atribusinya.
