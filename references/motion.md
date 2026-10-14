# Animasi

## Tiap antarmuka mulai dengan tiga animasi

Antarmuka yang sama sekali diam itu seperti screenshot: tekanan tanpa jawaban, perpindahan tanpa asal — pengguna hanya bisa menebak apa yang baru terjadi. Antarmuka baru dan antarmuka yang alur operasinya berubah, kerjakan dulu tiga ini:

1. **Feedback aksi utama.** Menekan langsung dijawab, menyelesaikan menyerahkan hasil: tombol tenggelam lalu memantul, centang tergambar, angka bergulir ke nilai baru.
2. **Satu perpindahan status dengan asal yang terlihat.** Saat memilih, membuka, mengganti view, atau menambah-menghapus item daftar, biarkan orang melihat benda datang dari mana dan ke mana, lihat “Transisi antarmuka” di bawah.
3. **Satu kemunculan saat pertama masuk.** Protagonis tiba lebih dulu, sisanya mengikuti urutan baca, dan hanya diputar saat pertama masuk.

Animasi tambahan di luar tiga ini, masing-masing harus memikul salah satu: feedback, panduan, kontinuitas, atau ekspresi brand; fade-in saat scroll, paralaks, mengikuti kursor, dan loop dekoratif paling mudah menjadi gangguan.

| Tujuan | Cara yang layak dipertimbangkan |
| --- | --- |
| Penekanan, focus, membuka, atau pergantian status biasa | Transisi native browser, atau transisi kecil bawaan komponen yang sudah ada |
| Pergantian antar view, elemen pindah posisi | Shared element transition, lihat “Transisi antarmuka” di bawah |
| Drag, gesture, perubahan posisi dan ukuran, animasi kerja sama banyak elemen | Library animasi matang yang sudah ada di proyek |
| Bidang brand khusus, material, efek fisika kompleks | Gambar, 3D, shader, atau video pra-render; pilih sesuai kebutuhan; kapan memakai 3D real-time lihat [Aset](media.md) |
| Mengendalikan progres satu narasi lewat mouse, sentuhan, atau scroll | Biarkan progres animasi mengikuti input secara langsung; scroll mundur dan operasi cepat keduanya harus tertangani baik; lihat [Narasi Scroll](scroll-narrative.md) |

Antarmuka yang butuh kendali status presisi, tulis animasinya dengan kode; bila perubahan gambarnya sudah pasti sejak awal, boleh memakai video hasil generate. Yang menampilkan data real-time atau kontrol yang benar-benar dioperasikan orang, tidak boleh digantikan video.

## Feel

Feel animasi diturunkan dari material dan tone arah; beri nama dan pilih parameter dengan “aksi + benda nyata” (stiffness / damping untuk spring):

| Aksi | Referensi benda nyata | Stiffness / damping | Cocok untuk |
| --- | --- | --- | --- |
| Klik | Magnet menempel, buckle, saklar tuas | 350–400 / 10–15 | Tombol, switch, dropdown membuka |
| Meluncur masuk | Penutup pintu pneumatik, damping laci | 250–300 / 20–25 | Panel bawah, drawer, lipatan |
| Mengalir | Menuang madu, kabut menyebar | 150–200 / 30–40 | Transisi halaman, kemunculan visual utama |
| Menghantam jatuh | Palu, benda berat jatuh ke meja | 400–500 / 5–10 | Konfirmasi pilihan, feedback selesai |
| Memantul | Bola karet, trampolin | 300 / 8 | Notifikasi perayaan, produk anak dan game |
| Melayang | Balon helium, serpihan kapas | 100 / 25 | Meditasi, scene fantasi, loop idle |

Material berat (batu, logam, keramik) condong ke klik dan menghantam jatuh; material ringan (kertas, kain, kabut) condong ke melayang dan mengalir; operasi frekuensi tinggi memakai aksi pendek, dan momen brand yang jarang baru memakai yang panjang. Arah yang riuh dan kasar boleh memakai hard cut, lompatan linear 80–150ms, dan drop frame sebagai ekspresi brand yang disengaja; yang dilarang hanyalah easing default yang tidak pernah dipikirkan.

