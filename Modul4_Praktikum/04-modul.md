# MODUL 4: DOUBLE & CIRCULAR LINKED LIST

---

**Mata Kuliah:** Struktur Data  
**Program Studi:** Sistem Informasi - Institut Teknologi Kalimantan  
**SKS:** 3 (2 Teori + 1 Praktikum)  
**Pertemuan:** 4 dari 16

---


# BAGIAN B: PRAKTIKUM DI LAB (100 Menit)

## Tujuan Praktikum
Mengimplementasikan Double Linked List dan Circular Linked List berdasarkan flowchart.

> ⚠️ **Catatan:** Kode yang dibuat di praktikum ini akan **dikembangkan lebih lanjut** di Tugas Terstruktur.

---

## Praktikum 4.1: Implementasi Double Linked List (50 menit)

### Spesifikasi ADT Double Linked List

```
ADT DoubleLinkedList:
    Data: 
        - head (pointer ke node pertama)
        - tail (pointer ke node terakhir)
    
    Operasi Dasar:
        - insert_at_beginning(data)
        - insert_at_end(data)
        - delete_at_beginning()
        - delete_at_end()
        - display()
        - display_reverse()
        - size()
        - is_empty()
```

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 4.1: Implementasi Double Linked List
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
1. Implementasikan class DNode dan DoublyLinkedList
2. Implementasikan setiap method berdasarkan flowchart
3. Jalankan test cases untuk memastikan implementasi benar
4. SIMPAN FILE INI - akan dikembangkan di Tugas Terstruktur
============================================================
"""

class DNode:
    """Class untuk node Double Linked List"""
    
    def __init__(self, data):
        """
        Inisialisasi node dengan data
        Parameter:
            data: nilai yang disimpan
        """
        # TODO: Implementasikan
        # self.data = ???
        # self.prev = ???
        # self.next = ???
        pass


class DoublyLinkedList:
    """Class untuk Double Linked List"""
    
    def __init__(self):
        """Inisialisasi DLL kosong dengan head dan tail"""
        # TODO: Implementasikan
        # self.head = ???
        # self.tail = ???
        pass
    
    def is_empty(self):
        """Cek apakah list kosong"""
        # TODO: Implementasikan
        pass
    
    def insert_at_beginning(self, data):
        """
        Insert node di awal DLL
        Kompleksitas: O(1)
        """
        # TODO: Implementasikan berdasarkan flowchart
        pass
    
    def insert_at_end(self, data):
        """
        Insert node di akhir DLL
        Kompleksitas: O(1) - karena ada tail
        """
        # TODO: Implementasikan berdasarkan flowchart
        pass
    
    def delete_at_beginning(self):
        """
        Delete node di awal DLL
        Kompleksitas: O(1)
        Return: data yang dihapus
        """
        # TODO: Implementasikan berdasarkan flowchart
        pass
    
    def delete_at_end(self):
        """
        Delete node di akhir DLL
        Kompleksitas: O(1) - karena ada tail
        Return: data yang dihapus
        """
        # TODO: Implementasikan berdasarkan flowchart
        pass
    
    def display(self):
        """
        Menampilkan DLL dari depan ke belakang
        Format: "DLL: 10 <-> 20 <-> 30 <-> NULL"
        """
        # TODO: Implementasikan
        pass
    
    def display_reverse(self):
        """
        Menampilkan DLL dari belakang ke depan
        Format: "DLL (reverse): 30 <-> 20 <-> 10 <-> NULL"
        """
        # TODO: Implementasikan berdasarkan flowchart TRAVERSE MUNDUR
        pass
    
    def size(self):
        """Menghitung jumlah node"""
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST DOUBLE LINKED LIST")
    print("=" * 50)
    
    dll = DoublyLinkedList()
    
    # Test 1: Initial state
    assert dll.is_empty() == True, "GAGAL: List baru harus kosong"
    print("✓ Test 1 PASSED: Inisialisasi")
    
    # Test 2: Insert at end
    dll.insert_at_end(10)
    dll.insert_at_end(20)
    dll.insert_at_end(30)
    dll.display()  # Expected: DLL: 10 <-> 20 <-> 30 <-> NULL
    assert dll.size() == 3, "GAGAL: Size harus 3"
    print("✓ Test 2 PASSED: Insert at end")
    
    # Test 3: Insert at beginning
    dll.insert_at_beginning(5)
    dll.display()  # Expected: DLL: 5 <-> 10 <-> 20 <-> 30 <-> NULL
    assert dll.size() == 4, "GAGAL: Size harus 4"
    print("✓ Test 3 PASSED: Insert at beginning")
    
    # Test 4: Display reverse
    dll.display_reverse()  # Expected: DLL (reverse): 30 <-> 20 <-> 10 <-> 5 <-> NULL
    print("✓ Test 4 PASSED: Display reverse")
    
    # Test 5: Delete at beginning
    deleted = dll.delete_at_beginning()
    assert deleted == 5, "GAGAL: Yang dihapus harus 5"
    dll.display()  # Expected: DLL: 10 <-> 20 <-> 30 <-> NULL
    print("✓ Test 5 PASSED: Delete at beginning")
    
    # Test 6: Delete at end
    deleted = dll.delete_at_end()
    assert deleted == 30, "GAGAL: Yang dihapus harus 30"
    dll.display()  # Expected: DLL: 10 <-> 20 <-> NULL
    print("✓ Test 6 PASSED: Delete at end")
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Praktikum 4.2: Implementasi Circular Linked List (30 menit)

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 4.2: Implementasi Single Circular Linked List
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
Implementasikan Single Circular Linked List
============================================================
"""

