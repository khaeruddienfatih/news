# Redaksi Umroh & Haji

Repositori ini adalah ruang redaksi untuk liputan profesional seputar **ibadah umroh dan haji**: regulasi, layanan, biaya, penyelenggara (PIHK/PPIU), kebijakan Arab Saudi, serta panduan untuk jamaah.

Semua pekerjaan disimpan di branch `main`.

## Struktur

| Folder / berkas | Isi |
|---|---|
| `artikel/` | Naskah berita, feature, dan panduan. Satu berkas per naskah, nama `YYYY-MM-DD-slug.md`. |
| `artikel/_template/` | Templat naskah (berita, feature, panduan). |
| `percakapan/` | Catatan arahan dan keputusan redaksi dari tiap sesi kerja, per tanggal. |
| `data-sumber/` | Catatan sumber, tautan rujukan, dan data pendukung. |
| `PEDOMAN-REDAKSI.md` | Standar etika, verifikasi, gaya bahasa. |

## Alur kerja

1. Arahan topik dicatat di `percakapan/`.
2. Naskah ditulis dari templat, status `draf`.
3. Fakta diverifikasi dan sumber dicantumkan, status `siap-terbit`.
4. Semua perubahan di-commit ke `main` dengan pesan yang jelas.
