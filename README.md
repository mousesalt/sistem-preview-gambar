# 🖼️ Sistem Preview Gambar

Aplikasi **web-based image preview** ringan untuk melihat banyak gambar secara cepat langsung dari browser tanpa perlu mengunggah file ke server.

Aplikasi ini dibuat menggunakan **HTML, CSS, dan JavaScript murni (Vanilla JavaScript)** sehingga dapat dijalankan secara lokal maupun melalui GitHub Pages.

## ✨ Fitur Utama

### 🖼️ Mode Klasik

* Menampilkan satu gambar dalam ukuran besar.
* Mendukung pemilihan beberapa gambar sekaligus.
* Thumbnail gambar ditampilkan sebagai navigasi.
* Navigasi menggunakan tombol **← / →** pada keyboard.
* Zoom menggunakan scroll mouse.
* Gambar dapat digeser menggunakan mouse.
* Reset posisi dan zoom saat memilih gambar lain.
* Gambar aktif ditampilkan dalam resolusi penuh.
* Dapat menghapus gambar dari daftar preview.

### 🔲 Grid Multi-File

* Menampilkan banyak gambar dalam bentuk grid.
* Dapat memilih banyak file sekaligus.
* Mendukung pemilihan satu folder.
* Membaca struktur folder melalui `webkitRelativePath`.
* Pencarian berdasarkan nama file.
* Menghapus gambar tertentu dari grid.
* Menampilkan informasi sumber folder.
* Klik gambar untuk membuka preview ukuran besar.

### ⚡ Optimasi Performa

Aplikasi dirancang untuk menangani koleksi gambar dalam jumlah besar.

* Lazy loading menggunakan `IntersectionObserver`.
* Thumbnail dibuat dalam ukuran lebih kecil sebelum ditampilkan.
* Gambar hanya diproses ketika mendekati area layar.
* Pemrosesan file dilakukan secara bertahap.
* `createImageBitmap()` digunakan untuk membantu pemrosesan gambar.
* Object URL yang sudah tidak digunakan dilepas dengan `URL.revokeObjectURL()`.
* Gambar aktif pada Mode Klasik dapat ditampilkan menggunakan resolusi penuh.

### 🎨 Tampilan

* Dark Mode.
* Light Mode.
* Pengaturan tema disimpan menggunakan `localStorage`.
* Tampilan responsif.
* Antarmuka tanpa framework eksternal.

### 📁 Format Gambar

Aplikasi mendukung berbagai format gambar yang didukung browser, termasuk:

* JPG / JPEG
* PNG
* WebP
* GIF
* BMP
* SVG

> Dukungan format tertentu tetap bergantung pada kemampuan browser yang digunakan.

---

## 🚀 Demo

**Live Demo:**
https://mousesalt.github.io/sistem-preview-gambar/

> Jika GitHub Pages belum diaktifkan, buka repository → **Settings → Pages** kemudian pilih branch `main` dan folder `/root`.

---

## 💻 Cara Menjalankan

### Cara 1 — Langsung dari Browser

Download atau clone repository:

```bash
git clone https://github.com/mousesalt/sistem-preview-gambar.git
```

Masuk ke folder:

```bash
cd sistem-preview-gambar
```

Kemudian buka:

```text
index.html
```

menggunakan browser.

Tidak diperlukan:

* Node.js
* npm
* database
* PHP
* server backend
* framework

---

## 🌐 Menjalankan dengan Local Server

Jika ingin menggunakan local server, salah satu cara paling mudah adalah menggunakan **VS Code + Live Server**.

1. Buka folder repository di VS Code.
2. Install extension **Live Server**.
3. Klik kanan `index.html`.
4. Pilih **Open with Live Server**.

---

## 🧭 Cara Menggunakan

### Mode Klasik

1. Buka aplikasi.
2. Pilih **Mode Klasik**.
3. Pilih satu atau beberapa gambar.
4. Pilih gambar melalui thumbnail.
5. Gunakan scroll mouse untuk zoom.
6. Drag gambar untuk menggeser posisi.
7. Gunakan tombol panah kiri/kanan untuk berpindah gambar.