class Node:
    """Class untuk node (sama seperti SLL)"""
    
    def __init__(self, data):
        self.data = data
        self.next = None


class CircularLinkedList:
    """Class untuk Single Circular Linked List"""
    
    def __init__(self):
        """Inisialisasi CLL kosong"""
        # TODO: Implementasikan
        pass
    
    def is_empty(self):
        """Cek apakah list kosong"""
        # TODO: Implementasikan
        pass
    
    def insert_at_beginning(self, data):
        """
        Insert di awal CLL
        Kompleksitas: O(n) - perlu cari node terakhir
        """
        # TODO: Implementasikan
        # Hint: 
        # 1. Jika kosong: new_node.next = new_node, head = new_node
        # 2. Jika tidak: cari last, new_node.next = head, last.next = new_node, head = new_node
        pass
    
    def insert_at_end(self, data):
        """
        Insert di akhir CLL
        Kompleksitas: O(n) - perlu cari node terakhir
        """
        # TODO: Implementasikan berdasarkan flowchart
        pass
    
    def delete_at_beginning(self):
        """
        Delete di awal CLL
        Kompleksitas: O(n) - perlu update last.next
        Return: data yang dihapus
        """
        # TODO: Implementasikan berdasarkan flowchart
        pass
    
    def display(self):
        """
        Menampilkan CLL
        Format: "CLL: 10 -> 20 -> 30 -> (head)"
        """
        # TODO: Implementasikan berdasarkan flowchart TRAVERSE CLL
        pass
    
    def size(self):
        """Menghitung jumlah node"""
        # TODO: Implementasikan
        # Hint: Hati-hati kondisi berhenti!
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST CIRCULAR LINKED LIST")
    print("=" * 50)
    
    cll = CircularLinkedList()
    
    # Test 1: Initial state
    assert cll.is_empty() == True, "GAGAL: List baru harus kosong"
    print("✓ Test 1 PASSED: Inisialisasi")
    
    # Test 2: Insert at end
    cll.insert_at_end(10)
    cll.insert_at_end(20)
    cll.insert_at_end(30)
    cll.display()  # Expected: CLL: 10 -> 20 -> 30 -> (head)
    assert cll.size() == 3, "GAGAL: Size harus 3"
    print("✓ Test 2 PASSED: Insert at end")
    
    # Test 3: Insert at beginning
    cll.insert_at_beginning(5)
    cll.display()  # Expected: CLL: 5 -> 10 -> 20 -> 30 -> (head)
    assert cll.size() == 4, "GAGAL: Size harus 4"
    print("✓ Test 3 PASSED: Insert at beginning")
    
    # Test 4: Delete at beginning
    deleted = cll.delete_at_beginning()
    assert deleted == 5, "GAGAL: Yang dihapus harus 5"
    cll.display()  # Expected: CLL: 10 -> 20 -> 30 -> (head)
    print("✓ Test 4 PASSED: Delete at beginning")
    
    # Test 5: Verify circular property
    # Traverse 2 kali putaran untuk memastikan circular
    print("✓ Test 5 PASSED: Circular property verified")
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Praktikum 4.3: Insert dan Delete di Posisi (20 menit)

