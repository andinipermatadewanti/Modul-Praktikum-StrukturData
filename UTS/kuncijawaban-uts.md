# KUNCI JAWABAN
# UJIAN TENGAH SEMESTER (UTS) STRUKTUR DATA

---

**RAHASIA - HANYA UNTUK DOSEN**

---

# KUNCI JAWABAN PAKET A

## BAGIAN I: PILIHAN GANDA (40%)

| No | Jawaban | Pembahasan Singkat |
|----|---------|-------------------|
| 1 | **B** | Struktur data adalah cara mengorganisasi dan menyimpan data agar efisien |
| 2 | **B** | ADT = abstraksi (apa), Struktur Data = implementasi (bagaimana) |
| 3 | **C** | Queue adalah struktur data linear. Tree, Graph, BST adalah non-linear |
| 4 | **C** | Nested loop n × n = O(n²) |
| 5 | **B** | O(1) < O(log n) < O(n) < O(n²) |
| 6 | **C** | Array: homogen, kontinu, index-based, fixed size |
| 7 | **A** | Akses array via index adalah O(1) - direct access |
| 8 | **C** | Index dimulai dari 0: baris ke-3 = index 2, kolom ke-4 = index 3 |
| 9 | **B** | Array unggul di random access O(1) |
| 10 | **C** | SLL node: data + pointer next |
| 11 | **A** | Delete di awal SLL: hanya ubah HEAD, O(1) |
| 12 | **B** | DLL node: data + prev + next |
| 13 | **B** | DLL bisa traverse maju dan mundur |
| 14 | **A** | DLL dengan TAIL: delete akhir O(1), langsung akses via tail.prev |
| 15 | **B** | CLL cocok untuk round robin karena bisa berputar terus |
| 16 | **B** | Stack = LIFO (Last In First Out) |
| 17 | **B** | Trace: push 5,10,15 → pop 15 → push 20 → pop 20 → pop 10. Hasil: 15, 20, 10 |
| 18 | **B** | Queue = FIFO (First In First Out) |
| 19 | **B** | False overflow: rear di akhir tapi ada ruang kosong di depan |
| 20 | **C** | Deque: insert/delete di front DAN rear |

---

## BAGIAN II: ESSAY (60%)

### Soal 1 (10%) - ADT vs Struktur Data Konkret

**a. Definisi ADT:**
ADT (Abstract Data Type) adalah model matematis untuk tipe data yang didefinisikan berdasarkan:
- Nilai/data yang dapat disimpan
- Operasi yang dapat dilakukan pada data
- TANPA menentukan bagaimana implementasinya

**b. Definisi Struktur Data Konkret:**
Struktur data konkret adalah implementasi nyata dari ADT dalam bahasa pemrograman tertentu, yang menentukan:
- Bagaimana data disimpan di memori
- Bagaimana operasi diimplementasikan

**c. Contoh:**
| ADT | Struktur Data Konkret |
|-----|----------------------|
| List | Array, Linked List |
| Stack | Array-based Stack, Linked Stack |
| Queue | Array Queue, Linked Queue, Circular Queue |
| Set | Hash Set, Tree Set |

**d. Pentingnya Pemisahan:**
- **Abstraksi:** Programmer fokus pada WHAT, bukan HOW
- **Fleksibilitas:** Bisa ganti implementasi tanpa ubah interface
- **Reusability:** Kode lebih modular dan dapat digunakan ulang
- **Maintenance:** Lebih mudah dipelihara dan di-debug

**Rubrik Penilaian:**
- Definisi ADT (2%)
- Definisi struktur data konkret (2%)
- Contoh lengkap (3%)
- Penjelasan pentingnya (3%)

---

### Soal 2 (10%) - Kompleksitas Array

