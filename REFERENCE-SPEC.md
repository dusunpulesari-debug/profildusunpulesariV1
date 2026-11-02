# REFERENCE SPEC — WEBSITE PROFIL DUSUN PULESARI

Status: Tahap 1 — analisis mockup dan penguncian spesifikasi desain  
Target implementasi: HTML statis, CSS dan JavaScript inline, GitHub Pages, penyematan Google Sites.

## 1. Tujuan

Website Profil Dusun Pulesari dirancang sebagai dashboard informasi dan administrasi dusun, bukan hanya landing page profil. Referensi visual utama adalah lima mockup yang dikirimkan pengguna: Produk Hukum Dusun, Kontak Kami, Data Penduduk, Program Dusun, serta Kegiatan & Agenda.

Seluruh angka, nama warga, nomor kontak, alamat terperinci, tanggal kegiatan, status dokumen, dan statistik yang terlihat di mockup dianggap sebagai contoh visual dan tidak boleh dipindahkan menjadi fakta website. Konten awal harus berupa placeholder yang jelas.

## 2. Arsitektur visual global

- Resolusi kerja desktop awal: 1536 × 1024 piksel.
- Sidebar kiri: perkiraan 243 px, penuh tinggi viewport, warna hijau gelap.
- Topbar: perkiraan 56 px, putih, berada di sisi kanan sidebar.
- Banner halaman: kira-kira 205–245 px, menggunakan foto panorama dengan overlay gelap.
- Konten utama: latar abu-abu sangat muda, padding sekitar 16–20 px.
- Kartu/panel: putih, border abu-abu tipis, radius 10–14 px, bayangan lembut.
- Layout dashboard desktop: grid utama dengan konten kiri sekitar 70–75% dan panel kanan 25–30% jika jenis halaman membutuhkannya.
- Jarak antarkomponen: 12–16 px; jarak dalam panel: 12–20 px.
- Semua nilai di atas merupakan baseline untuk implementasi dan harus dikalibrasi dengan screenshot pada resolusi yang sama.

## 3. Token warna

| Token | Nilai | Pemakaian |
|---|---|---|
| --pulesari-forest | #073B2B | Sidebar dan identitas utama |
| --pulesari-green | #087A50 | Tombol utama, status berhasil, navigasi aktif |
| --pulesari-gold | #F0A323 | Aksen judul, penanda menu aktif, garis banner |
| --pulesari-blue | #2457A7 | Ikon informasi, tautan, elemen navigasi sekunder |
| --pulesari-ink | #172B4D | Teks utama dan judul panel |
| --pulesari-muted | #64748B | Label dan teks keterangan |
| --pulesari-page | #F4F6F9 | Latar area konten |
| --pulesari-card | #FFFFFF | Kartu, formulir, tabel |
| --pulesari-line | #E1E7EF | Border dan garis pembagi |

Warna pastel tambahan dipakai untuk latar ikon statistik dan badge kategori, bukan untuk latar halaman utama.

## 4. Tipografi

- Judul banner: serif elegan (Georgia atau Playfair Display jika tersedia), tebal, sekitar 40–48 px di desktop.
- Judul panel: serif tebal, 18–21 px.
- Isi, kontrol, label dan tabel: sans-serif UI seperti Inter, system-ui, atau Arial; 12–15 px.
- Label kategori dan keterangan tabel: 11–13 px.
- Judul banner dua warna: kata utama putih; kata penekanan seperti “Pulesari” emas.
- Hindari tipografi terlalu besar pada kartu kecil; hierarki konten harus mirip mockup.

## 5. Sidebar dan topbar

### Sidebar

Menu, urutannya tetap:
1. Dashboard
2. Profil Dusun
3. Produk Hukum Dusun
4. Data Penduduk
5. Kelembagaan
6. Kegiatan & Agenda
7. Potensi Dusun
8. Peta Potensi
9. Surat Menyurat
10. Program Dusun
11. Kontak Kami
12. Pengaturan

Komponen sidebar:
- Logo/nama “DUSUN PULESARI” di bagian atas.
- Ikon di kiri, teks menu di kanan.
- Menu aktif menggunakan latar emas/jingga, teks putih, dan radius lembut.
- Slogan “Pulesari Migunani” di area bawah sebagai dekorasi.
- Pada desktop sidebar tetap. Pada tablet/ponsel, sidebar menjadi drawer yang dibuka melalui tombol menu.

