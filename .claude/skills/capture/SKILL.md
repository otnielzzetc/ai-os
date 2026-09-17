---
name: capture
description: >-
  Use when the user drops a thought, fact, decision, link, or file that needs to be kept, or
  says "catat ini", "simpan ini", "simpen", "masukin", "taruh di mana ini", "ingat ini",
  "capture this", "file this", "note this". Decides where the input belongs in this OS, files
  it there, and confirms in one line.
---

# Catat

Tugasnya memastikan tidak ada yang tercecer: setiap hal yang disodorkan masuk ke **tepat satu**
tempat yang benar, lalu dikonfirmasi.

## Ke mana perginya

| Kalau isinya... | Tempatnya | Caranya |
|---|---|---|
| Sesuatu yang harus **dikerjakan** | `tasks/todo.md` | pakai skill `tasks` |
| **Keputusan** yang sudah diambil | `decisions/log.md` | tambahkan di bawah, lengkap dengan tanggal dan alasan |
| Soal **proyek atau klien** tertentu | `projects/<nama>.md` | tambahkan ke kartunya; buat kartu baru kalau belum ada |
| **Fakta tentang saya** atau bisnis saya | `context/profil.md` | perbarui bagian yang relevan, jangan menumpuk salinan |
| **Bahan rujukan**: artikel, tautan, catatan teknis | `notes/<judul>.md` | ringkas intinya, simpan sumbernya |

Pembeda paling sederhana: akan **ditindaklanjuti** atau akan **dirujuk lagi**? Yang pertama
masuk tugas, proyek, atau keputusan. Yang kedua masuk `notes/`.

## Bentuk catatan

Berkas atau folder tujuan yang belum ada, buat dulu dengan bentuk di bawah. Folder ini bisa saja
baru di-clone.

**Keputusan** di `decisions/log.md`. Kalau berkasnya belum ada, awali dengan judul
`# Catatan Keputusan` dan satu kalimat: *hanya ditambah di bawah, keputusan yang dibatalkan dicatat
sebagai keputusan baru.*

```markdown
## YYYY-MM-DD — <keputusannya dalam satu kalimat>
- Alasan: <kenapa>
- Pilihan lain yang ditolak: <kalau ada>
- Terkait: [[nama proyek]]
```

**Kartu proyek** di `projects/<nama>.md`:

```markdown
---
tags:
  - proyek
status: berjalan
---

# <Nama proyek>

## Ringkas
<apa, untuk siapa, targetnya>

## Keadaan sekarang
<satu paragraf, diperbarui, bukan ditumpuk>

## Catatan
- YYYY-MM-DD — <yang terjadi>

## Terkait
```

## Aturan

- **Satu hal, satu tempat.** Jangan menyimpan fakta yang sama di dua berkas; begitu salah satunya
  diperbarui, keduanya jadi saling bertentangan.
- **Kalau ragu antara dua tempat, tanya sekali**, dengan pilihan yang jelas. Jangan menebak.
- **Jangan mengubah isi yang disodorkan.** Merapikan boleh, menambah fakta yang tidak disebut
  tidak boleh.
- Sesudah menyimpan, konfirmasi dalam satu kalimat: apa yang disimpan dan di mana.
