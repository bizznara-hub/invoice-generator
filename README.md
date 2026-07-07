# ScribeInvoice — Buat Invoice Profesional dalam 2 Menit, Tanpa Daftar, Tanpa Ribet

**Pernah butuh invoice mendadak, tapi malas daftar akun, verifikasi email, lalu mentok di paywall?** ScribeInvoice hadir untuk momen itu. Buka halamannya, isi datanya, unduh PDF-nya. Selesai.

> *Buka. Isi. Unduh. Tagih.*

## 🔒 Data Keuangan Anda Tidak Pernah Meninggalkan Laptop Anda

Ini bukan jargon marketing — ini arsitektur. ScribeInvoice berjalan **100% di browser Anda**. Tidak ada server yang menyimpan nilai kontrak Anda, tidak ada database berisi daftar klien Anda, tidak ada risiko kebocoran data dari pihak ketiga. Angka Rp 500 juta di invoice Anda? Hanya Anda dan browser Anda yang tahu.

## ⚡ Lihat Hasilnya Sebelum Anda Selesai Mengetik

Layar terbagi dua: ketik di kiri, dan kertas A4 di kanan langsung berubah — huruf demi huruf. Ganti diskon, total langsung terhitung. Ganti mata uang, format ribuan langsung menyesuaikan. Tidak ada tombol "Preview", karena semuanya *sudah* preview. Skala tampilan pun menyesuaikan otomatis di layar HP, tablet, maupun desktop.

## 🖨️ PDF Setajam Hasil Percetakan

Ekspor menggunakan render resolusi 300 DPI — logo tidak pecah, garis tidak buram, teks tetap tajam bahkan saat dicetak fisik dan disodorkan ke meja direktur keuangan klien Anda. Hasil unduhan dijamin identik dengan yang Anda lihat di preview.

## 🇮🇩 Dibuat dengan Mengerti Kebiasaan Bisnis Indonesia

- **Terbilang otomatis** — total langsung dikonversi jadi kalimat *"Enam puluh satu juta enam ratus lima ribu Rupiah"*, sesuai standar dokumen resmi.
- **PPN 11%** sudah jadi default, tinggal ubah kalau perlu.
- **Status LUNAS / BELUM LUNAS** yang mencolok, format tanggal Indonesia, dan dukungan IDR/USD.

## 💾 Kerjaan Tidak Hilang, Klien Tidak Perlu Diketik Ulang

Draf tersimpan otomatis di browser — tutup laptop hari ini, lanjutkan besok. Klien langganan cukup disimpan sekali, kunjungan berikutnya tinggal pilih dari dropdown. Butuh backup permanen atau pindah perangkat? Ekspor semuanya sebagai file JSON dan impor kembali kapan saja.

## 🆓 Gratis. Bukan "Gratis 14 Hari"

Karena tidak ada server yang harus dibayar, tidak ada alasan untuk menagih Anda. Tidak ada watermark, tidak ada batas jumlah invoice, tidak ada fitur yang dikunci.

**Untuk siapa?** Freelancer yang menagih klien pertamanya, agensi kecil yang butuh invoice rapi tanpa langganan software, UMKM yang ingin terlihat profesional — atau siapa pun yang percaya bahwa membuat satu lembar tagihan seharusnya tidak lebih rumit daripada pekerjaannya sendiri.

---

## 🛠️ Panduan Penggunaan

### 1. Pengaturan Identitas & Logo

- **Unggah Logo:** Seret dan lepas (drag & drop) file gambar logo perusahaan Anda ke area dropzone di panel kiri. Mendukung format PNG, JPG, dan WebP (Maks. 2MB).
- **Data Penerbit (Seller):** Isi detail perusahaan Anda. Alamat mendukung beberapa baris (multi-line) untuk tampilan yang lebih rapi.

### 2. Manajemen Transaksi & Klien

- **Nomor Invoice:** Gunakan penomoran unik sesuai sistem perusahaan Anda.
- **Mata Uang:** Pilih antara IDR (Rupiah) atau USD (Dolar). Format ribuan akan menyesuaikan secara otomatis.
- **Data Klien:** Masukkan rincian penerima tagihan. Gunakan fitur "Simpan Baru" untuk memasukkan data klien ke dropdown lokal browser agar mudah digunakan kembali pada kunjungan berikutnya.

