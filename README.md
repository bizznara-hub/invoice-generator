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

Customer Database: Simpan daftar pelanggan tetap di memori lokal browser untuk pengisian cepat di masa mendatang.

🛠️ Panduan Penggunaan

1. Pengaturan Identitas & Logo

Unggah Logo: Seret dan lepas (drag & drop) file gambar logo perusahaan Anda ke area dropzone di panel kiri. Mendukung format PNG, JPG, dan WebP (Maks. 2MB).

Data Penerbit (Seller): Isi detail perusahaan Anda. Alamat mendukung beberapa baris (multi-line) untuk tampilan yang lebih rapi.

2. Manajemen Transaksi & Klien

Nomor Invoice: Gunakan penomoran unik sesuai sistem perusahaan Anda.

Mata Uang: Pilih antara IDR (Rupiah) atau USD (Dolar). Format ribuan akan menyesuaikan secara otomatis.

Data Klien: Masukkan rincian penerima tagihan. Gunakan fitur "Simpan Baru" untuk memasukkan data klien ke dropdown agar mudah digunakan kembali.

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

Dibuat untuk profesional yang menghargai kecepatan dan privasi data.
