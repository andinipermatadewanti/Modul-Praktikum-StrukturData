# UJIAN TENGAH SEMESTER (UTS)
# STRUKTUR DATA - PAKET B

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

**1.** Tujuan utama mempelajari struktur data adalah...
- A. Untuk membuat tampilan program lebih menarik
- B. Untuk mengorganisasi data secara efisien sehingga program berjalan optimal
- C. Untuk memperbesar ukuran program
- D. Untuk membuat program lebih sulit dipahami

**2.** ADT (Abstract Data Type) adalah...
- A. Tipe data yang hanya ada di bahasa Python
- B. Model matematis yang mendefinisikan tipe data berdasarkan operasinya tanpa detail implementasi
- C. Struktur data yang paling cepat
- D. Tipe data untuk menyimpan angka abstrak

**3.** Yang BUKAN termasuk struktur data linear adalah...
- A. Array
- B. Stack
- C. Graph
- D. Queue

**4.** Perhatikan kode berikut:
```python
def func(arr):
    total = 0
    for x in arr:
        total += x
    return total
```
Jika arr memiliki n elemen, kompleksitas waktu Big-O adalah...
- A. O(1)
- B. O(n)
- C. O(n²)
- D. O(log n)

**5.** Manakah urutan kompleksitas yang BENAR dari tercepat ke terlambat?
- A. O(1), O(n), O(log n), O(n²)
- B. O(log n), O(1), O(n), O(n²)
- C. O(1), O(log n), O(n), O(n log n)
- D. O(n), O(1), O(n²), O(log n)

**6.** Manakah yang BUKAN karakteristik array?
- A. Elemen disimpan secara kontinu di memori
- B. Akses elemen menggunakan index
- C. Ukuran bisa berubah dengan mudah setelah dibuat
- D. Semua elemen memiliki tipe data yang sama

**7.** Kompleksitas waktu untuk insert elemen di awal array dengan n elemen adalah...
- A. O(1)
- B. O(n)
- C. O(log n)
- D. O(n²)

**8.** Jika sebuah matrix memiliki 3 baris dan 4 kolom, berapa total elemen yang dapat disimpan?
- A. 7
- B. 12
- C. 34
- D. 43

**9.** Keuntungan Linked List dibandingkan Array adalah...
- A. Akses random lebih cepat
- B. Insert dan delete di awal lebih efisien
- C. Menggunakan memori lebih sedikit
- D. Lebih mudah diimplementasikan

**10.** Pointer pada node Single Linked List yang menunjuk ke node berikutnya disebut...
- A. prev
- B. next
- C. head
- D. tail

**11.** Untuk mencari elemen di Single Linked List dengan n node, kompleksitas waktunya adalah...
- A. O(1)
- B. O(n)
- C. O(log n)
- D. O(n²)

**12.** Berapa banyak pointer yang dimiliki setiap node dalam Double Linked List?
- A. 0
- B. 1
- C. 2
- D. 3

**13.** Operasi yang menjadi lebih efisien di Double Linked List dibandingkan Single Linked List adalah...
- A. Insert di awal
- B. Delete di akhir (dengan pointer tail)
- C. Pencarian elemen
- D. Insert di akhir

**14.** Pada Circular Linked List, node terakhir menunjuk ke...
- A. NULL
- B. Node pertama (HEAD)
- C. Node di tengah
- D. Dirinya sendiri

**15.** Aplikasi yang paling cocok menggunakan Circular Linked List adalah...
- A. Undo/Redo pada text editor
- B. Antrian printer
- C. Music playlist dengan mode repeat
- D. Browser history

**16.** Operasi untuk menambahkan elemen ke Stack disebut...
- A. enqueue
- B. dequeue
- C. push
- D. insert

**17.** Jika dilakukan operasi berikut pada stack kosong:
```
push(A), push(B), pop(), push(C), push(D), pop(), pop()
```
Urutan elemen yang di-pop adalah...
- A. A, B, C
- B. B, D, C
- C. D, C, A
- D. B, C, D

**18.** Operasi untuk mengambil elemen dari Queue disebut...
- A. pop
- B. push
- C. dequeue
- D. delete

