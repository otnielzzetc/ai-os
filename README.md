# AI OS

Otak kerja pribadi yang dijalankan **Claude Code**. Isinya cuma berkas teks: aturan main di
`CLAUDE.md`, kemampuan di `.claude/skills/`, dan ingatan di folder-folder data. Tidak ada server,
tidak ada database, tidak ada yang perlu di-build.

Semua yang dipelajari AI tentang Anda tersimpan sebagai berkas teks di komputer Anda sendiri.

## Yang dibutuhkan

| Apa | Wajib? | Catatan |
|---|---|---|
| **Paket Claude berbayar** (Pro, Max, Team, atau Enterprise) | Wajib | Claude Code tidak bisa dipakai dengan akun gratis |
| **Claude Code** | Wajib | aplikasi desktop, atau CLI lewat `npm install -g @anthropic-ai/claude-code` |
| **Git** | Wajib | untuk meng-clone repo ini. Di Windows: Git for Windows |
| **Obsidian** | Opsional | untuk melihat catatan sebagai grafik |
| **Node.js** dan **Bun** | Opsional | hanya kalau memasang plugin yang membutuhkannya |

## Cara memasang

1. Clone repo ini ke folder tempat Anda mau menyimpan OS-nya:
   ```bash
   git clone <alamat-repo-ini> AI-OS
   ```
2. Buka folder `AI-OS` di Claude Code. Di aplikasi desktop: **Open folder**. Di terminal:
   masuk ke folder itu lalu jalankan `claude`.
3. Kalau ditanya apakah folder ini dipercaya, jawab **Yes**.
4. Mulai bicara. Di sesi pertama AI akan menawarkan beberapa pertanyaan singkat untuk mengenal
   Anda. Semua boleh dilewati, dan AI tetap menjawab permintaan Anda lebih dulu.

Berkas data seperti daftar tugas dan profil **dibuat otomatis** saat pertama kali dibutuhkan.

## Yang bisa langsung dipakai

- *"tugas saya apa hari ini?"*
- *"tambah tugas: bayar listrik tanggal 25"*
- *"catat ini: ..."*: AI menentukan sendiri tempat penyimpanannya
- *"minggu ini saya harus fokus ke mana?"*
- *"tulisin pesan WA ke pelanggan, pesanannya telat sehari"*: AI hanya menyusun, tidak pernah mengirim
- *"rangkum rapat ini"*, lalu tempel catatannya
- *"rangkum sesi ini"* sebelum menutup sesi, lalu *"lanjut kemarin"* di sesi berikutnya
- *"error nih"*, lalu tempel pesan errornya
- *"jadikan skill"*, untuk pekerjaan yang sering diulang

Untuk melihat semua kemampuan, tanyakan *"skill apa saja yang kamu punya?"*.

## Isi repo

| Tempat | Isinya |
|---|---|
| `CLAUDE.md` | aturan main yang dibaca AI di setiap sesi |
| `.claude/skills/` | kemampuan, satu folder satu skill |
| `context/` | profil, bisnis, dan prioritas Anda |
| `tasks/` | daftar tugas |
| `projects/` | satu kartu per proyek atau klien |
| `decisions/` | catatan keputusan beserta alasannya |
| `sessions/` | catatan akhir sesi dan katalognya |
| `notes/` | bahan rujukan |

## Data Anda tidak ikut ke git

Isi `context/`, `tasks/`, `projects/`, `decisions/`, `sessions/`, dan `notes/` **sengaja
dikecualikan dari git**. Yang ikut hanya README di tiap folder. Jadi kalau Anda meng-push fork
Anda sendiri, data pribadi tetap tinggal di komputer.

**Periksa sebelum push.** Pastikan `git status` tidak memuat berkas data pribadi.

Yang tetap keluar dari komputer adalah apa pun yang Anda ketik ke Claude, sama seperti
percakapan biasa. Jangan menempelkan sesuatu yang tidak boleh sampai ke pihak lain.

## Obsidian

Buka folder ini lewat **Open folder as vault**. Catatan-catatannya saling bertaut dengan
`[[wikilink]]` dan langsung tampil sebagai grafik. Tidak perlu pengaturan tambahan.

**Opsional: MCP Obsidian.** Pasang plugin komunitas *Local REST API* di vault ini, salin
`.mcp.json.example` menjadi `.mcp.json`, lalu isi kunci API dari pengaturan plugin itu.
`.mcp.json` dikecualikan dari git karena berisi kunci. Kalau Anda punya lebih dari satu vault
yang memakai plugin ini, bedakan port-nya, karena bawaannya sama-sama 27124.

## Masalah umum di Windows

- **`npm` atau `claude` ditolak dengan pesan "running scripts is disabled".** PowerShell di
  komputer kantor sering melarang skrip. Panggil versi `.cmd`: `npm.cmd` dan `claude.cmd`.
- **Plugin terpasang tapi tidak jalan, atau muncul "Bun not found".** Sebagian plugin
  membutuhkan Bun. Pasang dengan `npm.cmd install -g bun`.
- **Program baru terpasang tapi "is not recognized".** Jendela terminal yang sudah terbuka tidak
  membaca PATH yang baru. Buka jendela terminal baru. Kalau terminalnya dibuka dari dalam
  aplikasi Claude, tutup dan buka ulang aplikasinya.

## Menambah skill

Buat berkas `.claude/skills/<nama-skill>/SKILL.md`:

```markdown
---
name: nama-skill
description: Use when ... Tulis kata-kata yang memang biasa Anda ucapkan, misalnya "rekap kas".
---

# Judul
Langkah-langkahnya.
```

Bagian `description` inilah yang menentukan kapan skill dipakai, jadi tulis sespesifik mungkin.

Pekerjaan yang Anda ulang sampai tiga kali adalah kandidat skill yang bagus.

## Lisensi

[MIT](LICENSE). Bebas dipakai, diubah, dan dibagikan, asal pemberitahuan hak cipta di berkas
`LICENSE` tetap disertakan. Diberikan apa adanya, tanpa jaminan: Anda bertanggung jawab atas
tindakan AI di akun-akun yang Anda sambungkan.
