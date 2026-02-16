# MODUL 5: STACK

---

**Mata Kuliah:** Struktur Data  
**Program Studi:** Sistem Informasi - Institut Teknologi Kalimantan  
**SKS:** 3 (2 Teori + 1 Praktikum)  
**Pertemuan:** 5 dari 16

---


# BAGIAN B: PRAKTIKUM DI LAB (100 Menit)

## Tujuan Praktikum
Mengimplementasikan Stack dengan Array dan Linked List, serta aplikasinya.

> ⚠️ **Catatan:** Kode yang dibuat di praktikum ini akan **dikembangkan lebih lanjut** di Tugas Terstruktur.

---

## Praktikum 5.1: Implementasi Stack dengan Array (35 menit)

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 5.1: Implementasi Stack dengan Array
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
1. Implementasikan class ArrayStack
2. Jalankan test cases untuk memastikan implementasi benar
3. SIMPAN FILE INI - akan dikembangkan di Tugas Terstruktur
============================================================
"""

class ArrayStack:
    """Stack menggunakan Array dengan kapasitas tetap"""
    
    def __init__(self, capacity=10):
        """
        Inisialisasi stack dengan kapasitas tertentu
        Parameter:
            capacity: ukuran maksimum stack
        """
        # TODO: Implementasikan
        # self.capacity = ???
        # self.items = ???
        # self.top = ???  # -1 berarti kosong
        pass
    
    def is_empty(self):
        """
        Cek apakah stack kosong
        Return: True jika kosong
        """
        # TODO: Implementasikan
        pass
    
    def is_full(self):
        """
        Cek apakah stack penuh
        Return: True jika penuh
        """
        # TODO: Implementasikan
        pass
    
    def push(self, item):
        """
        Menambah elemen ke atas stack
        Kompleksitas: O(1)
        Raise: OverflowError jika stack penuh
        """
        # TODO: Implementasikan berdasarkan flowchart PUSH
        pass
    
    def pop(self):
        """
        Menghapus dan mengembalikan elemen teratas
        Kompleksitas: O(1)
        Raise: IndexError jika stack kosong
        """
        # TODO: Implementasikan berdasarkan flowchart POP
        pass
    
    def peek(self):
        """
        Melihat elemen teratas tanpa menghapus
        Kompleksitas: O(1)
        Raise: IndexError jika stack kosong
        """
        # TODO: Implementasikan berdasarkan flowchart PEEK
        pass
    
    def size(self):
        """Mengembalikan jumlah elemen dalam stack"""
        # TODO: Implementasikan
        pass
    
    def display(self):
        """
        Menampilkan isi stack
        Format: "Stack (top -> bottom): [top_elem, ..., bottom_elem]"
        """
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST ARRAY STACK")
    print("=" * 50)
    
    stack = ArrayStack(5)
    
    # Test 1: Initial state
    assert stack.is_empty() == True, "GAGAL: Stack baru harus kosong"
    assert stack.size() == 0, "GAGAL: Size harus 0"
    print("✓ Test 1 PASSED: Inisialisasi")
    
    # Test 2: Push
    stack.push(10)
    stack.push(20)
    stack.push(30)
    assert stack.size() == 3, "GAGAL: Size harus 3"
    assert stack.is_empty() == False, "GAGAL: Stack tidak kosong"
    stack.display()  # Stack (top -> bottom): [30, 20, 10]
    print("✓ Test 2 PASSED: Push")
    
    # Test 3: Peek
    assert stack.peek() == 30, "GAGAL: Peek harus 30"
    assert stack.size() == 3, "GAGAL: Peek tidak boleh menghapus"
    print("✓ Test 3 PASSED: Peek")
    
    # Test 4: Pop
    assert stack.pop() == 30, "GAGAL: Pop harus 30"
    assert stack.pop() == 20, "GAGAL: Pop harus 20"
    assert stack.size() == 1, "GAGAL: Size harus 1"
    print("✓ Test 4 PASSED: Pop")
    
    # Test 5: Stack overflow
    stack.push(40)
    stack.push(50)
    stack.push(60)
    stack.push(70)  # Stack penuh (capacity 5)
    try:
        stack.push(80)  # Harus error
        assert False, "GAGAL: Harus raise OverflowError"
    except OverflowError:
        print("✓ Test 5 PASSED: Overflow handled")
    
    # Test 6: Stack underflow
    while not stack.is_empty():
        stack.pop()
    try:
        stack.pop()  # Harus error
        assert False, "GAGAL: Harus raise IndexError"
    except IndexError:
        print("✓ Test 6 PASSED: Underflow handled")
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Praktikum 5.2: Implementasi Stack dengan Linked List (35 menit)

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 5.2: Implementasi Stack dengan Linked List
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
Implementasikan Stack menggunakan Linked List (tanpa batasan kapasitas)
============================================================
"""

