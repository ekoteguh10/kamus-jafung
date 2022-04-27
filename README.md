## Tentang Kamus Jafung (Jabatan Fungsional)

## Struktur Database

Secara umum, data yang disediakan pada kamus jafung memliki struktur tabel sebagai berikut:

* kode_unsur
* nama_unsur
* kode_sub_unsur
* nama_sub_unsur
* kode_butir_kegiatan
* nama_butir_kegiatan
* deskripsi
* satuan_hasil
* angka_kredit
* batasan_penilaian
* pelaksana
* bukti_fisik
* contoh_kegiatan

Untuk itu, kita perlu melakukan normalisasi atau penyesuaian menjadi beberapa tabel agar memudahkan untuk maintain database.

- tabel `unsur` dengan kolom `id`, `kode_unsur` dan `nama_unsur`
- tabel `sub_unsur` dengan kolom `id`, `kode_sub_unsur`, `nama_sub_unsur`, dan `id` pada tabel `unsur`
- tabel `pelaksana` dengan kolom `id`, `jabatan_pelaksana`, `jenjang_pelaksana`
- tabel `butir_kegiatan` dengan kolom `id`, `kode_butir_kegiatan`, `nama_butir_kegiatan`, `id` pada tabel `pelaksana`, `id` pada tabel `sub_unsur`, `id` pada tabel `unsur`, `angka_kredit`, `satuan_hasil`, `batasan_penilaian`
- tabel `detail_butir_kegiatan` dengan kolom `id`, `id` pada tabel `butir_kegiatan`, `deskripsi`, `bukti_fisik`, `contoh_kegiatan`


## Tim Pengembang
- Eko Teguh Widodo
- Ahlul Karom