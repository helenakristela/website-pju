# Website Penerangan Jalan Umum Dusun Kiarakoneng I

Situs statis (HTML/CSS murni, tanpa framework) yang berisi hal-hal yang perlu diketahui warga tentang Penerangan Jalan Umum yang dibuat oleh Kelompok 7 Pi7ar Cahaya KKN-D ITB 2026.

## Struktur File

```
site/
├── index.html
├── tentang-kami.html
├── cara-kerja-panel-surya.html
├── cara-memantau-kondisi-lampu.html
├── cara-mencegah-kerusakan.html
├── mekanisme-pelaporan.html
├── lokasi-titik-pju.html
├── perawatan-pju.html
├── kontak-pelaporan.html
├── style.css
└── vercel.json
```

## Yang Perlu Diisi Sebelum Publish

1. **kontak-pelaporan.html** — ganti nomor WhatsApp, email, dan kontak RT/RW.
2. **index.html** & **lokasi-titik-pju.html** — ganti `src` pada `<iframe>` peta dengan
   embed Google Maps lokasi dusun Anda yang sebenarnya:
   - Buka [Google Maps](https://maps.google.com), cari lokasi, klik **Bagikan** → **Sematkan peta**,
     lalu salin URL di dalam atribut `src="..."` iframe tersebut ke file HTML.
3. Sesuaikan teks di halaman lain (Tentang Kami, Cara Kerja, dll.) sesuai kondisi nyata di lapangan —
   teks yang ada sekarang adalah draf awal.

## Cara Deploy ke Vercel

### Opsi 1 — Vercel CLI (tercepat)
```bash
npm install -g vercel
cd site
vercel
vercel --prod
```

### Opsi 2 — Lewat GitHub + Vercel Dashboard
1. Buat repository baru di GitHub, lalu push seluruh isi folder `site/` ke repo tersebut.
2. Buka [vercel.com](https://vercel.com), klik **Add New → Project**, dan import repo GitHub tadi.
3. Pada bagian **Framework Preset**, pilih **Other** (situs ini statis, tidak butuh build command).
4. Klik **Deploy**. Vercel akan otomatis mempublikasikan situs ke `namaproyek.vercel.app`.

### Opsi 3 — Drag & drop
Di dashboard Vercel, buka **Add New → Project → Deploy** dan seret folder `site/` langsung ke area upload.

Tidak ada build step atau dependency yang diperlukan — semua file sudah siap disajikan sebagai situs statis.