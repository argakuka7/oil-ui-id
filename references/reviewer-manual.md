# Manual review visual dan interaksi (khusus sub-agent)

Manual ini dibaca oleh reviewer independen. Reviewer tidak ikut serta dalam pembuatan, dan hanya me-review berdasarkan screenshot terkini serta constraint yang diserahkan agent utama; skor diberikan mengikuti anchor di bagian 1, dan bila ragu, ambil tingkat yang lebih rendah.

Hanya memberikan review, tidak mengubah file, tidak memicu reviewer lain. Bedakan cacat yang terlihat dan preferensi gaya pribadi; bila tidak ada masalah yang jelas, katakan langsung — jangan mengarang revisi sekadar mengejar jumlah. Hal yang tidak terlihat atau tak bisa diverifikasi wajib dituliskan; dengan screenshot statis saja, jangan mengklaim animasi atau alur operasi sudah lulus.

## 1. Review antarmuka baru dan redesain (berskor)

**Sudut pandang review**: angkat standarnya, dan jadikan “bagaimana tim paling top di genre ini akan mengerjakannya” sebagai penggarisnya.

0. **Uji tiga detik (sebelum semua detail dan alur)**: kecilkan layar pertama ke lebar 480px (screenshot ponsel ke 180px), lihat tiga detik; lalu lihat versi tanpa teks tiga detik, dan tuliskan dua kalimat: produk seperti apa dari tahun berapa yang terasa; apa yang pertama terlihat, dan apakah hal itu tetap sah bila dipindah ke produk lain. Bila terasa produk generik bertahun lalu, default library komponen, atau gambar stok, tuliskan langsung dan skor total tidak melebihi 7; bila hal pertama yang terlihat tetap sah di produk mana pun, kekhasannya gagal. Bila bisa memakai alat screenshot, pakai untuk menghasilkan thumbnail dan versi tanpa teks.
1. **Uji kategori dan tolok ukur**: sebutkan dalam satu kalimat ini kategori apa (misalnya panel admin B2B, landing page pameran), dan bagaimana produk tolok ukur kategori itu membangun layar pertamanya. Tunjukkan bagian gambar yang melanggar konsensus kategori, dan nilai apakah itu inovasi yang disengaja atau menempel template default model. Bila bisa ditemukan, bandingkan berdampingan dengan satu-dua gambar nyata produk top sejenis, dan jelaskan di mana gap material, tekstur, dan tingkat penyelesaian scenenya.
2. **Default model (poin pengurang)**:
   - Dua kolom default “judul besar di kiri + penjelasan/gambar di kanan” tanpa alasan.
   - Kartu membulat di mana-mana, dan tiap lapisan diberi garis kotak (tempat yang sudah dipisahkan ruang kosong tetap diberi garis, membuat gambar terpecah-pecah).
   - Memberi kartu biasa atau kotak notifikasi satu garis sisi warna tebal sebagai dekorasi; item aktif sidebar dan garis kutipan body text tidak termasuk.
   - Gradasi, glow, dan ikon emoji tanpa alasan.
   - Copy metaforis yang kosong atau mengambang.
   - Palet tanpa dasar produk: baru dikurangi poin bila terhadap catatan pemilihan warna atau aset brand di serah terima tak bisa dijelaskan hubungannya dengan produk, dan sekadar menempel warna template yang paling lazim di kategori; hitam-putih-abu atau hue klasik dengan alasan yang berdiri tidak dikurangi.
   - Font dan aset terasa tua: system font dengan letter-spacing dibuka dijadikan wordmark atau judul; beberapa system font bergantian menyamar sebagai brand berbeda; seluruh rasa brand hanya bertumpu pada satu tombol warna solid jenuh; gambar hasil generate berkesan stok generik dan tak terasa milik produk ini.
   - Bila agent utama menyertakan “peringatan default practices” milik alat screenshot, periksa satu per satu apakah masih ada di layar. Yang masih ada dan tak diberi alasan di serah terima dikurangi sesuai bagian ini; yang diberi alasan, nilai apakah alasannya berasal dari produk ini.
   - Wordmark brand menggusur ruang tugas yang sedang berjalan: aplikasi menaruh logo plus nama produk di pojok kiri atas tiap layar, atau di bawah bar brand ditumpuk lagi satu baris judul halaman — kurangi poin. Landing page web, situs resmi, dan situs dokumentasi menaruh identitas di kiri atas tidak dikurangi; nameplate benda nyata di dalam gambar adalah bagian scene; bila agent utama menuliskannya sebagai requirement brand di constraint serah terima, tidak dikurangi.
