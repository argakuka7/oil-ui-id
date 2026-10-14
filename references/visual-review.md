# Protokol dispatch review visual (khusus agent utama)

Agent utama memakai file ini untuk mendispatch review independen. Standar penilaian dan aturan pemeriksaan ada di [Manual reviewer](reviewer-manual.md) dan dibaca oleh reviewer; agent utama tidak membacanya, hanya menyerah terima sesuai daftar di bawah.

## 1. Kapan harus dispatch? Mode apa yang terpicu?

Setelah menyelesaikan satu halaman kunci, satu proposal desain, atau satu perubahan, picu sub-agent review yang sesuai menurut daftar ini:

| Perubahan yang kamu kerjakan | Template prompt sub-agent |
| --- | --- |
| Mengeksplorasi antarmuka baru, atau membongkar kondisi yang ada dan mendesain ulang | `Baca references/reviewer-manual.md, lalu review screenshot-screenshot ini mengikuti standar【Review antarmuka baru dan redesain】, dan berikan skor 1–10.` |
| **Review antarmuka existing**: merapikan, meng-upgrade, memoles, atau mengembangkan di atas antarmuka yang sudah ada | `Baca references/reviewer-manual.md, lalu ikuti standar【Review polesan antarmuka existing】: bandingkan dengan spesifikasi kondisi saat ini yang diberikan, dan tunjukkan titik-titik penyimpangannya. Tanpa skor.` |
| Perubahan kecil, penyetelan jarak tunggal, atau warna | **Tanpa sub-agent**, agent utama memeriksa sendiri dengan konteks yang ada. |

Ganti path di template dengan path absolut di dalam direktori Skill ini: working directory sub-agent bukan direktori ini.

## 2. Sebelum dispatch, “daftar serah terima” yang disiapkan agent utama

Saat memanggil kemampuan eksekusi terisolasi milik host, materi berikut wajib disediakan:
- **Wajib**: screenshot/rekaman layar versi terkini (sebutkan viewport perangkatnya), tugas asli pengguna, serta batasan dan constraint desain; bila ada kartu arah, sertakan kalimat North Star-nya. Constraint keras lain di kartu arah yang perlu diketahui reviewer — misalnya brand mewajibkan wordmark tampil di tiap layar — diringkas satu kalimat ke dalam constraint, tanpa menyerahkan satu kartu arah utuh.
- **Bila ada**: spesifikasi warna proyek existing dan constraint komponen (proyek lama wajib diberikan); catatan pemilihan warna dari kartu arah, yaitu kalimat “dari apa warna ini berasal dalam produk ini” di kolom “Warna”; bila proyek punya `DESIGN.md` atau dokumen desain sejenis, review polesan existing menyerahkan satu dokumen utuh dan menjadikannya standar, sedangkan review antarmuka baru hanya menyaring aset brand dan daftar “jangan lakukan” ke dalam constraint.
- **Peringatan default practices milik alat screenshot**: berikan isian `lint` dari `report.json` apa adanya; butir yang kamu putuskan pertahankan, masing-masing disertai satu kalimat alasan.
- **Jangan diberikan**: source code, pembelaan atas pilihanmu sendiri, dan skor review-review sebelumnya (penilaian harus independen).

Screenshot harus milik versi terkini dan bisa diakses reviewer; status dan animasi yang tidak tersentuh ronde ini boleh mewarisi file bukti ronde sebelumnya, asal dicatat mana yang diwarisi saat serah terima. Halaman panjang menyediakan versi utuh sekaligus potongan lokal yang perlu; gambar detail tidak bisa menggantikan komposisi keseluruhan.

Animasi tidak perlu dibukukan satu per satu: cukup serahkan rekaman layar dari sesi pengambilan bukti itu. Bila reviewer bisa membuka halamannya sendiri, berikan juga alamat halamannya; yang tak terlihat jelas di rekaman akan ia operasikan sendiri.
Bila tidak ada eksekutor terisolasi yang bisa melihat gambar, agent utama memeriksa sendiri dengan manual yang sama dan mencantumkan “belum di-review independen” saat menyerahkan; tanpa gambar nyata, jangan memberi skor visual.

## 3. Cara agent utama memproses feedback reviewer

Setelah sub-agent mengembalikan laporan, revisi menurut prinsip ini:
- **Butir pertama berbunyi “kerjakan ulang”**: kembali ke kartu arah, tetapkan ulang kerangka atau visual utama blok yang disebut namanya; jangan menambal satu per satu.
- **Revisi mengikuti urutan daftar**: daftar masalah direvisi dari yang berdampak paling besar ke bawah; baris “pertahankan” dicatat ke catatan desain dan dijadikan pembanding saat merevisi — jangan justru menghaluskannya.
- **Butir peningkatan juga dikerjakan**: peningkatan kehalusan, rasa desain, dan animasi bukan saran opsional; kerjakan seperti masalah menurut daftar. Yang tak mampu dikerjakan, tuliskan alasannya di catatan penyerahan.
- **Default: hapus** untuk “teks tak berguna yang bisa langsung dihapus” yang didaftar sub-agent, kecuali menghapusnya menimbulkan ambiguitas fungsi.
- **Turunkan ke penyetelan konkret**: tuntutan tingkat tinggi sub-agent (misalnya “terlalu sesak”, “hierarki tak jelas”) diturunkan menjadi penyetelan nyata jarak, ukuran font, dan bayangan. Bila sub-agent mengusulkan mengubah warna brand yang dikunci pengguna atau kerangka besarnya, tuliskan satu kalimat alasan dan jangan diadopsi.
- **Cegah loop tak berujung**: bila opini estetika kedua pihak terkunci saling dorong, berbolak-balik tanpa perbaikan yang terlihat, pertahankan versi yang kamu nilai terbaik dan hentikan loop-nya.
