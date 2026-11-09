# Pixel Escape Room: Misi Bersama

Game escape room bergaya pixel art untuk team building. Satu orang membagikan layar (share screen) dan seluruh anggota grup memecahkan 6 kegiatan bersama. Tiap kegiatan memberi satu kata kunci, lalu grup harus menyusun dan menebak kalimat kunci untuk membuka pintu.

Situs ini statis: satu file `index.html` tanpa build step dan tanpa dependensi (hanya memuat font dari Google Fonts, dengan fallback bawaan).

## Isi folder

| File | Fungsi |
| --- | --- |
| `index.html` | Seluruh game (HTML, CSS, dan JavaScript) |
| `vercel.json` | Pengaturan Vercel (clean URL dan header keamanan dasar) |
| `.gitignore` | File yang tidak ikut masuk ke Git |
| `README.md` | Panduan ini |

## Cara upload ke GitHub (lewat browser)

1. Ekstrak file ZIP lebih dulu.
2. Buka https://github.com/new, isi nama repository (misalnya `pixel-escape-room`), pilih Public atau Private, lalu klik **Create repository**.
3. Di halaman repository yang kosong, klik **uploading an existing file**.
4. Seret **isi folder** (`index.html`, `vercel.json`, `.gitignore`, `README.md`) ke halaman itu. Pastikan `index.html` berada di akar repository, bukan di dalam subfolder.
5. Klik **Commit changes**.

## Cara deploy ke Vercel

1. Masuk ke https://vercel.com dan login dengan akun GitHub.
2. Klik **Add New... > Project**, lalu pilih repository `pixel-escape-room` (berikan izin akses kalau diminta).
3. Pada pengaturan project:
   - **Framework Preset:** Other
   - **Build Command:** kosongkan
   - **Output Directory:** kosongkan
   - **Install Command:** kosongkan
4. Klik **Deploy**. Setelah selesai, Vercel memberi link publik (`https://nama-project.vercel.app`) yang bisa dibuka siapa saja tanpa login.

Setiap kali kamu mengubah file di GitHub, Vercel akan men-deploy ulang secara otomatis.

## Mencoba di komputer sendiri

Klik dua kali `index.html` untuk membukanya di browser.

## Mengubah isi teka-teki

Semua konten ada di bagian `<script>` pada `index.html`:

- `ANS`: jawaban tiap kegiatan.
- `WD`: kata kunci yang didapat dari tiap kegiatan.
- `PH`: kalimat kunci lengkap, tanpa spasi dan huruf besar. Harus cocok dengan susunan semua kata di `WD`.
- `OB`: judul dan teks bantuan tiap kegiatan.
- `RULES` dan `TARGET`: aturan dan solusi Panel Lampu.

Kalau kamu mengubah satu teka-teki, pastikan jawabannya masih punya satu solusi yang pasti dan uji ulang sebelum acara.

## Catatan penting

- Game berjalan sepenuhnya di browser. Jawaban tersimpan di dalam kode halaman, jadi peserta yang membuka "View Source" bisa melihatnya. Untuk acara team building ini biasanya tidak masalah, tapi minta peserta bermain jujur.
- Progres tidak disimpan. Kalau halaman di-refresh, grup mulai dari awal.
- Waktu dan hasil dilaporkan secara manual: grup menyalin teks hasil dan menempelnya di chat Zoom.
