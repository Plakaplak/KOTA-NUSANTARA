# BRI Virtual City · Kota Nusantara

Prototipe interaktif berbentuk satu halaman web: berjalan-jalan bebas di kota Indonesia bergaya isometrik biru senja. Tidak ada misi atau poin, hanya menjelajah.

> **Catatan:** semua nama tempat, merek, dan layanan di dalam kota bersifat fiktif dan hanya untuk keperluan prototipe. Warga yang kamu ajak ngobrol adalah karakter simulasi, bukan pengguna sungguhan.

## Fitur

- **Pilih avatar** dari 12 karakter, lalu **ubah nama** (maksimal 14 huruf, tersimpan di browser).
- **Jalan-jalan bebas** dengan joystick, keyboard, atau ketuk di peta.
- **Naik kendaraan:** motor, taksi, bajaj, becak, angkot, bus kota, perahu, kapal pinisi, dan kereta komuter. Kendaraan bisa dipanggil dari menu.
- **Masuk gedung:** bank, hotel, museum, kafe, pasar, pusat belanja, masjid, dan dek pandang Menara Brilian, masing-masing dengan interior dan keterangan benda.
- **Ganti baju** dengan menu mirip game Roblox. **Dresscode:** Jas, Kaos, dan Jaket Mantri, plus set, atasan, bawahan, sepatu, topi, aksesori, rambut, dan warna kulit.
- **Ngobrol** dengan warga simulasi: balon ucapan di atas kepala, jendela chat, kalimat cepat, dan balasan otomatis.
- **Emote, lompat, dan klakson.**
- **Waktu:** senja, malam, dan siang.
- **Responsif** untuk HP (potret dan lanskap), tablet, dan desktop.

## Kontrol

| Aksi | Layar sentuh | Keyboard |
| --- | --- | --- |
| Jalan / mengemudi | Joystick kiri bawah, atau ketuk tanah | WASD / panah, atau klik tanah |
| Masuk gedung / naik / turun | Tombol kuning | `E` |
| Lompat / klakson | Tombol panah di kanan bawah | `Spasi` |
| Menu Jelajah | Tombol **Jelajah** | `J` |
| Kendaraan / Baju / Emote | Tiga tombol bulat | `V` / `B` / `G` |
| Profil dan nama | Tab **Profil** | `P` |
| Ngobrol | Tombol **Ngobrol** | `T` |
| Zoom | Cubit, atau tombol + dan − | Roda mouse, `+` / `-` |

## Menjalankan di komputer

Tidak perlu build atau instalasi. Buka `index.html` di browser, atau jalankan server lokal:

```bash
python3 -m http.server 8000
# lalu buka http://localhost:8000
```

## Publikasi dengan GitHub Pages

1. Buat repositori baru di GitHub, lalu unggah semua isi folder ini (`index.html`, `README.md`, `.nojekyll`, `.gitignore`).
2. Buka **Settings → Pages**.
3. Pada **Build and deployment**, pilih **Deploy from a branch**, lalu cabang `main` dan folder `/ (root)`, kemudian **Save**.
4. Setelah satu atau dua menit, halaman tersedia di `https://<nama-akun>.github.io/<nama-repo>/`.

Dengan Git dari terminal:

```bash
git init
git add .
git commit -m "Kota Nusantara: prototipe awal"
git branch -M main
git remote add origin https://github.com/<nama-akun>/<nama-repo>.git
git push -u origin main
```

## Catatan teknis

- Satu berkas HTML mandiri (HTML, CSS, dan JavaScript), tanpa dependensi dan tanpa permintaan jaringan.
- Dirender dengan Canvas 2D (proyeksi isometrik 2:1). Avatar dan benda kota digambar dengan kode.
- Nama pemain disimpan di `localStorage` dengan kunci `briCityNick`. Tidak ada data yang dikirim ke server.
- Kualitas gambar menyesuaikan otomatis bila perangkat terasa berat.
- Chat adalah simulasi lokal. Chat antarpengguna sungguhan memerlukan server (misalnya WebSocket) dan belum ada di prototipe ini.

## Lisensi

Belum ditentukan. Tambahkan berkas `LICENSE` sesuai kebutuhan sebelum repositori dibuat publik.
