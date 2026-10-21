# Website resume v2 — gratis di agathahah.github.io

Versi ini tanpa domain berbayar. Alamatnya: **https://agathahah.github.io**

## 1. Lepas custom domain (sekali saja)
1. Buka repo `agathahah.github.io` → **Settings → Pages**.
2. Di bagian **Custom domain**, klik **Remove**.
   GitHub akan menghapus file `CNAME` dari repo secara otomatis.

## 2. Unggah file versi baru
1. Buka tab **Code** di repo → **Add file → Upload files**.
2. Di Finder buka folder `resume-website-v2`, tekan **Cmd+A**, seret semua isinya ke halaman upload
   (isinya, bukan foldernya). File lama dengan nama sama akan tertimpa.
3. **Commit changes**.
4. Tunggu 1–3 menit, lalu buka https://agathahah.github.io dan tekan Cmd+Shift+R (refresh tanpa cache).

Jangan unggah file `CNAME` dari folder lama `resume-website`.

## 3. Lengkapi gambar (opsional, kapan saja)
| File | Isi |
|---|---|
| `assets/shots/finsight.png` | screenshot live demo FinSight |
| `assets/shots/creditlens.png` | screenshot dashboard CreditLens |
| `assets/shots/nusa.png` | screenshot dashboard Tableau NusaCommerce |
| `assets/logos/pacmann.png`, `dqlab.png`, `bins.png`, `bri.png` | logo resmi (PNG persegi, latar transparan) |
| `assets/Agatha-Silalahi-CV.pdf` | CV; tombol "Download CV" muncul otomatis |

Cara upload ke folder tertentu: buka foldernya di GitHub (misalnya `assets/shots`) → **Add file → Upload files**.
Selama gambar belum ada, kartu project menampilkan angka utama project itu, jadi website tetap rapi.

## Mengubah teks
Edit `index.html` langsung di GitHub (ikon pensil) → Commit. Data project ada di bagian `const P = [` di bawah file.
