# Sumber Rujukan Redaksi

Diperbarui: 2026-10-03

## Patokan utama (hierarki sumber)
1. **https://haji.go.id** — situs resmi Kementerian Haji dan Umrah RI (Kemenhaj). Sejak 2026 penyelenggaraan haji beralih dari Kemenag ke Kemenhaj. Patokan utama kebijakan, kuota, jadwal, biaya, dan pengumuman resmi.
2. Akun media sosial resmi Kemenhaj dan juru bicara Kemenhaj.
3. Siskohat (Sistem Informasi dan Komputerisasi Haji Terpadu) untuk pendataan porsi, pelunasan, dan pembatalan.
4. Kementerian Haji dan Umrah Arab Saudi, BPKH, Imigrasi (imigrasi.go.id) untuk aspek terkait.
5. Media arus utama sebagai pembanding, bukan sumber tunggal: Antara, Kompas, Bisnis.com, Kontan, Tirto, RRI.

## Catatan akses
- ~~`haji.go.id` diblokir~~ — sudah terbuka lewat terminal pada 2026-10-03; lihat bagian "Akses haji.go.id" di bawah.
- `kemenhaj.go.id` tidak ditemukan (DNS gagal). Jangan dipakai sebagai rujukan.

## Fakta awal terverifikasi lewat media (haji 1447 H / 2026)
- Keberangkatan jemaah: 22 April–21 Mei 2026; pemulangan: 1 Juni–1 Juli 2026.
- Hingga 26/4/2026 pukul 24.00 WIB: 88 kloter, 34.657 jemaah diberangkatkan; 78 kloter, 30.611 jemaah tiba di Madinah.
- Juru bicara Kemenhaj: Maria Assegaff.
- Sumber: [Kompas TV](https://www.kompas.tv/nasional/665523/update-haji-2026-34-657-jemaah-berangkat-pemerintah-pastikan-layanan-tetap-optimal), [Kontan](https://nasional.kontan.co.id/news/kemenhaj-pastikan-pelaksanaan-haji-2026-tetap-berjalan-sesuai-jadwal), [Bisnis.com](https://kabar24.bisnis.com/read/20260301/15/1956671/kemenhaj-pastikan-persiapan-haji-2026-tak-terdampak-konflik-as-israel-vs-iran)

## Antihoaks
- Rujukan cek fakta: [RRI — hoaks pendaftaran petugas haji 2027](https://rri.co.id/banjarmasin/cek-fakta/2177811/hoaks-kementerian-haji-dan-umrah-buka-pendaftaran-petugas-haji-2027), [Tirto — hoaks undian haji umrah gratis](https://tirto.id/hoaks-undian-haji-umrah-gratis-dari-kementerian-agama-hqQZ).

## Akses haji.go.id (diperbarui 2026-10-03)
Domain **sudah dapat dibaca lewat terminal (`curl`)**. `WebFetch` hanya mendapat kerangka halaman karena situs adalah aplikasi React yang memuat isi lewat JavaScript; render Chromium macet, jadi jangan diandalkan. Gunakan endpoint API publik situs:

| Endpoint | Isi |
|---|---|
| `https://haji.go.id/api/news` | Berita resmi (795 berita, 80 halaman; kategori: Siaran Pers, Nasional, Daerah, Internasional, Pengumuman, Klarifikasi Hoaks, Feature). Tiap item: `title`, `content`, `category`, `publishDate`, `slug`, `tags`. |
| `https://haji.go.id/api/hajj/waiting-list` | Kuota, masa tunggu, porsi terakhir, jumlah pendaftar, lunas tunda per provinsi (34 wilayah). **Tanpa tanggal pembaruan**; tulis "data diakses pada <tanggal>". |
| `https://haji.go.id/api/config` | Kontak resmi, media sosial resmi. |

Tautan publik berita: `https://haji.go.id/berita/<slug>`.

Kontak resmi (dari `/api/config`): kemenhaj.ri@haji.go.id, 021-3900021 / 021-3900020. Media sosial: @kemenhaj_ri (TikTok, X), @kemenhaj.ri (Instagram), facebook.com/kemenhaj.

Salinan data tersimpan di `data-sumber/haji-go-id/` (snapshot 2026-10-03).

### Berita terbaru resmi (per 2026-10-01)
- 1/10: Kemenhaj–Kemendagri padankan data jemaah haji (integrasi Siskohat–Dukcapil).
- 29/9: 189 aduan masuk, Kemenhaj perketat pengawasan travel umrah.
- 29/9: Kemenhaj tegaskan kewajiban travel berizin dan standar harga umrah (melindungi 200 ribu jemaah per bulan).
- 29/9: 50 persen travel umrah tak aktif, aturan dirombak dan perizinan didigitalisasi.
- 28/9: Presiden: tata kelola keuangan haji diaudit.
