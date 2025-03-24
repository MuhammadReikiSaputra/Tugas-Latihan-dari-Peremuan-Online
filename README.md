# Tugas Latihan OAK dari Peremuan Online
## MUHAMMAD REIKI SAPUTRA
## NIM : 09011382429139
## SKU2A

# 1. Jelaskan struktur antar hubungan dan beri contohnya.
Jawaban :

Dalam sistem komputer, struktur antar hubungan (interconnection structure) mengacu pada cara berbagai komponen perangkat keras berkomunikasi dan saling terhubung untuk membentuk sebuah sistem yang terpadu. Komponen utama sistem komputer meliputi CPU (Central Processing Unit), memori, perangkat input/output (I/O), dan bus. Hubungan antar komponen ini sangat penting untuk memastikan bahwa data dapat ditransfer dengan efisien dan sistem dapat berfungsi dengan baik.

Berikut adalah tiga komponen penting dalam struktur antar hubungan pada sistem komputer, beserta penjelasan dan contohnya:

### 1. **Bus**
   **Bus** adalah saluran komunikasi yang memungkinkan data berpindah antara berbagai komponen sistem komputer, seperti CPU, memori, dan perangkat I/O. Berikut penjelasan mendalam tentang masing-masing jenis bus:
   - **Data Bus**: Mengangkut data yang sedang diproses. Lebar data bus (misalnya 32-bit atau 64-bit) memengaruhi jumlah data yang dapat dikirim dalam satu waktu. *Contoh*: Dalam arsitektur komputer modern seperti Intel Core i7, data bus berukuran 64-bit memungkinkan pengangkutan data besar untuk aplikasi intensif seperti rendering grafis.
   - **Address Bus**: Mengangkut alamat lokasi memori untuk mengidentifikasi di mana data atau instruksi harus disimpan/dicari. *Contoh*: Saat CPU membaca data dari RAM, address bus menentukan blok memori spesifik yang berisi data itu.
   - **Control Bus**: Mengangkut sinyal kontrol untuk mengatur operasi perangkat keras, seperti membaca/menulis data, atau sinkronisasi. *Contoh*: Control bus mengirimkan sinyal ke memori untuk memberi tahu apakah CPU ingin membaca atau menulis data.

### 2. **Hierarki Memori**
   Hierarki memori mencakup berbagai level memori dengan karakteristik kecepatan dan kapasitas yang berbeda:
   - **Register**: Memori tercepat yang ada di CPU, digunakan untuk menyimpan data sementara selama eksekusi instruksi. *Contoh*: Register menyimpan hasil sementara saat CPU melakukan perhitungan matematika.
   - **Cache**: Memori kecil yang sangat cepat yang menyimpan data yang sering diakses. Cache dapat berupa level 1 (L1), level 2 (L2), atau level 3 (L3). *Contoh*: Dalam prosesor AMD Ryzen, L1 cache memiliki kecepatan tinggi untuk akses langsung oleh CPU.
   - **RAM (Random Access Memory)**: Memori utama yang digunakan oleh sistem saat menjalankan aplikasi. *Contoh*: Sebuah komputer gaming mungkin memiliki RAM 16 GB untuk mendukung aplikasi berat seperti game 3D.
   - **Penyimpanan Sekunder**: Seperti SSD atau hard drive, digunakan untuk penyimpanan jangka panjang. *Contoh*: SSD NVMe dengan kecepatan tinggi memungkinkan booting sistem dalam hitungan detik.

### 3. **Interkoneksi Perangkat I/O**
   Perangkat I/O (Input/Output) adalah antarmuka yang memungkinkan interaksi pengguna dengan sistem komputer. Hubungannya mencakup mekanisme berikut:
   - **Port dan Pengontrol I/O**: Port seperti USB atau HDMI memungkinkan perangkat terhubung. Pengontrol I/O bertugas mentransfer data dari format perangkat ke format yang dapat dibaca sistem. *Contoh*: USB pengontrol bertugas menerjemahkan data dari keyboard ke sinyal yang dapat dimengerti oleh CPU.
   - **Interkoneksi Jaringan**: Komputer dapat terhubung dengan perangkat lain melalui koneksi nirkabel (Wi-Fi atau Bluetooth). *Contoh*: Printer nirkabel terhubung dengan laptop melalui Bluetooth untuk mencetak dokumen.

