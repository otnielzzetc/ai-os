---
name: fokus-minggu
description: >-
  Weekly review and planning. Use when the user asks what to focus on, wants to plan or review
  the week, or says "fokus minggu ini", "minggu ini ngapain aja", "apa yang harus saya kerjakan
  minggu ini", "prioritas minggu ini", "review mingguan", "rencana minggu ini", "evaluasi
  minggu ini", "saya harus fokus ke mana", "what should I focus on this week", "weekly review",
  "plan my week". Reads the profile, tasks, projects, and recent decisions, then names what is
  overdue, the top three focuses tied to stated priorities, and projects that have stalled.
---

# Fokus Minggu Ini

Tujuannya menjawab satu pertanyaan dengan jujur: **minggu ini sebaiknya fokus ke mana, dan
kenapa.** Bukan daftar semua hal, melainkan pilihan.

## Langkah

1. **Pastikan tanggal hari ini.** Pakai tanggal dari lingkungan sesi. Kalau tidak diketahui,
   tanyakan. Semua hitungan terlambat dan macet bergantung padanya.
2. **Kumpulkan bahan**, lewati yang belum ada:
   - `context/profil.md`, terutama bagian prioritas
   - `tasks/todo.md`
   - semua `projects/*.md`
   - bagian akhir `decisions/log.md`
   - beberapa baris teratas `sessions/index.md`
3. **Kalau bahannya terlalu sedikit** (tidak ada prioritas, tugas, maupun proyek), jangan
   mengarang rencana. Katakan apa yang belum ada, lalu ajukan paling banyak tiga pertanyaan:
   apa yang paling penting minggu ini, apa yang sedang ditunggu orang lain, dan apa yang sudah
   lewat tenggat.
4. **Susun jawabannya** dengan bentuk di bawah.
5. **Tawarkan untuk memperbarui `tasks/todo.md`**, misalnya memindahkan ketiga fokus ke bagian
   Minggu ini. Ubah berkasnya hanya sesudah pengguna setuju.

## Bentuk jawaban

```markdown
## Terlambat
- <tugas> — tenggat <tanggal>, lewat <n> hari
(atau: tidak ada)

## Tiga fokus minggu ini
1. **<fokus>** — kenapa: <kaitannya dengan prioritas, tenggat, atau orang yang menunggu>
2. ...
3. ...

## Proyek yang macet
- <proyek> — catatan terakhir <tanggal>, <n> hari tanpa kabar
(atau: tidak ada)

## Bisa dilepas atau ditunda
- <hal> — <kenapa aman ditunda>

## Satu pertanyaan
<pertanyaan yang jawabannya paling mengubah rencana minggu ini>
```

## Aturan

- **Tepat tiga fokus, tidak lebih.** Kalau semuanya penting, berarti belum ada yang dipilih.
- **Setiap fokus harus punya alasan** yang merujuk ke prioritas, tenggat, atau orang yang
  menunggu. Fokus tanpa alasan dibuang.
- **Proyek dianggap macet** kalau catatan bertanggal terakhirnya lebih dari 14 hari lalu dan
  statusnya masih berjalan.
- **Jangan mengarang tugas, tenggat, atau proyek.** Semua yang disebut harus ada di berkas.
  Kalau sebuah fokus muncul dari penalaran, bukan dari berkas, tandai sebagai usulan.
- Jujur soal kelebihan beban. Kalau tugasnya jelas tidak muat dalam seminggu, katakan.
