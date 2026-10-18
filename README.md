# Dashboard UTS Algorithmic Trading – Kompas 100 (live Yahoo Finance)

Struktur:
- `index.html` – dashboard (satu file, data backtest tertanam)
- `api/batch.js` – mengambil banyak saham sekaligus dari Yahoo (paralel di server)
- `api/yahoo.js` – proxy per-saham (fallback)
- `vercel.json` – konfigurasi

## Deploy
1. Buat repo baru di GitHub, lalu dari folder ini:
   ```
   git init && git add . && git commit -m "dashboard"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
2. vercel.com → Add New → Project → pilih repo → Deploy (tanpa framework / build command, biarkan default).
3. Buka URL Vercel. Chip di pojok atas harus berubah menjadi "LIVE Yahoo".

Jika Yahoo memblokir IP Vercel, dashboard otomatis jatuh ke proxy CORS publik (lebih lambat).
