---
name: session-handoff
description: >-
  Use when the user wants to wrap up or save the current session before closing or clearing it,
  or says "rangkum sesi ini", "simpan sesi", "handoff", "session handoff", "wrap up", "rangkum
  dulu", "mau clear", "sebelum tutup". Writes a dated session note to sessions/, registers it in
  sessions/index.md, and prints the same summary in chat so the next session can continue
  without redoing settled work.
---

# Rangkum Sesi

Tujuannya satu: **sesi berikutnya bisa melanjutkan hanya dengan membaca catatan ini**, tanpa
mengulang pekerjaan yang sudah selesai dan tanpa membatalkan keputusan yang sudah diambil.

Pembacanya adalah AI di sesi berikutnya, bukan atasan. Tulis seperti operator yang serah terima
di akhir giliran jaga: konkret, tanpa pujian, tanpa emoji.

## Langkah

1. **Tinjau SELURUH percakapan**, bukan hanya beberapa pesan terakhir. Rangkuman yang cuma
   membaca bagian akhir hampir selalu melewatkan keputusan penting di tengah.
2. **Kumpulkan dari sesi ini saja:**
   - apa yang diminta dan batasan yang muncul di tengah jalan
   - keputusan yang diambil, beserta **alasannya**
   - berkas yang dibuat atau diubah
   - proses yang masih berjalan: server, terminal, proses latar, dan cara menghentikannya
   - cara memastikan hasilnya masih jalan
   - pertanyaan yang belum dijawab, dan hal yang sengaja ditunda
   Jangan menyisir folder atau riwayat git untuk mencari bahan. Kalau tidak disentuh di sesi ini,
   tidak masuk catatan.
3. **Tulis berkasnya** ke `sessions/YYYY-MM-DD <topik>.md`. Topik dua sampai empat kata, huruf
   kecil. Dua sesi dengan topik sama di hari yang sama, tambahkan `-2`.
4. **Daftarkan di `sessions/index.md`**, satu baris paling atas di tabelnya. Catatan yang tidak
   terdaftar tidak akan pernah ditemukan sesi berikutnya. Kalau `sessions/index.md` belum ada,
   buat dulu dengan bentuk katalog di bawah.
5. **Tampilkan rangkuman yang sama di chat.**

## Bentuk berkas

```markdown
---
tags:
  - sesi
tanggal: YYYY-MM-DD
topik: [kata, kunci]
---

# <Satu kalimat: sesi ini tentang apa>

## Konteks
<2-3 kalimat: apa yang diminta, dan batasan yang muncul>

## Keputusan dan yang sudah jadi
- <keputusan atau perubahan> — <alasannya, dan di mana tersimpan>

## Berkas penting untuk sesi berikutnya
- `<jalur>` — <kenapa perlu dibaca>

## Yang masih berjalan
- Proses: <nama, cara menghentikan>, atau "tidak ada"
- Server/port: <alamat>, atau "tidak ada"

## Cara memastikan masih jalan
- `<perintah>` — <hasil yang diharapkan>

## Terbuka dan ditunda
- Terbuka: <pertanyaan yang menunggu jawaban saya>
- Ditunda: <hal> — <kenapa ditunda>

## Lanjut dari sini
<1-2 kalimat: langkah paling mungkin berikutnya>

## Terkait
- [[index|Katalog sesi]]
```

Bentuk `sessions/index.md`:

```markdown
---
tags:
  - sesi
  - katalog
---

# Katalog Sesi

Baca berkas ini begitu topik sesi jelas. Baris terbaru di paling atas.

| Catatan | Tanggal | Keadaan terakhir |
|---|---|---|
| [[YYYY-MM-DD <topik>]] | YYYY-MM-DD | <keadaan terakhir dalam satu kalimat> |
```

## Aturan keras

- **Berkas dan chat, selalu dua-duanya.** Berkas untuk ingatan jangka panjang, chat untuk
  langsung dilanjutkan.
- **Jangan mengarang keadaan.** Bagian yang tidak ada isinya ditulis "tidak ada", bukan dihapus.
  Bentuk yang tetap itulah yang membuat catatan mudah dibaca ulang.
- **Keputusan tanpa alasan tidak ada gunanya.** Sesi berikutnya perlu tahu *kenapa*, supaya
  tidak membatalkannya karena mengira itu kekeliruan.
- Tautkan catatan lain yang benar-benar ada dengan `[[nama catatan]]`, dan hanya yang ada.
