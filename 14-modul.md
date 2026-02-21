# MODUL 14: SORTING LANJUTAN

---

**Mata Kuliah:** Struktur Data  
**Program Studi:** Sistem Informasi - Institut Teknologi Kalimantan  
**SKS:** 3 (2 Teori + 1 Praktikum)  
**Pertemuan:** 14 dari 16

---

## Tujuan Praktikum
Mengimplementasikan Merge Sort, Quick Sort, dan Heap Sort, serta membandingkan performa dengan sorting dasar.

> ⚠️ **Catatan:** Kode yang dibuat di praktikum ini akan **dikembangkan lebih lanjut** di Tugas Terstruktur.

---

## Praktikum 14.1: Implementasi Merge Sort (30 menit)

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 14.1: Implementasi Merge Sort
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
1. Implementasikan merge_sort dan merge
2. Jalankan test cases
3. SIMPAN FILE INI
============================================================
"""

def merge_sort(arr):
    """
    Merge Sort: Divide → Sort → Merge
    Return: array terurut (baru, tidak in-place)
    """
    # TODO: Implementasikan berdasarkan flowchart
    # Base case: len(arr) <= 1 → return arr
    # Divide: mid = len(arr) // 2
    # Conquer: rekursi left dan right
    # Combine: merge(left, right)
    pass


def merge(left, right):
    """
    Menggabungkan dua array terurut menjadi satu array terurut
    Berdasarkan flowchart MERGE
    """
    # TODO: Implementasikan
    # 1. Buat result kosong, i=0, j=0
    # 2. Selama i < len(left) DAN j < len(right):
    #    - Jika left[i] <= right[j]: append left[i], i++
    #    - Else: append right[j], j++
    # 3. Append sisa left atau right
    pass


def merge_sort_verbose(arr, depth=0):
    """
    Merge Sort dengan trace visual (untuk debugging)
    """
    indent = "  " * depth
    print(f"{indent}merge_sort({arr})")
    
    if len(arr) <= 1:
        print(f"{indent}→ return {arr}")
        return arr
    
    mid = len(arr) // 2
    left = merge_sort_verbose(arr[:mid], depth + 1)
    right = merge_sort_verbose(arr[mid:], depth + 1)
    result = merge(left, right)
    print(f"{indent}→ merge({left}, {right}) = {result}")
    return result


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST MERGE SORT")
    print("=" * 50)
    
    test_cases = [
        ([38, 27, 43, 3, 9, 82, 10], [3, 9, 10, 27, 38, 43, 82]),
        ([5, 4, 3, 2, 1], [1, 2, 3, 4, 5]),
        ([1, 2, 3, 4, 5], [1, 2, 3, 4, 5]),
        ([1], [1]),
        ([], []),
        ([3, 3, 1, 1, 2, 2], [1, 1, 2, 2, 3, 3]),
    ]
    
    for i, (input_arr, expected) in enumerate(test_cases):
        result = merge_sort(input_arr.copy())
        assert result == expected, f"GAGAL Test {i+1}: {input_arr} → {result}"
    print(f"✓ Semua {len(test_cases)} test PASSED!")
    
    # Test merge saja
    assert merge([1, 3, 5], [2, 4, 6]) == [1, 2, 3, 4, 5, 6], "GAGAL merge"
    assert merge([], [1, 2]) == [1, 2], "GAGAL merge empty"
    assert merge([1, 2], []) == [1, 2], "GAGAL merge empty"
    print("✓ Merge function tests PASSED!")
    
    # Test stability
    data = [(3, 'a'), (1, 'b'), (3, 'c'), (1, 'd')]
    
    def merge_sort_stable(arr):
        if len(arr) <= 1:
            return arr
        mid = len(arr) // 2
        left = merge_sort_stable(arr[:mid])
        right = merge_sort_stable(arr[mid:])
        result = []
        i = j = 0
        while i < len(left) and j < len(right):
            if left[i][0] <= right[j][0]:
                result.append(left[i])
                i += 1
            else:
                result.append(right[j])
                j += 1
        result.extend(left[i:])
        result.extend(right[j:])
        return result
    
    sorted_data = merge_sort_stable(data)
    assert sorted_data == [(1, 'b'), (1, 'd'), (3, 'a'), (3, 'c')], f"GAGAL stability: {sorted_data}"
    print("✓ Stability test PASSED!")
    
    # Verbose trace
    print("\n--- Trace Merge Sort ---")
    merge_sort_verbose([38, 27, 43, 3])
    
    print("\n" + "=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Praktikum 14.2: Implementasi Quick Sort (35 menit)

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 14.2: Implementasi Quick Sort
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
1. Implementasikan quick_sort (simple) dan in-place
2. Jalankan test cases
============================================================
"""