Amplitudo overshoot mengikuti luas area. Halaman penuh dan panel berarea besar, overshoot tidak lebih dari 1–2%, kalau tidak seluruh gambar bergoyang; badge dan tanda centang benda kecil boleh overshoot 10–20% agar terasa elastis. Parameter dengan damping rendah di tabel hanya dipakai untuk benda kecil.

Web bisa menuliskan spring sebagai kurva easing: integrasikan numerik perpindahan berdasarkan stiffness dan damping, ambil 20–30 titik sampel masukkan ke `linear()`, durasi diambil pada saat perpindahan stabil di dalam 0,5% dari titik akhir. Browser yang tidak mendukung mundur ke `cubic-bezier` yang mirip.

## Keterhubungan: biarkan aksi-aksi tersambung

Perubahan yang dipicu satu aksi merambat menyusuri jalur yang sama; titik akhir segmen sebelumnya adalah titik awal segmen berikutnya. Jangan biarkan tombol, panel, dan angka bergerak masing-masing.

- **Berangkat dari tempat yang dioperasikan.** Tekan “Tambah ke tas”, produk mengecil menjadi satu titik dan terbang masuk ke tas, angka di tas melompat sekali; hapus satu baris, ia menguncup ke arah tombol hapus, baris di bawahnya naik mengisi.
- **Satu perpindahan satu arah.** Kartu bergeser ke kiri, judul, nomor, dan warna latar ikut berganti ke kiri; angka menggulir naik, progres juga naik. Begitu arahnya kacau, menjadi beberapa animasi yang tak berhubungan.
- **Protagonis bergerak dulu, sisanya terseret.** Yang terdampak menyusul dalam 40–80ms dengan amplitudo lebih kecil, seperti ditarik oleh protagonis. Semua berlari serentak dengan amplitudo sama hanya terlihat berkedip bersama.
- **Bentuk bertitipan.** Elemen di status sebelumnya menjadi elemen di status berikutnya: tombol mengembang menjadi panel, ikon pencarian memanjang menjadi input, tombol play menjadi pause. Pengguna sekali lihat tahu itu benda yang sama.
- **Cara bergerak dan gambar adalah material yang sama.** Berat-ringannya aksi, jeda, dan pantulan diturunkan dari mesin generatif dan tata bahasa kontrol di kartu arah.

### Sentuhan cerdas dicari dari produk

Sentuhan cerdas membuat satu animasi menceritakan hal khas produk ini sendiri, bukan menambah lagi variasi. Tuliskan dalam satu kalimat: benda apa di produk ini, karena aksi pengguna yang mana, mengalami perubahan yang hanya terjadi padanya.

Bila tak menemukan aksi seperti itu, kerjakan tiga animasi dasar dengan benar; jangan memaksakan. Satu halaman paling banyak satu-dua sentuhan cerdas, animasi lainnya tenang dan pendek.

## Transisi antarmuka

**Kontinu.** Hal yang diklik pengguna adalah protagonis layar berikutnya. Dari daftar masuk detail, item yang diklik membesar menjadi detail, item lain memudar; kembali ia mengecil ke posisi semula, dan halaman kembali ke posisi scroll semula. Bila posisi aslinya sudah keluar viewport, scroll dulu sampai terlihat, baru mengecil kembali.

**Arah konsisten.** Item berikutnya masuk dari kanan, item sebelumnya dari kiri; membuka dan menutup saling berkebalikan; panel samping meluncur masuk-keluar dari sisi tempatnya berada. Animasi dengan arah sembarangan lebih membingungkan daripada tanpa animasi.

**Hanya berubah bentuk, jangan cross-fade.** Mengganti viewport, filter, membuka penjelasan, zoom — pada perubahan seperti ini isinya tetap benda yang sama, yang berubah hanya ukuran dan posisi. Biarkan bingkai luar bermetamorfosis langsung dan konten langsung menampilkan status baru. Cross-fade menumpuk dua gambar dengan skala berbeda dan menghasilkan bayangan ganda. Fade hanya dipakai bila isinya memang berganti.