### Kode Praktikum

```python
"""
============================================================
PRAKTIKUM 4.3: Insert dan Delete di Posisi (DLL)
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________

Instruksi: 
Tambahkan method untuk insert dan delete di posisi tertentu pada DLL
============================================================
"""

# COPY class DNode dan DoublyLinkedList dari Praktikum 4.1

class DoublyLinkedList:
    # ... (copy dari praktikum 4.1) ...
    
    def insert_at_position(self, data, position):
        """
        Insert di posisi tertentu
        Kompleksitas: O(n)
        """
        # TODO: Implementasikan
        # Hint: Perlu update 4 pointer (prev dan next dari node baru dan tetangga)
        pass
    
    def delete_at_position(self, position):
        """
        Delete di posisi tertentu
        Kompleksitas: O(n)
        Return: data yang dihapus
        """
        # TODO: Implementasikan
        pass
    
    def get(self, position):
        """
        Mengambil data di posisi tertentu
        Kompleksitas: O(n)
        """
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST INSERT DAN DELETE DI POSISI (DLL)")
    print("=" * 50)
    
    dll = DoublyLinkedList()
    dll.insert_at_end(10)
    dll.insert_at_end(20)
    dll.insert_at_end(30)
    dll.insert_at_end(40)
    dll.display()  # DLL: 10 <-> 20 <-> 30 <-> 40 <-> NULL
    
    # Test insert_at_position
    dll.insert_at_position(25, 2)
    dll.display()  # Expected: DLL: 10 <-> 20 <-> 25 <-> 30 <-> 40 <-> NULL
    assert dll.get(2) == 25, "GAGAL: Position 2 harus 25"
    print("✓ Test insert_at_position PASSED")
    
    # Test delete_at_position
    deleted = dll.delete_at_position(2)
    assert deleted == 25, "GAGAL: Yang dihapus harus 25"
    dll.display()  # Expected: DLL: 10 <-> 20 <-> 30 <-> 40 <-> NULL
    print("✓ Test delete_at_position PASSED")
    
    # Test get
    assert dll.get(0) == 10, "GAGAL: get(0)"
    assert dll.get(2) == 30, "GAGAL: get(2)"
    print("✓ Test get PASSED")
    
    # Verify reverse still works
    dll.display_reverse()
    
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
| **Deadline** | Pertemuan 5 (sebelum kuliah dimulai) |
| **Format** | File Python (.py) |
| **Nama File** | `Tugas4_NIM_Nama.py` |
| **Pengumpulan** | Upload ke github |

---

## Tugas 1: Pengembangan Double Linked List (40 menit)

### Deskripsi
Kembangkan class `DoublyLinkedList` dengan menambahkan method baru:

| Method Baru | Deskripsi | Kompleksitas |
|-------------|-----------|--------------|
| `reverse()` | Membalik urutan DLL | O(n) |
| `find_min()` | Mencari nilai minimum | O(n) |
| `find_max()` | Mencari nilai maksimum | O(n) |
| `swap_nodes(pos1, pos2)` | Menukar data dua node | O(n) |
| `is_palindrome()` | Cek apakah DLL palindrome | O(n) |

### Flowchart REVERSE DLL

```mermaid
flowchart TD
    START([🟢 START]) --> CHECK{HEAD == NULL?}
    CHECK -->|Ya| END([🔴 END])
    CHECK -->|Tidak| INIT[current = HEAD]
    INIT --> LOOP{current != NULL?}
    LOOP -->|Tidak| SWAP[Tukar HEAD dan TAIL]
    LOOP -->|Ya| SAVE[temp = current.prev]
    SAVE --> SWAP_PTR[current.prev = current.next<br/>current.next = temp]
    SWAP_PTR --> MOVE[current = current.prev<br/>karena pointer sudah ditukar]
    MOVE --> LOOP
    SWAP --> END
    
    style START fill:#70AD47,color:#fff
    style END fill:#C00000,color:#fff
    style CHECK fill:#FFC000
    style LOOP fill:#FFC000