### Pentingnya Struktur Antar Hubungan
Desain struktur antar hubungan ini bertujuan untuk mengoptimalkan kinerja sistem. Sebagai contoh, **sistem multiprosesor** sering kali menggunakan bus bersama untuk memungkinkan komunikasi antar prosesor. Selain itu, penggunaan **DMA (Direct Memory Access)** memungkinkan perangkat I/O mengakses memori tanpa harus melewati CPU, yang mengurangi beban kerja CPU.


# 2. Bila terlalu banyak modul atau perangkat dihubungkan pada bus maka akan terjadi penurunan kinerja, sebutkan penyebabnya? 

Jawaban :

Ketika terlalu banyak modul atau perangkat dihubungkan pada bus, penurunan kinerja bisa terjadi karena beberapa alasan berikut:

1. **Kepadatan Lalu Lintas Data (Traffic Congestion)**:
   - Semakin banyak perangkat yang terhubung, semakin besar jumlah data yang mengalir melalui bus. Hal ini menyebabkan antrian data, di mana perangkat harus menunggu giliran untuk mengakses bus.
   - *Contoh*: Jika ada beberapa perangkat I/O seperti hard drive, printer, dan scanner yang secara bersamaan mengakses bus, waktu tunggu untuk akses meningkat, yang mengakibatkan latensi lebih tinggi.

2. **Konflik Penggunaan Bus (Bus Contention)**:
   - Ketika banyak perangkat mencoba mengakses bus pada saat yang sama, terjadi konflik akses. Sistem harus menggunakan mekanisme arbitrasi (bus arbitration) untuk menentukan perangkat mana yang diberikan akses terlebih dahulu, sehingga memperlambat proses keseluruhan.
   - *Contoh*: Dalam sistem dengan beberapa prosesor yang berbagi bus, salah satu prosesor harus menunggu sementara yang lain menyelesaikan transfer data.

3. **Penurunan Kecepatan Transfer**:
   - Dengan banyak perangkat yang berbagi bus, bandwidth total bus harus dibagi di antara mereka. Semakin banyak perangkat, semakin sedikit bandwidth yang tersedia untuk masing-masing perangkat.
   - *Contoh*: Hard drive dengan kecepatan tinggi mungkin tidak dapat mencapai kinerja optimal karena harus berbagi bandwidth dengan perangkat lain.

4. **Penambahan Kapasitansi dan Resistansi Listrik**:
   - Setiap perangkat yang ditambahkan ke bus meningkatkan beban kapasitansi dan resistansi listrik, yang dapat memperlambat sinyal dan mengurangi efisiensi komunikasi.
   - *Contoh*: Pada bus paralel dengan banyak perangkat, sinyal digital dapat terdistorsi atau tertunda karena peningkatan kapasitansi kabel.

5. **Kinerja Mekanisme Sinkronisasi**:
   - Pada sistem sinkron, clock harus mengoordinasikan semua perangkat. Penambahan perangkat membuat sinkronisasi lebih rumit dan meningkatkan peluang terjadinya penundaan.
   - *Contoh*: Dalam bus dengan kecepatan tinggi, jika perangkat yang lebih lambat terhubung, clock cycle keseluruhan mungkin harus disesuaikan agar semua perangkat dapat berfungsi.

6. **Masalah Skalabilitas**:
   - Desain bus tradisional mungkin tidak dirancang untuk mendukung banyak perangkat. Keterbatasan arsitektur membuat sistem menjadi kurang efisien saat skala perangkat bertambah.
   - *Contoh*: Bus PCI konvensional memiliki batasan jumlah perangkat yang dapat dihubungkan sebelum kinerjanya mulai menurun.

