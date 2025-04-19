# Tugas 8 Sistem Operasi

**Nama:** Firas Rasendriya Athaillah  
**NRP:** 3124500042  
**Kelas:** D3 IT B
**Dosen Pengampu:** Dr. Ferry Astika Saputra, S.T., M.Sc  

**PROGRAM STUDI D3 TEKNIK INFORMATIKA**  
**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA (PENS)**  
**TAHUN 2024**

---

## 1. Jelaskan dalam 2 paragraf disertai dengan gambar tentang konsep single thread dan multithread!

**Single Thread** merupakan model eksekusi di mana sebuah program hanya menjalankan satu alur instruksi dalam satu waktu. Ini berarti CPU menangani satu tugas secara berurutan, meskipun ada banyak proses yang harus diproses. Model ini lebih sederhana dan mudah dipahami, serta minim risiko kondisi balapan (*race conditions*). Namun, pendekatan ini kurang optimal pada prosesor multi-core dan kurang efisien untuk menangani banyak proses atau aplikasi interaktif.

Sementara itu, **Multithread** memungkinkan satu proses untuk memiliki beberapa thread yang bisa berjalan bersamaan. Setiap thread dapat menangani bagian berbeda dari tugas secara paralel, sehingga meningkatkan kinerja, terutama di sistem dengan banyak inti prosesor. Pendekatan ini umum digunakan dalam aplikasi modern seperti browser, game, dan server, karena mampu memberikan respons yang lebih cepat. Meski begitu, manajemen multithreading cukup kompleks dan rentan terhadap masalah seperti *deadlock* atau *race conditions* jika tidak dikelola dengan baik.

![Single vs Multithread](https://github.com/user-attachments/assets/d48ea74f-5372-461d-81aa-68857d7a6bbb)

---

## 2. Programming Exercise

### a. Contoh Penggunaan Thread di Linux dengan `SumTask.java`

![Screenshot 2025-04-19 191251](https://github.com/user-attachments/assets/508885be-c867-483e-bc49-ceb064a164ad)


**Langkah-langkah:**

```bash
java -version
sudo apt-get update
sudo apt-cache search openjdk
sudo apt-get install openjdk-17-jdk
java -version
nano SumTask.java
```

Salin kode dari: [SumTask.java](https://github.com/ferryastika/osc10e/blob/master/ch4/SumTask.java)

```bash
javac SumTask.java
java SumTask
```

### b. Implementasi Thread di Linux dengan `thrd-posix.c`

![Screenshot 2025-04-19 191912](https://github.com/user-attachments/assets/fe7c5230-7552-419f-93f5-054513070a3b)

**Langkah-langkah:**

```bash
gcc --version
nano thrd-posix.c
```

Salin kode dari: [thrd-posix.c](https://github.com/ferryastika/osc10e/blob/master/ch4/thrd-posix.c)

```bash
gcc -pthread thrd-posix.c -o thrd-posix
./thrd-posix 10
```
## Penjelasan Esai

### a. Java Multithreading (`SumTask.java`)

Dalam tugas ini, kita mengimplementasikan multithreading menggunakan Java melalui program `SumTask.java`. Java mendukung multithreading dengan menyediakan kelas Thread dan interface Runnable. Program ini bertugas menghitung total dari sebuah array, lalu membagi tugas ke dua thread yang masing-masing menghitung setengah dari array.

Dengan pendekatan paralel ini, proses penjumlahan menjadi lebih cepat dibanding dilakukan secara berurutan. Ini mencerminkan konsep kerja paralel dan efisiensi melalui pembagian tugas. Program dikompilasi dan dijalankan di terminal Linux, memperlihatkan kemampuan Java dalam memanfaatkan fitur multitasking yang ditawarkan oleh sistem operasi.

### b. Thread di Linux (`thrd-posix.c`)

Pada bagian ini, kita mengeksplorasi bagaimana thread dikelola menggunakan bahasa C di sistem operasi Linux. Kita menggunakan pustaka pthread, standar untuk pengelolaan thread pada sistem berbasis UNIX.

Program `thrd-posix.c` membuat dua thread yang menjalankan fungsi pencetak angka. Ini merupakan ilustrasi sederhana dari cara kerja thread di tingkat sistem rendah, di mana kita perlu secara eksplisit membuat dan menggabungkan thread. Program dikompilasi dengan `gcc` menggunakan flag `-pthread` sebagai syarat untuk mengaktifkan pustaka thread.

### c. Thread di Windows (`thrd-win32.c`)

Bagian ini menampilkan implementasi thread di sistem operasi Windows dengan bahasa C. Berbeda dari Linux, Windows menggunakan API-nya sendiri seperti `CreateThread` dan `WaitForSingleObject`.

Program `thrd-win32.c` juga membuat dua thread yang bertugas mencetak angka. Meskipun logika multitasking serupa, pendekatannya bergantung pada struktur dan sintaksis Windows API. Untuk menjalankannya, digunakan kompiler seperti MinGW atau Visual Studio. Ini menunjukkan bahwa meskipun multithreading bersifat universal, implementasinya sangat bergantung pada sistem operasi.

---

## 3. Membuat PPT: Evolusi Prosesor Intel

**Tautan Presentasi:** 

https://docs.google.com/presentation/d/1p7DhvzJzNJ7HFcEAsElM3UJC69o3Hu_O/edit?usp=sharing&ouid=118399304365511840784&rtpof=true&sd=true

---

## 4. Chapter 4 Exercise

### 4.1 Tiga contoh program yang lebih efisien dengan multithreading:

1. **Pembuatan Thumbnail Gambar:** Setiap gambar diproses oleh thread berbeda, memungkinkan proses paralel.  
2. **Web Browser:** Thread terpisah digunakan untuk mengambil data dan menampilkannya secara bersamaan.  
3. **Pengolah Kata:** Thread berbeda untuk input pengguna, pengecekan ejaan, dan tampilan grafis.

### 4.2 Perhitungan Amdahl's Law dengan 60% bagian paralel

Rumus:
```
Speedup = 1 / (S + (1 - S)/N)
S = 0.4
```

- **2 Core:** `Speedup ≈ 1 / (0.4 + 0.6/2) = ~1.43`
- **4 Core:** `Speedup ≈ 1 / (0.4 + 0.6/4) = ~1.82`

### 4.3 Jenis paralelisme pada multithreaded web server?

*Web server tersebut menggunakan **task parallelism**, karena tiap thread melayani klien berbeda secara bersamaan.*

### 4.4 Dua perbedaan antara user-level thread dan kernel-level thread:

| Aspek | User-level | Kernel-level |
|-------|-------------|----------------|
| Manajemen | Diatur oleh pustaka user | Dikelola oleh OS |
| Pemblokiran | Semua thread terblokir | Thread lain tetap jalan |

**Kapan lebih baik?**  
- **User-level:** untuk tugas ringan dan cepat.  
- **Kernel-level:** cocok untuk pemrosesan paralel di sistem multi-core.

### 4.5 Proses context-switching oleh kernel antar thread:

1. **Simpan konteks:** Status thread aktif disimpan (register, stack, dsb).
2. **Pilih thread baru:** Scheduler memilih thread berikutnya.
3. **Muat konteks baru:** Status thread baru dimuat.
4. **Lanjutkan eksekusi:** CPU melanjutkan eksekusi dari thread baru tersebut.

---

**Referensi kode:**  
https://github.com/ferryastika/osc10e/tree/master/ch4
