# LUKAS — Laporan Uang Kas
*Uang Kas Transparan, Kelas Lebih Teratur.*

## Isi repositori ini
- `supabase/migrations/001_schema.sql` — tabel, RLS, saldo atomik, RPC (`record_payment`, `submit_expense`, `review_expense`, `complete_expense`, `correct_transaction`), bucket storage privat.
- `.env.example` — konfigurasi (isi sendiri, jangan di-commit).

## Cara pakai
1. Buat proyek di [supabase.com](https://supabase.com), jalankan `001_schema.sql` di SQL Editor.
2. Buat admin pertama: daftar lewat Supabase Auth, lalu di SQL Editor insert baris `classes` dan `profiles` (role `admin`) untuk user tersebut.
3. Frontend (React + TS + Tailwind + shadcn/ui): paste prompt LUKAS ke [Lovable](https://lovable.dev), sambungkan ke Supabase di atas, lalu pakai **Connect to GitHub** di Lovable agar kode otomatis tersinkron ke repo ini.

## Upload ke GitHub
```bash
git init && git add . && git commit -m "LUKAS: skema database awal"
git branch -M main
git remote add origin https://github.com/USERNAME/lukas.git
git push -u origin main
```

## Belum termasuk
Frontend, ekspor PDF/Excel, jadwal pengingat otomatis, push notification, data DEMO, dan pembatasan login (diatur di Supabase Auth).
