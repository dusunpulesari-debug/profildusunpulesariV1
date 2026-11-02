# Profil Dusun Pulesari — Paket Website Final

Paket ini menggabungkan 12 halaman utama beserta halaman 404, aset visual, dan dokumentasi dalam satu struktur root agar mudah diunggah ke GitHub Pages. Desain mengikuti mockup pengguna: sidebar hijau tua, topbar, banner panorama, kartu statistik, panel, tabel, kalender, katalog, dan tata letak responsif.

## Halaman website

| File | Halaman |
|---|---|
| `index.html` | Dashboard utama |
| `profil-dusun.html` | Profil Dusun |
| `produk-hukum-dusun.html` | Produk Hukum Dusun |
| `data-penduduk.html` | Data Penduduk (prototipe; jangan masukkan data sensitif ke situs publik) |
| `kelembagaan.html` | Kelembagaan |
| `kegiatan-agenda.html` | Kegiatan & Agenda |
| `potensi-dusun.html` | Potensi Dusun |
| `peta-potensi.html` | Peta Potensi |
| `surat-menyurat.html` | Surat Menyurat |
| `program-dusun.html` | Program Dusun |
| `kontak.html` | Kontak Kami |
| `pengaturan.html` | Pengaturan prototipe |
| `404.html` | Halaman tidak ditemukan |

## Isi paket

- Semua file HTML berada langsung di root.
- CSS dan JavaScript halaman ditanam di masing-masing file HTML.
- Logo dan gambar WebP berada di root.
- `.nojekyll` disertakan untuk GitHub Pages.
- Panduan upload, Google Sites, inventaris halaman, spesifikasi desain, pedoman gaya, rencana QA, dan laporan QA disertakan.

## Cara mencoba secara lokal

1. Ekstrak ZIP ke satu folder.
2. Buka `index.html` dengan browser untuk melihat halaman awal.
3. Untuk hasil uji navigasi yang lebih representatif, jalankan server statis dari folder proyek, misalnya `python -m http.server 8000`, lalu buka `http://localhost:8000`.
4. Peta Google Maps dan tautan eksternal memerlukan koneksi internet.

## Publikasi ke GitHub Pages

1. Buat atau buka repository GitHub yang akan digunakan.
2. Ekstrak ZIP final di komputer.
3. Unggah **semua isi folder ini** langsung ke root repository. Pastikan `index.html`, `.nojekyll`, semua file HTML, semua gambar, dan dokumentasi ikut terunggah. Jangan hanya mengunggah file ZIP.
4. Commit perubahan.
5. Buka **Settings → Pages**, pilih deploy dari branch utama dan folder root (`/`).
6. Tunggu hingga GitHub Pages menampilkan URL situs; buka URL tersebut dan periksa menu serta gambar.

## Menyematkan di Google Sites

1. Terbitkan dan uji website terlebih dahulu melalui GitHub Pages.
2. Buka halaman Google Sites.
3. Pilih **Sisipkan → Sematkan → URL**.
4. Tempelkan URL GitHub Pages, sesuaikan ukuran bingkai, lalu publikasikan Google Sites.

Google Sites tidak mengeksekusi ZIP secara langsung. Situs HTML perlu dipublikasikan sebagai situs web terlebih dahulu, lalu disematkan melalui URL. Bila tampilan embed terlalu sempit, gunakan lebar halaman penuh dan tinggi bingkai yang cukup.

## Fitur dan batasan prototipe

Fitur yang berjalan di sisi browser antara lain navigasi ant halaman, layout responsif, pencarian/filter pada beberapa katalog, interaksi kalender, filter lokasi/potensi, dialog/FAQ, serta pengaturan tampilan tertentu. Preferensi Pengaturan yang tersedia disimpan pada browser lokal dan tidak tersinkron ke pengguna lain.

Paket ini **belum memiliki backend, database bersama, autentikasi admin, unggah dokumen, pengiriman formulir, notifikasi nyata, atau penyimpanan pengajuan**. Jangan menganggap formulir atau kontrol prototipe sebagai layanan administrasi aktif. Fitur tersebut memerlukan backend atau layanan database/formulir yang dikelola dengan aman.

## Data dan aset yang harus diperbarui sebelum peluncuran

- Nama, alamat, sejarah, visi-misi, struktur pengelola, nama lembaga, kontak, jam layanan, kegiatan, program, dokumen, kategori layanan, serta rincian potensi masih perlu dikonfirmasi.
- Statistik yang belum tersedia ditampilkan sebagai placeholder atau keadaan kosong; tidak boleh diganti angka yang tidak bersumber.
- `hero-pulesari.webp` dan `logo-pulesari.webp` merupakan aset visual sementara dari referensi desain, bukan foto lapangan terverifikasi atau file logo resmi.
- `program-card-01.webp` sampai `program-card-08.webp` adalah potongan visual sementara dari mockup yang dikirimkan, bukan dokumentasi kegiatan nyata. Ganti dengan foto yang sah sebelum publikasi umum.
- Peta skematik hanya untuk visual; titik selain lokasi acuan pengguna harus diverifikasi sebelum ditambahkan.

## Privasi dan keamanan

Jangan menaruh NIK, tanggal lahir lengkap, alamat rinci keluarga, nomor pribadi, atau dokumen internal di repository publik. Informasi individu hanya boleh dikelola jika ada dasar kewenangan, pembatasan akses, kebijakan retensi, dan sistem backend yang aman. Repository publik dan GitHub Pages adalah tempat publikasi statis, bukan penyimpanan aman untuk data pribadi.

## Acuan desain

Resolusi desktop untuk pencocokan awal adalah 1536 × 1024 piksel. Sidebar sekitar 243 px, topbar sekitar 56 px, banner sekitar 244 px, dengan breakpoint responsif untuk tablet dan ponsel. Ukuran ini adalah titik awal desain, bukan ukuran wajib di semua layar.