| Operasi | Kompleksitas | Alasan |
|---------|--------------|--------|
| a. Akses elemen di index ke-i | **O(1)** | Direct access, langsung hitung alamat memori |
| b. Pencarian (search) elemen | **O(n)** | Worst case: harus cek semua elemen (linear search) |
| c. Insert di akhir (ada ruang) | **O(1)** | Langsung taruh di posisi berikutnya |
| d. Insert di awal | **O(n)** | Harus geser semua elemen ke kanan |
| e. Delete di posisi tengah | **O(n)** | Harus geser elemen setelahnya ke kiri |

**Rubrik Penilaian:**
- Setiap baris benar dengan alasan: 2%
- Total: 5 × 2% = 10%

---

### Soal 3 (10%) - Operasi Single Linked List

**a. Insert 25 setelah 20:**

**Langkah 1:** Buat node baru dengan nilai 25
```
new_node = [25|NULL]
```

**Langkah 2:** Traverse ke node 20
```
HEAD → [10] → [20] → [30] → [40] → [50] → NULL
              ↑
           current
```

**Langkah 3:** Set new_node.next = current.next
```
new_node.next = [30]
[25] → [30]
```

**Langkah 4:** Set current.next = new_node
```
HEAD → [10] → [20] → [25] → [30] → [40] → [50] → NULL
```

**b. Delete 30:**

**Langkah 1:** Traverse ke node sebelum 30 (yaitu 25)
```
HEAD → [10] → [20] → [25] → [30] → [40] → [50] → NULL
                      ↑
                   current
```

**Langkah 2:** Set current.next = current.next.next (skip 30)
```
current.next = [40]
```

**c. Hasil Akhir:**
```
HEAD → [10] → [20] → [25] → [40] → [50] → NULL
```

**Rubrik Penilaian:**
- Insert dengan langkah benar (4%)
- Delete dengan langkah benar (4%)
- Hasil akhir benar (2%)

---

### Soal 4 (10%) - Perbandingan Array vs Linked List

| Aspek | Array | Linked List |
|-------|-------|-------------|
| a. Penyimpanan di memori | Kontinu (berurutan) | Tersebar (tidak berurutan) |
| b. Akses elemen | O(1) - random access | O(n) - sequential access |
| c. Insert di awal | O(n) - geser semua elemen | O(1) - ubah pointer |
| d. Insert di akhir | O(1) jika ada ruang | O(n) atau O(1) dengan tail |
| e. Penggunaan memori | Lebih hemat (data saja) | Lebih boros (data + pointer) |
| f. Kapan digunakan | Data tetap, perlu random access | Data dinamis, sering insert/delete |

**Rubrik Penilaian:**
- Setiap baris benar: ~1.5%
- Total: 6 × ~1.5% ≈ 10%

---

### Soal 5 (10%) - Balanced Parentheses

**a. Algoritma:**
1. Buat stack kosong
2. Scan ekspresi dari kiri ke kanan
3. Jika karakter adalah buka kurung `(`, `{`, `[`: PUSH ke stack
4. Jika karakter adalah tutup kurung `)`, `}`, `]`:
   - Jika stack kosong → NOT BALANCED
   - POP dari stack, cek apakah cocok
   - Jika tidak cocok → NOT BALANCED
5. Setelah selesai, jika stack kosong → BALANCED, jika tidak → NOT BALANCED

**b. Trace untuk `{[A + B] * (C - D)}`:**

| Langkah | Karakter | Aksi | Isi Stack |
|---------|----------|------|-----------|
| 1 | `{` | Push | `{` |
| 2 | `[` | Push | `{[` |
| 3 | `A` | Skip (bukan kurung) | `{[` |
| 4 | `+` | Skip | `{[` |
| 5 | `B` | Skip | `{[` |
| 6 | `]` | Pop `[`, cocok ✓ | `{` |
| 7 | `*` | Skip | `{` |
| 8 | `(` | Push | `{(` |
| 9 | `C` | Skip | `{(` |
| 10 | `-` | Skip | `{(` |
| 11 | `D` | Skip | `{(` |
| 12 | `)` | Pop `(`, cocok ✓ | `{` |
| 13 | `}` | Pop `{`, cocok ✓ | `` (kosong) |

