# Permainan dan kontrol dengan feel kuat

Mini-game, undian, gachapon, petualangan berbasis timer, serta kontrol dengan feel kuat seperti knob, tuas, dan joystick — prosesnya sendiri adalah produknya: pengguna datang menonton roda melambat, koin terdorong jatuh, atau boneka nyaris terjatuh. Antarmuka seperti ini membaca dokumen ini dulu; spesifikasi lainnya tetap berlaku seperti biasa.

## Proses adalah permainan

- Pertunjukan boleh lebih panjang daripada pergantian antarmuka biasa, misalnya tiga roda berhenti bergiliran total sekitar 2 detik; tidak dipangkas mengikuti “lebih dari 500ms membuat orang menunggu”.
- Setelah biaya terpotong dan hasil keluar, simpan dulu: refresh tidak menghilangkannya, biaya tidak terpotong dua kali, dan reward hanya dicairkan satu kali. Pada momen apa disimpan, ditentukan oleh mekanik permainannya.
- Selama pertunjukan, tuliskan jelas operasi mana yang terkunci; tekanan beruntun tidak boleh memotong biaya dua kali.
- Gesture seperti knob dan tuas mengikuti tangan mulai dari posisi ditekan; melewati titik efektif baru dihitung sekali, dan dilepas sebelum sampai tidak dipotong biayanya.
- Saat reduce motion, permainan tetap menghitung hasilnya seperti biasa; hanya gambarnya yang langsung di posisi akhir. Jangan menghentikan permainan itu sendiri.
- Feel dinilai lewat rekaman layar: apakah pelanannya kontinu, apakah berhentinya tersendat, dan dari mana ke mana reward-nya terbang. Tiga frame hanya bisa membuktikan status.

## Aset dan rendering

- Karakter, koleksi, properti, simbol, dan texture material adalah protagonis antarmuka jenis ini, dan default-nya dibuat dengan gambar hasil generate; sebelum mulai, susun dulu daftar asetnya. SVG gambar tangan dan CSS hanya menggambar ikon antarmuka dan bentuk sederhana — memakai keduanya untuk karakter dan properti akan jatuh ke kesan paket ikon. Cara menghasilkan aset set lihat “Aset set” di [Aset](media.md); bila host tak punya kemampuan generate, serahkan brief aset dengan file yang sama dan jangan menyamarkan gambar tangan sebagai hasil akhir.
- Bila keseruannya berasal dari ruang dan fisika, render scene-nya dengan 3D real-time — misalnya menumpuk, bertabrakan, mendorong, berayun, atau material transparan dan logam; gambar hasil generate dipakai sebagai texture dan sprite, caranya lihat “3D real-time” di [Aset](media.md). Perubahan natural seperti pohon tumbuh atau cuaca biasanya lebih baik memakai rangkaian gambar hasil generate.
- Setelah aset masuk scene, lihat sekali lagi: pencahayaannya konsisten dengan scene, ada contact shadow, dan saat bersandar, terbalik, atau jatuh tidak memperlihatkan tepi kertasnya. Gambar sudah jadi bukan berarti langsung terpercaya di dalam scene.
