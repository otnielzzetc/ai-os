---
name: lanjutkan
description: >-
  Use when the user wants to pick up earlier work or asks where things were left off, or says
  "lanjut", "lanjutkan", "lanjut kemarin", "lanjut kerjaan kemarin", "terakhir sampai mana",
  "kemarin ngapain", "kemarin sampai mana", "kita lagi ngerjain apa", "resume", "continue where
  we left off", "pick up where we left off". Finds the matching note in sessions/index.md,
  reads it, and restates the locked decisions, what may still be running, and the next step.
  The counterpart of session-handoff.
---

# Lanjutkan

`session-handoff` menyimpan keadaan sebuah sesi. Skill ini **memuatnya kembali**, supaya sesi
baru tidak mengulang pekerjaan yang sudah beres dan tidak membatalkan keputusan yang sudah
dikunci.

## Langkah

1. **Buka `sessions/index.md`.** Kalau berkasnya tidak ada atau tabelnya kosong, katakan terus
   terang bahwa belum ada catatan sesi, lalu tanyakan apa yang mau dikerjakan. Selesai.
2. **Pilih catatannya.**
   - Kalau pengguna menyebut topik ("lanjut invoice", "yang soal website"), cari baris yang
     cocok dengan topik itu.
   - Kalau tidak menyebut topik, ambil baris paling atas, yaitu yang terbaru.
   - Kalau ada lebih dari satu yang sama cocoknya, tampilkan paling banyak tiga pilihan beserta
     tanggalnya, lalu tanya mau yang mana. Jangan menebak.
3. **Baca catatannya sampai habis.**
4. **Periksa ulang hal yang bisa sudah berubah.** Catatan ditulis di masa lalu. Sebelum
   menyebut sesuatu *masih* berjalan atau *masih* terbuka, periksa kalau bisa diperiksa: apakah
   berkas yang disebut masih ada, apakah proses atau server yang disebut masih hidup. Yang tidak
   bisa diperiksa, sebut sebagai *"menurut catatan tanggal sekian"*.
5. **Sampaikan dengan bentuk di bawah**, lalu tanyakan apakah mau lanjut dari langkah itu.
   **Jangan langsung mengerjakan apa pun** sebelum pengguna mengiyakan.

## Bentuk jawaban

```markdown
**Melanjutkan:** <judul catatan> (<tanggal>)

**Keadaan terakhir:** <2-3 kalimat>

**Sudah diputuskan, jangan diubah tanpa alasan:**
- <keputusan> — <alasannya>

**Mungkin masih berjalan:** <sudah diperiksa / menurut catatan>, atau "tidak ada"

**Masih terbuka:**
- <pertanyaan atau pekerjaan yang belum selesai>

**Langkah berikutnya menurut catatan:** <satu kalimat>

Lanjut dari situ?
```

## Aturan

- **Keputusan di catatan dianggap berlaku.** Kalau ada alasan kuat untuk mengubahnya, sampaikan
  alasannya dan minta persetujuan. Jangan diubah diam-diam.
- **Jangan menambah isi yang tidak ada di catatan.** Kalau catatannya tidak menyebut sesuatu,
  katakan tidak tercatat.
- Kalau catatannya ternyata tidak cocok dengan keadaan sekarang, misalnya berkas yang disebut
  sudah tidak ada, katakan dengan jelas. Keadaan sekarang yang menang.
