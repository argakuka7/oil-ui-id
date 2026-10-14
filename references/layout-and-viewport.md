# Tata letak dan viewport

## Rekonstruksi presisi

Catat dulu ukuran viewport yang sesuai gambar referensi atau ukuran piksel yang diketahui, cakupan lengkap gambar, serta area mana yang dipatok tidak bergerak. Jumlah piksel gambar bukan ukuran viewport — misalnya gambar 2× harus dibagi dua; bila tidak bisa dipastikan, tuliskan berdasarkan asumsi apa kamu bekerja.

Ukur proporsi tiap area utama, elemen mana yang berbagi satu garis perataan, seberapa besar teksnya, bagaimana gambar di-crop, dan hubungan antar jaraknya. Samakan dulu posisi keseluruhan, proporsi, dan fontnya, baru menangani border, bayangan, dan detail; tugas rekonstruksi tidak mengeksplorasi ulang gaya.

Bandingkan perbedaannya dengan viewport yang sama seperti referensi dan konten yang mirip. Layar sempit dan status lain yang tidak ada di referensi dilengkapi sesuai kebutuhan konten, dan ditandai mana yang direkonstruksi mengikuti referensi dan mana yang perpanjangan wajar buatanmu sendiri.

Menilai sendiri seberapa mirip hasil rekonstruksinya biasanya terlalu optimis; satu thumbnail halaman penuh pun tak bisa memperlihatkan seberapa jauh melesetnya ukuran font, jarak, dan perataan. Setelah tiap ronde perubahan, gunakan `--compare` milik alat screenshot untuk menghasilkan gambar pembanding (lihat [Alat](tools.md)); perbaiki dulu sel-sel dengan perbedaan terbesar, lalu di gambar overlay periksa garis perataan, ukuran font, dan crop gambar; jangan mengumumkan “sudah direkonstruksi” berdasarkan kesan.

## Fokus verifikasi

Lihat sendiri sekali kondisi konten yang sangat panjang, konten kosong, serta tiap status yang terdampak perubahan ini. Di ponsel, perhatikan perubahan tinggi viewport, keyboard yang muncul, dan safe area layar; aksi utama tidak boleh tertutup keyboard atau bar yang dipatok.

Periksa lagi: apakah halaman meluap horizontal tanpa sengaja, apakah scroll terjadi di blok yang memang seharusnya scroll, apakah focus dan menu terlihat; dan setelah zoom atau penyusunan ulang, apakah urutan membaca dan beroperasi masih jelas.
