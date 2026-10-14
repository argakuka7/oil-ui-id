# Halaman perbandingan gaya

Letakkan beberapa kandidat berdampingan di satu halaman untuk dipilih pengguna. Pengguna bisa melihat berdampingan atau per kandidat, membuka ukuran asli, memilih, dan menyalin arahnya. Cangkang halaman perbandingan hanya bertugas membandingkan dan memilih; ia tidak membawa kecenderungan gaya dan tidak dijadikan rujukan kandidat.

Konten inti, aksi utama, dan pengguna target para kandidat tetap konsisten; yang berubah adalah komposisi, cara informasi diorganisasikan, karakter font, relasi warna, kepadatan, dan cara memakai gambar. Berapa banyak kandidat diletakkan, tergantung berapa yang diminta pengguna dan berapa yang benar-benar berbeda; jangan menggandakan seluruh produk sekadar mengejar jumlah.

## Siapkan input

Satu ronde hanya menghasilkan satu halaman perbandingan. Kandidat yang bisa berjalan memakai halaman nyata: mockup HTML yang ditulis terpisah di-embed langsung, proposal di dalam proyek memakai alamat localhost, dan screenshot hanya dipakai bila halaman yang bisa dijalankan tak tersedia. Satu proposal, satu gambar: proyek existing memilih pintu masuk atau langkah yang paling berbeda; proposal satu situs hanya meletakkan halaman representatifnya.

Di satu direktori letakkan `manifest.json` beserta file kandidat. Gambar, font, dan video yang dirujuk kandidat juga diletakkan di direktori itu atau subdirektorinya, dirujuk dengan path relatif, dan generator akan meng-inline-nya ke halaman perbandingan. Manifest minimal ditulis seperti ini, isi bagian dalam tanda siku dengan isi nyata kandidat ronde ini, dan arahnya mengikuti yang tertulis di kartu arah:

```json
{
  "schemaVersion": 1,
  "project": "<nama proyek>",
  "brief": "<isi dan tugas utama yang diekspresikan bersama semua kandidat>",
  "round": "<ronde, misalnya 01>",
  "candidates": [
    {
      "id": "<identitas unik huruf kecil>",
      "name": "<nama arah>",
      "concept": "<North Star: satu kalimat niat pengalaman yang memandu trade-off>",
      "typography": "<font family, weight, dan hubungan skala yang benar-benar dipakai>",
      "palette": ["<nilai hex>", "<nilai hex>", "<nilai hex>"],
      "traits": ["<karakteristik teramati>", "<karakteristik teramati>"],
      "source": "<path relatif file kandidat>"
    }
  ]
}
```

| Kondisi | Yang ditambahkan ke manifest |
| --- | --- |
| Antarmuka berkanvas tetap, tidak menyusun ulang mengikuti lebar | Tulis `"nativeViewport": "<lebar>x<tinggi>"` di level atas atau di kandidat. Halaman perbandingan merender dengan viewport itu lalu menskalakan seluruhnya secara proporsional; kandidat tak perlu menulis skalanya sendiri |
| Mockup interaktif buatan sendiri | Kandidat ditambah `"interactive": true` |
| Halaman proyek yang harus dijalankan dulu | `kind` kandidat diset `"url"` dengan `url` menunjuk dev server lokal; level atas menuliskan perintah start di `serve` |
| Mengubah halaman yang sudah ada | Masukkan juga kondisi saat ini, ditambah `"baseline": true` |
| Hanya punya screenshot | `kind` kandidat diset `"image"` |

Cara menulis dan batasan tiap field lihat `--help` milik generator.

## Generate dan buka

```text
<python> <skill>/scripts/build_explorer.py <direktori manifest>/manifest.json
```

Halaman perbandingan dihasilkan di samping manifest dengan nama file `style-explorer.html`. Bila ada kesalahan tulis, generator mendaftarkan sekaligus semua yang harus diperbaiki; perbaiki sesuai daftar lalu jalankan lagi; bila file bernama sama sudah ada, tambahkan `--force`. Bila generator tidak bisa dijalankan, biarkan manifest dan kandidat untuk dilihat langsung oleh pengguna, dan nyatakan bahwa halaman perbandingan belum dirakit; jangan mengarang alat pengganti dadakan.

Bila ada kandidat berbasis localhost, saat menyerahkan biarkan dev server tetap menyala. Setelahnya pengguna berkata “buka halaman perbandingan”: baca `serve` di dalam manifest, jalankan `command` di background pada `cwd`, tunggu sampai `url` bisa diakses, baru buka halaman perbandingannya.

## Mencatat pilihan

Saat pengguna menekan “Pilih”, satu kalimat tersalin, misalnya “<ronde>: pilih 03 <nama arah>”. Setelah pengguna menempelkannya atau langsung menyebutkan pilihannya, cocokkan ronde dan nomornya dengan manifest saat ini untuk memastikan itu ronde yang benar, perbarui pilihan dan catatannya ke catatan desain, lalu kembali ke alur yang menghasilkan halaman perbandingan ini dan lanjutkan pekerjaan. Halaman perbandingan tidak menulis balik ke file mana pun, dan tidak mengirim pesan otomatis ke agent.

Sebelum menyerahkan, cocokkan kandidatnya: tiap gambar sesuai dengan halaman, status, dan viewport yang tertulis di manifest, dan font yang dipakai benar-benar ter-render (bukan fallback default). Untuk menilai ukuran teks dan detail, gunakan “ukuran asli 100%” pada mode per kandidat; gambar kecil yang menyesuaikan jendela tidak boleh dijadikan dasar lolos keterbacaan. Fungsi halaman perbandingan sendiri dijamin oleh test bawaan Skill; di dalam tugas tidak perlu diverifikasi dan tidak perlu membaca source template-nya.