**Keluar, masuk, dan bertahan dipisah.** Yang dihapus memudar keluar, yang baru masuk memudar masuk, yang bertahan meluncur ke posisi baru. Bila ketiganya memakai fade yang sama, seluruh daftar berkedip serempak.

**Indikator selection memakai satu slider yang berpindah.** Segmented control, tab, item aktif daftar — semuanya memakai bidang dasar yang sama yang meluncur ke posisi baru, bukan yang lama padam dan yang baru menyala. Saat lebar opsinya berbeda, lebarnya ikut bertransisi. Saat pertama tampil, saat jendela di-zoom, dan setelah font selesai dimuat, langsung diletakkan di posisinya; jangan tumbuh dari lebar 0.

**Siapkan dulu tujuannya.** Konten yang harus dimuat di tujuan — misalnya gambar atau halaman ter-embed — dimuat atau pra-render dulu; kalau tidak, animasi berhenti di satu bidang putih. View yang bolak-balik diganti pra-render dan dibiarkan di dalam halaman; saat berganti hanya dipindahkan, tidak dimuat ulang. Fade-in dilakukan setelah konten selesai dimuat, bukan berkedip putih dulu.

**Keluar lebih cepat dari masuk.** Durasi keluar sekitar 60–70% dari masuk, memakai kurva akselerasi; masuk memakai kurva deselerasi atau spring.

**Sampai ujung harus ada feedback.** Saat sudah di item pertama atau terakhir, dorongkan sekali dengan lembut (bolak-balik 10–15px), bukan tanpa reaksi.

### Trade-off stabilitas transisi satu halaman penuh

Pergantian halaman penuh berbeda dari transisi komponen: halaman lama harus di-unload, halaman baru harus di-mount. Dibagi tiga menurut seberapa stabil dan seberapa sulit dibuat:

- **Curtain / wipe.** Satu bidang warna solid, tekstur, atau bentuk geometris menyapu atau menutupi seluruh layar; selagi menutup, halaman lama dilepas dan halaman baru dipasang. Paling sederhana dan paling stabil; struktur kedua halaman bebas tak berhubungan — cocok untuk hampir semua halaman.
- **Overlapping.** Halaman lama dan baru tampil bersamaan di layar, bergeser, saling mendorong, atau fade berlapis. Terlihat mengalir, tetapi DOM kedua halaman harus hidup bersamaan; lapisan dan memorinya harus dikelola baik.
- **Shared element.** Satu elemen kunci bermetamorfosis dari halaman lama terus ke halaman baru — misalnya thumbnail membesar menjadi gambar utama halaman detail. Terlihat paling mulus dan paling rawan bermasalah: dobel-klik cepat, interupsi di tengah, back, atau perubahan viewport semuanya mudah menyebabkan salah posisi dan kedipan; wajib menyediakan jalan mundur — bila bermasalah, langsung tampilkan status final di posisinya.

Splash saat pertama masuk situs boleh menampilkan narasi atau progres pendek selagi menunggu file besar dimuat; perpindahan halaman di dalam situs memakai nilai durasi pergantian halaman penuh pada “Durasi dan amplitudo” di bawah, dan tidak membiarkan transisi menghalangi pengguna melihat isi.

## Durasi dan amplitudo

| Objek | Durasi | Poin |
| --- | --- | --- |
| Tekan, switch, indikator selection | 150–300ms | Saat ditekan mengecil ke 0.96–0.98, efektif seketika saat ditekan (±80ms), memantul kembali saat dilepas |
| Dropdown, bubble, tooltip | 180–250ms | Membuka dari arah pemicunya, skala mulai sekitar 0.96, bukan dari 0 |
| Panel, drawer, sidebar | 250–400ms | Nilai diambil dari jarak gerak; makin jauh makin panjang |
| Pergantian halaman penuh atau view | 350–500ms | Lebih dari 500ms membuat orang menunggu |
| Kemunculan berurutan saat pertama masuk | jeda antar item 40–80ms | Total tidak lebih dari 600ms; hanya diputar saat pertama masuk, tidak diputar ulang saat re-render dan pemulihan status |

