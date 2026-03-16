# Pertamini v1.0

Aplikasi pencatatan cashflow untuk pom mini. Lacak penjualan, pembelian, stok BBM, dan estimasi profit harian.

## Fitur
- Input kasir dengan numpad kalkulator + shortcut tombol A/B/C
- Harga jual, harga beli, dan harga promo per liter
- Kalkulasi volume (liter) otomatis
- Riwayat transaksi dengan ringkasan harian (jual, beli, profit)
- Filter tipe dan periode (hari ini, 7 hari, bulan ini, kustom)
- Dashboard saldo kas + estimasi profit + sisa BBM
- Tambah saldo modal
- Export JSON (backup) dan CSV (spreadsheet)
- Import JSON (restore/merge)
- Dark/light mode
- Penyimpanan lokal (localStorage)

## Struktur File
```
pertamini/
├── index.html        # App utama
├── manifest.json     # PWA manifest
├── sw.js             # Service worker (offline support)
├── icons/
│   ├── icon-192.png  # App icon 192x192
│   └── icon-512.png  # App icon 512x512
└── generate-icons.html  # Helper generate icons (tidak perlu di-deploy)
```

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub (mis. `pertamini`)
2. Upload semua file kecuali `generate-icons.html`
3. Masuk ke **Settings → Pages**
4. Source: **Deploy from a branch** → branch `main` → folder `/` (root)
5. Save — app akan live di `https://username.github.io/pertamini`

## Buat Icons
Buka `generate-icons.html` di browser, icon akan otomatis ter-generate dan ter-download. Letakkan di folder `icons/`.

## Catatan
- Data tersimpan di localStorage browser — tidak sinkron antar device
- Gunakan fitur Export JSON untuk backup berkala
- Untuk pindah device, Export JSON di device lama → Import JSON di device baru