import random


def quick_sort_simple(arr):
    """
    Quick Sort versi sederhana (tidak in-place)
    Mudah dipahami, tapi butuh extra space
    """
    # TODO: Implementasikan berdasarkan flowchart
    # Base case: len(arr) <= 1
    # Pilih pivot (elemen terakhir)
    # Partisi: left (< pivot), middle (== pivot), right (> pivot)
    # Return quick_sort(left) + middle + quick_sort(right)
    pass


def quick_sort_inplace(arr, low=0, high=None):
    """
    Quick Sort in-place menggunakan Lomuto Partition
    """
    # TODO: Implementasikan
    # Base case: low >= high → return
    # pivot_idx = partition(arr, low, high)
    # Rekursi kiri dan kanan
    pass


def partition(arr, low, high):
    """
    Lomuto Partition
    Pivot = elemen terakhir (arr[high])
    Return: posisi akhir pivot
    """
    # TODO: Implementasikan berdasarkan flowchart PARTITION
    # 1. pivot = arr[high]
    # 2. i = low - 1
    # 3. Untuk j dari low sampai high-1:
    #    Jika arr[j] <= pivot: i++, swap arr[i]↔arr[j]
    # 4. Swap arr[i+1]↔arr[high] (letakkan pivot)
    # 5. Return i+1
    pass


