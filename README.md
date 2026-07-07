ScribeInvoice — Premium Client-Side Invoice Generator

ScribeInvoice adalah generator invoice berbasis web kelas premium yang dirancang dengan filosofi "Zero-Server". Aplikasi ini menawarkan pengalaman pembuatan invoice yang instan, privat, dan estetis, terinspirasi oleh standar desain modern seperti Linear dan Vercel.

🚀 Mengapa ScribeInvoice?

Berbeda dengan aplikasi invoice SaaS pada umumnya, ScribeInvoice berjalan 100% di browser Anda.

Privasi Mutlak: Data keuangan Anda tidak pernah meninggalkan perangkat Anda. Tidak ada database awan, tidak ada risiko kebocoran data di server.

Performa Instan: Kalkulasi matematis dilakukan secara real-time tanpa delay loading server.

Bebas Biaya Pemeliharaan: Karena berbasis client-side (file statis), aplikasi ini bisa di-host gratis selamanya di platform seperti Vercel atau GitHub Pages.

✨ Fitur Utama

Split-Screen Editor: Edit data di panel kiri dan lihat perubahan langsung pada kertas A4 di panel kanan secara real-time.

Auto-Scaling Preview: Algoritma cerdas yang secara otomatis menyesuaikan ukuran (zoom) invoice agar pas di layar HP, tablet, maupun desktop.

Ultra-Crisp PDF Export: Menggunakan skala render 3x (300 DPI) untuk memastikan teks, garis, dan logo tetap tajam saat dicetak fisik.

Local History Storage: Fitur penyimpanan draf otomatis ke dalam localStorage browser. Anda bisa menutup browser dan melanjutkan draf nanti.

Ekspor/Impor JSON: Fitur cadangan fisik. Anda bisa mengunduh draf sebagai file .json ke komputer dan mengunggahnya kembali kapan saja.

Indonesian "Terbilang" Engine: Konversi otomatis angka total menjadi kalimat teks (Contoh: Dua juta Rupiah).

Customer Database: Simpan daftar pelanggan tetap di penyimpanan lokal browser untuk pengisian cepat di masa mendatang.

✅ Catatan Perbaikan Stabilitas

Versi ini tetap mempertahankan filosofi tanpa login, tanpa backend, dan langsung pakai dari browser. Beberapa perbaikan teknis telah ditambahkan agar pengalaman client-side lebih aman dan konsisten:

Tanggal invoice default kini mengikuti tanggal hari ini secara otomatis, dengan tenggat waktu default 14 hari setelah tanggal terbit.

Daftar pelanggan tersimpan kini benar-benar disimpan di localStorage browser, bukan hanya di memori sesi, sehingga tetap tersedia setelah browser di-refresh.

Penyimpanan draft dan pelanggan kini memiliki penanganan error. Jika localStorage browser penuh, aplikasi akan menampilkan notifikasi agar pengguna dapat menghapus draft lama atau mengecilkan logo.

Impor JSON kini dinormalisasi sebelum dimuat ke aplikasi. Data item, pelanggan, seller, pajak, mata uang, status pembayaran, dan logo dipastikan berada dalam format yang aman untuk mencegah preview invoice error.

Nilai qty, harga, diskon, dan PPN kini dibatasi di sisi logika aplikasi agar total invoice tidak menjadi negatif atau tidak masuk akal akibat data JSON yang rusak.

Elemen Alpine.js yang memakai x-cloak kini benar-benar tersembunyi sebelum JavaScript siap, sehingga toast, overlay, dan tab tidak berkedip saat halaman pertama kali dibuka.

Export JSON kini membersihkan object URL setelah file diunduh untuk menghindari kebocoran memori kecil pada sesi penggunaan panjang.

🛠️ Panduan Penggunaan

1. Pengaturan Identitas & Logo

Unggah Logo: Seret dan lepas (drag & drop) file gambar logo perusahaan Anda ke area dropzone di panel kiri. Mendukung format PNG, JPG, dan WebP (Maks. 2MB).

Data Penerbit (Seller): Isi detail perusahaan Anda. Alamat mendukung beberapa baris (multi-line) untuk tampilan yang lebih rapi.

2. Manajemen Transaksi & Klien

Nomor Invoice: Gunakan penomoran unik sesuai sistem perusahaan Anda.

Mata Uang: Pilih antara IDR (Rupiah) atau USD (Dolar). Format ribuan akan menyesuaikan secara otomatis.

Data Klien: Masukkan rincian penerima tagihan. Gunakan fitur "Simpan Baru" untuk memasukkan data klien ke dropdown lokal browser agar mudah digunakan kembali pada kunjungan berikutnya.

3. Daftar Item & Kalkulasi

Masukkan deskripsi pekerjaan, jumlah (Qty), dan harga.

Diskon: Berikan diskon per baris item (dalam persentase).

PPN: Atur persentase pajak (default 11%). Seluruh kalkulasi subtotal dan total akhir diperbarui secara instan.

4. Penyimpanan & Pengunduhan

Simpan Draf: Masuk ke tab Riwayat Draf dan klik "Simpan Draf Aktif". Ini akan mengabadikan data di browser Anda.

Unduh PDF: Klik tombol biru besar di bawah. Tunggu hingga proses rendering selesai (biasanya 1-2 detik) dan file PDF resmi akan langsung terunduh ke komputer Anda.

🚢 Cara Deploy (Hosting)

Aplikasi ini hanyalah satu file index.html. Anda bisa menjalankannya secara lokal cukup dengan mengeklik file tersebut, atau meng-host secara profesional:

Vercel: Hubungkan repository GitHub Anda atau tarik folder yang berisi index.html ke dashboard Vercel.

GitHub Pages: Unggah file ke repository Anda, masuk ke Settings > Pages, lalu aktifkan hosting dari branch main.

🛡️ Keamanan & Privasi

ScribeInvoice tidak menggunakan backend API. Semua data disimpan menggunakan API localStorage browser. Kami menyarankan untuk melakukan Ekspor JSON secara berkala jika Anda ingin menyimpan cadangan draf permanen di luar browser.

Catatan penting: karena aplikasi tidak memakai akun/login, data draft dan pelanggan bersifat lokal pada browser dan perangkat yang sama. Membersihkan site data/browser storage dapat menghapus data tersebut. Gunakan Ekspor JSON sebagai backup jika invoice perlu dipindahkan ke perangkat lain atau disimpan jangka panjang.

Dibuat untuk profesional yang menghargai kecepatan dan privasi data.
