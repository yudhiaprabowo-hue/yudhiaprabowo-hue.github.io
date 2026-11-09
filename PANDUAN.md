# Panduan Blog "Per Aspera Ad Astra"

Blog ini dibuat dengan Jekyll dan di-hosting gratis di GitHub Pages. Setiap tulisan adalah satu berkas teks di folder `_posts`. Tidak perlu memasang program apa pun di komputer; semuanya dapat dilakukan melalui situs github.com, termasuk dari ponsel.

## A. Menerbitkan blog pertama kali (sekali saja)

1. **Buat akun GitHub** di https://github.com/signup. Nama akun akan menjadi bagian alamat blog, misalnya `budisantoso` → `https://budisantoso.github.io`.
2. **Buat repositori baru**: klik tombol **+** di kanan atas → **New repository**.
   - Isi *Repository name* dengan `NAMA-AKUN.github.io` (persis nama akun Anda), agar alamat blog menjadi `https://NAMA-AKUN.github.io`.
   - Pilih **Public**, lalu klik **Create repository**.
3. **Unggah berkas blog**: ekstrak berkas ZIP, buka repositori tadi, klik **uploading an existing file**, lalu seret **seluruh isi** folder `jurnal` (bukan foldernya) ke halaman itu. Klik **Commit changes**.
   - Folder yang namanya diawali garis bawah (`_posts`, `_layouts`, `_includes`) harus ikut terunggah. Jika browser tidak mengunggah folder, gunakan GitHub Desktop (https://desktop.github.com).
4. **Aktifkan GitHub Pages**: buka **Settings** → **Pages** → bagian *Build and deployment*, pilih *Source*: **Deploy from a branch**, *Branch*: **main** dan folder **/ (root)**, lalu **Save**.
5. Tunggu 1–3 menit, lalu buka `https://NAMA-AKUN.github.io`.

## B. Mengubah pengaturan dasar

Buka berkas `_config.yml` di GitHub, klik ikon pensil (Edit), lalu ubah:

| Baris | Isi |
|---|---|
| `title` | Nama blog |
| `tagline` dan `description` | Kalimat singkat tentang blog |
| `author: name` | Nama Anda |
| `url` | `https://NAMA-AKUN.github.io` |
| `social` | Email, akun Instagram, atau LinkedIn (boleh dikosongkan) |

Klik **Commit changes**. Ubah juga isi `tentang.md` untuk halaman "Tentang saya".

## C. Menambah tulisan baru

1. Buka folder `_posts` di repositori → **Add file** → **Create new file**.
2. Beri nama berkas dengan format `TAHUN-BULAN-TANGGAL-judul-singkat.md`, misalnya `2026-11-12-hari-pertama-kkn.md`. Gunakan huruf kecil dan tanda hubung, tanpa spasi.
3. Salin isi berkas `templat-tulisan.md`, lalu ganti judul dan isinya.
4. Klik **Commit changes**. Tulisan tampil di blog dalam 1–3 menit.

Tulisan yang tanggalnya di masa depan tidak akan ditampilkan sampai tanggal tersebut tiba.

**Format penulisan singkat (Markdown):**

| Tulis | Hasil |
|---|---|
| `## Subjudul` | Subjudul |
| `**tebal**` | **tebal** |
| `*miring*` | *miring* |
| `- butir` | Daftar berbutir |
| `> kutipan` | Kutipan |
| `[teks](https://alamat)` | Tautan |
| `![keterangan](/assets/gambar/foto.jpg)` | Gambar |

**Menambah gambar:** unggah foto ke folder `assets/gambar` (buat foldernya saat unggah pertama), lalu panggil dengan baris gambar di atas. Perkecil ukuran foto terlebih dahulu (lebar ±1.600 piksel) agar halaman cepat dimuat.

**Menyembunyikan tulisan sementara:** tambahkan baris `published: false` di bagian atas berkas (di antara tanda `---`).

## D. Agar muncul di Google

1. Buka https://search.google.com/search-console dan masuk dengan akun Google.
2. Pilih **URL prefix**, isi `https://NAMA-AKUN.github.io/`.
3. Pilih metode verifikasi **HTML tag**. Salin kode yang diberikan, lalu tambahkan ke `_config.yml`:
   ```
   google_site_verification: KODE-DARI-GOOGLE
   ```
   Isi hanya bagian kodenya (nilai `content="..."`). Commit, tunggu 2 menit, lalu klik **Verify**.
4. Buka menu **Sitemaps**, isi `sitemap.xml`, lalu **Submit**.

Google biasanya mulai menampilkan blog dalam beberapa hari hingga beberapa minggu. Peta situs (`sitemap.xml`), RSS (`feed.xml`), dan data pencarian (judul, deskripsi) sudah dibuat otomatis.

## E. Menggunakan domain sendiri (opsional)

Beli domain (misalnya `namaanda.id` atau `.com`), lalu di **Settings → Pages → Custom domain** isi nama domain dan ikuti petunjuk pengaturan DNS dari GitHub. Setelah aktif, ubah baris `url` di `_config.yml` menjadi alamat domain baru.

## F. Catatan penting

- Repositori berstatus *Public*, sehingga seluruh berkas, termasuk tulisan yang disembunyikan, dapat dilihat orang di github.com. Jangan menyimpan tulisan yang bersifat rahasia di sini.
- Jangan memuat dokumen, data pemohon, atau informasi kedinasan yang tidak untuk publik.
- Jika blog tidak berubah setelah commit, buka tab **Actions** di repositori untuk melihat pesan kesalahan.