**c. Kesimpulan:** 
Ekspresi **BALANCED** karena:
- Semua kurung buka memiliki pasangan tutup yang cocok
- Stack kosong di akhir proses

**Rubrik Penilaian:**
- Algoritma benar (3%)
- Trace lengkap dan benar (5%)
- Kesimpulan dengan penjelasan (2%)

---

### Soal 6 (10%) - Circular Queue

**a. Mengapa Circular Queue mengatasi False Overflow:**

Linear Queue:
```
Index:   0    1    2    3    4
       [  ] [  ] [30] [40] [50]
                  ↑         ↑
                front     rear

rear = 4 (posisi terakhir), tidak bisa enqueue lagi!
Padahal index 0 dan 1 kosong = FALSE OVERFLOW
```

Circular Queue:
- Menggunakan formula: `rear = (rear + 1) % capacity`
- Setelah index terakhir, kembali ke index 0
- Ruang kosong di depan bisa digunakan kembali

**b. Trace Operasi:**

| No | Operasi | front | rear | size | Isi Queue |
|----|---------|-------|------|------|-----------|
| 0 | (awal) | 0 | -1 | 0 | `[ _, _, _, _, _ ]` |
| 1 | enqueue(10) | 0 | 0 | 1 | `[10, _, _, _, _ ]` |
| 2 | enqueue(20) | 0 | 1 | 2 | `[10, 20, _, _, _ ]` |
| 3 | enqueue(30) | 0 | 2 | 3 | `[10, 20, 30, _, _ ]` |
| 4 | dequeue() → 10 | 1 | 2 | 2 | `[ _, 20, 30, _, _ ]` |
| 5 | dequeue() → 20 | 2 | 2 | 1 | `[ _, _, 30, _, _ ]` |
| 6 | enqueue(40) | 2 | 3 | 2 | `[ _, _, 30, 40, _ ]` |
| 7 | enqueue(50) | 2 | 4 | 3 | `[ _, _, 30, 40, 50]` |
| 8 | enqueue(60) | 2 | 0 | 4 | `[60, _, 30, 40, 50]` ← wrap around! |

**c. Formula:**
```
rear_baru = (rear_lama + 1) % capacity
```

Contoh: rear = 4, capacity = 5
```
rear_baru = (4 + 1) % 5 = 5 % 5 = 0 (kembali ke awal)
```

**Rubrik Penilaian:**
- Penjelasan false overflow (3%)
- Trace operasi benar (5%)
- Formula benar dengan contoh (2%)

---

# KUNCI JAWABAN PAKET B

## BAGIAN I: PILIHAN GANDA (40%)

| No | Jawaban | Pembahasan Singkat |
|----|---------|-------------------|
| 1 | **B** | Tujuan: mengorganisasi data agar program efisien |
| 2 | **B** | ADT = model matematis dengan operasi tanpa implementasi |
| 3 | **C** | Graph adalah non-linear |
| 4 | **B** | Single loop n kali = O(n) |
| 5 | **C** | O(1) < O(log n) < O(n) < O(n log n) |
| 6 | **C** | Array ukuran tetap setelah dibuat |
| 7 | **B** | Insert awal array = geser semua = O(n) |
| 8 | **B** | 3 × 4 = 12 elemen |
| 9 | **B** | Linked List: insert/delete awal O(1) |
| 10 | **B** | Pointer ke node berikutnya = next |
| 11 | **B** | Search SLL = sequential = O(n) |
| 12 | **C** | DLL: 2 pointer (prev dan next) |
| 13 | **B** | DLL dengan tail: delete akhir O(1) |
| 14 | **B** | CLL: last node → HEAD |
| 15 | **C** | Playlist repeat = circular |
| 16 | **C** | Tambah ke stack = push |
| 17 | **B** | Trace: push A,B → pop B → push C,D → pop D → pop C. Hasil: B, D, C |
| 18 | **C** | Ambil dari queue = dequeue |
| 19 | **C** | Circular Queue mengatasi false overflow |
| 20 | **B** | Priority Queue: keluar berdasarkan prioritas |