3. **Pemeriksaan animasi (lihat bergerak atau tidak, bukan mengaudit kelengkapan bukti)**: tonton rekaman layar dengan kecepatan normal; bila tak terlihat jelas atau tidak ada, buka halamannya dan operasikan sendiri sekali. Hanya menilai apakah tempat yang seharusnya bergerak benar bergerak:
   - Apakah aksi utama punya feedback; apakah satu perpindahan status punya asal yang terlihat; apakah masuk pertama kali ada kemunculannya.
   - Landing page, halaman brand, halaman peluncuran, dan halaman pameran diperiksa dua hal lagi: apakah tiap section muncul sesuai isinya — satu halaman penuh fade-in naik yang seragam dihitung belum mengerjakan; dan apakah ada sedikitnya satu segmen narasi di mana protagonis berubah mencolok mengikuti scroll — satu titik bergerak menyusuri garis atau node menyala satu per satu dihitung belum mengerjakan.
   - Produk mini-game, undian, dan petualangan timer: tiga animasi dasar hanya garis bawahnya; periksa lagi “proses adalah permainan” dan “aset dan rendering” sesuai [Permainan](play.md).
   - Yang benar-benar tidak dikerjakan dituliskan ke masalah. Yang dikerjakan, bagus-tidaknya dinilai di butir “peningkatan: animasi”, tidak dibahas di sini.
   - Jangan membongkar rekaman per frame dan jangan mengaudit file bukti. Bila rekaman dan screenshot tidak cocok, atau cacatnya hanya terlihat di frame tertentu, yang berlaku adalah yang terlihat pada kecepatan normal. Bila hanya ada screenshot statis dan halaman tak bisa dibuka, tuliskan satu kalimat “animasi tidak terlihat”, jangan menduga.
4. **Peningkatan: kehalusan, rasa desain, animasi**: halaman yang cacatnya nol sering kali baru “cukup”. Tiga butir ini dilihat satu per satu, dan hanya dituliskan bila ada gap yang terlihat; tiap butir menuliskan posisi, level saat ini, dan seperti apa yang dihitung sampai; butir yang memang tidak ada, tulis “tidak ada” beserta dasarnya. Peningkatan adalah mengerjakan yang sudah ada lebih baik, bukan menambah hal baru. Bila butir pertama berbunyi “kerjakan ulang”, peningkatan tidak ditulis.
   - **Kehalusan**: zoom ke 200%, komponen atau tata letak mana yang paling terlihat kasarnya: letter-spacing dan line-height, keselarasan ikon dengan teks, bayangan dan stroke, apakah tiap status konsisten; lalu di 100% periksa pemenggalan baris, kata yatim, dan format angka.
   - **Rasa desain**: apakah protagonis terlihat di thumbnail 480px dan seberapa besar porsinya; bagian mana yang paling mendekati level terbaik kategorinya dan apa yang masih kurang; bagian mana yang masih tampak default library komponen. Bila semua tempat cukup tetapi tak ada satu pun yang membekas, tuliskan di sini, dan tunjukkan satu tempat yang paling layak difokuskan.
   - **Animasi**: jangan hanya lihat ada-tidaknya. Bagian mana yang bergerak mekanis: kecepatan seragam, bergerak sendiri-sendiri, satu halaman penuh fade-in naik, tak tersambung dengan operasi; bagian mana yang paling layak diberi feel sehingga orang ingin mengoperasikannya lagi atau menggulirnya sekali lagi. Feel ditulis dengan “aksi + referensi benda nyata”, bukan kata sifat.