### Topbar

- Tombol hamburger.
- Kolom pencarian global.
- Notifikasi dengan indikator angka (indikator hanya visual jika belum ada backend).
- Avatar, label “Admin Pulesari” dan menu profil (visual/prototipe bila belum memakai autentikasi).
- Tanggal dan jam otomatis dalam zona waktu Asia/Jakarta.

## 6. Banner halaman

- Foto panorama yang sama pada seluruh halaman untuk konsistensi.
- Overlay gelap transparan; bagian kiri dibuat lebih gelap agar teks terbaca.
- Breadcrumb kecil di bagian atas banner.
- Garis emas vertikal di samping judul.
- Judul serif besar, putih dengan aksen emas.
- Deskripsi maksimal dua baris pada desktop.
- Slogan/logo dapat ditempatkan di kanan banner apabila foto dan kontras memungkinkan.
- Foto resmi Pulesari belum disediakan pada tahap analisis, sehingga wajib menggunakan placeholder yang diganti setelah aset terverifikasi tersedia.

## 7. Rincian layout per halaman

### 7.1 Dashboard — `index.html`
- Banner selamat datang.
- Baris kartu ringkasan untuk kategori informasi dusun; angka kosong sampai data resmi tersedia.
- Area utama berisi agenda terbaru, program, pengumuman atau pintasan layanan.
- Panel samping untuk agenda/pengumuman.

### 7.2 Profil Dusun — `profil-dusun.html`
- Identitas wilayah, sejarah, kondisi geografis, visi-misi, struktur pengelola, dan galeri.
- Teks sejarah, batas wilayah, serta struktur organisasi tidak boleh direka.

### 7.3 Produk Hukum Dusun — `produk-hukum-dusun.html`
- Tab kategori dokumen.
- Empat kartu ringkasan tanpa angka rekaan.
- Pencarian judul dan filter jenis/tahun/status.
- Tabel dokumen dengan kolom nomor, judul, jenis, nomor dokumen, tahun, status, dan aksi.
- Panel kanan untuk kategori dan dokumen terbaru.
- Bila dokumen belum dimasukkan, tampilkan pesan kosong yang jelas.

### 7.4 Kontak Kami — `kontak.html`
- Kartu alamat, telepon/WhatsApp, email dan media sosial.
- Layout tiga kolom: peta/lokasi; formulir pesan; layanan cepat.
- Area bawah untuk jam layanan, tautan media sosial dan petugas jika data resmi tersedia.
- Form tanpa backend harus menjelaskan bahwa pengiriman belum tersimpan; jangan menampilkan sukses palsu.

### 7.5 Data Penduduk — `data-penduduk.html`
- Kartu statistik demografi tanpa angka rekaan.
- Tab semua penduduk, per KK, per RT, kategori, statistik, dan grafik sesuai data yang nantinya tersedia.
- Pencarian/filter dan tabel.
- Panel kanan menampilkan grafik hanya dari data sumber yang sah.
- Jangan gunakan data pribadi/NIK palsu. Jangan publikasikan NIK, tanggal lahir rinci, atau daftar keluarga di halaman publik.

### 7.6 Kelembagaan — `kelembagaan.html`
- Kartu lembaga, fungsi, pengurus (jika disetujui), program, dan dokumentasi.
- Kategori lembaga bisa diubah setelah struktur resmi diterima.

### 7.7 Kegiatan & Agenda — `kegiatan-agenda.html`
- Kartu ringkasan kegiatan.
- Tab kalender, daftar, agenda rutin, program kerja, kategori, arsip.
- Kalender bulanan di kiri, daftar agenda mendatang di tengah, panel kategori/agenda rutin di kanan.
- Kalender harus bisa berpindah bulan; data acara tetap kosong sampai ada data resmi.

### 7.8 Potensi Dusun — `potensi-dusun.html`
- Grid kartu potensi berisi foto, nama, ringkasan, kategori dan lokasi bila tersedia.
- Kategori awal: UMKM, pertanian, wisata, budaya, lingkungan, fasilitas; kategori dapat disesuaikan.

### 7.9 Peta Potensi — `peta-potensi.html`
- Peta/lokasi acuan dari tautan Google Maps yang diberikan pengguna.
- Filter kategori, marker dan panel detail hanya ditambahkan untuk lokasi yang sudah diverifikasi.
- Tautan acuan: https://maps.app.goo.gl/eLzpGyxQdvcxtYuH6

