# UJIAN TENGAH SEMESTER (UTS)
# STRUKTUR DATA - PAKET A

---

**Program Studi:** Sistem Informasi  
**Institut:** Teknologi Kalimantan  
**Semester:** 2 (Dua) | **Tahun Akademik:** 2025/2026  
**Hari/Tanggal:** .............................  
**Waktu:** 100 menit  
**Sifat Ujian:** Closed Book

---

| Nama | NIM | Kelas | Tanda Tangan |
|------|-----|-------|--------------|
| | | | |

---

## PETUNJUK UMUM

1. Berdoalah sebelum mengerjakan soal
2. Tuliskan nama, NIM, dan kelas pada lembar jawaban
3. Kerjakan soal yang dianggap mudah terlebih dahulu
4. Tidak diperkenankan menggunakan alat bantu elektronik
5. Tidak diperkenankan bekerja sama dengan peserta lain

---

# BAGIAN I: PILIHAN GANDA (40%)

**Petunjuk:** Pilihlah satu jawaban yang paling tepat!

---

**1.** Struktur data adalah...
- A. Bahasa pemrograman untuk membuat aplikasi
- B. Cara mengorganisasi dan menyimpan data agar dapat diakses dan dimodifikasi secara efisien
- C. Perangkat keras komputer untuk menyimpan data
- D. Software untuk mengelola database

**2.** Perbedaan utama antara Abstract Data Type (ADT) dan struktur data konkret adalah...
- A. ADT lebih cepat dari struktur data konkret
- B. ADT mendefinisikan operasi tanpa detail implementasi, sedangkan struktur data konkret adalah implementasinya
- C. Struktur data konkret hanya bisa digunakan di Python
- D. ADT hanya untuk data numerik

**3.** Manakah yang termasuk struktur data linear?
- A. Tree
- B. Graph
- C. Queue
- D. Binary Search Tree

**4.** Perhatikan kode berikut:
```python
def mystery(n):
    for i in range(n):
        for j in range(n):
            print(i, j)
```
Kompleksitas waktu Big-O dari kode tersebut adalah...
- A. O(1)
- B. O(n)
- C. O(n²)
- D. O(log n)

**5.** Urutan kompleksitas waktu dari yang tercepat ke terlambat adalah...
- A. O(n) < O(1) < O(n²) < O(log n)
- B. O(1) < O(log n) < O(n) < O(n²)
- C. O(log n) < O(1) < O(n) < O(n²)
- D. O(1) < O(n) < O(log n) < O(n²)

**6.** Karakteristik array yang BENAR adalah...
- A. Elemen disimpan secara acak di memori
- B. Ukuran dapat berubah dengan mudah setelah deklarasi
- C. Semua elemen harus bertipe data sama dan disimpan secara kontinu
- D. Tidak bisa diakses menggunakan index

**7.** Kompleksitas waktu untuk mengakses elemen array pada index tertentu adalah...
- A. O(1)
- B. O(n)
- C. O(log n)
- D. O(n²)

**8.** Pada array 2D dengan 4 baris dan 5 kolom, untuk mengakses elemen di baris ke-3 dan kolom ke-4, sintaks yang benar adalah...
- A. arr[3][4]
- B. arr[4][3]
- C. arr[2][3]
- D. arr[3,4]

**9.** Keuntungan array dibandingkan linked list adalah...
- A. Insert di awal lebih cepat
- B. Akses random dengan O(1)
- C. Ukuran lebih fleksibel
- D. Tidak perlu alokasi memori di awal

**10.** Dalam Single Linked List, setiap node terdiri dari...
- A. Data saja
- B. Data dan pointer ke node sebelumnya
- C. Data dan pointer ke node berikutnya
- D. Data, pointer ke node sebelumnya, dan pointer ke node berikutnya

**11.** Kompleksitas waktu untuk menghapus node di awal Single Linked List adalah...
- A. O(1)
- B. O(n)
- C. O(log n)
- D. O(n²)

**12.** Double Linked List berbeda dari Single Linked List karena...
- A. Tidak menggunakan pointer
- B. Setiap node memiliki pointer ke node sebelumnya dan berikutnya
- C. Hanya bisa menyimpan data numerik
- D. Tidak bisa melakukan operasi delete

**13.** Keunggulan Double Linked List dibandingkan Single Linked List adalah...
- A. Menggunakan memori lebih sedikit
- B. Bisa melakukan traversal dua arah
- C. Insert di awal lebih cepat
- D. Implementasi lebih sederhana

**14.** Dalam Double Linked List yang memiliki pointer TAIL, kompleksitas delete di akhir adalah...
- A. O(1)
- B. O(n)
- C. O(log n)
- D. O(n²)

**15.** Circular Linked List paling cocok digunakan untuk...
- A. Menyimpan data yang tidak pernah berubah
- B. Implementasi Round Robin Scheduling
- C. Akses random yang cepat
- D. Menyimpan data dalam jumlah kecil

