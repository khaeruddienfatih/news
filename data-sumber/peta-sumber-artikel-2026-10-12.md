# Peta Sumber Artikel Umroh & Haji — uji akses 2026-10-12

Tujuan: menentukan sumber lokal (Indonesia), Arab Saudi, dan negara lain yang bisa dipakai sebagai bahan artikel, serta apa yang benar-benar bisa dibaca dari lingkungan kerja ini.

## Cara uji
- `curl` lewat terminal ke 62 alamat (beranda, RSS, API).
- `WebFetch` ke 8 alamat sampel (Antara, Arab News, SPA, haj.gov.sa, Google News, Detik, Saudi Gazette, Tabung Haji).
- `WebSearch` (mesin pencari) dengan 5 kueri.

## Hasil akses

| Tingkat | Sumber | Cara | Catatan |
|---|---|---|---|
| **A — terbaca penuh** | haji.go.id (`/api/news`, `/api/hajj/waiting-list`) | curl | Isi berita lengkap + kategori + tanggal. Berita terbaru 11/10/2026. Bahan utama. |
| **A — terbaca penuh** | kemenag.go.id | curl | Beranda terbaca; RSS `/rss` error 500. Haji sudah pindah ke Kemenhaj, jadi relevansinya terbatas (indeks kepuasan jemaah, keagamaan). |
| **B — hanya cuplikan** | Semua media & situs lain | WebSearch | Dapat judul, URL, dan ringkasan, **bukan teks penuh**. Cukup untuk menemukan topik dan cek silang, tidak cukup untuk mengutip. |
| **C — diblokir** | Semua alamat lain | curl 403 (proxy), WebFetch DNS gagal | Ditolak kebijakan jaringan environment. |

Supaya kelompok B/C bisa dibaca penuh, pemilik perlu menambah domain ke **Allowed domains** di pengaturan Network access environment (lihat https://code.claude.com/docs/en/cloud-environments#network-access).

## Daftar sumber yang disarankan (urut prioritas)

### Indonesia — resmi
| Sumber | Alamat | Kegunaan |
|---|---|---|
| Kemenhaj RI | haji.go.id (API) | Patokan utama: kebijakan, siaran pers, klarifikasi hoaks, antrean. **Sudah terbaca.** |
| BPKH | bpkh.go.id | Dana haji, nilai manfaat |
| Imigrasi | imigrasi.go.id | Paspor jemaah |
| Kemenkes / Pusat Kesehatan Haji | kemkes.go.id | Istithaah kesehatan, vaksin meningitis |

### Indonesia — media pembanding
Antara (antaranews.com, termasuk biro daerah), Republika/Ihram (republika.co.id), Detik Hikmah (detik.com/hikmah), Kompas, Kontan, Bisnis.com, Tirto, RRI (termasuk Voice of Indonesia berbahasa Inggris), Okezone Muslim, NU Online (nu.or.id), Muhammadiyah, MUI (fatwa — rujuk lembaga, bukan klaim sendiri).

### Arab Saudi — resmi
| Sumber | Alamat | Kegunaan |
|---|---|---|
| Kementerian Haji dan Umrah | haj.gov.sa (Media Center → Ministry News) | Kalender musim umrah, aturan visa, rapat dengan kantor urusan haji 75+ negara |
| Nusuk | nusuk.sa | Izin Raudhah, pemesanan paket/hotel, aturan platform |
| Saudi Press Agency | spa.gov.sa | Pengumuman resmi pemerintah Saudi |
| Kemenkes Saudi | moh.gov.sa | Syarat kesehatan haji/umrah |
| Otoritas Dua Masjid Suci | alharamain.gov.sa | Layanan Masjidil Haram & Nabawi |
| Haramain High Speed Railway | hhr.sa | Jadwal kereta Makkah–Madinah |

### Arab Saudi & Teluk — media
Arab News, Saudi Gazette, Okaz, Al Riyadh, Sabq (Arab), Gulf News, Khaleej Times, The National, Al Arabiya.

### Negara lain (sudut pembanding / regional)
| Negara | Sumber | Contoh topik yang muncul |
|---|---|---|
| Malaysia | Tabung Haji (th.com.my), Bernama, Berita Harian | Surat tawaran haji 1448 H/2027 untuk 31.600 calon jemaah; biaya Muassasah RM33.300 (Bernama, 9/9/2026) |
| Pakistan | Ministry of Religious Affairs (mora.gov.pk), Dawn | Skema haji pemerintah |
| India | Haj Committee of India (hajcommittee.gov.in) | Kuota & jadwal |
| Bangladesh | Ittefaq | Aturan visa umrah baru |
| Brunei | Pelita Brunei | Jemaah Brunei |

## Peringatan dari hasil pencarian
- Banyak hasil teratas adalah **blog agen/OTA** (Wego, visitworld.today, umrahservices.in). Jangan dipakai sebagai sumber fakta; telusuri ke haj.gov.sa/SPA.
- Antar-sumber sering **bertentangan** (mis. tanggal akhir visa umrah: 9 Maret 2027 vs 1 September 2026; masa tinggal setelah masuk). Wajib cek ke sumber resmi Saudi sebelum terbit.
- Klaim "izin PPIU dicabut Oktober 2026" tidak ditemukan; yang ada: blokir Siskopatuh 3 PPIU (1/9), moratorium izin baru dan verifikasi ±3.900 PPIU (3/9). Untuk KBIHU: izin KBIHU Al-Fatah Purwakarta dicabut (haji.go.id, 9/10).

## Calon topik artikel dari haji.go.id (siap ditulis, sumber terbaca penuh)
1. 11/10 — Kemenhaj imbau WNI di Arab Saudi tingkatkan kewaspadaan (Siaran Pers).
2. 10/10 — 345 calon jemaah pernah gagal berangkat; Menhaj ingatkan kesehatan sejak dini.
3. 9/10 — Izin KBIHU Al-Fatah Purwakarta dicabut karena pungli dan manipulasi data jemaah.
4. 9/10 — Integrasi data kependudukan (Dukcapil) untuk lindungi hak jemaah.
5. 10–11/10 — Bali Expo: UMKM dan "Haji dan Umrah Store" (sudut ekonomi haji).

## Alur kerja yang diusulkan
1. Ambil topik dan fakta inti dari **haji.go.id API** (terbaca penuh).
2. Cari sudut Saudi/negara lain lewat **WebSearch**; catat URL sebagai rujukan.
3. Fakta dari sumber kelompok B ditandai `belum diverifikasi langsung` (sesuai Pedoman Redaksi) sampai domainnya dibuka atau dicek manual.
