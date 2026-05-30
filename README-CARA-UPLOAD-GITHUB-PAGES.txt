# Pulang Zikir PWA — GitHub Pages Kit

Ini versi PWA-ready yang menggunakan design `zikir_pagi_petang.html`.

## Apa dalam folder ini

- `index.html` — app utama
- `manifest.json` — metadata supaya boleh Add to Home Screen
- `service-worker.js` — cache/offline selepas first load
- `icons/` — icon app untuk Home Screen

## Cara upload ke GitHub Pages, langkah paling selamat

1. Buka GitHub dan create repository baru. Contoh nama: `pulang-zikir`.
2. Extract zip ini.
3. Upload **isi folder ini** ke repository root.
   Pastikan file nampak begini di GitHub:

   ```
   index.html
   manifest.json
   service-worker.js
   icons/icon-192.png
   icons/icon-512.png
   ```

   Jangan upload folder bersarang seperti `pulang-zikir-design-pwa-github-pages/index.html`, kecuali awak memang mahu URL ada folder itu.

4. Pergi ke repository → Settings → Pages.
5. Source: pilih `Deploy from a branch`.
6. Branch: pilih `main` dan folder `/root`.
7. Save.
8. Tunggu 1–5 minit.
9. GitHub akan beri link lebih kurang:
   `https://USERNAME.github.io/pulang-zikir/`

## Cara test PWA di phone

### iPhone
1. Buka link GitHub Pages guna Safari.
2. Tekan Share.
3. Tekan Add to Home Screen.
4. Buka icon baru di Home Screen.

### Android
1. Buka link guna Chrome.
2. Tekan menu tiga titik.
3. Tekan Install app / Add to Home screen.

## Kalau update tak keluar

PWA ada cache. Kalau awak edit file tapi phone masih tunjuk versi lama:

1. Delete icon app lama dari Home Screen.
2. Buka link di Safari/Chrome.
3. Refresh 2–3 kali.
4. Add to Home Screen semula.

Kalau masih degil, buka `service-worker.js` dan naikkan version ini:

```js
const CACHE_NAME = "pulang-zikir-design-v1.0.2";
```

Contoh tukar v1.0.1 kepada v1.0.2, kemudian upload semula.

## Nota penting untuk GitHub Pages

- `start_url` dan `scope` dalam `manifest.json` telah ditetapkan kepada `./` supaya lebih selamat untuk GitHub Pages project URL.
- Status bar iPhone telah diberi safe-area padding supaya topbar tidak masuk bawah jam/notch.
- App ini public jika repository public. Jangan letak content premium/private dalam repo public.
