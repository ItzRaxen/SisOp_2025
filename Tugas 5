# Laporan Pengujian FLOPS-IOPS dan Sejarah Sistem Operasi

**Nama:** Firas Rasendriya Athaillah  
**NRP:** 3124500042  
**Kelas:** D3 IT B


## A. Pengujian FLOPS dan IOPS

### 1. Menyalin Repository flops-iops melalui Terminal Linux
Untuk memulai, buka terminal dan salin repositori dengan perintah berikut:
```bash
git clone https://github.com/ferryastika/flops-iops.git
```
Jika perintah tersebut gagal, jalankan:
```bash
su -
apt install git
sudo apt update && sudo apt install -y build-essential
exit
```

### 2. Masuk ke Direktori flops-iops
```bash
cd flops-iops
```

### 3. Kompilasi Program Benchmark
```bash
make
```

### 4. Menjalankan Uji FLOPS dan IOPS

#### a. Menjalankan IOPS 32-bit
```bash
./iops32 $(nproc)
```
**Output:**
```
Benchmarking for 32 Bit Integer operations per second
1 Tr 1: 7466128771 Tr 2: 7466481121 IOPS 14932609892
Maximum CPU Throughput: 14.932611 Gigaiops.
Maximum Single Core Throughput: 7.466481 Gigaiops.
```

#### b. Menjalankan IOPS 64-bit
```bash
./iops64 $(nproc)
```
**Output:**
```
Benchmarking for 64 Bit Integer operations per second
1 Tr 1: 7239078522 Tr 2: 7310366180 IOPS = 14549444702
Maximum CPU Throughput: 14.549444 Gigaiops.
Maximum Single Core Throughput: 7.310366 Gigaiops.
```

#### c. Menjalankan FLOPS 32-bit
```bash
./flops32 $(nproc)
```
**Output:**
```
Benchmarking for 32 Bit Floating point operations per second
1 Tr 1: 4695619711 Tr 2: 4694721658 FLOPS = 9390341369
Maximum CPU Throughput: 9.390341 Gigaflops.
Maximum Single Core Throughput: 4.695620 Gigaflops.
Segmentation fault
```

#### d. Menjalankan FLOPS 64-bit
```bash
./flops64 $(nproc)
```
**Output:**
```
Benchmarking for 64 Bit Floating point operations per second
1 Tr 1: 6248587358 Tr 2: 6229297776 FLOPS = 12477885134
Maximum CPU Throughput: 12.477885 Gigaflops.
Maximum Single Core Throughput: 6.248587 Gigaflops.
```

---

## B. Ringkasan Lampiran dan Penambahan Garis Waktu OS

### 1. Transformasi Fitur
Beberapa fitur dari sistem besar (mainframe) diadaptasi ke komputer kecil (mikrokomputer). Contohnya, sistem MULTICS memperkenalkan sistem file hierarkis dan mekanisme proteksi berbasis ring yang menginspirasi UNIX.

### 2. Perkembangan Awal Sistem Operasi
- **Sistem Tunggal**: Programmer merangkap sebagai operator.
- **Sistem Terpusat**: Operator mengelola dan mengelompokkan tugas untuk efisiensi.
- **I/O Paralel**: Menggunakan tape magnetik untuk mengoptimalkan kinerja CPU saat menangani perangkat input/output.

### 3. Atlas (1950-an)
Atlas dari Universitas Manchester merupakan pelopor dalam penggunaan **paging** untuk manajemen memori dan **spooling** untuk pengelolaan perangkat secara efisien.

### 4. XDS-940 (1960-an)
XDS-940 mendukung **time-sharing** dan **paging untuk relokasi memori**, tetapi belum mengadopsi **demand paging**.

### 5. THE (1960-an)
Sistem **THE** dari Technische Hogeschool Eindhoven memperkenalkan **struktur berlapis**, **semaphore**, dan **algoritma banker**.

### 6. RC 4000 (1960-an)
RC 4000 memperkenalkan **konsep kernel** dan komunikasi antar proses melalui **sistem pesan**.

### 7. CTSS (1961)
**CTSS** memungkinkan penggunaan komputer oleh banyak pengguna secara bersamaan dan memperkenalkan **swapping** serta **multilevel feedback queue**.

### 8. MULTICS (1965-1970)
MULTICS menghadirkan:
- **Struktur direktori bertingkat**
- **Proteksi akses berbasis ring**

### 9. IBM OS/360 (1960-an)
OS/360 mendukung banyak konfigurasi perangkat keras dan menekankan pentingnya **desain modular**.

### 10. TOPS-20 (1970-an)
TOPS-20 memperkenalkan **memori virtual** dan **komputasi jaringan** melalui fitur **time-sharing**.

### 11. CP/M dan MS-DOS (1980-an)
- **CP/M**: OS awal mikrokomputer.
- **MS-DOS**: OS utama IBM PC dengan fitur lebih lengkap.

### 12. Mac OS & Windows (1980-an)
- **Mac OS**: GUI pertama yang revolusioner.
- **Windows**: Membawa GUI ke platform IBM PC.

### 13. Mach (1980-an)
**Mach** adalah **microkernel** yang mendukung **multiprosesor** dan komunikasi antar proses.

### 14. Sistem Berbasis Kemampuan
- **Hydra** dan **CAP** memperkenalkan sistem proteksi berbasis kemampuan.

### 15. Sistem Operasi Lain yang Berpengaruh
- **MCP** dan **SCOPE**: Mendukung multiprosesor dan koordinasi proses.

---

## C. Garis Waktu Perkembangan Sistem Operasi

### 1940â€“1950-an: Awal Komputer
- *Manchester Mark 1 (1949)*: Komputer dengan konsep stored-program.
- *GM-NAA I/O (1956)*: Sistem batch pertama.

### 1960-an: Multiprogramming dan Time-Sharing
- *CTSS (1961)*: Sistem time-sharing pertama.
- *MULTICS (1965)*: Sistem file hierarkis, proteksi ring.
- *UNIX (1969)*: Dasar OS modern.

### 1970-an: Komputer Mini dan Mikro
- *CP/M (1974)*: OS mikrokomputer.
- *IBM OS/360*: OS mainframe serbaguna.

### 1980-an: GUI dan Komputasi Personal
- *MS-DOS (1981)*: OS dominan IBM PC.
- *Mac OS (1984)*: GUI inovatif.
- *Windows 1.0 (1985)*: GUI berbasis MS-DOS.

### 1990-an: OS Modern dan Open Source
- *Windows 95 (1995)*: GUI maju, plug and play.
- *Linux (1991)*: OS open-source berbasis UNIX.

### 2000-an â€“ Kini: Mobile dan Cloud
- *Windows XP (2001)*: OS Windows populer dan stabil.
- *macOS X (2001)*: Stabil dan berbasis UNIX.
- *Android (2008)* dan *iOS (2007)*: OS mobile terkemuka.
- *Windows 10 (2015)*: Dukungan cloud.
- *Windows 11 (2021)*: Tampilan modern, optimalisasi perangkat terbaru.
