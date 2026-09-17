---
name: bikin-skill
description: >-
  Turns a repeated workflow into a new skill for this AI OS. Use when the user wants to automate
  something they do often, or says "jadikan skill", "bikin skill", "buat skill baru", "tambah
  skill", "otomatisin ini", "saya sering ngerjain ini", "biar nggak ngulang terus", "tiap minggu
  saya harus", "make this a skill", "create a skill", "automate this". Also offer it when the
  same kind of request has come up three times. Writes .claude/skills/<name>/SKILL.md with
  trigger phrases in the user's own words.
---

# Bikin Skill

Mengubah pekerjaan yang diulang-ulang menjadi skill, supaya lain kali cukup disebut dan AI
langsung tahu caranya. Inilah cara OS ini tumbuh.

## Langkah

1. **Pahami pekerjaannya.** Kalau pekerjaan itu baru saja dikerjakan di sesi ini, ambil
   langkah-langkahnya dari percakapan. Kalau belum, tanyakan paling banyak empat hal:
   - Kapan biasanya pekerjaan ini diminta, dan dengan kata-kata apa?
   - Bahan apa yang dibutuhkan?
   - Langkah-langkahnya apa saja?
   - Hasil akhirnya seperti apa, dan apa yang tidak boleh terjadi?
2. **Cek skill yang sudah ada** di `.claude/skills/`. Kalau sudah ada yang mirip, tawarkan untuk
   memperluas skill itu daripada membuat duplikat.
3. **Tentukan nama**: huruf kecil, dipisah tanda hubung, dua sampai tiga kata, misalnya
   `rekap-penjualan`.
4. **Tulis `description`-nya dengan teliti.** Bagian inilah yang menentukan kapan skill dipakai,
   dan penyebab paling umum skill tidak pernah terpicu ada di sini.
   - Awali dengan **kapan** skill dipakai: *"Use when ..."*.
   - Masukkan **paling sedikit lima frasa pemicu**, pakai kata-kata yang benar-benar diucapkan
     pengguna, termasuk bentuk tidak baku dan salah ketik yang lazim.
   - Sertakan padanan bahasa Inggrisnya.
   - Tutup dengan satu kalimat tentang **apa hasilnya**.
5. **Tulis isinya** dengan bentuk di bawah. Usahakan di bawah 150 baris. Skill yang panjang
   jarang dibaca sampai habis.
6. **Simpan** ke `.claude/skills/<nama>/SKILL.md`.
7. **Beri tahu cara mencobanya**: ucapkan salah satu frasa pemicu. Kalau skill belum terpicu,
   mulai sesi baru, karena daftar skill dibaca saat sesi dimulai.

## Bentuk skill

```markdown
---
name: <nama-skill>
description: >-
  Use when <situasinya>, or says "<frasa 1>", "<frasa 2>", "<frasa 3>", "<frasa 4>",
  "<frasa 5>". <Hasilnya dalam satu kalimat.>
---

# <Judul>

<Satu atau dua kalimat: tujuan skill ini.>

## Langkah
1. ...

## Bentuk hasil
<contoh keluaran>

## Aturan
- <apa yang tidak boleh terjadi>
```

## Aturan

- **Satu skill, satu pekerjaan.** Kalau pekerjaannya bercabang jauh, pecah jadi dua.
- **Tulis aturan yang mencegah kerugian nyata**, bukan aturan yang terdengar bagus: jangan
  mengirim tanpa izin, jangan menebak tanggal, jangan mengarang angka.
- **Skill hanya boleh menulis ke tempat yang semestinya.** Data pribadi masuk ke folder data,
  bukan ke folder skill, karena folder skill ikut ke git.
- Jangan menambahkan daftar skill ke `CLAUDE.md` atau `README.md`. Skill yang terpasang sudah
  menjadi daftarnya sendiri.
