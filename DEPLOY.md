# Deploy website resume ke agathasilalahi.com

Hasil akhir: `https://agathasilalahi.com` (dan `www.agathasilalahi.com` otomatis diarahkan ke sana).
Hosting: GitHub Pages (gratis). Yang dibayar hanya domain, per tahun.

Tampilan dan interaksi website **sama persis** dengan yang kamu lihat di laptop: GitHub Pages hanya
mengirim file `index.html` dan `assets/` apa adanya, tidak mengubah apa pun.

Total waktu: sekitar 30–45 menit kerja, lalu menunggu DNS (biasanya beberapa menit sampai beberapa jam).

---

## Bagian A — Cek dulu di Mac (5 menit)

1. Buka folder `NEW & URGENT/resume-website/`.
2. Klik dua kali `index.html` → terbuka di browser. Cek teks, angka, dan link.
3. (Opsional) Masukkan logo resmi ke `assets/logos/` dengan nama `unimed.png`, `ui.png`, `pacmann.png`,
   `dqlab.png`, `bins.png`, `bri.png`, dan CV ke `assets/Agatha-Silalahi-CV.pdf`.
   Bisa juga ditambahkan nanti setelah website tayang.

## Bagian B — Tayangkan gratis di GitHub Pages (15 menit)

1. Login ke github.com dengan akun **Agathahah**.
2. Klik **+** (kanan atas) → **New repository**.
   - Repository name: `agathahah.github.io` (harus persis: username + `.github.io`)
   - Pilih **Public**
   - Jangan centang "Add a README"
   - Klik **Create repository**
3. Di halaman repo yang masih kosong, klik link **uploading an existing file**.
4. Di Finder, buka folder `resume-website`, pilih **semua isinya** (Cmd+A: `index.html`, `assets`, `CNAME`,
   `robots.txt`, `sitemap.xml`, `DEPLOY.md`), lalu seret ke halaman upload GitHub.
   - Seret **isi** foldernya, bukan folder `resume-website`-nya. Kalau foldernya yang terseret, website akan
     ada di alamat `/resume-website/`, bukan di halaman utama.
   - Pastikan `assets/favicon.svg`, `assets/og-image.png`, dan `assets/logos/README.md` ikut terunggah.
5. Di kotak "Commit changes" tulis `Launch resume website` → **Commit changes**.
   (Commit lewat web otomatis atas nama akun kamu saja.)
6. Buka tab **Settings** → menu kiri **Pages**.
   - Build and deployment → Source: **Deploy from a branch**
   - Branch: **main**, folder **/(root)** → **Save**
7. Tunggu 1–3 menit (cek tab **Actions**, tunggu centang hijau), lalu buka `https://agathahah.github.io`.
   Website kamu sudah online di alamat gratis ini.

> File `CNAME` berisi `agathasilalahi.com`. Selama domain belum dibeli dan DNS belum diatur, GitHub bisa
> menampilkan peringatan domain di halaman Settings → Pages. Itu normal; lanjutkan ke Bagian C.

## Bagian C — Beli domain agathasilalahi.com (10 menit)

1. Pilih registrar, misalnya **Rumahweb**, **DomaiNesia**, atau **Niagahoster/Hostinger** (bayar rupiah lewat
   transfer/VA/QRIS/e-wallet), atau **Cloudflare Registrar** (harga dasar tanpa markup, perlu kartu kredit).
2. Cari `agathasilalahi.com` di kolom pencarian domain. Pastikan statusnya tersedia.
3. Beli **domain saja, 1 tahun**:
   - Tolak paket hosting, email hosting, dan SSL berbayar. Hosting sudah gratis di GitHub, dan HTTPS juga gratis.
   - Aktifkan **WHOIS privacy / domain privacy** kalau gratis, supaya alamat dan nomor HP kamu tidak publik.
   - Cek **harga perpanjangan** tahun berikutnya (sering lebih mahal dari tahun pertama).
   - Aktifkan **auto-renew** supaya domain tidak hangus saat CV-mu sudah tersebar.
