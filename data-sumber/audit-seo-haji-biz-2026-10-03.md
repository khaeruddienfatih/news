# Audit SEO haji.biz — 2026-10-03

**Cakupan:** 64 post (43 terbit, 20 terjadwal, 1 draf), 11 halaman, 33 kategori, 12 tag, 276 media (30 teratas diperiksa). Isi dibaca penuh untuk 3 post (#811, #297, #750). Metode: konektor WordPress.com, hanya baca.
**Tidak bisa diperiksa** (haji.biz diblokir dari lingkungan ini): robots.txt, sitemap, meta robots/canonical di HTML, Core Web Vitals, tautan balik, Search Console. Penilaian di bawah adalah penilaian saya, bukan skor alat.

## Ringkasan skor (perkiraan)
| Area | Nilai | Catatan |
|---|---|---|
| Teknis | Belum dapat dinilai | Pengaturan situs aman; sisanya tak terverifikasi |
| On-page | C | Judul panjang, banyak tanpa gambar unggulan, alt kosong, anchor TOC rusak |
| Konten | B− | Artikel baru (Okt) terstruktur baik; artikel lama tumpang tindih dan generik |
| Kepercayaan (E-E-A-T) | D | Fakta saling bertentangan antar halaman (lihat P0) |
| Off-page | Tidak diketahui | Trafik 7 pengunjung/minggu, sinyal eksternal tampak minim |

## P0 — Perbaiki dulu (kepercayaan dan cacat nyata)
1. **Nomor SK PIHK tidak konsisten.** Halaman `haji-plus` (#197) menulis "SK No.848/2020"; halaman `paket-haji-plus` (#113), #750, #811, dan #761 menulis "SK No.846 Tahun 2020". Satu dari keduanya salah. Cocokkan dengan dokumen izin asli, lalu seragamkan di seluruh situs dan Organization schema.
2. **Masa tunggu bertentangan:** #197 "8–10 tahun", #297 "5–9 tahun", #750 "6–10 tahun" (juga "sistem Kemenhaj ±10 tahun"), #713 "6–7 tahun", #811 tabel antrean 2027–2032 tanpa sumber. Tentukan satu rumusan, cantumkan tanggal dan rujukan resmi (haji.go.id/Siskohat).
3. **Harga bertentangan:** #713 menulis USD 9.000–15.000; #811 dan paket 1448 H menulis Silver 12.000 hingga Platinum 20.000 (empat per kamar). Seragamkan dan beri tanggal berlaku.
4. **Besaran setoran awal perlu diverifikasi.** Situs menulis 4.000 USD; sebagian sumber publik menyebut 4.500 USD untuk 2025. Cek angka terbaru di haji.go.id sebelum dipakai sebagai klaim utama.
5. **Rujukan otoritas usang.** Banyak tautan keluar ke `kemenag.go.id` dan frasa "Resmi Kemenag". Sejak 2026 haji dipegang Kemenhaj. Tautkan ke `haji.go.id` dan sistem verifikasi PIHK yang berlaku.
6. **Karakter rusak (mojibake) di #750:** "uang tunggu â€” dana", "ðŸ“‘ Daftar Isi" muncul di isi dan kutipan. Simpan ulang dengan encoding UTF-8 yang benar.
7. **Anchor daftar isi rusak** di #297 dan #750: tautan memakai `/#id` sehingga mengarah ke beranda, bukan ke bagian halaman. Ubah menjadi `#id`.
8. **Kemungkinan duplikasi host www vs non-www:** hasil pencarian menampilkan `www.haji.biz`, sedangkan WordPress memakai `haji.biz`. Pastikan satu versi saja (301 dari yang lain) dan canonical konsisten; di Search Console pakai properti Domain.
9. **Verifikasi indeksasi** (lihat audit sebelumnya): sitemap, `noindex`, Page indexing.

## P1 — Kanibalisasi dan konten tipis
Kluster yang saling berebut kata kunci (gabungkan ke satu pilar, sisanya 301 atau diubah fokusnya):
| Kluster | Post/halaman | Saran |
|---|---|---|
| "Haji plus termurah / terpercaya / Jakarta" | #276, #280, #297, #302, #322, #761 | Satu pilar, sisanya dirapikan atau 301 |
| Halaman kota (Bandung, Tangerang, Depok, Bekasi, Bogor) | #347, #342, #336, #331, #763 | Isi seragam bergaya templat; tambahkan data lokal asli (alamat kantor, jadwal manasik lokal, testimoni) atau gabungkan |
| Cara daftar dan syarat | #727 (judul huruf kecil), #725 (draf), #707, #720 | Satu panduan "Cara Daftar Haji Plus 2027" |
| Biaya | #576, #713, #814, #813 | Satu pilar biaya + artikel pendukung |
| Antrean/masa tunggu | #490, #811 | Satu pilar, perbarui dengan data resmi |
| Haji khusus umum | #495, #750, #608, #581, #586 | Tetapkan pilar "Apa itu haji khusus/haji plus" |
| Halaman paket | #113, #197, #226, #742 | Satu target "haji plus" (#197), tiga lainnya fokus berbeda |
Catatan: #259 "Shalat Jenazah" tidak relevan dengan fokus situs; pertimbangkan dihapus atau dialihkan.

## P2 — On-page
- **Judul:** banyak 60–100 karakter ("Paket Haji Plus Jakarta: Panduan Lengkap Perjalanan Ibadah Bersama Elharamain Wisata"). Pangkas ke ≤60, kata kunci di depan, merek di belakang. Cek apakah judul SEO Rank Math berbeda dari judul post.
- **Gambar unggulan:** sekitar 26 dari 64 post tidak punya (semua 12 post umroh terjadwal, post kota, #713, #297, #267, dll.).
- **Teks alt:** 28 dari 30 media teratas di perpustakaan tidak punya alt; #297 punya gambar `alt=""`. Isi alt deskriptif.
- **Judul tidak rapi:** #727 "cara daftar haji plus: langkah…" (huruf kecil).
- **Taksonomi:** 33 kategori, sebagian besar sisa templat (Bali Tours, Hiking, Sport, Science, Politics, Money, Globe News, West Bali, dll.), banyak kategori berisi 1 post dan berjudul seperti kata kunci (arsip tipis). 12 tag sisa templat, semua kosong. Sisakan 5–7 kategori (Haji Plus, Haji Khusus, Umroh, Manasik, Panduan, Berita) dan hapus tag kosong.
- **Tautan internal:** artikel baru hanya punya 2 tautan "Baca juga"; tambahkan tautan ke pilar dengan anchor deskriptif dan tautan balik dari pilar ke artikel.
- **Markup:** #811 memasukkan blok `<style>` dan `<script>` inline di isi post; pindahkan CSS ke tema/CSS khusus agar ringan dan seragam. FAQPage schema ada, tetapi Google sejak 2023 membatasi rich result FAQ untuk situs pemerintah/kesehatan terkemuka, jadi jangan berharap tampilan khusus.
- **Privacy Policy** masih draf: terbitkan versi yang sesuai bisnis.
- Pembacaan isi beranda (#197) lewat API gagal ("Invalid JSON response… markup document"), kemungkinan ada keluaran peringatan atau halaman Elementor ±137 KB yang bermasalah; periksa di PageSpeed Insights.

## P3 — Konten, merek, dan sinyal eksternal
- Ikuti `strategi-kata-kunci-haji-plus.md` (biaya, cara daftar, perbandingan, legalitas, pindah jalur, cicilan).
- 20 post umroh terjadwal (4–7 Okt) membelokkan fokus topikal dari "haji plus"; buat hub "Umroh" terpisah dan jangan menerbitkan massal tanpa nilai tambah (risiko dinilai konten massal bermutu rendah).
- Tampilkan penulis/penelaah, tanggal pembaruan, dan sumber resmi di artikel; cantumkan izin, alamat, rekening resmi (sudah ada di #816, bagus).
- Google Business Profile untuk 6 kantor (Bekasi, Jakarta, Depok, Tangerang, Bandung, Bogor), ulasan asli.
- Tautan balik relevan (asosiasi, media lokal), pantau di Search Console.

## Yang sudah baik
- Situs publik, URL `/%postname%/`, kolom meta/kutipan ringkas di artikel Oktober, tabel dan FAQ jelas, ada halaman Lokasi Kantor dan Tentang Kami, rekening resmi dan peringatan penipuan (#816).

## Rencana 30 hari
| Minggu | Tindakan |
|---|---|
| 1 | P0: seragamkan SK, masa tunggu, harga, setoran; perbaiki mojibake dan anchor; cek www/non-www dan Search Console |
| 2 | Gabungkan kluster kanibalisasi, atur 301; bersihkan kategori/tag; terbitkan Privacy Policy |
| 3 | Judul ≤60 karakter, gambar unggulan, alt; tautan internal ke pilar |
| 4 | Terbitkan 3 pilar baru (biaya, cara daftar, perbandingan); kirim sitemap; mulai GBP dan ulasan |
