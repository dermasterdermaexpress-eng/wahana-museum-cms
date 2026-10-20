# Wahana Museum CMS — Demo Lokal

CMS demo terpisah untuk website museum React + Three.js bergaya first-person. Dashboard memakai data simulasi; belum terhubung ke analytics produksi atau database backend.

## Kebutuhan
- Node.js 18+ (disarankan Node.js 20 LTS)
- npm

## Menjalankan di Ubuntu / Windows
1. Ekstrak ZIP.
2. Buka folder `wahana-museum-cms` di VS Code.
3. Buka terminal pada folder tersebut.
4. Jalankan:
   ```bash
   npm install
   npm run dev
   ```
5. Buka alamat yang muncul di terminal, biasanya `http://localhost:5173`.

## Build produksi lokal
```bash
npm run build
npm run preview
```

## Fitur demo
- Dashboard: KPI pengunjung, sesi, durasi, bounce rate, grafik traffic, sumber traffic, perangkat, area populer, aktivitas terbaru.
- Asset Manager: upload gambar ke sesi browser, pratinjau, pencarian, filter kategori, tandai favorit, edit nama/kategori, hapus.
- Konten: daftar area/booth/eksibisi dan status publikasi demo.
- Analytics: rentang waktu demo dan ringkasan metrik.
- Pengaturan: status integrasi simulasi dan ekspor data asset ke JSON.
- Data asset disimpan di `localStorage`; file gambar yang diunggah hanya tersimpan di browser/perangkat ini. Hapus data browser dapat menghapus data tersebut.

## Integrasi ke proyek museum
Ini aplikasi admin yang berdiri sendiri agar tidak mengubah proyek Three.js Anda. Untuk produksi, buat API backend/authentication/database dan event tracking dari frontend museum (misalnya event `scene_enter`, `booth_view`, `asset_interaction`). Dashboard saat ini menggunakan data contoh dan **angka traffic bukan data pengunjung asli**.