```

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 1: Pengembangan Double Linked List
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

class DNode:
    def __init__(self, data):
        self.data = data
        self.prev = None
        self.next = None


class DoublyLinkedList:
    # ========== METHOD DARI PRAKTIKUM (COPY) ==========
    def __init__(self):
        self.head = None
        self.tail = None
    
    # ... (copy semua method dari praktikum) ...
    
    # ========== METHOD BARU (TUGAS) ==========
    def reverse(self):
        """
        Membalik urutan DLL (in-place)
        Kompleksitas: O(n)
        """
        # TODO: Implementasikan berdasarkan flowchart
        pass
    
    def find_min(self):
        """
        Mencari nilai minimum
        Kompleksitas: O(n)
        """
        # TODO: Implementasikan
        pass
    
    def find_max(self):
        """
        Mencari nilai maksimum
        Kompleksitas: O(n)
        """
        # TODO: Implementasikan
        pass
    
    def swap_nodes(self, pos1, pos2):
        """
        Menukar DATA dua node di posisi berbeda
        Kompleksitas: O(n)
        Note: Hanya tukar data, bukan node-nya
        """
        # TODO: Implementasikan
        pass
    
    def is_palindrome(self):
        """
        Mengecek apakah DLL adalah palindrome
        Kompleksitas: O(n)
        Return: True jika palindrome, False jika tidak
        
        Contoh palindrome: 1 <-> 2 <-> 3 <-> 2 <-> 1
        """
        # TODO: Implementasikan
        # Hint: Bandingkan dari depan dan belakang secara bersamaan
        pass
    
    def to_list(self):
        """Konversi ke Python list"""
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST PENGEMBANGAN DLL")
    print("=" * 50)
    
    dll = DoublyLinkedList()
    for val in [10, 20, 30, 40, 50]:
        dll.insert_at_end(val)
    dll.display()  # DLL: 10 <-> 20 <-> 30 <-> 40 <-> 50 <-> NULL
    
    # Test to_list
    assert dll.to_list() == [10, 20, 30, 40, 50], "GAGAL: to_list"
    print("✓ Test to_list PASSED")
    
    # Test find_min, find_max
    assert dll.find_min() == 10, "GAGAL: find_min"
    assert dll.find_max() == 50, "GAGAL: find_max"
    print("✓ Test find_min/max PASSED")
    
    # Test swap_nodes
    dll.swap_nodes(1, 3)  # Tukar 20 dan 40
    assert dll.to_list() == [10, 40, 30, 20, 50], "GAGAL: swap_nodes"
    print("✓ Test swap_nodes PASSED")
    
    # Test reverse
    dll.reverse()
    dll.display()  # Expected: DLL: 50 <-> 20 <-> 30 <-> 40 <-> 10 <-> NULL
    assert dll.to_list() == [50, 20, 30, 40, 10], "GAGAL: reverse"
    print("✓ Test reverse PASSED")
    
    # Test is_palindrome
    palindrome_dll = DoublyLinkedList()
    for val in [1, 2, 3, 2, 1]:
        palindrome_dll.insert_at_end(val)
    assert palindrome_dll.is_palindrome() == True, "GAGAL: is_palindrome True"
    
    not_palindrome = DoublyLinkedList()
    for val in [1, 2, 3, 4, 5]:
        not_palindrome.insert_at_end(val)
    assert not_palindrome.is_palindrome() == False, "GAGAL: is_palindrome False"
    print("✓ Test is_palindrome PASSED")
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Tugas 2: Aplikasi DLL - Text Editor Undo/Redo (40 menit)

### Deskripsi
Buat simulasi **Text Editor** dengan fitur Undo/Redo menggunakan Double Linked List.

```mermaid
flowchart LR
    subgraph History
        H1[State 1] <--> H2[State 2] <--> H3[State 3] <--> H4[State 4]
    end
    
    CURRENT[Current] --> H3
    
    UNDO[Undo] -.-> |move left| H2
    REDO[Redo] -.-> |move right| H4
