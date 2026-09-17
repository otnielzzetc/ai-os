---
name: diagnosa
description: >-
  Troubleshoots problems with this AI OS, Claude Code, plugins, MCP servers, or connected tools.
  Use when something fails or behaves oddly, or the user says "error", "eror", "ga jalan",
  "gak jalan", "nggak jalan", "tidak jalan", "ga jawab", "ga bales", "ga mau", "ga muncul",
  "rusak", "kok gini", "kenapa ini", "macet", "stuck", "is not recognized", "tidak dikenali",
  "not working", "broken", "failed", "doctor", or pastes an error message. Diagnoses one step at
  a time from the exact error, fixes only what is safe, and never deletes or resets anything.
---

# Diagnosa

Mencari penyebab masalah **satu langkah demi satu langkah**, berdasarkan bukti, tanpa merusak
apa pun. Tebakan yang terdengar yakin lebih berbahaya daripada "belum tahu".

## Langkah

1. **Dapatkan pesan error yang persis.** Minta ditempel apa adanya, atau baca langsung dari
   terminal kalau bisa. Tanpa teks errornya, jangan mulai menyimpulkan.
2. **Cocokkan dengan daftar penyebab umum di bawah**, mulai dari yang paling cocok dengan
   teks errornya.
3. **Periksa dulu sebelum menyimpulkan.** Satu pemeriksaan kecil yang membuktikan penyebabnya
   lebih baik daripada tiga perbaikan yang dicoba bergantian.
4. **Perbaiki satu hal**, lalu **buktikan** hasilnya dengan menjalankan ulang hal yang tadi
   gagal. Jangan menyebut sudah beres sebelum terbukti.
5. **Kalau tidak bisa diperbaiki**, susun pesan singkat untuk dimintakan bantuan: apa yang
   dicoba, teks error persisnya, sistem operasi, dan versi program yang terlibat.

## Penyebab umum

| Gejala | Penyebab yang sering | Periksa atau lakukan |
|---|---|---|
| AI tidak mengikuti aturan di `CLAUDE.md` | sesi dibuka di folder lain | pastikan sesinya dibuka di folder OS ini |
| `... is not recognized` atau `command not found` | programnya belum terpasang, atau jendela terminal dibuka sebelum program dipasang | cek keberadaan programnya; buka jendela terminal baru, atau mulai ulang aplikasi yang membuka terminal itu |
| `running scripts is disabled on this system` (Windows) | PowerShell melarang skrip `.ps1` | panggil versi `.cmd`, misalnya `npm.cmd` atau `claude.cmd` |
| Plugin atau MCP gagal tersambung, atau `... not found` saat sesi dimulai | runtime yang dibutuhkan belum ada (Node.js, Bun, Python) | baca perintah server di konfigurasi plugin atau `.mcp.json`, lalu pastikan runtime itu bisa dipanggil |
| MCP ke aplikasi lokal menolak sambungan | aplikasinya tidak sedang jalan, port salah, atau kunci API salah | buka aplikasinya, cocokkan port dan kunci di `.mcp.json` |
| Skill tidak pernah terpicu | kata-kata pengguna tidak ada di `description` skill | tambahkan kata-kata yang benar-benar diucapkan pengguna ke `description` |
| `being used by another process` | berkas sedang dipegang proses lain | tunggu sebentar lalu ulangi; kalau terus terjadi, cari proses yang memegangnya |
| Bot atau sambungan saling berebut, muncul `409 Conflict` | dua proses memakai token yang sama | pastikan hanya satu proses yang berjalan |
| Diminta login lagi, atau akses ditolak | sesi login habis, atau paket tidak mendukung fitur itu | login ulang; cek paket akun |
| AI terus menawarkan penyiapan dan tidak menjawab | ada aturan penyiapan yang memblokir di `CLAUDE.md` | cari dan hapus aturan yang menahan jawaban |

## Aturan keras

- **Jangan menghapus, mereset, atau menimpa** berkas, pengaturan, atau data pengguna untuk
  "mencoba". Kalau perlu mengubah berkas konfigurasi, buat cadangannya dulu.
- **Jangan mengubah pengaturan keamanan** seperti execution policy, firewall, atau izin
  sistem. Cari jalan yang tidak memerlukannya, seperti memanggil versi `.cmd`.
- **Memasang program adalah keputusan pengguna.** Berikan perintahnya dan biarkan pengguna yang
  menjalankan.
- **Jangan menyebut penyebab yang belum diperiksa sebagai fakta.** Tulis sebagai dugaan dan
  sebutkan cara memastikannya.
- Kalau dugaan pertama ternyata salah, katakan terang-terangan lalu lanjut ke kemungkinan
  berikutnya.
