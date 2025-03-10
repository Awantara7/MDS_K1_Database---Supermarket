# WA-ONE SWALAYAN Dashboard

**WA-ONE SWALAYAN Dashboard** adalah aplikasi dashboard interaktif berbasis **Shiny** yang dirancang untuk memantau berbagai aspek operasional di supermarket, seperti penjualan, produk, segmentasi pelanggan, serta performa cabang. Aplikasi ini dibangun dengan menggunakan **R**, **Shiny**, dan **bs4Dash** sehingga memiliki tampilan modern dan responsif.  

---

## Fitur-Fitur Utama

Aplikasi ini menyediakan beberapa tab dengan fitur-fitur berikut:

### 1. Dashboard Penjualan
- **KPI Utama:**  
  - **Total Penjualan:** Menampilkan total penjualan dengan format rupiah.
  - **Cabang Terbaik:** Menunjukkan ID cabang yang mencatat omzet tertinggi.
  - **Produk Terjual:** Menghitung jumlah total produk yang terjual.
  - **Total Transaksi:** Menampilkan jumlah transaksi penjualan.
- **Grafik Penjualan:**  
  - Grafik *line chart* interaktif yang menampilkan total penjualan per waktu dan per kategori.
  - Grafik *bar chart* berdasar produk terlaris.
- **Frekuensi Belanja:**  
  - Grafik kolom yang memperlihatkan frekuensi berbelanja pelanggan (jumlah transaksi per pelanggan).
- **Peta Penjualan:**  
  - Peta interaktif yang menunjukkan lokasi kota dengan total penjualan, dilengkapi dengan informasi pop-up.
- **Tabel Data Transaksi:**  
  - Tabel interaktif menggunakan **DT** yang menampilkan data transaksi lengkap.

### 2. Produk & Kategori
- **Distribusi Kategori:**  
  - Grafik pie yang menampilkan proporsi penjualan berdasarkan kategori produk.
- **Perbandingan Produk:**  
  - Grafik bar horizontal yang membandingkan jumlah penjualan antar produk.
- **Tren Penjualan Produk:**  
  - Grafik *spline* (highchart) untuk memantau tren penjualan produk selama periode waktu tertentu.

### 3. Segmentasi Pelanggan
Mengelompokkan pelanggan berdasarkan berbagai aspek:
- **Demografi Pelanggan:**  
  - Grafik pie yang memvisualisasikan distribusi pelanggan berdasarkan jenis kelamin.
- **RFM Analysis:**  
  - Grafik scatter untuk analisis RFM (Recency, Frequency, Monetary) guna mengidentifikasi segmen pelanggan penting.
- **Segmentasi Berdasarkan Jenis Pelanggan:**  
  - Grafik bar untuk mengelompokkan dan menampilkan jumlah pelanggan berdasarkan kategori _Jenis_Pelanggan_.
- **Segmentasi Berdasarkan Tipe Pelanggan:**  
  - Grafik bar yang menampilkan jumlah pelanggan sesuai dengan _Tipe_Pelanggan_.
- **Segmentasi Berdasarkan Jenis Pembayaran:**  
  - Grafik pie yang memvisualisasikan jumlah transaksi berdasarkan metode pembayaran (_Pembayaran_).

### 4. Performa Cabang
- **Omzet per Cabang:**  
  - Grafik bar (dengan koordinat terbalik untuk tampilan horizontal) yang menampilkan omzet setiap cabang.
- **Analisa Cabang Terbaik & Terburuk:**  
  - Grafik bar yang menampilkan perbandingan omzet antara cabang dengan performa tertinggi dan terendah.
- **Peta Cabang:**  
  - Peta interaktif menggunakan **Leaflet** yang menampilkan lokasi cabang beserta informasi (ID dan kota).

### 5. Data Quality
- **Tabel Data Lengkap:**  
  - Menampilkan seluruh data transaksi yang telah direkonsiliasi.
- **Tabel Data Inconsistency:**  
  - Menampilkan data yang memiliki inkonsistensi, misalnya perbedaan perhitungan antara `computed_total` dan `Total_Harga`.