4. Selesaikan pembayaran dan verifikasi email dari registrar (biasanya wajib dalam 15 hari, kalau tidak domain
   bisa disuspend).

## Bagian D — Hubungkan domain ke GitHub (10 menit + menunggu)

1. Di panel registrar, buka **Kelola DNS / DNS Management / Zone Editor** untuk `agathasilalahi.com`.
   Biarkan nameserver bawaan registrar.
2. Hapus record bawaan untuk `@` dan `www` (biasanya A record ke "parking page" atau CNAME bawaan).
3. Tambahkan record berikut (TTL biarkan default):

| Type | Name / Host | Value / Points to |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `agathahah.github.io` |

   Opsional (IPv6): AAAA `@` ke `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`,
   `2606:50c0:8003::153`.

4. Kembali ke GitHub → repo → **Settings → Pages → Custom domain**: isi `agathasilalahi.com` → **Save**.
   GitHub akan mengecek DNS ("DNS check in progress" lalu "DNS check successful").
5. Cek dari Terminal Mac (opsional):

   ```bash
   dig agathasilalahi.com +short       # harus muncul 185.199.108.153 dst.
   dig www.agathasilalahi.com +short   # harus muncul agathahah.github.io
   ```

6. Setelah DNS lolos, centang **Enforce HTTPS** di halaman yang sama. Sertifikat gratis bisa butuh
   beberapa menit sampai 24 jam; selama itu centangnya mungkin belum bisa diklik.
7. Disarankan, supaya domain tidak bisa diklaim akun lain: klik foto profil → **Settings → Pages →
   Add a domain** → `agathasilalahi.com`. GitHub memberi satu **TXT record**; tambahkan di DNS registrar,
   lalu klik **Verify**.

## Bagian E — Cek setelah tayang

- [ ] `https://agathasilalahi.com` terbuka dengan ikon gembok
- [ ] `www.agathasilalahi.com` otomatis pindah ke `agathasilalahi.com`
- [ ] Dibuka dari HP: tidak ada geser ke samping, tombol A/B/C dan Fit check jalan
- [ ] Tempel link di linkedin.com/post-inspector → gambar preview muncul
- [ ] Semua tombol Repository / Live demo / Tableau terbuka
- [ ] Pasang link di LinkedIn (Contact info + Featured), header CV, dan bio GitHub

## Mengubah isi nanti

- Lewat web: buka file di repo → ikon pensil → edit → **Commit changes**. Atau **Add file → Upload files**
  untuk menambah logo/CV (unggah ke folder `assets/logos/` atau `assets/`).
- Lewat Terminal:

  ```bash
  git clone https://github.com/Agathahah/agathahah.github.io.git
  cd agathahah.github.io
  git config user.name  "Agatha Silalahi"
  git config user.email "silalahiagatha15@gmail.com"
  # edit file, lalu:
  git add . && git commit -m "Update resume" && git push
  ```

Website diperbarui otomatis 1–2 menit setelah commit. Data project ada di `index.html` (cari `const P =`),
urutan project per role di `ORDER`, skill untuk Fit check di `SK`.

## Kalau ada masalah

| Gejala | Penyebab umum | Solusi |
|---|---|---|
| 404 di agathahah.github.io | File ada di dalam subfolder `resume-website/` | Pastikan `index.html` ada di halaman utama repo |
| "Domain does not resolve to the GitHub Pages server" | DNS belum menyebar, atau record parking lama belum dihapus | Tunggu 1–2 jam, cek ulang tabel DNS di Bagian D |
| Enforce HTTPS tidak bisa dicentang | Sertifikat belum terbit | Tunggu sampai 24 jam |
| Gambar preview LinkedIn tidak muncul | Cache LinkedIn | Tempel ulang link di Post Inspector |
| Custom domain hilang setelah upload | File `CNAME` terhapus | Pastikan file `CNAME` berisi `agathasilalahi.com` ada di repo |