```

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 2: Aplikasi DLL - Text Editor Undo/Redo
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

class StateNode:
    """Node untuk menyimpan state text"""
    
    def __init__(self, text):
        self.text = text
        self.prev = None
        self.next = None


class TextEditor:
    """Text Editor dengan Undo/Redo menggunakan DLL"""
    
    def __init__(self):
        # State awal: text kosong
        initial_state = StateNode("")
        self.current = initial_state
        self.head = initial_state
    
    def type_text(self, new_text):
        """
        Mengetik text baru (mengganti text saat ini)
        Jika ada history setelah current, hapus semua (karena branching)
        """
        # TODO: Implementasikan
        # Hint:
        # 1. Buat node baru dengan new_text
        # 2. Hapus semua node setelah current (jika ada)
        # 3. Hubungkan current ke new_node
        # 4. Pindah current ke new_node
        pass
    
    def append_text(self, text):
        """
        Menambahkan text ke text saat ini
        """
        # TODO: Implementasikan
        # Hint: Gabungkan current text dengan text baru, lalu type_text
        pass
    
    def undo(self):
        """
        Kembali ke state sebelumnya
        Return: True jika berhasil, False jika sudah di awal
        """
        # TODO: Implementasikan
        pass
    
    def redo(self):
        """
        Maju ke state berikutnya (jika ada)
        Return: True jika berhasil, False jika tidak ada redo
        """
        # TODO: Implementasikan
        pass
    
    def get_text(self):
        """Return text saat ini"""
        # TODO: Implementasikan
        pass
    
    def can_undo(self):
        """Cek apakah bisa undo"""
        # TODO: Implementasikan
        pass
    
    def can_redo(self):
        """Cek apakah bisa redo"""
        # TODO: Implementasikan
        pass
    
    def show_history(self):
        """
        Menampilkan history editing
        Format:
        History: "" <-> "Hello" <-> "Hello World" <-> "Hello World!"
                                      ^current
        """
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST TEXT EDITOR")
    print("=" * 50)
    
    editor = TextEditor()
    
    # Test initial state
    assert editor.get_text() == "", "GAGAL: Initial text harus kosong"
    print("✓ Test initial state PASSED")
    
    # Test type_text
    editor.type_text("Hello")
    assert editor.get_text() == "Hello", "GAGAL: type_text"
    print("✓ Test type_text PASSED")
    
    # Test append_text
    editor.append_text(" World")
    assert editor.get_text() == "Hello World", "GAGAL: append_text"
    print("✓ Test append_text PASSED")
    
    editor.append_text("!")
    assert editor.get_text() == "Hello World!", "GAGAL: append_text 2"
    
    editor.show_history()
    
    # Test undo
    assert editor.can_undo() == True, "GAGAL: can_undo"
    editor.undo()
    assert editor.get_text() == "Hello World", "GAGAL: undo"
    print("✓ Test undo PASSED")
    
    editor.undo()
    assert editor.get_text() == "Hello", "GAGAL: undo 2"
    
    # Test redo
    assert editor.can_redo() == True, "GAGAL: can_redo"
    editor.redo()
    assert editor.get_text() == "Hello World", "GAGAL: redo"
    print("✓ Test redo PASSED")
    
    # Test branching (type setelah undo menghapus redo history)
    editor.type_text("Hi")
    assert editor.get_text() == "Hi", "GAGAL: branching"
    assert editor.can_redo() == False, "GAGAL: redo harus hilang setelah branching"
    print("✓ Test branching PASSED")
    
    editor.show_history()
    
    print("=" * 50)
    print("🎉 SEMUA TEST PASSED!")
    print("=" * 50)
```

