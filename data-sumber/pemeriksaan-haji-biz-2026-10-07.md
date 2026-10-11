# Pemeriksaan haji.biz (WordPress.com + HTML live)

Tanggal: 7–11 Oktober 2026. ID situs WordPress.com: 257739192. Melengkapi `audit-seo-haji-biz-2026-10-03.md`.

## Kondisi umum
- Bahasa `id_ID`, publik, halaman depan statis "Haji Plus" (ID 197). 12 halaman, 65 posting (4 terjadwal 7 Okt), 287 gambar.
- Rank Math + Rank Math Pro (tanpa plugin SEO ganda). Plugin AI 1.4.0 aktif; penyedia Anthropic, Google, OpenAI terpasang. Classic Editor sudah nonaktif. Image Optimization (Elementor) aktif.

## Yang baik
- Home, halaman paket, dan artikel punya title, meta description (Home 149 karakter), canonical, OG, Twitter card, H1.
- Artikel contoh `miqat-jiranah` memuat skema FAQPage dan alt gambar lengkap.
- Sitemap Rank Math bersih: 61 artikel, 10 halaman, 16 kategori, news sitemap. Arsip pencarian, 404, dan penulis `noindex`.
- Respons Home/artikel sekitar 0,4–1,3 detik.

## Temuan
1. **Kategori sebagai halaman kata kunci tipis**: sitemap memuat 16 kategori (mis. `paket-haji-plus-jakarta`, `biaya-haji-khusus-2027`), arsip `index, follow`, banyak yang berisi 1 artikel. Disarankan gabung ke 3–4 kategori utama atau `noindex` untuk yang kurang dari 3 artikel.
2. **Schema salah jenis**: Home, halaman paket, dan artikel semuanya `NewsArticle`. Halaman sebaiknya Organization/TravelAgency/WebPage.
3. **Alt text kosong**: Home 18 dari 108 gambar; Paket Haji Plus 12 dari 119; Media Library 82 dari 100 sampel.
4. `/blog/` tanpa H1 dan tanpa meta description.
5. 11 dari 20 posting terbaru tanpa featured image.
6. Artikel dibangun dari satu blok Custom HTML dengan CSS tertanam per artikel; fitur AI per blok (ubah teks, terjemahan, catatan editorial) tidak akan bekerja pada teks artikel.
7. Home 108 gambar, 26 script, 13 stylesheet; `/paket-haji-plus/` 119 gambar dan 2,7 detik.
8. Privacy Policy masih draft. robots.txt memblokir crawler AI (Jetpack).
9. Jadwal posting padat (3–4 per hari) dengan pola judul mirip; periksa risiko konten tipis/kanibalisasi.

## Konektor AI (plugin AI di WordPress)
- Error "The google AI connector has not been approved for use by ai/ai.php" berasal dari fitur Connector Approvals, bukan masalah jaringan atau API key. Perbaikan: setujui konektor untuk plugin AI di wp-admin (Pengaturan → Connectors/AI).
- Konektor Anthropic hanya menghasilkan teks; gambar dari Google (Gemini/Imagen) atau OpenAI.
- Fitur plugin AI sifatnya manual; penulisan artikel utuh dan otomatisasi masih "Coming Soon" menurut README plugin.

## Pembersihan Media Library (11 Oktober 2026)
Atas persetujuan pemilik, 7 gambar sisa template dihapus permanen setelah dicek tidak dipakai di 71 halaman/artikel live: `travel` (455), `fitnes` (449), `diet-3` (446), `rafting` (463), `honeymoon` (461), `kubu-kauh` (465), `placeholder` (424).
Masih ada sisa template lain (mis. `travel2`–`travel7`, `fitnes-2`, `fitness-3`, `um-*`, `ts-*`, `ww-*`); belum dihapus, perlu cek pemakaian di Elementor.