Tabel ini mengatur operasi antarmuka. Durasi pertunjukan game dan undian lihat [Permainan](play.md).

Hover terangkat 2–4px, bayangan ikut menguat. Efek hover dengan perpindahan lebih dari 20px terkesan picak.

## Hasil yang tak terlihat harus diucapkan

Bila satu klik menimbulkan efek samping yang tak terlihat — tersalin ke clipboard, tersimpan di background, terkirim — sampaikan hasilnya sendiri dengan satu notifikasi singkat, misalnya “Tersalin: …”, bukan sekadar “berhasil”. Momen konfirmasi seperti selection atau penyelesaian boleh memakai satu pop kecil, hanya diputar saat status berubah pertama kali; tekanan berulang tidak memutar ulang.

## Pengalaman dan performa

Ritme animasi dan kemampuan komponen yang sudah ada di proyek dipakai lebih dulu. Operasi yang sering dilakukan, feedback-nya langsung; jangan biarkan animasi memperlambat hal itu sendiri.

Animasi harus bisa diinterupsi. Saat dioperasikan cepat beruntun, animasi baru melanjutkan dari posisi saat ini, tidak melompat ke awal dan memutar ulang. Transisi CSS berangkat lagi dari nilai saat ini, cocok untuk pergantian frekuensi tinggi; keyframe animation diputar ulang dari awal, cocok untuk kemunculan sekali jalan. Status bisnis diperbarui seketika, tidak menunggu animasi selesai.

Animasi yang berjalan kontinu di web, utamakan hanya menganimasikan transform dan opacity; di dalam transisi hanya tulis properti yang benar-benar berubah. Blok indikator yang sangat kecil boleh langsung mentransisi width-height. Kode yang dieksekusi tiap frame harus punya syarat berhenti dan pembersihan; jangan bolak-balik membaca lalu menulis layout; berhenti saat keluar layar atau tak ada yang dikerjakan. Selama transisi halaman penuh, halaman biasanya tak bisa diklik, jadi transisi halaman penuh harus pendek.

Tempat dengan perpindahan, zoom, atau efek scroll yang mencolok, perlakukan pengguna yang mengaktifkan “reduce motion”: saat itu semua status langsung di posisinya, isinya tidak berkurang sedikit pun. Informasi yang penting dan aksi utama tidak boleh menunggu autoplay, suara, atau animasi selesai baru muncul.

## Periksa animasi

Operasikan sekali dengan kecepatan normal, lalu operasikan mundur sekali dan tekan cepat beberapa kali: tidak ada bayangan ganda dan lompatan, elemen tidak muncul tiba-tiba, tidak terbang dari posisi aneh, tidak terjebak di status tengah. Setelah “reduce motion” aktif, konten langsung terbaca. Frame rate atau perbaikan performa hanya dilaporkan setelah diukur nyata.

## Tips implementasi web

- View transition native browser cocok untuk “benda yang sama berubah dari satu tempat ke tempat lain”: beri nama transisi yang sama pada elemen yang mewakili benda yang sama di status sebelum dan sesudah; nama itu harus unik pada satu saat yang sama.
- Di transisi yang hanya berubah bentuk, sembunyikan snapshot lama dan langsung tampilkan status baru, maka bayangan ganda tidak muncul.
- Pseudo-elemen transisi hanya bisa mengikuti sedikit pseudo-class seperti `:only-child`; menulis `:not(...)` membuat seluruh rule gagal. Bila perlu membedakan rule per skenario, tambahkan satu atribut di elemen root untuk mengganti.
- Halaman ter-embed dan gambar akan terpotong menjadi snapshot di dalam transisi; bila transisi dimulai sebelum tujuan selesai dimuat, hasilnya bidang kosong.