---

## Tugas 3: Aplikasi CLL - Round Robin Scheduler (40 menit)

### Deskripsi
Buat simulasi **CPU Scheduler** dengan algoritma **Round Robin** menggunakan Circular Linked List.

```mermaid
flowchart LR
    subgraph Processes
        P1[Process A<br/>Time: 3] --> P2[Process B<br/>Time: 5]
        P2 --> P3[Process C<br/>Time: 2]
        P3 --> P1
    end
    
    CPU[CPU<br/>Quantum: 2] --> P1
```

### Template Kode

```python
"""
============================================================
TUGAS TERSTRUKTUR 3: Aplikasi CLL - Round Robin Scheduler
============================================================
Nama  : ____________________
NIM   : ____________________
Kelas : ____________________
============================================================
"""

class ProcessNode:
    """Node untuk menyimpan informasi proses"""
    
    def __init__(self, pid, name, burst_time):
        self.pid = pid                    # Process ID
        self.name = name                  # Nama proses
        self.burst_time = burst_time      # Total waktu yang dibutuhkan
        self.remaining_time = burst_time  # Sisa waktu
        self.next = None


class RoundRobinScheduler:
    """CPU Scheduler dengan Round Robin menggunakan CLL"""
    
    def __init__(self, quantum):
        """
        Inisialisasi scheduler
        Parameter:
            quantum: time slice untuk setiap proses
        """
        self.head = None
        self.quantum = quantum
        self.current_time = 0
        self.completed = []  # List proses yang sudah selesai
    
    def add_process(self, pid, name, burst_time):
        """
        Menambahkan proses baru ke antrian (circular)
        """
        # TODO: Implementasikan
        pass
    
    def remove_process(self, process):
        """
        Menghapus proses dari circular list
        """
        # TODO: Implementasikan
        pass
    
    def execute_one_cycle(self):
        """
        Menjalankan satu cycle untuk proses saat ini
        
        Return: dict dengan info eksekusi
        {
            'process': nama proses,
            'executed_time': waktu yang dieksekusi,
            'remaining': sisa waktu proses,
            'completed': True/False
        }
        """
        # TODO: Implementasikan
        # Hint:
        # 1. Ambil proses di head
        # 2. Kurangi remaining_time dengan quantum (atau habiskan jika < quantum)
        # 3. Jika selesai (remaining_time <= 0), hapus dari list
        # 4. Jika belum, pindah ke proses berikutnya
        pass
    
    def run(self):
        """
        Menjalankan semua proses sampai selesai
        Tampilkan timeline eksekusi
        """
        # TODO: Implementasikan
        pass
    
    def display_queue(self):
        """
        Menampilkan antrian proses saat ini
        """
        # TODO: Implementasikan
        pass
    
    def get_statistics(self):
        """
        Menghitung statistik scheduling
        Return: dict dengan average waiting time, turnaround time, dll
        """
        # TODO: Implementasikan
        pass


# === TEST CASES ===
if __name__ == "__main__":
    print("=" * 50)
    print("TEST ROUND ROBIN SCHEDULER")
    print("=" * 50)
    
    # Buat scheduler dengan quantum = 2
    scheduler = RoundRobinScheduler(quantum=2)
    
    # Tambah proses
    scheduler.add_process(1, "Process A", 5)
    scheduler.add_process(2, "Process B", 3)
    scheduler.add_process(3, "Process C", 4)
    
    print("Initial Queue:")
    scheduler.display_queue()
    
    print("\n" + "=" * 50)
    print("EXECUTION TIMELINE")
    print("=" * 50)
    
    # Jalankan scheduler
    scheduler.run()
    
    """
    Expected output (kurang lebih):
    Time 0-2: Process A executed (remaining: 3)
    Time 2-4: Process B executed (remaining: 1)
    Time 4-6: Process C executed (remaining: 2)
    Time 6-8: Process A executed (remaining: 1)
    Time 8-9: Process B completed
    Time 9-11: Process C completed
    Time 11-12: Process A completed
    
    All processes completed!
    """
    
    print("\n" + "=" * 50)
    print("STATISTICS")
    print("=" * 50)
    stats = scheduler.get_statistics()
    print(f"Total execution time: {stats.get('total_time', 'N/A')}")
    
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
1. **Goodrich et al., Chapter 7.4-7.6** - Doubly Linked Lists, Circular Lists
2. **GeeksforGeeks** - [Doubly Linked List](https://www.geeksforgeeks.org/doubly-linked-list/)
3. **GeeksforGeeks** - [Circular Linked List](https://www.geeksforgeeks.org/circular-linked-list/)

### Bacaan Tambahan:
- [Visualgo - Linked List](https://visualgo.net/en/list)
- Round Robin Scheduling Algorithm

---

## D2. Video Tutorial (40 menit)

Tonton dan buat catatan:

1. **Doubly Linked List Explained** (~15 menit)
   - https://www.youtube.com/watch?v=JdQeNxWCguQ
   
2. **Circular Linked List** (~10 menit)
   - https://www.youtube.com/watch?v=HMkdlu5sP4A

3. **Round Robin Scheduling** (~15 menit)
   - https://www.youtube.com/watch?v=TxjIlNYRZ5M

---

## D3. Latihan Mandiri (60 menit)

### Soal Pilihan Ganda

**1.** Berapa pointer yang dimiliki setiap node dalam Double Linked List?
- [ ] a. 1
- [ ] b. 2
- [ ] c. 3
- [ ] d. 0

**2.** Keuntungan utama DLL dibanding SLL adalah...
- [ ] a. Menggunakan memori lebih sedikit
- [ ] b. Bisa traverse dua arah
- [ ] c. Insert di awal lebih cepat
- [ ] d. Search lebih cepat

**3.** Dalam Circular Linked List, node terakhir menunjuk ke...
- [ ] a. NULL
- [ ] b. Node pertama (HEAD)
- [ ] c. Node tengah
- [ ] d. Dirinya sendiri

**4.** Kompleksitas delete di akhir DLL (dengan pointer tail) adalah...
- [ ] a. O(1)
- [ ] b. O(n)
- [ ] c. O(log n)
- [ ] d. O(n²)

**5.** Circular Linked List cocok untuk implementasi...
- [ ] a. Stack
- [ ] b. Round Robin Scheduling
- [ ] c. Binary Search
- [ ] d. Hash Table

### Latihan Coding (Opsional)

Kerjakan di platform online:
- **LeetCode Medium #146** - LRU Cache (menggunakan DLL)
- **LeetCode Easy #876** - Middle of the Linked List
- Implementasi Josephus Problem dengan CLL

---

## D4. Persiapan Pertemuan Berikutnya (30 menit)

Baca materi tentang **Stack**:
- Apa itu Stack dan prinsip LIFO?
- Operasi dasar Stack (push, pop, peek)
- Implementasi Stack dengan Array dan Linked List
- Aplikasi Stack dalam kehidupan nyata

---


**Selamat Belajar! 🚀**

*Modul ini disusun oleh Aidil Saputra Kirsan (myst-tech.com), Institut Teknologi Kalimantan.*