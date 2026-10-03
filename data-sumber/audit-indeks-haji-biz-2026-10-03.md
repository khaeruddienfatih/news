# Audit Indeksasi haji.biz — 2026-10-03

Metode: konektor WordPress.com (hanya baca). Domain haji.biz diblokir dari lingkungan kerja, jadi robots.txt, sitemap, HTML, dan Search Console **belum bisa diperiksa langsung**.

## Terverifikasi
| Item | Hasil |
|---|---|
| Status situs | launched, visibility `public`, `blog_public=1` (tidak menghalangi mesin pencari) |
| Permalink | `/%postname%/` (baik) |
| Konten | 65 post: 43 terbit, 20 terjadwal (4–7 Okt, belum tayang), 2 lain; 14 halaman (11 terdaftar, 1 draf: Privacy Policy) |
| Pola terbit | 15 post terbit 1–3 Okt (5/hari, tiap 3 jam), sisanya bertanggal Jan–Sep 2026 |
| Trafik 26 Sep–3 Okt | 112 tampilan, 7 pengunjung |
| Rank Math (cek sebelumnya, via koneksi lama) | Search Console terhubung, keyword 30 hari terakhir kosong; skor SEO semua post "tidak tersedia" |
| Beranda `haji-plus` (id 197) | Elementor, data ±137 KB |

## Tidak terbukti penyebab
- Situs tidak privat, tidak "coming soon", tidak ada `discourage_search`.

## Belum bisa diperiksa
- robots.txt, sitemap, meta robots/canonical di HTML, status di Google Search Console (Page indexing), hasil `site:haji.biz`.

## Dugaan penyebab (urut kemungkinan)
1. Domain/situs baru dipindah ke WordPress.com (dibuat 3 Okt): Google perlu waktu mengcrawl ulang; otoritas rendah.
2. Banyak post baru terbit sekaligus dengan pola seragam (paket, hotel, harga) → rawan status "Discovered/Crawled – currently not indexed".
3. 20 post masih terjadwal, jadi belum bisa terindeks.
4. Tumpang tindih topik antar post (mis. #821 vs draf wukuf), risiko kanibalisasi.