---

## BAGIAN II: ESSAY (60%)

### Soal 1 (10%) - Big-O Notation

**a. Definisi dan Pentingnya:**
- Big-O Notation adalah notasi matematika untuk menggambarkan **batas atas** pertumbuhan waktu/ruang algoritma
- Penting untuk: membandingkan efisiensi algoritma, memprediksi performa saat data membesar

**b. Penjelasan Kompleksitas:**

| Notasi | Nama | Penjelasan |
|--------|------|------------|
| O(1) | Constant | Waktu konstan, tidak tergantung ukuran input |
| O(n) | Linear | Waktu bertambah linear dengan input |
| O(n²) | Quadratic | Waktu bertambah kuadratik (nested loop) |
| O(log n) | Logarithmic | Waktu bertambah logaritmik (data dibagi setengah) |

**c. Contoh:**
- O(1): Akses array[i], push/pop stack
- O(n): Linear search, traverse linked list
- O(n²): Bubble sort, nested loop
- O(log n): Binary search

**d. Aturan Penyederhanaan:**
1. **Abaikan konstanta:** O(2n) → O(n), O(100) → O(1)
2. **Ambil term dominan:** O(n² + n) → O(n²), O(n³ + n² + n) → O(n³)

**Rubrik Penilaian:**
- Definisi dan pentingnya (2%)
- Penjelasan 4 kompleksitas (4%)
- Contoh masing-masing (2%)
- Aturan penyederhanaan (2%)

---

### Soal 2 (10%) - Operasi Single Linked List

**a. Insert 20 setelah 15:**

```
Sebelum:
HEAD → [5] → [15] → [25] → [35] → [45] → NULL

Langkah 1: Buat node baru [20]
Langkah 2: Traverse ke node 15 (current)
Langkah 3: new_node.next = current.next (→[25])
Langkah 4: current.next = new_node

Hasil:
HEAD → [5] → [15] → [20] → [25] → [35] → [45] → NULL
```

**b. Delete 25:**

```
Sebelum:
HEAD → [5] → [15] → [20] → [25] → [35] → [45] → NULL

Langkah 1: Traverse ke node sebelum 25 (yaitu 20)
Langkah 2: current.next = current.next.next (skip 25)

Hasil:
HEAD → [5] → [15] → [20] → [35] → [45] → NULL
```

**c. Kompleksitas:**
- Insert di posisi tertentu: **O(n)** - perlu traverse untuk menemukan posisi
- Delete di posisi tertentu: **O(n)** - perlu traverse untuk menemukan node sebelumnya

**Rubrik Penilaian:**
- Insert dengan gambar (4%)
- Delete dengan gambar (4%)
- Kompleksitas dengan penjelasan (2%)

---

### Soal 3 (10%) - Perbandingan Linked List

| Aspek | Single LL | Double LL | Circular LL |
|-------|-----------|-----------|-------------|
| a. Jumlah pointer per node | 1 (next) | 2 (prev, next) | 1 atau 2 |
| b. Navigasi/Traversal | Maju saja | Maju dan mundur | Berputar terus |
| c. Delete akhir (dengan tail) | O(n) | O(1) | O(n) |
| d. Penggunaan memori | Paling hemat | Paling boros | Sedang |
| e. Contoh aplikasi | Playlist sederhana | Browser history, Text editor | Round robin, Music repeat |

**Rubrik Penilaian:**
- Setiap baris benar: 2%
- Total: 5 × 2% = 10%

---

### Soal 4 (10%) - Konversi Infix ke Postfix

