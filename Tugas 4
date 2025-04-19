# Laporan Sistem Operasi

## 1. Perbedaan antara Multi Programming dan Multi Tasking

### A. Multi Programming

Multi programming adalah metode yang memungkinkan beberapa program dimuat dalam memori utama secara bersamaan, namun hanya satu program yang dijalankan oleh CPU pada satu waktu. Ketika sebuah program harus menunggu operasi I/O (seperti membaca data dari disk), CPU akan segera berpindah menjalankan program lain yang siap dieksekusi. Tujuan utamanya adalah untuk memaksimalkan pemanfaatan CPU dengan meminimalkan waktu menganggur.

**Contoh**: Dalam sistem batch, sistem operasi mengisi memori dengan sejumlah tugas dan menjalankannya secara bergantian.

### B. Multi Tasking

Multi tasking merupakan teknik di mana beberapa proses atau tugas dapat dijalankan secara bersamaan dengan cara membagi waktu CPU menggunakan sistem time-sharing. CPU akan berpindah dengan sangat cepat dari satu proses ke proses lainnya dalam jeda waktu pendek (time slice), sehingga seolah-olah semua proses berjalan secara paralel. Tujuan dari multitasking adalah menciptakan pengalaman penggunaan yang responsif dengan memungkinkan banyak aplikasi berjalan bersamaan.

**Contoh**: Di sistem operasi seperti Windows atau Linux, pengguna bisa menjalankan browser, aplikasi musik, dan perangkat lunak lainnya secara simultan.

### C. Perbandingan Utama

| Aspek      | Multi Programming                          | Multi Tasking                              |
|------------|--------------------------------------------|--------------------------------------------|
| Pendekatan | Menjalankan beberapa program secara bergiliran dalam memori | Menangani banyak tugas dengan cepat dalam waktu yang terbagi |
| Tujuan     | Mengoptimalkan penggunaan CPU               | Meningkatkan interaktivitas bagi pengguna |
| Metode     | Bergantung pada proses I/O                  | Menggunakan teknik time-sharing            |
| Contoh OS  | Sistem batch, sistem operasi lama           | Windows, Linux, macOS                      |

Multi programming lebih menitikberatkan pada efisiensi penggunaan CPU, sedangkan multi tasking lebih fokus pada pengalaman pengguna yang interaktif.

---

## 2. Fungsi Sistem Operasi

Sistem operasi memiliki peran penting dalam mengatur dan mengelola sumber daya komputer agar sistem dapat bekerja secara optimal. Salah satu fungsi utamanya adalah:

- **Manajemen Proses**  
  Mengelola pelaksanaan program-program yang aktif, menjadwalkan proses dengan algoritma seperti FCFS, Round Robin, dan Priority Scheduling, serta menangani multitasking, multithreading, dan multiprocessing.

- **Manajemen Memori**  
  Mengalokasikan dan membebaskan ruang memori untuk program yang berjalan, menggunakan teknik seperti paging dan segmentation, serta mendukung memori virtual.

- **Manajemen Perangkat I/O**  
  Mengendalikan perangkat seperti keyboard, printer, dan mouse dengan bantuan driver, buffer, dan caching.

- **Manajemen Sistem File**  
  Mengatur struktur direktori, hak akses file (read, write, execute), serta mendukung sistem file seperti FAT32, NTFS, dan ext4.

- **Keamanan dan Proteksi**  
  Menyediakan autentikasi (password, biometrik), mengatur hak akses, dan melindungi dari ancaman eksternal dengan firewall dan enkripsi.

- **Manajemen Jaringan**  
  Mengatur komunikasi antar perangkat menggunakan protokol TCP/IP, HTTP, dan UDP, serta mendukung file sharing dan remote access.

- **Antarmuka Pengguna**  
  Menyediakan GUI (seperti di Windows, macOS) atau CLI (seperti Command Prompt, Linux Terminal).

**Kesimpulan**: Sistem operasi adalah pusat kendali utama yang memungkinkan koordinasi dan efisiensi antara perangkat keras dan perangkat lunak komputer.

---

## 3. Virtualisasi Container

### Pengertian

Virtualisasi container adalah teknologi yang memungkinkan aplikasi berjalan dalam lingkungan terisolasi (container). Container berbagi kernel dari OS host, namun memiliki sistem berkas dan pustaka sendiri. Hal ini memungkinkan aplikasi berjalan secara konsisten di berbagai lingkungan tanpa perlu sistem operasi tersendiri seperti pada VM.

Container memanfaatkan fitur OS seperti `cgroups` dan `namespaces` untuk isolasi dan manajemen sumber daya.

### Jenis-Jenis Container

1. **Container Sistem**
   - Menyediakan lingkungan hampir seperti OS lengkap.
   - Contoh: `LXC`, `OpenVZ`.

2. **Container Aplikasi**
   - Menjalankan satu aplikasi beserta dependensinya dalam satu container.
   - Contoh: `Docker`, `Podman`.

3. **Container Orkestrasi**
   - Mengelola banyak container dalam skala besar.
   - Contoh: `Kubernetes`, `Docker Swarm`.

### Perbandingan Container dan Virtual Machine

| Aspek              | Container                                | Virtual Machine                          |
|--------------------|-------------------------------------------|-------------------------------------------|
| Sistem Operasi     | Berbagi kernel host                       | OS terpisah untuk tiap VM                 |
| Konsumsi Sumber Daya| Lebih ringan                              | Lebih berat karena memuat OS penuh        |
| Kecepatan Eksekusi | Sangat cepat                              | Butuh waktu untuk booting                 |
| Isolasi            | Terbatas                                  | Lebih
