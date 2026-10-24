# Portofolio Putri Christianti Harefa

Situs portofolio satu halaman (`index.html`) yang bisa langsung dipasang di GitHub Pages. Tidak perlu instalasi apa pun.

## Isi folder repositori

```
username.github.io/
├── index.html
├── README.md
└── images/
    ├── foto-diri.jpeg
    ├── pengalaman-pln-1.jpeg
    ├── pengalaman-pln-2.jpeg
    ├── pengalaman-asisten-lab.jpeg
    ├── proyek-buck-chopper.jpeg
    ├── proyek-pembersih-panel-surya.jpeg
    ├── proyek-inverter-5-level.jpeg
    ├── proyek-plc-scada-1.jpeg
    ├── proyek-plc-scada-2.jpeg
    ├── sertifikat-1.png
    └── sertifikat-2.png
```

Bagian Organisasi & Kepanitiaan tidak memakai gambar.

---

## Cara 1: Lewat browser (paling mudah, tanpa Git)

1. Masuk ke [github.com](https://github.com) dan buat akun jika belum punya.
2. Klik tombol **+** di kanan atas, lalu **New repository**.
3. Isi **Repository name** dengan `USERNAME.github.io` (ganti `USERNAME` dengan username GitHub-mu, huruf kecil semua). Contoh: `putrichristianti.github.io`.
4. Pilih **Public**, lalu klik **Create repository**.
5. Klik **uploading an existing file**, lalu seret `index.html` dan `README.md` ke halaman itu. Klik **Commit changes**.
6. Buat folder gambar: klik **Add file → Create new file**, ketik `images/.gitkeep` pada kolom nama, lalu **Commit changes**.
7. Buka folder `images`, klik **Add file → Upload files**, lalu unggah semua foto dengan nama persis seperti daftar di atas. Klik **Commit changes**.
8. Tunggu 1 sampai 3 menit, lalu buka `https://USERNAME.github.io`. Portofolio sudah online.

> Jika repositori **tidak** bernama `USERNAME.github.io`, aktifkan Pages manual: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**. Alamatnya menjadi `https://USERNAME.github.io/NAMA-REPO/`.

---

## Cara 2: Lewat Git (terminal)

```bash
git clone https://github.com/USERNAME/USERNAME.github.io.git
cd USERNAME.github.io

# salin index.html dan folder images ke sini, lalu:
git add .
git commit -m "Tambah portofolio"
git push origin main
```

---

## Cara mengubah isi

Buka `index.html` (di GitHub: klik file, lalu ikon pensil). Cari tulisan `EDIT DI SINI` di bagian `<script>`. Semua konten ada di empat daftar berikut.

| Daftar | Isi |
|---|---|
| `EXPERIENCE` | Pengalaman kerja/magang (dengan foto) |
| `ORGS` | Organisasi & kepanitiaan (tanpa foto) |
| `PROJECTS` | Proyek (dengan foto) |
| `CERTS` | Sertifikat (dengan gambar) |
| `SKILLS` | Keahlian |

### Menambah proyek baru

Salin satu blok proyek, tempel setelah blok terakhir (jangan lupa koma di antara blok), lalu ganti isinya:

```js
{title:"Judul proyek",date:"Jan 2026 – Mar 2026",role:"Peran kamu",img:"images/proyek-baru.jpg",
 points:["Apa yang kamu kerjakan.","Hasil atau kontribusimu."],
 tags:["PLC","SCADA"]},
```

### Menambah sertifikat

```js
{title:"Nama sertifikat",issuer:"Penerbit · 2026",img:"images/sertifikat-3.jpg"},
```

### Mengganti foto

Cukup unggah foto baru ke folder `images/` dengan **nama yang sama**, atau ubah nilai `img` di `index.html` agar sesuai nama file barumu.

---

## Tips gambar

- Ekstensi file bebas: halaman otomatis mencoba `.jpg.jpeg`, `.jpeg`, `.jpg`, `.png`, dan `.webp`. Yang penting nama sebelum ekstensi sama persis (misalnya `foto-diri`).
- Gunakan format `.jpg` atau `.webp`, ukuran sebaiknya di bawah 500 KB per file supaya halaman cepat dimuat.
- Rasio yang pas: foto diri 3:4 (potret), pengalaman 16:9 (1 foto) atau 4:3 (2 foto), sertifikat 4:3, proyek 16:10.
- Nama file bersifat **huruf besar-kecil** (case sensitive). `Foto-Diri.JPG` tidak sama dengan `foto-diri.jpg`.
- Hindari spasi pada nama file. Pakai tanda hubung (`-`).
- Jika gambar tidak muncul, yang tampil adalah gambar pengganti bertuliskan "Tambahkan foto". Cek ulang nama file dan lokasinya di folder `images/`.

---

## Masalah umum

| Masalah | Solusi |
|---|---|
| Halaman 404 | Tunggu beberapa menit setelah upload pertama, lalu cek **Settings → Pages**. Pastikan file bernama persis `index.html` di folder utama. |
| Perubahan tidak muncul | Tunggu 1 sampai 2 menit, lalu muat ulang paksa (`Ctrl + Shift + R`). |
| Gambar tidak tampil | Periksa nama file, huruf besar-kecil, dan folder `images/`. |
| Halaman kosong setelah mengedit | Biasanya ada tanda kutip atau koma yang hilang di daftar `EXPERIENCE`, `ORGS`, `PROJECTS`, atau `CERTS`. Kembalikan ke versi sebelumnya lewat riwayat commit. |

---

## Opsional: domain sendiri

Beli domain, lalu di **Settings → Pages → Custom domain** isi domain-mu. Ikuti petunjuk DNS yang ditampilkan GitHub.