5. **Peringkasan dan cacat**:
   - Teks pengisi: huruf kecil yang dimasukkan demi menyeimbangkan dua ujung layout — misalnya kalimat pendek yang terdengar puitis tapi tak menunjuk objek, aksi, atau data mana pun — atau catatan desain yang ditulis di antarmuka. Sebutkan satu per satu dan minta dihapus.
   - Daftarkan secara eksplisit teks tak berguna lain yang bisa langsung dihapus (misalnya “contoh”, “perlu verifikasi”, “antarmuka sistem”).
   - Di luar teks, daftarkan juga panel, data, dan dekorasi yang seharusnya dihapus atau digabung: tiap layar hanya satu protagonis, yang berlebih disebutkan satu per satu. Setelah dihapus protagonis tidak membesar-menguat dan gambar hanya menjadi kosong — itu juga dihitung masalah.

Periksa apakah komposisi, font, aset, dan interaksi semuanya menyambut North Star desain. Untuk halaman alat, panel admin, dan penjelajahan konten, jelaskan jumlah objek di layar pertama, posisi baris konten pertama, serta jarak aksi utama dari objek saat ini, dan bandingkan kepadatannya dengan produk sekelas yang bagus.

Karya referensi adalah baseline arah dan kualitas, bukan tuntutan menyalin; tugas rekonstruksi presisi mengikuti gambar referensi yang diberikan. Bila ada screenshot karya sekelas bagus, boleh diurutkan bersama gambar saat ini menurut tingkat penyelesaiannya beserta penjelasan gap-nya. Media pinjaman hanyalah sumber gaya; jangan menambah komponen tak berguna demi “lebih mirip”.

**Requirement output**:

- Tulis masalah dulu, baru peningkatan. Masalah hanya menuliskan yang menghambat tugas, tak terbaca, atau jelas merupakan default model, diurutkan dari dampak terbesar, maksimal 5 butir; peningkatan maksimal 5 butir, dan ketiga aspek — kehalusan, rasa desain, animasi — semuanya wajib bersuara. Tiap butir menuliskan posisi, bukti yang diamati, dampaknya, hasil yang harus dicapai setelah diperbaiki, dan cara verifikasinya. Cara perbaikan hanya menuliskan targetnya; jangan menentukan komposisi pihak pembuat, jangan mengatur berapa objek atau data yang diletakkan, dan jangan menyarankan menambah fitur atau volume data demi kesan nyata; bila menuntut elemen baru apa pun, di butir yang sama tuliskan apa yang harus dihapus untuk memberi ruang; masalah yang lebih kecil digabung menjadi satu kalimat di bagian akhir. Agent utama akan merevisi mengikuti urutan ini dan di ronde berikutnya memeriksa ulang dengan daftar ini, jadi tiap butir harus tertulis sampai tingkat yang perubahannya bisa terlihat setelah diperbaiki.
- Bila kerangka layar pertama masih template default model, atau visual utamanya jauh di bawah level kelasinya sehingga skornya jatuh ke 6 ke bawah, butir pertama menuliskan “Kerjakan ulang: …”, menyebutkan blok yang harus dikerjakan ulang dan alasannya, tanpa lagi memberi saran tambalan untuk blok itu. Menambal di atas kerangka yang sudah dinilai buruk hanya membuatnya terlihat lebih rapi.
- Baris kedua terakhir menuliskan “Pertahankan: …”, menyebutkan satu-dua hal yang tidak boleh terhaluskan saat merevisi — biasanya bagian paling khas dari arah ini.
- Baris terakhir memberikan skor total 1–10.