### 7.10 Surat Menyurat — `surat-menyurat.html`
- Kartu kategori pelayanan, persyaratan, alur dan tautan formulir jika sudah tersedia.
- Pengajuan dan pelacakan status tidak boleh diklaim aktif tanpa backend.

### 7.11 Program Dusun — `program-dusun.html`
- Kartu ringkasan program.
- Tab kategori program.
- Grid kartu program dengan foto/ilustrasi, kategori, nama, deskripsi, periode dan status jika ada data.
- Panel samping program unggulan dan agenda mendatang.
- Jangan isi progress/persentase tanpa laporan resmi.

### 7.12 Pengaturan — `pengaturan.html`
- Pengaturan antarmuka dan metadata prototipe.
- Pengaturan akun/hak akses nyata perlu autentikasi dan backend.

### 7.13 Halaman fallback — `404.html`
- Pesan halaman tidak ditemukan dan tautan kembali ke `index.html`.

## 8. Aturan data kosong

- Statistik: gunakan “—” atau “Belum diisi”.
- Tabel: tampilkan empty state, bukan baris contoh warga/dokumen fiktif.
- Kalender: bulan dapat ditampilkan tanpa acara.
- Grafik: jangan menggambar data seolah-olah nyata. Tampilkan empty state sampai sumber tersedia.
- Foto yang belum ada: gunakan placeholder dan label bila perlu.
- Alamat, nomor telepon, email, sosial media, struktur lembaga dan jam layanan hanya dimasukkan setelah konfirmasi.

## 9. Responsivitas

- Desktop lebar: sidebar tetap, topbar, banner dan grid dengan panel kanan.
- Tablet: sidebar bisa diciutkan; grid berubah 2 kolom; panel kanan berpindah ke bawah jika sempit.
- Ponsel: sidebar menjadi drawer; kartu 1–2 kolom; panel menjadi vertikal; tabel memiliki scroll horizontal atau kartu responsif; banner dan judul lebih kecil.
- Pastikan tombol memiliki fokus keyboard dan ukuran sentuh yang cukup.

## 10. Arsitektur teknis yang mengikuti SPENSABA SMART SPACE

- `index.html` harus langsung berada di root repository.
- Seluruh HTML halaman utama berada langsung di root, bukan dalam folder bersarang.
- CSS dan JavaScript utama di-inline di masing-masing HTML; tidak ada dependency wajib stylesheet/script eksternal.
- Aset visual `.webp` berada langsung di root agar mudah diunggah melalui GitHub Web.
- Sertakan `.nojekyll`, `404.html`, `README.md`, `STYLE.md`, `APP.md`, `SITE-INVENTORY.txt`, `QA-REPORT.txt`, `GOOGLE-SITES-PANDUAN.md`, dan `PANDUAN-UPLOAD-GITHUB.txt`.
- Konten dasar harus tetap terlihat tanpa JavaScript (progressive enhancement); sertakan `noscript` dan fallback untuk elemen animasi.
- Pencarian, filter dan kalender statis bekerja di sisi klien bila memungkinkan. Data disimpan hanya pada browser jika memakai localStorage.
- GitHub Pages adalah hosting statis; autentikasi sungguhan, penyimpanan data bersama dan pengiriman formulir memerlukan backend/layanan tepercaya.

## 11. Acuan pemeriksaan visual

Semua screenshot uji diambil pada viewport yang sama dengan screenshot acuan, dimulai dari 1536 × 1024. Periksa:
1. Posisi dan lebar sidebar.
2. Tinggi topbar dan banner.
3. Padding area konten.
4. Jumlah kolom dan proporsi panel.
5. Ukuran judul, label dan tabel.
6. Warna, radius, border dan bayangan.
7. Crop dan kontras foto banner.
8. Status menu aktif.
9. Tampilan kosong untuk data yang belum tersedia.
10. Perilaku pada tablet/ponsel.

Spesifikasi ini menjadi acuan desain untuk paket final. Implementasi prototipe 12 halaman beserta halaman 404 telah digabungkan. Pemeriksaan struktural dan render akhir dicatat dalam `QA-REPORT.txt`; pencocokan piksel sepenuhnya, verifikasi data resmi, dan publikasi ke akun GitHub/Google Sites masih perlu dilakukan sebelum peluncuran publik.
