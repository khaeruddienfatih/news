# Audit SEO news.elharamainwisata.com

Tanggal pemeriksaan: 6–7 Oktober 2026. ID situs WordPress.com: 257737206.

## Cakupan dan batasan
- Dibaca penuh: pengaturan situs, daftar plugin, 11 kategori, 13 halaman, satu artikel sampel, halaman Home.
- Dibaca sebagian (sampel): 100 dari 1.688 artikel, 100 dari 1.679 gambar, 100 dari 2.011 tag. Persentase di bawah berasal dari sampel.
- HTML live dibaca setelah domain diizinkan di network policy environment.
- Field meta Rank Math tidak terdaftar di REST, sehingga tidak bisa dibaca atau ditulis lewat API.

## Temuan (kondisi awal, sebelum perbaikan)
1. Sitemap hanya memuat 857 URL artikel (200 + 657) dari 1.688 artikel. Indeks sitemap mencantumkan `attachment-sitemap` 1 dan 2 yang mengembalikan 404.
2. Home: tanpa meta description yang layak, tanpa OG/schema, tanpa H1, title 212 karakter, tiga tombol "View All" mengarah ke `/`.
3. `<html lang="en-US">` dan `og:locale = en_US` padahal konten berbahasa Indonesia.
4. Artikel: H1 benar, tetapi ada ~20 H2 yang berasal dari widget sidebar/footer; isi artikel sendiri tanpa H2.
5. Alt text: gambar utama artikel `alt=""`; 100 dari 100 gambar sampel di Media Library tanpa alt.
6. Judul panjang: 84 dari 100 artikel berjudul lebih dari 60 karakter; 30 dari 100 slug lebih dari 75 karakter.
7. Excerpt kosong sehingga excerpt/description otomatis terpotong di tengah kalimat.
8. Tag: 2.011, hampir semua dipakai 0–1 artikel, ada varian ganda (`air zam-zam`/`air zamzam`, `Arab Saudi`/`arabsaudi`). Arsip tag dan kategori sudah `noindex, follow` (baik).
9. Kategori "Berita" (1.264) dan "Umroh & Haji" (1.208) tumpang tindih; "Tanya Jawab" kosong. Halaman statis `/berita/`, `/umroh-haji/` dst. memakai slug yang sama dengan kategori.
10. robots.txt memblokir crawler AI lewat Jetpack (GPTBot, ClaudeBot, Google-Extended, CCBot, Applebot-Extended, Amazonbot, Bytespider, meta-externalagent). Keputusan bisnis pemilik situs.

## Perubahan yang sudah diterapkan
- Bahasa situs diubah ke `id_ID` (terverifikasi di HTML live: `lang="id"`, `og:locale = id_ID`).
- Home: disisipkan H1 tersembunyi secara visual (`screen-reader-text`): "Elharamain News: Berita Umroh, Haji, dan Update Jamaah Terbaru".
- Home: excerpt diisi sehingga meta description tidak lagi "Headline" (terverifikasi di HTML live).
- Pemilik situs menghapus plugin Yoast; Rank Math Pro aktif. robots.txt bersih dari blok Yoast.

## Yang masih perlu dikerjakan di wp-admin
- Rank Math → Sitemap Settings: simpan ulang, matikan sitemap attachment, kosongkan cache (indeks sitemap masih memuat stylesheet `wordpress-seo` dari cache). Periksa lagi jumlah URL artikel.
- Rank Math → Titles & Meta: title Home (`Elharamain News: Berita Umroh, Haji & Update Jamaah Terbaru`), template description artikel (`%excerpt%`).
- Widget sidebar/footer: ganti pembungkus H2 menjadi `<p>`/H3.
- Tombol "View All" di Home: arahkan ke arsip yang relevan.
- Alt text gambar, gabung tag duplikat, tentukan peran halaman statis yang bentrok dengan kategori.
