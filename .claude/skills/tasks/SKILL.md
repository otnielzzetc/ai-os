---
name: tasks
description: >-
  The user's to-do list. Use when they add a task, ask what is on their plate, mark something
  done, move or cancel a task, or mention a deadline, or say "tambah tugas", "catat tugas",
  "tugas saya apa", "kerjaan hari ini", "apa yang harus saya kerjakan", "sudah selesai", "udah
  beres", "ingetin", "add task", "todo", "what's on my plate". Owns tasks/todo.md and nothing
  else.
---

# Tugas

Satu-satunya berkas yang dikelola skill ini: `tasks/todo.md`. Kalau belum ada, buat dengan bentuk
di bawah.

## Bentuk berkas

```markdown
# Tugas

## Hari ini
- [ ] Bayar listrik ruko — tenggat: 2026-09-25

## Minggu ini
- [ ] ...

## Nanti
- [ ] ...

## Selesai
- [x] Kirim penawaran ke klien — selesai: 2026-09-17
```

## Yang dikerjakan

- **Menambah.** Masukkan ke bagian yang sesuai tenggatnya. Tanpa tenggat, masuk **Nanti**.
- **Tanggal tidak pernah ditebak.** "Minggu depan", "akhir bulan", atau "besok pagi" yang tidak
  jelas tanggalnya, tanyakan dulu. Salah tanggal di daftar tugas lebih buruk daripada tidak
  ada tanggal sama sekali. Tulis tanggal sebagai `YYYY-MM-DD`.
- **Menandai selesai.** Pindahkan ke **Selesai**, centang, tambahkan tanggal selesainya.
  **Jangan dihapus**, supaya jelas apa yang sudah dikerjakan.
- **Membatalkan.** Pindahkan ke **Selesai** dengan keterangan `dibatalkan: YYYY-MM-DD`.
- **Menampilkan.** Urutkan: yang lewat tenggat dulu, lalu hari ini, lalu minggu ini. Sebutkan
  terang-terangan kalau ada yang **terlambat**.
- **Merapikan.** Setiap kali berkas dibuka, geser tugas yang tenggatnya sudah masuk ke bagian
  yang tepat, misalnya dari **Minggu ini** ke **Hari ini**.

## Batasnya

- Tugas yang ternyata sebuah **proyek** (banyak langkah, ada klien, berjalan berminggu-minggu),
  tawarkan untuk dibuatkan kartu di `projects/`. Tugas di sini cukup langkah berikutnya saja.
- Jadwal dengan jam tertentu (rapat, janji temu) bukan tugas. Tawarkan untuk dimasukkan ke
  kalender kalau kalender sudah tersambung.

Sesudah mengubah berkas, konfirmasi dalam satu kalimat apa yang berubah.
