---
name: catat-rapat
description: >-
  Turns meeting notes, a call transcript, or a pasted chat into decisions and action items. Use
  when the user pastes notes or a conversation and wants it summarized, or says "catat rapat",
  "notulen", "bikin notulen", "rangkum meeting", "hasil meeting", "hasil rapat", "ringkas
  obrolan ini", "rangkum chat ini", "siapa ngerjain apa", "action item", "meeting notes",
  "summarize this call", "summarize this chat". Separates what was decided from what was only
  discussed, and lists who does what by when without guessing.
---

# Catat Rapat

Mengubah catatan rapat, transkrip, atau obrolan grup menjadi hal yang bisa ditindaklanjuti:
**apa yang diputuskan, siapa mengerjakan apa, dan kapan.**

## Langkah

1. **Baca seluruh bahannya.** Kalau bahannya belum ditempel, minta ditempel.
2. **Pisahkan tiga hal ini**, karena campurannya adalah sumber salah paham paling umum:
   - **Diputuskan:** sudah disepakati.
   - **Dibahas:** muncul, tapi belum disepakati.
   - **Ditugaskan:** ada orang yang harus mengerjakan sesuatu.
3. **Susun hasilnya** dengan bentuk di bawah.
4. **Tawarkan tindak lanjut**, dan kerjakan hanya yang disetujui:
   - tugas milik pengguna dimasukkan ke `tasks/todo.md` lewat skill `tasks`
   - keputusan dicatat ke `decisions/log.md` lewat skill `capture`
   - kalau rapatnya jelas tentang satu proyek, ringkasannya ditambahkan ke `projects/<nama>.md`

## Bentuk hasil

```markdown
# <Topik rapat> — <tanggal, kalau disebut>

**Hadir:** <nama-nama, kalau disebut>

## Ringkasan
- <3 sampai 5 poin paling penting>

## Keputusan
- <keputusan>

## Tugas
| Siapa | Apa | Tenggat |
|---|---|---|
| <nama> | <tugas> | <tanggal atau "belum ditentukan"> |

## Masih dibahas, belum diputuskan
- <hal>

## Pertanyaan terbuka
- <hal yang perlu dijawab seseorang>
```

## Aturan

- **Hanya yang ada di bahan.** Jangan menambah keputusan, nama, atau tenggat.
- **Pemilik dan tenggat yang tidak disebut ditulis "belum ditentukan"**, bukan ditebak. Tugas
  tanpa pemilik adalah temuan penting, jadi sebutkan di bagian pertanyaan terbuka.
- **"Nanti dicek", "kayaknya bisa", "coba diusahakan"** bukan keputusan. Masukkan ke bagian
  "masih dibahas".
- Kalau tanggal ditulis relatif ("Jumat depan", "akhir bulan") dan tanggal rapatnya tidak
  diketahui, tulis apa adanya lalu tanyakan tanggal pastinya.
- Jangan mengubah daftar tugas atau catatan keputusan tanpa persetujuan.
