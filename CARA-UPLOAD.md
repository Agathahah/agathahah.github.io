# Website resume final (EN + ID) — cara upload

Alamat: https://agathahah.github.io
Versi bahasa: tombol EN / ID di kanan atas. Link langsung: `?lang=id` atau `?lang=en`
(contoh: https://agathahah.github.io/?lang=id untuk dikirim ke rekruter Indonesia).

## Upload (sekali, sekitar 3 menit)
1. Buka https://github.com/Agathahah/agathahah.github.io
2. Klik **Add file → Upload files**.
3. Di Finder buka folder `resume-website-final`, tekan **Cmd+A**, lalu seret semuanya ke halaman upload:
   `index.html`, folder `assets`, `robots.txt`, `sitemap.xml`, dan file ini.
   File dengan nama yang sama di GitHub akan tertimpa otomatis.
4. Klik **Commit changes**.
5. Tunggu 1–3 menit, buka https://agathahah.github.io lalu tekan **Cmd+Shift+R**.

## Rapikan repo (opsional)
File lama yang tidak dipakai lagi: `photo.jpg` (di folder utama, 2 MB), `assets/logos/pacman.png`, `DEPLOY.md`.
Cara hapus: buka file di GitHub → menu **⋯** (kanan atas) → **Delete file** → Commit.

## Cek setelah tayang
- Foto muncul, logo UI, UNIMED, Pacmann, DQLab muncul.
- Tombol EN / ID mengganti seluruh teks; pilihan bahasa diingat saat halaman dibuka lagi.
- Filter proyek (Semua, Risiko kredit, Fraud, LLM & NLP, Data & analitik) berfungsi.
- Klik screenshot proyek → gambar membesar; tekan Esc untuk menutup.
- Tempel link di https://www.linkedin.com/post-inspector/ untuk melihat gambar preview.

## Menambah nanti
- CV (`assets/Agatha-Silalahi-CV.pdf`) sudah disertakan, jadi tombol "Download CV / Unduh CV" akan muncul. CV ini memuat nomor HP; hapus file ini dari repo kalau tidak ingin nomor HP bisa diunduh publik.
- Logo BI dan BRI sudah disertakan (`assets/logos/bins.png`, `assets/logos/bri.png`).
- `assets/shots/pipeline.png`, `assets/shots/sigap.png` → screenshot proyek muncul otomatis.
- Teks bahasa Inggris ada langsung di `index.html`; teks bahasa Indonesia ada di bagian `const ID = {` dan di data proyek `const P = [` (kolom `en` dan `id`).
