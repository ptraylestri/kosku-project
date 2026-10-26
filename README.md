# RuangNyaman

Prototipe pencarian kos di Surabaya (HTML, CSS, JavaScript, Leaflet + OpenStreetMap).

## Menjalankan
Buka folder ini di VS Code, lalu jalankan dengan **Live Server** (port 5501 sudah diatur di `.vscode/settings.json`).
Jangan buka lewat `file://` karena data dimuat dari `data/kos.json`.

## Struktur
```
index.html        Beranda
cari.html         Pencarian: daftar + peta
detail.html       Detail kos (?id=kos-001)
favorit.html      Daftar favorit
favicon.ico
css/
  base.css        Variabel, reset, header (dipakai cari, detail, favorit)
  transitions.css Animasi (semua halaman)
  pages/          home.css, cari.css, detail.css, favorit.css
js/
  core/           util, storage (favorit), filter, maps, transitions
  pages/          home, cari, detail, favorit
img/              logo & ikon
data/kos.json     Data kos contoh
```
Urutan memuat script: `storage` → `util` → (`filter`, `maps` bila perlu) → skrip halaman → `transitions`.