class Node:
    """Node untuk Linked List"""
    def __init__(self, data):
        self.data = data
        self.next = None


class LinkedStack:
    """Stack menggunakan Linked List (dinamis)"""
    
    def __init__(self):
        """Inisialisasi stack kosong"""
        # TODO: Implementasikan
        # self.top = ???  # Pointer ke node teratas
        # self._size = ???
        pass
    
    def is_empty(self):
        """Cek apakah stack kosong"""
        # TODO: Implementasikan
        pass
    
    def push(self, item):
        """
        Menambah elemen ke atas stack
        Kompleksitas: O(1)
        """
        # TODO: Implementasikan
        # Hint: Insert di awal linked list
        pass
    
    def pop(self):
        """
        Menghapus dan mengembalikan elemen teratas
        Kompleksitas: O(1)
        """
        # TODO: Implementasikan
        # Hint: Delete di awal linked list
        pass
    
    def peek(self):
        """Melihat elemen teratas tanpa menghapus"""
        # TODO: Implementasikan
        pass
    
    def size(self):
        """Mengembalikan jumlah elemen"""
        # TODO: Implementasikan
        pass
    
    def display(self):
        """Menampilkan isi stack"""
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST LINKED STACK")
    print("=" * 50)
    
    stack = LinkedStack()
    
    # Test 1: Initial state
    assert stack.is_empty() == True, "GAGAL: Stack baru harus kosong"
    print("✓ Test 1 PASSED: Inisialisasi")
    
    # Test 2: Push
    stack.push(10)
    stack.push(20)
    stack.push(30)
    assert stack.size() == 3, "GAGAL: Size harus 3"
    stack.display()
    print("✓ Test 2 PASSED: Push")
    
    # Test 3: Peek
    assert stack.peek() == 30, "GAGAL: Peek harus 30"
    print("✓ Test 3 PASSED: Peek")
    
    # Test 4: Pop
    assert stack.pop() == 30, "GAGAL: Pop harus 30"
    assert stack.pop() == 20, "GAGAL: Pop harus 20"
    assert stack.size() == 1, "GAGAL: Size harus 1"
    print("✓ Test 4 PASSED: Pop")
    
    # Test 5: No overflow (dinamis)
    for i in range(100):
        stack.push(i)
    assert stack.size() == 101, "GAGAL: Linked stack tidak ada overflow"
    print("✓ Test 5 PASSED: No overflow (dinamis)")
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Praktikum 5.3: Aplikasi Balanced Parentheses (30 menit)

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 5.3: Aplikasi Stack - Balanced Parentheses
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
Implementasikan fungsi untuk mengecek balanced parentheses
============================================================
"""

# Gunakan class Stack dari praktikum sebelumnya atau Python list

def is_balanced(expression):
    """
    Mengecek apakah tanda kurung dalam expression seimbang
    
    Parameter:
        expression: string yang berisi tanda kurung
    
    Return:
        True jika seimbang, False jika tidak
    
    Contoh:
        is_balanced("()") -> True
        is_balanced("([{}])") -> True
        is_balanced("(]") -> False
        is_balanced("([)]") -> False
    """
    # TODO: Implementasikan berdasarkan flowchart
    pass


def check_balance_detailed(expression):
    """
    Mengecek balance dengan detail error
    
    Return:
        tuple (is_balanced, message)
    """
    # TODO: Implementasikan
    # Return pesan error yang informatif:
    # - "Valid: All parentheses are balanced"
    # - "Invalid: Missing closing bracket for '(' at position X"
    # - "Invalid: Extra closing bracket ')' at position X"
    # - "Invalid: Mismatched bracket ')' at position X, expected ']'"
    pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST BALANCED PARENTHESES")
    print("=" * 50)
    
    # Test cases valid
    valid_cases = [
        "()",
        "[]",
        "{}",
        "([])",
        "([{}])",
        "{[()]}",
        "((()))",
        "()[]{}",
        "({[]})",
        ""  # Empty string is valid
    ]
    
    print("Testing VALID cases:")
    for expr in valid_cases:
        result = is_balanced(expr)
        status = "✓" if result == True else "✗"
        print(f"  {status} is_balanced('{expr}') = {result}")
        assert result == True, f"GAGAL: '{expr}' harus True"
    
    # Test cases invalid
    invalid_cases = [
        "(",
        ")",
        "(]",
        "([)]",
        "{{}",
        "(()",
        "())",
        "[(])",
        "{[(})]"
    ]
    
    print("\nTesting INVALID cases:")
    for expr in invalid_cases:
        result = is_balanced(expr)
        status = "✓" if result == False else "✗"
        print(f"  {status} is_balanced('{expr}') = {result}")
        assert result == False, f"GAGAL: '{expr}' harus False"
    
    # Test detailed messages
    print("\nTesting DETAILED messages:")
    test_detail = [
        "([{}])",
        "((",
        "())",
        "(]"
    ]
    for expr in test_detail:
        balanced, msg = check_balance_detailed(expr)
        print(f"  '{expr}': {msg}")
    
    print("=" * 50)
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
| **Deadline** | Pertemuan 6 (sebelum kuliah dimulai) |
| **Format** | File Python (.py) |
| **Nama File** | `Tugas5_NIM_Nama.py` |
| **Pengumpulan** | Upload ke github |

---

## Tugas 1: Pengembangan Stack dengan Method Baru (30 menit)

### Deskripsi
Kembangkan class `ArrayStack` atau `LinkedStack` dengan method baru:

| Method Baru | Deskripsi |
|-------------|-----------|
| `get_min()` | Mendapatkan nilai minimum dalam stack |
| `get_max()` | Mendapatkan nilai maksimum dalam stack |
| `clear()` | Menghapus semua elemen |
| `to_list()` | Konversi stack ke Python list |
| `copy()` | Membuat salinan stack |

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 1: Pengembangan Stack
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

class Stack:
    # ========== METHOD DARI PRAKTIKUM (COPY) ==========
    def __init__(self):
        self.items = []
    
    def is_empty(self):
        return len(self.items) == 0
    
    def push(self, item):
        self.items.append(item)
    
    def pop(self):
        if self.is_empty():
            raise IndexError("Stack Underflow")
        return self.items.pop()
    
    def peek(self):
        if self.is_empty():
            raise IndexError("Stack Empty")
        return self.items[-1]
    
    def size(self):
        return len(self.items)
    
    # ========== METHOD BARU (TUGAS) ==========
    def get_min(self):
        """
        Mendapatkan nilai minimum dalam stack
        Kompleksitas: O(n)
        Raise: ValueError jika stack kosong
        """
        # TODO: Implementasikan
        pass
    
    def get_max(self):
        """
        Mendapatkan nilai maksimum dalam stack
        Kompleksitas: O(n)
        """
        # TODO: Implementasikan
        pass
    
    def clear(self):
        """Menghapus semua elemen"""
        # TODO: Implementasikan
        pass
    
    def to_list(self):
        """
        Konversi ke Python list (bottom to top)
        Return: list dengan elemen dari bottom ke top
        """
        # TODO: Implementasikan
        pass
    
    def copy(self):
        """
        Membuat salinan stack baru
        Return: Stack baru dengan elemen yang sama
        """
        # TODO: Implementasikan
        pass
    
    def reverse(self):
        """
        Membalik urutan elemen dalam stack
        Hint: Bisa gunakan auxiliary stack atau rekursi
        """
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST PENGEMBANGAN STACK")
    print("=" * 50)
    
    stack = Stack()
    for val in [30, 10, 50, 20, 40]:
        stack.push(val)
    
    # Test get_min, get_max
    assert stack.get_min() == 10, "GAGAL: get_min"
    assert stack.get_max() == 50, "GAGAL: get_max"
    print("✓ Test get_min/max PASSED")
    
    # Test to_list
    assert stack.to_list() == [30, 10, 50, 20, 40], "GAGAL: to_list"
    print("✓ Test to_list PASSED")
    
    # Test copy
    stack_copy = stack.copy()
    assert stack_copy.to_list() == stack.to_list(), "GAGAL: copy"
    stack_copy.pop()
    assert stack.size() == 5, "GAGAL: copy harus independent"
    print("✓ Test copy PASSED")
    
    # Test reverse
    stack.reverse()
    assert stack.to_list() == [40, 20, 50, 10, 30], "GAGAL: reverse"
    print("✓ Test reverse PASSED")
    
    # Test clear
    stack.clear()
    assert stack.is_empty() == True, "GAGAL: clear"
    print("✓ Test clear PASSED")
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Tugas 2: Konversi dan Evaluasi Ekspresi (45 menit)

### Deskripsi
Implementasikan konversi Infix ke Postfix dan evaluasi ekspresi Postfix.

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 2: Konversi dan Evaluasi Ekspresi
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

def get_precedence(operator):
    """Mengembalikan prioritas operator"""
    precedence = {'+': 1, '-': 1, '*': 2, '/': 2, '^': 3}
    return precedence.get(operator, 0)


def is_operator(char):
    """Cek apakah karakter adalah operator"""
    return char in ['+', '-', '*', '/', '^']


def infix_to_postfix(expression):
    """
    Konversi ekspresi infix ke postfix
    
    Parameter:
        expression: string ekspresi infix (dengan spasi)
                   contoh: "A + B * C"
    
    Return:
        string ekspresi postfix
        contoh: "A B C * +"
    """
    # TODO: Implementasikan berdasarkan flowchart
    pass


def evaluate_postfix(expression):
    """
    Mengevaluasi ekspresi postfix
    
    Parameter:
        expression: string ekspresi postfix (dengan spasi)
                   contoh: "3 4 + 2 *"
    
    Return:
        hasil evaluasi (number)
        contoh: 14
    """
    # TODO: Implementasikan berdasarkan flowchart
    pass


def calculate(infix_expression):
    """
    Menghitung hasil ekspresi infix
    
    Langkah:
    1. Konversi infix ke postfix
    2. Evaluasi postfix
    
    Parameter:
        infix_expression: string ekspresi infix
    
    Return:
        hasil perhitungan
    """
    # TODO: Implementasikan
    pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST KONVERSI DAN EVALUASI EKSPRESI")
    print("=" * 50)
    
    # Test infix to postfix
    test_cases_convert = [
        ("A + B", "A B +"),
        ("A + B * C", "A B C * +"),
        ("( A + B ) * C", "A B + C *"),
        ("A + B * C - D", "A B C * + D -"),
        ("( A + B ) * ( C - D )", "A B + C D - *"),
        ("A ^ B ^ C", "A B C ^ ^"),  # Right associative
    ]
    
    print("Testing Infix to Postfix:")
    for infix, expected in test_cases_convert:
        result = infix_to_postfix(infix)
        status = "✓" if result == expected else "✗"
        print(f"  {status} '{infix}' -> '{result}' (expected: '{expected}')")
    
    # Test evaluate postfix
    test_cases_eval = [
        ("3 4 +", 7),
        ("3 4 + 2 *", 14),
        ("5 1 2 + 4 * + 3 -", 14),
        ("2 3 ^", 8),
        ("10 2 /", 5),
    ]
    
    print("\nTesting Evaluate Postfix:")
    for postfix, expected in test_cases_eval:
        result = evaluate_postfix(postfix)
        status = "✓" if result == expected else "✗"
        print(f"  {status} '{postfix}' = {result} (expected: {expected})")
    
    # Test full calculation
    test_cases_calc = [
        ("3 + 4", 7),
        ("3 + 4 * 2", 11),
        ("( 3 + 4 ) * 2", 14),
        ("10 / 2 + 3", 8),
        ("2 ^ 3", 8),
    ]
    
    print("\nTesting Full Calculation:")
    for infix, expected in test_cases_calc:
        result = calculate(infix)
        status = "✓" if result == expected else "✗"
        print(f"  {status} '{infix}' = {result} (expected: {expected})")
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Tugas 3: Aplikasi Stack - Browser History (45 menit)

### Deskripsi
Buat simulasi **Browser History** dengan fitur Back, Forward, dan Visit.

```mermaid
flowchart LR
    subgraph BackStack [Back Stack]
        B1[Page 1]
        B2[Page 2]
    end
    
    subgraph Current [Current Page]
        C[Page 3]
    end
    
    subgraph ForwardStack [Forward Stack]
        F1[Page 4]
    end
    
    BACK[← Back] -.-> BackStack
    FORWARD[Forward →] -.-> ForwardStack
```

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 3: Aplikasi Stack - Browser History
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

class BrowserHistory:
    """
    Simulasi Browser History menggunakan 2 Stack
    - back_stack: menyimpan halaman sebelumnya
    - forward_stack: menyimpan halaman yang di-back
    """
    
    def __init__(self, homepage="about:blank"):
        """
        Inisialisasi browser dengan homepage
        """
        # TODO: Implementasikan
        # self.back_stack = ???
        # self.forward_stack = ???
        # self.current_page = ???
        pass
    
    def visit(self, url):
        """
        Mengunjungi halaman baru
        - Push current page ke back_stack
        - Set current page ke url baru
        - Clear forward_stack (karena history baru)
        """
        # TODO: Implementasikan
        pass
    
    def back(self):
        """
        Kembali ke halaman sebelumnya
        Return: url halaman sebelumnya, atau None jika tidak bisa
        """
        # TODO: Implementasikan
        pass
    
    def forward(self):
        """
        Maju ke halaman berikutnya (setelah back)
        Return: url halaman berikutnya, atau None jika tidak bisa
        """
        # TODO: Implementasikan
        pass
    
    def current(self):
        """Return halaman saat ini"""
        # TODO: Implementasikan
        pass
    
    def can_go_back(self):
        """Cek apakah bisa back"""
        # TODO: Implementasikan
        pass
    
    def can_go_forward(self):
        """Cek apakah bisa forward"""
        # TODO: Implementasikan
        pass
    
    def history(self):
        """
        Menampilkan history lengkap
        Format:
        Back Stack: [page1, page2]
        Current: page3
        Forward Stack: [page4]
        """
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST BROWSER HISTORY")
    print("=" * 50)
    
    browser = BrowserHistory("google.com")
    
    # Test initial state
    assert browser.current() == "google.com", "GAGAL: Homepage"
    assert browser.can_go_back() == False, "GAGAL: Can't go back initially"
    print("✓ Test initial state PASSED")
    
    # Test visit
    browser.visit("youtube.com")
    browser.visit("github.com")
    browser.visit("stackoverflow.com")
    assert browser.current() == "stackoverflow.com", "GAGAL: Visit"
    print("✓ Test visit PASSED")
    
    browser.history()
    
    # Test back
    assert browser.can_go_back() == True, "GAGAL: Can go back"
    browser.back()
    assert browser.current() == "github.com", "GAGAL: Back 1"
    browser.back()
    assert browser.current() == "youtube.com", "GAGAL: Back 2"
    print("✓ Test back PASSED")
    
    # Test forward
    assert browser.can_go_forward() == True, "GAGAL: Can go forward"
    browser.forward()
    assert browser.current() == "github.com", "GAGAL: Forward"
    print("✓ Test forward PASSED")
    
    browser.history()
    
    # Test visit clears forward stack
    browser.visit("twitter.com")
    assert browser.can_go_forward() == False, "GAGAL: Forward cleared"
    assert browser.current() == "twitter.com", "GAGAL: New visit"
    print("✓ Test visit clears forward PASSED")
    
    browser.history()
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

# BAGIAN D: BELAJAR MANDIRI (190 Menit)

> 📚 **Bagian ini dikerjakan mahasiswa secara mandiri di luar kelas**
> **Tidak dikumpulkan**, tetapi penting untuk pemahaman materi.

---

## D1. Membaca Referensi (60 menit)

### Bacaan Wajib:
1. **Goodrich et al., Chapter 6.1** - Stacks
2. **GeeksforGeeks** - [Stack Data Structure](https://www.geeksforgeeks.org/stack-data-structure/)

### Bacaan Tambahan:
- [Visualgo - Stack](https://visualgo.net/en/list)
- Infix, Prefix, Postfix expressions
- Call Stack in Programming

---

## D2. Video Tutorial (40 menit)

Tonton dan buat catatan:

1. **Stack Data Structure** (~15 menit)
   - https://www.youtube.com/watch?v=F1F2imiOJfk
   
2. **Infix to Postfix using Stack** (~15 menit)
   - https://www.youtube.com/watch?v=vq-nUF0G4fI

3. **Balanced Parentheses** (~10 menit)
   - https://www.youtube.com/watch?v=WTzjTskDFMg

---

## D3. Latihan Mandiri (60 menit)

### Soal Pilihan Ganda

**1.** Stack menggunakan prinsip...
- [ ] a. FIFO (First In First Out)
- [ ] b. LIFO (Last In First Out)
- [ ] c. Random Access
- [ ] d. Priority Based

**2.** Kompleksitas waktu operasi push pada Stack adalah...
- [ ] a. O(1)
- [ ] b. O(n)
- [ ] c. O(log n)
- [ ] d. O(n²)

**3.** Jika stack berisi [10, 20, 30] dengan 30 di top, setelah pop() dan push(40), isi stack adalah...
- [ ] a. [10, 20, 40]
- [ ] b. [10, 20, 30, 40]
- [ ] c. [40, 10, 20]
- [ ] d. [10, 40]

**4.** Aplikasi Stack yang BUKAN tepat adalah...
- [ ] a. Undo operation
- [ ] b. Balanced parentheses checking
- [ ] c. BFS (Breadth First Search)
- [ ] d. Function call management

**5.** Ekspresi infix `A + B * C` dalam postfix adalah...
- [ ] a. `A B + C *`
- [ ] b. `A B C * +`
- [ ] c. `+ A * B C`
- [ ] d. `A B C + *`

### Latihan Coding (Opsional)

Kerjakan di platform online:
- **LeetCode Easy #20** - Valid Parentheses
- **LeetCode Easy #155** - Min Stack
- **LeetCode Medium #150** - Evaluate Reverse Polish Notation

---

## D4. Persiapan Pertemuan Berikutnya (30 menit)

Baca materi tentang **Queue**:
- Apa itu Queue dan prinsip FIFO?
- Operasi dasar Queue (enqueue, dequeue)
- Circular Queue dan Priority Queue
- Aplikasi Queue dalam kehidupan nyata

---



**Selamat Belajar! 🚀**

*Modul ini disusun oleh Aidil Saputra Kirsan (myst-tech.com), Institut Teknologi Kalimantan.*