### Grid Multi-File

1. Pilih **Grid Multi-File**.
2. Pilih beberapa file atau satu folder.
3. Tunggu proses thumbnail.
4. Gunakan kotak pencarian untuk mencari nama file.
5. Klik gambar untuk melihat preview besar.
6. Gunakan tombol **Hapus** untuk menghapus gambar dari tampilan.

---

## 🔒 Privasi

Aplikasi ini dirancang untuk bekerja secara **client-side**.

File gambar yang dipilih pengguna diproses langsung oleh browser dan tidak memerlukan proses upload ke server aplikasi.

Artinya aplikasi ini cocok digunakan untuk preview gambar yang bersifat pribadi atau sensitif selama dijalankan pada perangkat pengguna.

> Tetap perhatikan keamanan browser dan lingkungan tempat aplikasi dijalankan.

---

## 🛠️ Teknologi

Aplikasi dibuat menggunakan:

| Teknologi              | Penggunaan          |
| ---------------------- | ------------------- |
| HTML5                  | Struktur aplikasi   |
| CSS3                   | Tampilan dan layout |
| JavaScript             | Logika aplikasi     |
| Canvas API             | Pembuatan thumbnail |
| File API               | Membaca file lokal  |
| Blob URL               | Preview file        |
| `createImageBitmap()`  | Pemrosesan bitmap   |
| `IntersectionObserver` | Lazy loading        |
| `localStorage`         | Penyimpanan tema    |

Tidak menggunakan framework JavaScript maupun backend.

---

## 📂 Struktur Project

```text
sistem-preview-gambar/
│
├── index.html
├── README.md
├── LICENSE
├── .gitignore
│
└── screenshots/
    ├── landing.png
    ├── mode-klasik.png
    └── mode-grid.png
```

---

## ⚙️ Persyaratan

Browser modern yang mendukung API web seperti:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

Disarankan menggunakan browser versi terbaru untuk kompatibilitas terbaik.

---

## 📌 Catatan Performa

Untuk koleksi gambar yang sangat besar, performa tetap bergantung pada:

* jumlah file
* resolusi gambar
* ukuran file
* RAM perangkat
* kemampuan browser
* CPU/GPU perangkat

Aplikasi menggunakan thumbnail dan lazy loading untuk mengurangi beban pemrosesan ketika menangani banyak gambar.

---

## 🔮 Rencana Pengembangan

Beberapa fitur yang dapat dikembangkan selanjutnya:

* [ ] Drag & drop file
* [ ] Drag & drop folder
* [ ] Fullscreen preview
* [ ] Rotasi gambar
* [ ] Tombol zoom in / zoom out
* [ ] Download gambar
* [ ] Copy gambar
* [ ] Sorting berdasarkan nama file
* [ ] Sorting berdasarkan ukuran file
* [ ] Sorting berdasarkan tanggal
* [ ] Filter berdasarkan format
* [ ] Informasi metadata gambar
* [ ] EXIF viewer
* [ ] Slideshow
* [ ] Navigasi gambar pada modal
* [ ] Virtualized rendering untuk koleksi gambar sangat besar
* [ ] PWA / installable web app

---

## 🤝 Kontribusi

Kontribusi sangat terbuka.

1. Fork repository.
2. Buat branch baru:

```bash
git checkout -b fitur-baru
```

3. Lakukan perubahan.
4. Commit:

```bash
git add .
git commit -m "Menambahkan fitur baru"
```

5. Push:

```bash
git push origin fitur-baru
```

6. Buat Pull Request.

---

## 📄 Lisensi

Project ini dapat menggunakan lisensi **MIT License**.

Lihat file [`LICENSE`](LICENSE) untuk informasi lengkap.

---

## 👨‍💻 Pengembang

**Faridzoel Mossal / mousesalt**

GitHub:
https://github.com/mousesalt

Repository:
https://github.com/mousesalt/sistem-preview-gambar

---

## ⭐ Dukungan

Jika project ini bermanfaat, silakan berikan ⭐ **Star** pada repository.

Terima kasih telah menggunakan **Sistem Preview Gambar**.