**16.** Stack menggunakan prinsip...
- A. FIFO (First In First Out)
- B. LIFO (Last In First Out)
- C. Random Access
- D. Priority Based

**17.** Jika dilakukan operasi berikut pada stack kosong:
```
push(5), push(10), push(15), pop(), push(20), pop(), pop()
```
Nilai yang di-pop secara berurutan adalah...
- A. 5, 10, 15
- B. 15, 20, 10
- C. 20, 15, 10
- D. 15, 10, 5

**18.** Queue menggunakan prinsip...
- A. LIFO (Last In First Out)
- B. FIFO (First In First Out)
- C. Random Access
- D. LIFO dan FIFO

**19.** Masalah "false overflow" pada Linear Queue terjadi ketika...
- A. Queue benar-benar penuh
- B. Ada ruang kosong di depan tetapi rear sudah di posisi terakhir
- C. Queue kosong
- D. Terjadi error pada program

**20.** Deque (Double-Ended Queue) berbeda dari Queue biasa karena...
- A. Lebih cepat
- B. Hanya bisa menyimpan 2 elemen
- C. Bisa melakukan insert dan delete di kedua ujung (front dan rear)
- D. Tidak bisa overflow

---

# BAGIAN II: ESSAY (60%)

**Petunjuk:** Jawablah pertanyaan berikut dengan jelas dan sistematis!

---

## Soal 1 (10%)

**Jelaskan perbedaan antara Abstract Data Type (ADT) dan struktur data konkret!**

Dalam jawaban Anda, sertakan:
- a. Definisi ADT
- b. Definisi struktur data konkret
- c. Contoh ADT dan implementasinya dalam struktur data konkret
- d. Mengapa pemisahan ADT dan implementasi penting dalam pemrograman?

---

## Soal 2 (10%)

**Analisis kompleksitas Big-O untuk operasi-operasi berikut pada Array TIDAK TERURUT dengan n elemen:**

| Operasi | Kompleksitas | Alasan |
|---------|--------------|--------|
| a. Akses elemen di index ke-i | | |
| b. Pencarian (search) elemen | | |
| c. Insert di akhir (jika masih ada ruang) | | |
| d. Insert di awal | | |
| e. Delete di posisi tengah | | |

---

## Soal 3 (10%)

**Diberikan Single Linked List sebagai berikut:**

```
HEAD → [10] → [20] → [30] → [40] → [50] → NULL
```

**Kerjakan:**
- a. Gambarkan langkah-langkah untuk menyisipkan node dengan nilai **25** setelah node **20**
- b. Gambarkan langkah-langkah untuk menghapus node dengan nilai **30**
- c. Gambarkan hasil akhir setelah kedua operasi di atas

---

## Soal 4 (10%)

**Bandingkan Array dan Linked List berdasarkan aspek-aspek berikut:**

| Aspek | Array | Linked List |
|-------|-------|-------------|
| a. Penyimpanan di memori | | |
| b. Akses elemen (random access) | | |
| c. Insert di awal | | |
| d. Insert di akhir | | |
| e. Penggunaan memori | | |
| f. Kapan sebaiknya digunakan | | |

---

## Soal 5 (10%)

**Aplikasi Stack - Balanced Parentheses**

Diberikan ekspresi: **`{[A + B] * (C - D)}`**

**Kerjakan:**
- a. Jelaskan algoritma untuk mengecek apakah tanda kurung dalam ekspresi tersebut seimbang (balanced) menggunakan Stack
- b. Trace langkah demi langkah proses pengecekan menggunakan tabel berikut:

| Langkah | Karakter | Aksi | Isi Stack |
|---------|----------|------|-----------|
| 1 | | | |
| 2 | | | |
| ... | | | |

- c. Apakah ekspresi tersebut balanced? Jelaskan!

---

## Soal 6 (10%)

**Circular Queue**

Diberikan Circular Queue dengan **kapasitas 5** (index 0-4). Kondisi awal: **front = 0, rear = -1, size = 0**.

**Kerjakan:**
- a. Jelaskan mengapa Circular Queue dapat mengatasi masalah "false overflow" pada Linear Queue!
- b. Trace operasi berikut dan gambarkan kondisi queue setelah setiap operasi:

```
1. enqueue(10)
2. enqueue(20)
3. enqueue(30)
4. dequeue()
5. dequeue()
6. enqueue(40)
7. enqueue(50)
8. enqueue(60)
```

Gunakan format tabel:

| No | Operasi | front | rear | size | Isi Queue |
|----|---------|-------|------|------|-----------|
| 0 | (awal) | 0 | -1 | 0 | [ _, _, _, _, _ ] |
| 1 | enqueue(10) | | | | |
| ... | | | | | |

- c. Tuliskan formula untuk menghitung posisi rear baru saat enqueue pada Circular Queue!

---

# SELAMAT MENGERJAKAN!

---

*"The only way to learn a new programming language is by writing programs in it."*
*— Dennis Ritchie*

---