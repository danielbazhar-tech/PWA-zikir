PULANG ZIKIR PWA — CARA UPLOAD KE GITHUB PAGES (FOOL-PROOF)
===============================================================

A. APA YANG ADA DALAM FOLDER INI
--------------------------------
1. index.html          = app utama
2. manifest.json       = setting supaya website boleh jadi macam app di phone
3. service-worker.js   = offline cache selepas first load
4. icons/              = icon app

JANGAN rename fail-fail ini.
Pastikan index.html berada di ROOT folder repo, bukan dalam subfolder.


B. CARA PALING MUDAH UPLOAD KE GITHUB PAGES
-------------------------------------------
1. Login GitHub.
2. Klik + di kanan atas > New repository.
3. Nama repo contoh: pulang-zikir
4. Set Public.
5. Klik Create repository.
6. Dalam repo baru, klik "uploading an existing file".
7. Drag SEMUA isi folder ini:
   - index.html
   - manifest.json
   - service-worker.js
   - folder icons
8. Klik Commit changes.


C. AKTIFKAN GITHUB PAGES
------------------------
1. Pergi ke tab Settings dalam repo.
2. Klik Pages di sidebar kiri.
3. Under "Build and deployment":
   - Source: Deploy from a branch
   - Branch: main
   - Folder: /root
4. Klik Save.
5. Tunggu 1-5 minit.
6. Link akan jadi lebih kurang:
   https://USERNAME.github.io/pulang-zikir/

PENTING:
- Untuk GitHub Pages, link biasanya ada slash di hujung.
- Contoh betul: https://USERNAME.github.io/pulang-zikir/
- Kalau icon/offline tak jalan, cuba refresh 2-3 kali dan tunggu 2 minit.


D. CARA INSTALL DI PHONE
------------------------
ANDROID / CHROME:
1. Buka link GitHub Pages.
2. Tap menu tiga titik.
3. Pilih "Install app" atau "Add to Home screen".
4. Icon akan muncul di home screen.

IPHONE / SAFARI:
1. Buka link GitHub Pages di Safari.
2. Tap butang Share.
3. Pilih "Add to Home Screen".
4. Tap Add.

Nota: iPhone biasanya tidak tunjuk pop-up install. Kena guna Share > Add to Home Screen.


E. KALAU UPDATE CONTENT
-----------------------
1. Edit index.html.
2. Upload semula ke GitHub.
3. Dalam service-worker.js, tukar:
   const CACHE_NAME = 'pulang-zikir-v1';
   kepada contoh:
   const CACHE_NAME = 'pulang-zikir-v2';
4. Commit changes.

Ini penting supaya phone user ambil versi baru, bukan cache lama.


F. CHECKLIST SEBELUM SHARE LINK
-------------------------------
[ ] Link GitHub Pages boleh buka.
[ ] Button hamburger jalan.
[ ] Copy Arabic jalan.
[ ] Manifest tidak error.
[ ] Icon muncul bila Add to Home Screen.
[ ] Test Android/Chrome jika ada.
[ ] Test iPhone/Safari jika ada.


G. NOTA AMANAH
--------------
Produk ini memudahkan susunan zikir dan rujukan. Jangan claim semua bacaan setaraf Bukhari-Muslim jika ada yang hasan/khilaf. Label status dalam app sudah sengaja dibuat berhati-hati.