**a. Algoritma:**
1. Scan dari kiri ke kanan
2. Jika operand: langsung ke output
3. Jika operator:
   - Pop operator dari stack yang prioritasnya ≥ operator sekarang ke output
   - Push operator sekarang ke stack
4. Setelah selesai, pop semua dari stack ke output

**b. Trace `A + B * C - D`:**

| Langkah | Karakter | Aksi | Stack | Output |
|---------|----------|------|-------|--------|
| 1 | A | Output | | A |
| 2 | + | Push | + | A |
| 3 | B | Output | + | A B |
| 4 | * | Push (* > +) | + * | A B |
| 5 | C | Output | + * | A B C |
| 6 | - | Pop *, Pop +, Push - | - | A B C * + |
| 7 | D | Output | - | A B C * + D |
| 8 | (end) | Pop semua | | A B C * + D - |

**c. Hasil Postfix:** `A B C * + D -`

**Rubrik Penilaian:**
- Algoritma benar (3%)
- Trace lengkap dan benar (5%)
- Hasil akhir benar (2%)

---

### Soal 5 (10%) - Aplikasi Queue

**a & b. 3 Contoh Aplikasi Queue:**

1. **Antrian Printer (Print Spooler)**
   - Dokumen dicetak sesuai urutan masuk
   - FIFO tepat: yang pertama dikirim, pertama dicetak

2. **Antrian Customer Service**
   - Pelanggan dilayani sesuai urutan kedatangan
   - FIFO adil: yang datang duluan, dilayani duluan

3. **CPU Process Scheduling**
   - Proses menunggu giliran CPU
   - FIFO (dalam round robin): setiap proses dapat giliran

**c. Queue vs Priority Queue:**

| Queue Biasa | Priority Queue |
|-------------|----------------|
| FIFO murni | Berdasarkan prioritas |
| Contoh: Antrian biasa | Contoh: UGD RS |
| Semua sama penting | Ada yang lebih urgent |
| Yang duluan = dilayani duluan | Prioritas tinggi = duluan |

**Rubrik Penilaian:**
- 3 contoh dengan penjelasan (6%)
- Mengapa FIFO tepat (2%)
- Perbedaan Queue vs Priority Queue (2%)

---

### Soal 6 (10%) - Pemilihan Struktur Data

| No | Kasus | Struktur Data | Alasan |
|----|-------|---------------|--------|
| a | Undo/Redo | **Stack** | LIFO: aksi terakhir di-undo pertama |
| b | Antrian RS dengan prioritas | **Priority Queue** | Pasien darurat didahulukan |
| c | Data mahasiswa dicari by NIM | **Array** (sorted) atau **Hash Table** | Akses cepat O(1) atau O(log n) |
| d | Playlist next/prev/repeat | **Double Circular LL** | Navigasi 2 arah + repeat (circular) |
| e | Browser Back | **Stack** | LIFO: halaman terakhir di-back pertama |

**Rubrik Penilaian:**
- Setiap baris: struktur data benar (1%) + alasan tepat (1%) = 2%
- Total: 5 × 2% = 10%

---

# PEDOMAN PENSKORAN

## Total Nilai

| Bagian | Bobot |
|--------|-------|
| Pilihan Ganda (20 soal × 2%) | 40% |
| Essay (6 soal × 10%) | 60% |
| **TOTAL** | **100%** |

## Konversi Nilai

| Rentang | Huruf | Keterangan |
|---------|-------|------------|
| 85-100 | A | Sangat Baik |
| 80-84 | A- | |
| 75-79 | B+ | Baik |
| 70-74 | B | |
| 65-69 | B- | |
| 60-64 | C+ | Cukup |
| 55-59 | C | |
| 50-54 | C- | |
| 40-49 | D | Kurang |
| 0-39 | E | Tidak Lulus |

---

*Kunci jawaban ini bersifat RAHASIA dan hanya untuk keperluan penilaian oleh dosen.*