**19.** Circular Queue mengatasi masalah pada Linear Queue yaitu...
- A. Kecepatan akses yang lambat
- B. Penggunaan memori yang besar
- C. Ruang kosong di depan tidak bisa digunakan (false overflow)
- D. Tidak bisa menyimpan banyak elemen

**20.** Priority Queue berbeda dari Queue biasa karena...
- A. Lebih cepat
- B. Elemen dikeluarkan berdasarkan prioritas, bukan urutan masuk
- C. Hanya bisa menyimpan angka
- D. Tidak bisa overflow

---

# BAGIAN II: ESSAY (60%)

**Petunjuk:** Jawablah pertanyaan berikut dengan jelas dan sistematis!

---

## Soal 1 (10%)

**Jelaskan konsep Big-O Notation dalam analisis algoritma!**

Dalam jawaban Anda, sertakan:
- a. Apa itu Big-O Notation dan mengapa penting?
- b. Jelaskan arti dari: O(1), O(n), O(n²), dan O(log n)
- c. Berikan contoh operasi/algoritma untuk masing-masing kompleksitas di atas
- d. Jelaskan aturan penyederhanaan Big-O (abaikan konstanta, ambil term dominan)

---

## Soal 2 (10%)

**Diberikan Single Linked List sebagai berikut:**

```
HEAD → [5] → [15] → [25] → [35] → [45] → NULL
```

**Kerjakan:**
- a. Gambarkan langkah-langkah untuk menyisipkan node dengan nilai **20** setelah node **15**
- b. Gambarkan langkah-langkah untuk menghapus node dengan nilai **25** (node hasil insert)
- c. Berapa kompleksitas waktu untuk masing-masing operasi? Jelaskan!

---

## Soal 3 (10%)

**Bandingkan Single Linked List, Double Linked List, dan Circular Linked List:**

| Aspek | Single LL | Double LL | Circular LL |
|-------|-----------|-----------|-------------|
| a. Jumlah pointer per node | | | |
| b. Navigasi/Traversal | | | |
| c. Delete di akhir (dengan tail) | | | |
| d. Penggunaan memori | | | |
| e. Contoh aplikasi | | | |

---

## Soal 4 (10%)

**Stack - Konversi Infix ke Postfix**

Diberikan ekspresi infix: **`A + B * C - D`**

Tabel prioritas operator:
| Operator | Prioritas |
|----------|-----------|
| + , - | 1 |
| * , / | 2 |

**Kerjakan:**
- a. Jelaskan secara singkat algoritma konversi infix ke postfix menggunakan Stack
- b. Trace langkah demi langkah proses konversi menggunakan tabel berikut:

| Langkah | Karakter | Aksi | Stack | Output |
|---------|----------|------|-------|--------|
| 1 | A | | | |
| 2 | + | | | |
| ... | | | | |

- c. Tuliskan hasil akhir ekspresi postfix!

---

## Soal 5 (10%)

**Aplikasi Queue dalam Kehidupan Nyata**

- a. Sebutkan dan jelaskan **3 contoh aplikasi Queue** dalam kehidupan nyata atau sistem komputer!
- b. Untuk setiap contoh, jelaskan mengapa Queue (FIFO) adalah struktur data yang tepat!
- c. Jelaskan perbedaan penggunaan Queue biasa vs Priority Queue dengan contoh kasus!

---

## Soal 6 (10%)

**Analisis Pemilihan Struktur Data**

Diberikan kasus-kasus berikut. Tentukan struktur data yang paling tepat dan jelaskan alasannya!

| No | Kasus | Struktur Data | Alasan |
|----|-------|---------------|--------|
| a. | Sistem Undo/Redo pada aplikasi pengolah kata | | |
| b. | Antrian pasien di rumah sakit (ada prioritas darurat) | | |
| c. | Menyimpan data mahasiswa yang sering dicari berdasarkan NIM | | |
| d. | Playlist musik dengan fitur next, previous, dan repeat | | |
| e. | Browser history dengan tombol Back | | |

---

# SELAMAT MENGERJAKAN!

---

*"First, solve the problem. Then, write the code."*
*— John Johnson*

---