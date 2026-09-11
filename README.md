# BSBM GitHub Pages — FIX FINAL

Paket ini memperbaiki halaman GitHub BSBM yang tampil sebagai HTML polos.

## Perbaikan
- CSS dibuat inline sehingga tidak bergantung pada path `assets/site.css`.
- JavaScript dibuat inline sehingga tidak bergantung pada `assets/site.js`.
- Logo resmi BSBM disisipkan langsung ke `index.html`.
- Favicon tersedia di `assets/favicon.png`.
- Iframe Apps Script mendukung kamera/mikrofon/geolocation.
- Ada fallback **Buka aplikasi langsung** jika iframe tidak diizinkan.
- Struktur tetap sederhana dan ringan.

## PENTING
Buka `index.html`, cari:

```js
const APPS_SCRIPT_URL =
  "https://script.google.com/macros/s/GANTI_DENGAN_DEPLOYMENT_ID/exec";
```

Ganti dengan URL Web App Apps Script BSBM Anda yang berakhiran `/exec`.

## Upload ke GitHub
Upload **isi folder ini** langsung ke root repository `bsbm-app`:

```text
index.html
README.md
assets/
```

Jangan membuat `bsbm-app/bsbm-app/`.

## GitHub Pages
Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save.

URL:
`https://banksampahberkahmandiri05.github.io/bsbm-app/`

## Apps Script
Code.gs BSBM yang dikirim sebelumnya sudah menggunakan:

```js
.setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)
```

Jika Anda mengubah Code.gs, lakukan Deploy/Manage deployments dan pastikan deployment `/exec` menggunakan versi terbaru.