### 6. Pengaturan
- **Update Password:**  
  - Fitur untuk mengubah password pengguna.
- **Preferensi Aplikasi:**  
  - Pilihan pengaturan seperti mode gelap dan notifikasi via email.

### 7. About Dashboard
- **Deskripsi Dashboard:**  
  - Informasi singkat mengenai tujuan dan penggunaan dashboard ini.
- **Kontributor:**  
  - Daftar tim pengembang beserta foto, nama, NIM, dan link ke akun Instagram serta GitHub masing-masing.  
  - Gambar kontributor diambil langsung dari GitHub menggunakan URL raw sehingga selalu terupdate.
  
---

## Filter Data
Aplikasi menyediakan **controlbar** di sisi kanan untuk memfilter data berdasarkan:
- **Tahun:** Pilih tahun yang diinginkan untuk memfilter data transaksi.
- **Produk (Kategori):** Pilih kategori produk spesifik untuk memfilter data transaksi.

Filter ini akan diterapkan secara otomatis ke seluruh visualisasi dan tabel yang ada di dashboard.

---

## Instalasi dan Cara Menjalankan

1. **Clone repositori ini:**

   ```bash
   git clone https://github.com/Awantara7/MDS_K1_Database---Supermarket.git
2. **Set Working Directory: Buka RStudio dan atur working directory ke folder proyek yang sudah di-clone.**
3. **Install Paket Terkait: Pastikan Anda telah menginstal paket-paket berikut:**
    ```bash
    install.packages(c("shiny", "bs4Dash", "shinymanager", "shinyWidgets", "highcharter", "echarts4r", "DT", "leaflet", "dplyr", "DBI", "RMariaDB", "glue", "shinyjs"))
4. **Jalankan Aplikasi: Aplikasi terintegrasi dalam file app.R. Jalankan aplikasi dengan:**
      ```bash
   shiny::runApp("app.R")
5. **Otentikasi: Setelah aplikasi berjalan, login menggunakan kredensial (contoh: admin dengan password admin123).**

## Kontributor
**Front-End Developer**

<img src="https://raw.githubusercontent.com/Awantara7/MDS_K1_Database---Supermarket/64bd08985f540880822d3d34cab26c3af01d36be/images/front_end.jpg" width="150" height="150" alt="Foto Tim" style="border-radius: 50%;">

- Nama: Muh. Akbar Idris

- Instagram: @muhakbaridris

- GitHub: muhakbaridris

**Back-End Developer**

<img src="images/back_end2.jpg" width="150" height="150" alt="Foto Tim" style="border-radius: 50%;">

- Nama: I Gede Awantara

- Instagram: @igedeawantara

- GitHub: awantara7

**DB-Manager**

<img src="images/db_manager.jpg" width="150" height="150" alt="Foto Tim" style="border-radius: 50%;">

- Nama: Wawan Saputra

- Instagram: @w2nspt_

- GitHub: wawan2105

**Designer-DB**

<img src="https://raw.githubusercontent.com/Awantara7/MDS_K1_Database---Supermarket/64bd08985f540880822d3d34cab26c3af01d36be/images/designer_db.jpg" width="150" height="150" alt="Foto Tim" style="border-radius: 50%;">

- Nama: Lisa Amelia

- Instagram: @amllsaa

- GitHub: lisaamelia

**Technical-Writer**

<img src="https://raw.githubusercontent.com/Awantara7/MDS_K1_Database---Supermarket/64bd08985f540880822d3d34cab26c3af01d36be/images/technical_writer.jpg" width="150" height="150" alt="Foto Tim" style="border-radius: 50%;">

- Nama: Nabila Fida Milliati

- Instagram: @nabilafida

- GitHub: nabilafida

## Struktur Proyek

      MDS_K1_Database---Supermarket/
      ├── app.R
      ├── README.md
      ├── LICENSE
      └── (file dan folder pendukung lainnya)

## License
**Proyek ini dilisensikan berdasarkan MIT License.**