Skor diberikan mengikuti anchor di bawah: lihat tugas dulu, baru visualnya; masalah yang bisa menghilangkan data, menghentikan alur, atau menipu pengguna dengan “berhasil” dikurangi lebih dulu daripada masalah visual apa pun. Seluruh tugas bisa dilalui pun belum berarti 8; visual utamanya juga harus lolos ambang.

| Skor | Ambang |
| --- | --- |
| 10 | Tak bisa ditemukan cacat yang teramati, dan minimal ada satu praktik baik yang belum pernah terlihat di kategori ini |
| 9 | Alur utama, status abnormal, dan detail semuanya sah; peningkatan tinggal bagian kecil; minimal satu hal mencapai level terbaik kategorinya |
| 8 | Arahnya tegas, alur utama bisa dilalui, tanpa penghambatan dan kehilangan data; bila halaman punya visual utama atau aset kunci, tingkat penyelesaiannya mencapai produk kelas satu sejenis; masih dikenali sebagai karya mana saat dikecilkan ke 480px; ada beberapa masalah sedang |
| 7 | Arahnya berdiri, tetapi ada satu masalah yang membuat pengguna kehilangan data, salah jalan, atau macet; atau struktur layar pertamanya masih membawa default model yang mencolok; atau visual utamanya berhenti di level vektor gambar tangan, pseudo-perspektif datar, atau teks pengganti bentuk; atau di uji tiga detik terasa produk generik dari suatu tahun |
| 5–6 | Arahnya terlihat, tetapi kerangkanya template default model, atau alur utamanya macet di banyak tempat |
| 1–4 | Tugas utama tak bisa dilalui, atau gambar memiliki kesalahan dasar seperti tumpang-tindih, terpotong, atau tak terbaca |

Skor dituliskan pada anchor-nya, dan berikan “apa yang masih kurang untuk naik satu tingkat” — ditulis dari kehalusan, rasa desain, dan animasi, bukan “tambahkan satu status lagi”.

Penilaian wajib menyertakan gap yang konkret; angka dari model berbeda tidak dibandingkan langsung, dan penilaian pengguna berlaku lebih dulu. Jangan menebak file dan nomor baris yang tidak ada.

## 2. Review polesan antarmuka existing (hanya keselarasan standar, tanpa skor)

**Sudut pandang review**: jangan membayangkan gaya idemu; ikuti dengan ketat spesifikasi desain yang sudah ada pada produk ini (palet, jarak).

Agent utama menyediakan spesifikasi tertulis atau spesifikasi kondisi saat ini yang disarikan dari variabel desain, komponen bersama, dan halaman sejenis, beserta hal-hal yang tidak boleh diubah: brand, font, warna utama, library komponen, dan navigasi. Bila kondisinya tidak konsisten, ikuti praktik mayoritas dan catat praktik minoritas sebagai perlu diseragamkan; bila spesifikasinya sendiri bermasalah, daftarkan terpisah dan serahkan keputusannya ke pengguna.

1. **Pemeriksaan penyimpangan spesifikasi**: tunjukkan satu per satu di mana gambar saat ini memakai warna/ukuran font/radius di luar spesifikasi, atau mengarang komponen sendiri padahal komponen yang sudah ada tersedia.
2. **Layout dan struktur**: dalam batas spesifikasi, tunjukkan tiga masalah yang paling memengaruhi tingkat penyelesaian (hierarki, perataan, ruang kosong, pengurangan).
3. **Pemeriksaan animasi**: lihat apakah animasi yang terdampak perubahan ini cukup dan apakah animasi yang lama justru dirusak; bila pengguna meminta eksplisit atau seluruh halaman di-upgrade, periksa lagi seluruh halaman sesuai “Pemeriksaan animasi” di bagian 1.
4. **Requirement output**: hanya memberikan saran perbaikan objektif, dan mendaftarkan teks yang bisa dikurangi. **Tanpa skor**. Jangan menyarankan mengganti warna brand atau font secara menyeluruh.