### 3. Daftar Item & Kalkulasi

- Masukkan deskripsi pekerjaan, jumlah (Qty), dan harga.
- **Diskon:** Berikan diskon per baris item (dalam persentase).
- **PPN:** Atur persentase pajak (default 11%). Seluruh kalkulasi subtotal dan total akhir diperbarui secara instan.

### 4. Penyimpanan & Pengunduhan

- **Simpan Draf:** Masuk ke tab Riwayat Draf dan klik "Simpan Draf Aktif". Ini akan mengabadikan data di browser Anda.
- **Unduh PDF:** Klik tombol biru besar di bawah. Tunggu hingga proses rendering selesai (biasanya 1-2 detik) dan file PDF resmi akan langsung terunduh ke komputer Anda.

## 🚢 Cara Deploy (Hosting)

Aplikasi ini hanyalah satu file `index.html`. Anda bisa menjalankannya secara lokal cukup dengan mengeklik file tersebut, atau meng-host secara profesional:

- **Vercel:** Hubungkan repository GitHub Anda atau tarik folder yang berisi `index.html` ke dashboard Vercel.
- **GitHub Pages:** Unggah file ke repository Anda, masuk ke Settings > Pages, lalu aktifkan hosting dari branch main.

## ✅ Catatan Perbaikan Stabilitas

Versi ini tetap mempertahankan filosofi tanpa login, tanpa backend, dan langsung pakai dari browser. Beberapa perbaikan teknis telah ditambahkan agar pengalaman client-side lebih aman dan konsisten:

- Ekspor PDF kini menggunakan **html2canvas-pro** sehingga posisi teks pada badge status pembayaran dan kapsul Total Akhir di PDF identik dengan preview (memperbaiki bug baseline teks html2canvas lama di Chrome modern).
- Tanggal invoice default kini mengikuti tanggal hari ini secara otomatis, dengan tenggat waktu default 14 hari setelah tanggal terbit.
- Daftar pelanggan tersimpan kini benar-benar disimpan di localStorage browser, bukan hanya di memori sesi, sehingga tetap tersedia setelah browser di-refresh.
- Penyimpanan draft dan pelanggan kini memiliki penanganan error. Jika localStorage browser penuh, aplikasi akan menampilkan notifikasi agar pengguna dapat menghapus draft lama atau mengecilkan logo.
- Impor JSON kini dinormalisasi sebelum dimuat ke aplikasi. Data item, pelanggan, seller, pajak, mata uang, status pembayaran, dan logo dipastikan berada dalam format yang aman untuk mencegah preview invoice error.
- Nilai qty, harga, diskon, dan PPN kini dibatasi di sisi logika aplikasi agar total invoice tidak menjadi negatif atau tidak masuk akal akibat data JSON yang rusak.
- Elemen Alpine.js yang memakai `x-cloak` kini benar-benar tersembunyi sebelum JavaScript siap, sehingga toast, overlay, dan tab tidak berkedip saat halaman pertama kali dibuka.
- Export JSON kini membersihkan object URL setelah file diunduh untuk menghindari kebocoran memori kecil pada sesi penggunaan panjang.

## 🛡️ Keamanan & Privasi

ScribeInvoice tidak menggunakan backend API. Semua data disimpan menggunakan API localStorage browser. Kami menyarankan untuk melakukan Ekspor JSON secara berkala jika Anda ingin menyimpan cadangan draf permanen di luar browser.

**Catatan penting:** karena aplikasi tidak memakai akun/login, data draft dan pelanggan bersifat lokal pada browser dan perangkat yang sama. Membersihkan site data/browser storage dapat menghapus data tersebut. Gunakan Ekspor JSON sebagai backup jika invoice perlu dipindahkan ke perangkat lain atau disimpan jangka panjang.

---

*Dibuat untuk profesional yang menghargai kecepatan dan privasi data.*