Untuk mengatasi masalah ini, arsitektur modern sering kali menggunakan teknik seperti **bus segmentasi**, **switching fabric**, atau mengganti bus dengan **interkoneksi point-to-point** seperti yang digunakan dalam PCI Express (PCIe).


# 3. Umumnya perangkat berprioritas paling rendah memiliki waktu tunggu rata-rata yang paling singkat. Dengan dasar ini biasanya CPU diberi perioritas tertinggi pada SBI. Sebutkan alasan perangkat berprioritas 16 memiliki waktu tunggu rata-rata paling rendah? Dibawah kondisi seperti apa keadaan diatas tidak berlaku?

Jawaban :

### **1. Alasan Perangkat Prioritas 16 Memiliki Waktu Tunggu Rata-rata yang Pendek**:
   - **Frekuensi Permintaan Akses Lebih Rendah**: Perangkat dengan prioritas rendah sering kali tidak membutuhkan akses ke bus secara intensif atau sering. Ini memungkinkan mereka untuk mengantre dengan lebih efisien saat mereka membutuhkan akses.
   - **Penghindaran Konflik Akses**: Karena perangkat prioritas tinggi lebih sering mengakses bus, perangkat prioritas rendah biasanya hanya "masuk antrean" ketika bus tidak sibuk, sehingga waktu tunggu rata-rata menjadi lebih singkat.
   - **Interaksi Minimal**: Perangkat dengan prioritas rendah mungkin memiliki sifat pekerjaan I/O yang bersifat batch atau interval besar, sehingga tidak mempengaruhi antrian bus terlalu signifikan.

   *Contoh*: Sebuah printer (prioritas rendah) hanya mengakses bus ketika ada data cetak, sedangkan CPU (prioritas tinggi) mengakses bus hampir setiap siklus clock.

---

### **2. Kondisi Di Mana Keadaan Ini Tidak Berlaku**:
Ada situasi tertentu di mana perangkat dengan prioritas rendah justru memiliki waktu tunggu rata-rata lebih panjang. Kondisi-kondisi ini meliputi:

   - **Beban Kerja Tinggi pada Perangkat Prioritas Tinggi**:
     Ketika perangkat prioritas tinggi seperti CPU atau memori intensif terus-menerus menggunakan bus, perangkat prioritas rendah mungkin mengalami kelambatan signifikan.
     - *Contoh*: Jika CPU terus menerus melakukan proses berat, seperti menjalankan aplikasi intensif, perangkat prioritas rendah seperti printer atau hard drive dapat tertunda aksesnya.

   - **Implementasi Arbiter yang Tidak Efisien**:
     Sistem dengan mekanisme arbitrasi bus yang tidak optimal dapat memberikan prioritas terlalu tinggi pada perangkat prioritas atas, sehingga perangkat prioritas rendah menunggu terlalu lama.
     - *Contoh*: Pada sistem round-robin arbiter yang tidak menyeimbangkan antrian, perangkat prioritas rendah dapat sering kali terlewat.

   - **Gangguan atau Interupsi Berulang**:
     Jika perangkat dengan prioritas tinggi terus menginterupsi atau menggunakan bus secara sporadis, perangkat prioritas rendah bisa menghadapi penundaan dalam mendapatkan akses.
     - *Contoh*: Dalam sistem real-time yang memiliki banyak interupsi kritis dari perangkat prioritas tinggi.

   - **Ketergantungan Antar Perangkat**:
     Jika perangkat prioritas rendah bergantung pada hasil dari perangkat prioritas tinggi, waktu tunggunya akan bertambah, terlepas dari prioritasnya.
     - *Contoh*: Perangkat penyimpanan yang menunggu data dari CPU untuk diproses sebelum dapat melanjutkan operasi.

Dengan demikian, desain arsitektur dan pengelolaan bus menjadi sangat penting untuk memastikan efisiensi, terlepas dari prioritas perangkat.