def quick_sort_random(arr, low=0, high=None):
    """Quick Sort dengan random pivot"""
    if high is None:
        high = len(arr) - 1
    
    if low < high:
        # TODO: Implementasikan
        # 1. Pilih random index antara low dan high
        # 2. Swap elemen random ke posisi high
        # 3. Partition biasa
        # 4. Rekursi kiri dan kanan
        pass
    return arr


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST QUICK SORT")
    print("=" * 50)
    
    test_cases = [
        ([38, 27, 43, 3, 9, 82, 10], [3, 9, 10, 27, 38, 43, 82]),
        ([5, 4, 3, 2, 1], [1, 2, 3, 4, 5]),
        ([1, 2, 3, 4, 5], [1, 2, 3, 4, 5]),
        ([1], [1]),
        ([], []),
        ([3, 3, 1, 1, 2, 2], [1, 1, 2, 2, 3, 3]),
        ([7, 7, 7, 7], [7, 7, 7, 7]),
    ]
    
    # Test Simple Quick Sort
    print("\n--- Quick Sort (Simple) ---")
    for i, (input_arr, expected) in enumerate(test_cases):
        result = quick_sort_simple(input_arr.copy())
        assert result == expected, f"GAGAL Test {i+1}: {input_arr} → {result}"
    print(f"✓ Semua {len(test_cases)} test PASSED!")
    
    # Test In-place Quick Sort
    print("\n--- Quick Sort (In-place) ---")
    for i, (input_arr, expected) in enumerate(test_cases):
        arr = input_arr.copy()
        quick_sort_inplace(arr, 0, len(arr) - 1 if arr else 0)
        assert arr == expected, f"GAGAL Test {i+1}: {input_arr} → {arr}"
    print(f"✓ Semua {len(test_cases)} test PASSED!")
    
    # Test Random Pivot
    print("\n--- Quick Sort (Random Pivot) ---")
    for i, (input_arr, expected) in enumerate(test_cases):
        arr = input_arr.copy()
        quick_sort_random(arr, 0, len(arr) - 1 if arr else 0)
        assert arr == expected, f"GAGAL Test {i+1}: {input_arr} → {arr}"
    print(f"✓ Semua {len(test_cases)} test PASSED!")
    
    # Test partition
    arr = [38, 27, 43, 3, 9, 82, 10]
    pivot_pos = partition(arr, 0, 6)
    assert arr[pivot_pos] == 10, f"GAGAL: pivot harus di posisi benar"
    assert all(arr[j] <= 10 for j in range(pivot_pos)), "GAGAL: kiri harus <= pivot"
    assert all(arr[j] >= 10 for j in range(pivot_pos, len(arr))), "GAGAL: kanan harus >= pivot"
    print(f"✓ Partition test PASSED! (pivot 10 di index {pivot_pos})")
    
    print("\n" + "=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Praktikum 14.3: Implementasi Heap Sort (35 menit)

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 14.3: Implementasi Heap Sort
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
1. Implementasikan heapify dan heap_sort
2. Jalankan test cases
============================================================
"""

def heapify(arr, n, i):
    """
    Memastikan subtree berakar di index i memenuhi Max Heap property
    n: ukuran heap (bukan ukuran array)
    Berdasarkan flowchart HEAPIFY
    """
    # TODO: Implementasikan
    # 1. largest = i
    # 2. left = 2*i + 1, right = 2*i + 2
    # 3. Jika left < n dan arr[left] > arr[largest] → largest = left
    # 4. Jika right < n dan arr[right] > arr[largest] → largest = right
    # 5. Jika largest != i → swap dan heapify(arr, n, largest)
    pass


def heap_sort(arr):
    """
    Heap Sort - O(n log n) in-place
    Tahap 1: Build Max Heap
    Tahap 2: Extract max satu per satu
    """
    # TODO: Implementasikan
    # Tahap 1: Build Max Heap
    # for i in range(n//2 - 1, -1, -1): heapify(arr, n, i)
    #
    # Tahap 2: Extract max
    # for i in range(n-1, 0, -1):
    #   swap arr[0]↔arr[i]
    #   heapify(arr, i, 0)
    pass


def heap_sort_verbose(arr):
    """Heap Sort dengan trace visual"""
    n = len(arr)
    print(f"Array awal: {arr}")
    
    # Build Max Heap
    print("\n--- Build Max Heap ---")
    for i in range(n // 2 - 1, -1, -1):
        heapify(arr, n, i)
        print(f"  heapify(i={i}): {arr}")
    print(f"Max Heap: {arr}")
    
    # Extract max
    print("\n--- Extract Max ---")
    for i in range(n - 1, 0, -1):
        arr[0], arr[i] = arr[i], arr[0]
        heapify(arr, i, 0)
        sorted_part = arr[i:]
        heap_part = arr[:i]
        print(f"  step {n-i}: swap → heap={heap_part}, sorted={sorted_part}")
    
    print(f"\nHasil: {arr}")
    return arr


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST HEAP SORT")
    print("=" * 50)
    
    test_cases = [
        ([38, 27, 43, 3, 9, 82, 10], [3, 9, 10, 27, 38, 43, 82]),
        ([5, 4, 3, 2, 1], [1, 2, 3, 4, 5]),
        ([1, 2, 3, 4, 5], [1, 2, 3, 4, 5]),
        ([1], [1]),
        ([], []),
        ([3, 3, 1, 1, 2, 2], [1, 1, 2, 2, 3, 3]),
    ]
    
    for i, (input_arr, expected) in enumerate(test_cases):
        arr = input_arr.copy()
        result = heap_sort(arr)
        assert result == expected, f"GAGAL Test {i+1}: {input_arr} → {result}"
    print(f"✓ Semua {len(test_cases)} test PASSED!")
    
    # Test heapify
    arr = [3, 9, 82]
    heapify(arr, 3, 0)
    assert arr[0] == 82, f"GAGAL heapify: root harus 82, dapat {arr[0]}"
    print("✓ Heapify test PASSED!")
    
    # Verbose trace
    print("\n--- Trace Heap Sort ---")
    heap_sort_verbose([38, 27, 43, 3, 9, 82, 10])
    
    print("\n" + "=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

# BAGIAN C: TUGAS TERSTRUKTUR (120 Menit)

> 📝 **Pengembangan dari Praktikum**
> 
> Tugas ini mengembangkan kode yang sudah dibuat di praktikum.
> Kerjakan setelah praktikum selesai, kumpulkan pada pertemuan berikutnya.

---

## 📋 Informasi Pengumpulan

| Item | Keterangan |
|------|------------|
| **Deadline** | Pertemuan 15 (sebelum kuliah dimulai) |
| **Format** | File Python (.py) |
| **Nama File** | `Tugas14_NIM_Nama.py` |
| **Pengumpulan** | Upload ke github |

---

## Tugas 1: Perbandingan Sorting Dasar vs Lanjutan (40 menit)

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 14.1: Perbandingan Sorting Dasar vs Lanjutan
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

import time
import random


# ============ SORTING DASAR ============
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key
    return arr


def selection_sort(arr):
    n = len(arr)
    for i in range(n - 1):
        min_idx = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        if min_idx != i:
            arr[i], arr[min_idx] = arr[min_idx], arr[i]
    return arr


# ============ SORTING LANJUTAN ============
# COPY dari praktikum 14.1, 14.2, 14.3:

def merge_sort(arr):
    # COPY dari praktikum
    pass

def quick_sort_inplace(arr, low=0, high=None):
    # COPY dari praktikum
    pass

def heap_sort(arr):
    # COPY dari praktikum
    pass


# ============ BENCHMARK ============
def measure_sort(sort_func, arr, inplace=False):
    data = arr.copy()
    start = time.perf_counter()
    if inplace:
        sort_func(data)
    else:
        sort_func(data)
    end = time.perf_counter()
    return end - start


if __name__ == "__main__":
    print("=" * 80)
    print("PERBANDINGAN: SORTING DASAR O(n²) vs SORTING LANJUTAN O(n log n)")
    print("=" * 80)
    
    sizes = [500, 1000, 2000, 5000, 10000, 20000]
    
    # ============ Random Data ============
    print("\n--- Data Acak (Random) ---")
    print(f"{'n':>7} | {'Insertion':>10} | {'Selection':>10} | "
          f"{'Merge':>10} | {'Quick':>10} | {'Heap':>10} | {'Python':>10}")
    print("-" * 85)
    
    for n in sizes:
        data = [random.randint(1, n * 10) for _ in range(n)]
        
        t_ins = measure_sort(insertion_sort, data)
        t_sel = measure_sort(selection_sort, data)
        t_merge = measure_sort(merge_sort, data)
        
        # Quick Sort in-place
        qdata = data.copy()
        start = time.perf_counter()
        quick_sort_inplace(qdata, 0, len(qdata) - 1)
        t_quick = time.perf_counter() - start
        
        t_heap = measure_sort(heap_sort, data)
        
        # Python built-in
        start = time.perf_counter()
        sorted(data)
        t_python = time.perf_counter() - start
        
        print(f"{n:>7} | {t_ins:>9.4f}s | {t_sel:>9.4f}s | "
              f"{t_merge:>9.4f}s | {t_quick:>9.4f}s | {t_heap:>9.4f}s | {t_python:>9.4f}s")
    
    # ============ Nearly Sorted ============
    print("\n--- Data Hampir Terurut ---")
    print(f"{'n':>7} | {'Insertion':>10} | {'Merge':>10} | {'Quick':>10} | {'Heap':>10}")
    print("-" * 55)
    
    for n in sizes:
        data = list(range(n))
        # Tukar 5% elemen secara random
        for _ in range(n // 20):
            i, j = random.randint(0, n-1), random.randint(0, n-1)
            data[i], data[j] = data[j], data[i]
        
        t_ins = measure_sort(insertion_sort, data)
        t_merge = measure_sort(merge_sort, data)
        
        qdata = data.copy()
        start = time.perf_counter()
        quick_sort_inplace(qdata, 0, len(qdata) - 1)
        t_quick = time.perf_counter() - start
        
        t_heap = measure_sort(heap_sort, data)
        
        print(f"{n:>7} | {t_ins:>9.4f}s | {t_merge:>9.4f}s | "
              f"{t_quick:>9.4f}s | {t_heap:>9.4f}s")
    
    print("=" * 80)


# ============================================================
# JAWABAN TUGAS (ISI DI BAWAH INI)
# ============================================================
"""
BAGIAN A: TABEL HASIL OBSERVASI

| n | Insertion | Selection | Merge | Quick | Heap | Python |
|---|-----------|-----------|-------|-------|------|--------|
| 1000 | | | | | | |
| 5000 | | | | | | |
| 10000 | | | | | | |
| 20000 | | | | | | |


BAGIAN B: PERTANYAAN

1. Pada ukuran n berapa mulai terlihat perbedaan signifikan antara 
   O(n²) dan O(n log n)?
   Jawab:


2. Manakah yang paling cepat di antara Merge, Quick, dan Heap Sort? 
   Mengapa?
   Jawab:


3. Mengapa Python built-in sort (Timsort) paling cepat?
   Jawab:


4. Pada data hampir terurut, Insertion Sort bisa lebih cepat dari 
   sorting lanjutan untuk n kecil. Pada n berapa batasnya?
   Jawab:


5. Jika Anda diminta merancang sorting library dari nol, algoritma 
   mana yang akan Anda pilih sebagai basis? Jelaskan!
   Jawab:

"""
```

---

## Tugas 2: Studi Kasus — Sorting pada Data Kompleks (40 menit)

### Deskripsi
Implementasikan sorting lanjutan untuk mengurutkan data kompleks (objek/dict) dengan berbagai kriteria.

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 14.2: Sorting pada Data Kompleks
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

def merge_sort_by_key(arr, key=None, reverse=False):
    """
    Merge Sort yang mendukung custom key dan reverse
    Stable sort — menjaga urutan relatif elemen dengan key sama
    """
    # TODO: Implementasikan
    # Modifikasi merge_sort agar menggunakan key() untuk perbandingan
    # Jika reverse=True, balik urutan
    pass


def quick_sort_by_key(arr, key=None, reverse=False):
    """
    Quick Sort yang mendukung custom key dan reverse
    """
    # TODO: Implementasikan
    pass


def multi_key_sort(arr, keys):
    """
    Sort berdasarkan multiple keys (prioritas dari kiri ke kanan)
    keys: list of tuples (key_func, reverse)
    Contoh: keys=[(lambda x: x['grade'], False), (lambda x: x['nama'], False)]
    
    Trick: Sort dari key terakhir ke pertama menggunakan stable sort!
    """
    # TODO: Implementasikan
    # Iterasi keys dari belakang ke depan
    # Gunakan merge_sort_by_key (stable) untuk setiap key
    pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 60)
    print("TEST SORTING DATA KOMPLEKS")
    print("=" * 60)
    
    # Test 1: Sort dict by field
    products = [
        {"nama": "Laptop", "harga": 15000000, "rating": 4.5},
        {"nama": "Mouse", "harga": 250000, "rating": 4.8},
        {"nama": "Keyboard", "harga": 500000, "rating": 4.2},
        {"nama": "Monitor", "harga": 3000000, "rating": 4.7},
        {"nama": "Headset", "harga": 750000, "rating": 4.5},
    ]
    
    # Sort by harga ascending
    result = merge_sort_by_key(products.copy(), key=lambda x: x["harga"])
    names = [p["nama"] for p in result]
    assert names == ["Mouse", "Keyboard", "Headset", "Monitor", "Laptop"], f"GAGAL: {names}"
    print(f"✓ Test 1 PASSED: Sort by harga = {names}")
    
    # Test 2: Sort by rating descending
    result = merge_sort_by_key(products.copy(), key=lambda x: x["rating"], reverse=True)
    names = [p["nama"] for p in result]
    assert names[0] == "Mouse", f"GAGAL: rating tertinggi harus Mouse"
    print(f"✓ Test 2 PASSED: Sort by rating DESC = {names}")
    
    # Test 3: Sort by nama ascending
    result = quick_sort_by_key(products.copy(), key=lambda x: x["nama"])
    names = [p["nama"] for p in result]
    assert names == ["Headset", "Keyboard", "Laptop", "Monitor", "Mouse"], f"GAGAL: {names}"
    print(f"✓ Test 3 PASSED: Sort by nama = {names}")
    
    # Test 4: Multi-key sort
    students = [
        {"nama": "Andi", "grade": "B", "nilai": 78},
        {"nama": "Budi", "grade": "A", "nilai": 92},
        {"nama": "Citra", "grade": "B", "nilai": 85},
        {"nama": "Dina", "grade": "A", "nilai": 88},
        {"nama": "Eko", "grade": "C", "nilai": 65},
        {"nama": "Fitri", "grade": "A", "nilai": 90},
    ]
    
    # Sort by grade ascending, then by nama ascending
    result = multi_key_sort(students.copy(), [
        (lambda x: x["grade"], False),
        (lambda x: x["nama"], False),
    ])
    result_info = [(s["grade"], s["nama"]) for s in result]
    expected = [("A", "Budi"), ("A", "Dina"), ("A", "Fitri"),
                ("B", "Andi"), ("B", "Citra"), ("C", "Eko")]
    assert result_info == expected, f"GAGAL: {result_info}"
    print(f"✓ Test 4 PASSED: Multi-key sort = {result_info}")
    
    # Test 5: Sort by grade ascending, then by nilai descending
    result = multi_key_sort(students.copy(), [
        (lambda x: x["grade"], False),
        (lambda x: x["nilai"], True),
    ])
    result_info = [(s["grade"], s["nama"], s["nilai"]) for s in result]
    # A: Budi(92) > Fitri(90) > Dina(88)
    assert result_info[0] == ("A", "Budi", 92), f"GAGAL: {result_info}"
    assert result_info[1] == ("A", "Fitri", 90), f"GAGAL: {result_info}"
    print(f"✓ Test 5 PASSED: Grade ASC, Nilai DESC")
    
    print("\n" + "=" * 60)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 60)
```

---

## Tugas 3: Counting Sort dan Hybrid Sort (40 menit)

### Deskripsi
Implementasikan **Counting Sort** (sorting non-comparison O(n)) dan **Hybrid Sort** yang menggabungkan Quick Sort + Insertion Sort.

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 14.3: Counting Sort dan Hybrid Sort
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

import random
import time


def counting_sort(arr):
    """
    Counting Sort - O(n + k) di mana k = range nilai
    Hanya untuk integer non-negatif
    STABLE sort
    """
    # TODO: Implementasikan
    # 1. Cari nilai max di arr
    # 2. Buat count array ukuran max+1, isi 0
    # 3. Hitung frekuensi setiap elemen
    # 4. Hitung cumulative sum (prefix sum)
    # 5. Bangun output array dari belakang (untuk stability)
    pass


def hybrid_sort(arr, threshold=32):
    """
    Hybrid Sort: Quick Sort + Insertion Sort
    Jika sub-array kecil (len <= threshold), gunakan Insertion Sort
    Ini mirip dengan strategi Timsort dan IntroSort
    """
    # TODO: Implementasikan
    # Jika len(arr) <= threshold → gunakan insertion_sort
    # Jika tidak → gunakan quick_sort dengan random pivot
    pass


def _insertion_sort_range(arr, low, high):
    """Insertion Sort pada range [low, high]"""
    for i in range(low + 1, high + 1):
        key = arr[i]
        j = i - 1
        while j >= low and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key


def _hybrid_sort_helper(arr, low, high, threshold):
    """Helper rekursif untuk hybrid sort"""
    # TODO: Implementasikan
    # Jika high - low + 1 <= threshold → insertion_sort_range
    # Else → partition + rekursi
    pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 60)
    print("TEST COUNTING SORT DAN HYBRID SORT")
    print("=" * 60)
    
    # Test 1: Counting Sort
    arr = [4, 2, 2, 8, 3, 3, 1]
    result = counting_sort(arr.copy())
    assert result == [1, 2, 2, 3, 3, 4, 8], f"GAGAL: {result}"
    print(f"✓ Test 1 PASSED: Counting Sort = {result}")
    
    # Test 2: Counting Sort stability
    data = [(4, 'a'), (2, 'b'), (4, 'c'), (2, 'd'), (1, 'e')]
    # Sort by first element using counting sort idea
    max_val = max(d[0] for d in data)
    count = [0] * (max_val + 1)
    for d in data:
        count[d[0]] += 1
    for i in range(1, len(count)):
        count[i] += count[i-1]
    output = [None] * len(data)
    for d in reversed(data):
        count[d[0]] -= 1
        output[count[d[0]]] = d
    assert output == [(1, 'e'), (2, 'b'), (2, 'd'), (4, 'a'), (4, 'c')], f"GAGAL stability"
    print("✓ Test 2 PASSED: Counting Sort is stable")
    
    # Test 3: Hybrid Sort
    arr = [random.randint(1, 1000) for _ in range(100)]
    result = hybrid_sort(arr.copy())
    assert result == sorted(arr), "GAGAL"
    print("✓ Test 3 PASSED: Hybrid Sort (n=100)")
    
    # Test 4: Hybrid Sort larger
    arr = [random.randint(1, 100000) for _ in range(10000)]
    result = hybrid_sort(arr.copy())
    assert result == sorted(arr), "GAGAL"
    print("✓ Test 4 PASSED: Hybrid Sort (n=10000)")
    
    # Test 5: Perbandingan performa
    print("\n--- Perbandingan Quick Sort vs Hybrid Sort ---")
    print(f"{'n':>7} | {'Quick Sort':>12} | {'Hybrid Sort':>12} | {'Python sort':>12}")
    print("-" * 50)
    
    def quick_sort_basic(arr):
        if len(arr) <= 1:
            return arr
        pivot = arr[len(arr) // 2]
        left = [x for x in arr if x < pivot]
        mid = [x for x in arr if x == pivot]
        right = [x for x in arr if x > pivot]
        return quick_sort_basic(left) + mid + quick_sort_basic(right)
    
    for n in [1000, 5000, 10000, 50000]:
        data = [random.randint(1, n * 10) for _ in range(n)]
        
        start = time.perf_counter()
        quick_sort_basic(data.copy())
        t_quick = time.perf_counter() - start
        
        start = time.perf_counter()
        hybrid_sort(data.copy())
        t_hybrid = time.perf_counter() - start
        
        start = time.perf_counter()
        sorted(data)
        t_python = time.perf_counter() - start
        
        print(f"{n:>7} | {t_quick:>11.4f}s | {t_hybrid:>11.4f}s | {t_python:>11.4f}s")
    
    print("\n" + "=" * 60)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 60)
```

---

# BAGIAN D: BELAJAR MANDIRI (190 Menit)

> 📚 **Bagian ini dikerjakan mahasiswa secara mandiri di luar kelas**
> **Tidak dikumpulkan**, tetapi penting untuk pemahaman materi.

---

## D1. Membaca Referensi (60 menit)

### Bacaan Wajib:
1. **Goodrich et al., Chapter 12.2-12.5** - Merge Sort, Quick Sort, Sorting Lower Bound
2. **Cormen et al. (CLRS), Chapter 6, 7, 8** - Heapsort, Quicksort, Sorting in Linear Time

### Bacaan Tambahan:
- [Visualgo - Sorting](https://visualgo.net/en/sorting)
- [GeeksforGeeks - Merge Sort](https://www.geeksforgeeks.org/merge-sort/)
- [GeeksforGeeks - Quick Sort](https://www.geeksforgeeks.org/quick-sort/)
- [GeeksforGeeks - Heap Sort](https://www.geeksforgeeks.org/heap-sort/)

---

## D2. Video Tutorial (40 menit)

Tonton dan buat catatan:

1. **Merge Sort - CS50** (~13 menit)
   - https://www.youtube.com/watch?v=Ns7tGNbtvV4

2. **Quick Sort - mycodeschool** (~13 menit)
   - https://www.youtube.com/watch?v=COk73cpQbFQ

3. **Heap Sort - Abdul Bari** (~14 menit)
   - https://www.youtube.com/watch?v=HqPJF2L5h9U

---

## D3. Latihan Mandiri (60 menit)

### Soal Pilihan Ganda

**1.** Prinsip Divide and Conquer terdiri dari langkah...
- [ ] a. Split, Process, Join
- [ ] b. Divide, Conquer, Combine
- [ ] c. Input, Process, Output
- [ ] d. Plan, Execute, Review

**2.** Merge Sort memiliki worst case...
- [ ] a. O(n)
- [ ] b. O(n log n)
- [ ] c. O(n²)
- [ ] d. O(log n)

**3.** Quick Sort worst case O(n²) terjadi ketika...
- [ ] a. Data acak
- [ ] b. Pivot selalu elemen terbesar/terkecil
- [ ] c. Data memiliki duplikat
- [ ] d. Array sangat besar

**4.** Algoritma sorting lanjutan yang membutuhkan O(n) extra space adalah...
- [ ] a. Quick Sort
- [ ] b. Heap Sort
- [ ] c. Merge Sort
- [ ] d. Insertion Sort

**5.** Heap Sort menggunakan struktur data...
- [ ] a. Stack
- [ ] b. Queue
- [ ] c. Binary Heap (Max Heap)
- [ ] d. Binary Search Tree

### Latihan Coding (Opsional)

Kerjakan di platform online:
- **LeetCode Easy #912** - Sort an Array
- **LeetCode Medium #148** - Sort List (Merge Sort pada Linked List)
- **LeetCode Medium #215** - Kth Largest Element (Quick Select / Heap)
- **LeetCode Medium #75** - Sort Colors (Dutch National Flag = 3-way partition)
- **LeetCode Hard #23** - Merge k Sorted Lists

---

## D4. Persiapan Pertemuan Berikutnya (30 menit)

Baca materi tentang **Struktur Data untuk Big Data & AI**:
- Apa itu Trie dan bagaimana cara kerjanya?
- Apa itu Tensor dan hubungannya dengan AI/Machine Learning?
- Review semua materi untuk persiapan UAS

---

**Selamat Belajar! 🚀**

*Modul ini disusun oleh Aidil Saputra Kirsan (myst-tech.com), Institut Teknologi Kalimantan.*