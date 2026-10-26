# UML LAB. — Website Pembelajaran UML

Website statis untuk materi Analisis dan Perancangan Sistem Informasi (Pertemuan 4). Dibuat dengan HTML, CSS, dan JavaScript agar mudah dijalankan dari VS Code serta dipublikasikan melalui GitHub Pages.

## Isi proyek

- `index.html` — landing page dan daftar lima topik
- `materi.html` — template halaman materi; pilih topik menggunakan parameter URL
- `feedback.html` — halaman formulir feedback
- `css/style.css` — desain responsif
- `js/app.js` — navigasi, pencarian topik, materi dinamis, popup feedback, dan Web3Forms
- `assets/hero-analyst.jpg` — visual hero

## Menjalankan secara lokal

1. Ekstrak ZIP proyek.
2. Buka folder proyek melalui VS Code—folder yang berisi `index.html`.
3. Buka `index.html` di browser. Disarankan memakai ekstensi **Live Server** pada VS Code untuk pengalaman pengembangan yang lebih nyaman.
4. Coba kelima topik. Setiap halaman dapat dibuka lewat `materi.html?topik=uml`, `materi.html?topik=usecase`, `materi.html?topik=pembelian`, `materi.html?topik=waterfall`, atau `materi.html?topik=kebutuhan`.

Tidak diperlukan `npm install`, framework, atau proses build.

## Menghubungkan Web3Forms

Form feedback disiapkan, tetapi belum dapat mengirim pesan sampai access key milikmu dimasukkan.

1. Buka <https://web3forms.com/> dan buat access key untuk email penerima.
2. Buka `feedback.html`.
3. Cari `YOUR_WEB3FORMS_ACCESS_KEY`.
4. Ganti teks itu dengan access key milikmu. Jangan memasukkan password email atau kredensial lain.
5. Jalankan website melalui Live Server dan uji formulir. Setelah website online di GitHub Pages, uji kembali dari alamat online.

Tanpa access key, formulir sengaja menampilkan pesan konfigurasi dan tidak mengklaim bahwa feedback sudah dikirim.

## Publikasi menggunakan GitHub Pages

1. Buat repository baru di GitHub.
2. Upload seluruh **isi** folder proyek ke root repository, bukan folder pembungkusnya. Pastikan `index.html` terlihat di halaman utama repository dan struktur ini tetap utuh:
   - `css/style.css`
   - `js/app.js`
   - `assets/hero-analyst.jpg`
   - `materi.html`
   - `feedback.html`
3. Pastikan perubahan sudah diunggah ke branch `main` (commit dan push jika menggunakan Git).
4. Buka **Settings → Pages**.
5. Pada bagian Build and deployment, pilih **Deploy from a branch**, pilih branch `main` dan folder `/(root)`, lalu simpan.
6. Tunggu deployment selesai, buka URL GitHub Pages yang diberikan, lalu uji halaman beranda, semua tautan materi, dan halaman feedback.

Path file pada HTML/CSS bersifat relatif terhadap lokasi file dan harus cocok persis, termasuk huruf besar/kecil. Contohnya, `index.html` memuat `css/style.css` dan `js/app.js`, sedangkan gambar hero dirujuk dari CSS sebagai `../assets/hero-analyst.jpg`. Jangan memindahkan atau mengganti nama file/folder tanpa memperbarui rujukannya.

Jika website online masih menampilkan versi lama atau tanpa CSS/JavaScript, pastikan commit terbaru sudah masuk ke branch dan folder yang dipakai GitHub Pages, periksa struktur file di repository, lalu tunggu deployment selesai dan lakukan refresh paksa pada browser.

Karena ini website statis, GitHub Pages tidak menjalankan backend server. Web3Forms menangani submit formulir feedback dari sisi layanan eksternal.

## Keputusan desain dan 8 Golden Rules

1. **Consistency:** tipografi, navigasi, warna, tombol, dan judul bab digunakan secara konsisten.
2. **Shortcuts:** pencarian materi, daftar isi, tautan semua topik, dan kembali ke atas tersedia.
3. **Informative feedback:** interaksi popup, status formulir, serta pesan gagal/berhasil menjelaskan apa yang terjadi.
4. **Closure:** pengiriman feedback menampilkan konfirmasi; setiap materi mempunyai ringkasan.
5. **Error prevention/handling:** validasi kolom wajib, tipe email, batas panjang pesan, dan deteksi access key yang belum dikonfigurasi.
6. **Reversal:** popup dapat ditutup, form dapat dikoreksi sebelum dikirim, dan pengguna dapat berpindah topik.
7. **Internal locus of control:** pengguna memilih topik dan mengendalikan navigasi; tidak ada perpindahan paksa.
8. **Reduce memory load:** breadcrumb, daftar isi materi, nomor bab, label tombol, dan rangkuman membantu orientasi.

## Catatan materi akademis

Isi disusun berdasarkan topik yang muncul pada PDF pertemuan ke-4: definisi UML, konsep Use Case, studi kasus pembelian, Waterfall (Planning), dan analisis kebutuhan fungsional. Definisi diringkas/parafrasekan dan diberi sumber yang tersedia di bahan kuliah; jangan mengubah parafrasa menjadi kutipan langsung tanpa memeriksa sumber asli.

PDF menyebut referensi berikut:

- Satzinger, J. W., Jackson, R. B., & Burd, S. D. (2015). *Introduction to Systems Analysis and Design: An Agile, Iterative Approach* (7th ed.).
- Valacich, J. S., & George, J. F. (2017). *Modern Analysis and Design Methods* (8th ed.).
- Sukamto & Shalahuddin (2013), Tohari (2014), serta Dennis et al. (2015), sebagaimana disebutkan pada slide. Detail bibliografi lengkap dan nomor halaman perlu dicocokkan dengan buku asli sebelum pengumpulan tugas.

Studi kasus pembelian dan elemen perencanaan diadaptasi dari bahan presentasi. Contoh diagram tambahan adalah ilustrasi pembelajaran yang perlu divalidasi apabila dipakai sebagai spesifikasi sistem nyata.
