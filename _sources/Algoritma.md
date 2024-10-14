---
title: Algoritma

---

# Algoritma
## 1. Definisi Algoritma
Pengertian umum dari suatu algoritma adalah urutan dari sejumlah langkah logis dan sistematis untuk memecahkan suatu masalah tertentu.
### A. Algoritma Sequential Search
Pencarian sekuensial digunakan apabila data dalam keadaan acak atau tidak terurut.
dapat dijelaskan sebagai berikut : pencarian dimulai dari
data paling awal, kemudian ditelusuri dengan menaikkan indeks data, apabila data sama
dengan kunci pencarian dihentikan dan diberikan nilai pengembalian true, apabila
sampai indeks terakhir data tidak ditemukan maka diberikan nilai pengembalian false. 

![image](https://hackmd.io/_uploads/SJN2UDKyyx.png)

Data[4]=3 sama dengan kunci=3 maka data ditemukan dan diberikan nilai pengembalian i (posisi) dan proses dihentikan. Apabila data tidak ditemukan, maka fungsi akan mengembalikan nilai -1 
### B. Algoritma Binary Search
Pencarian biner digunakan pada data yang sudah dalam keadaan urut.
Salah satu syarat agar pencarian biner dapat dilakukan adalah data sudah dalam keadaan urut. Dengan kata lain, apabila data belum dalam keadaan urut, pencarian biner tidak dapat dilakukan. 

![image](https://hackmd.io/_uploads/B1lOLwDtkyg.png)

Data[1]=3 sama dengan kunci=3 maka data ditemukan dan diberikan nilai pengembalian i (posisi) dan proses dihentikan. Apabila data tidak ditemukan, maka fungsi akan mengembalikan nilai -1 
## 2. Pseudocode adalah
Pseudocode adalah cara penulisan kode dan algoritma menggunakan bahasa umum yang digunakan sehari-hari sehingga lebih mudah dipahami. Karena itu pseudocode juga disebut sebagai false code atau representation code.
### Contoh Sederhana Pseudocode
#### Menyeleksi nilai murid yang tidak ikut remedial
Pseudocode digunakan untuk menyeleksi murid yang ikut remedial. Aturannya adalah murid yang mendapatkan nilai 60 ke atas, maka dianggap lulus. Sedangkan anak dengan nilai kurang dari 60 dinyatakan remedial.
Maka pseudocode-nya tertulis:

If student's grade is greater than or equal to 60
Print "passed"
else
Print "failed"

## 3. Big O Algoritma
Notasi Big-O adalah cara untuk mengekspresikan kompleksitas waktu (atau ruang) suatu algoritma. Notasi ini memberikan perkiraan kasar tentang berapa lama waktu yang dibutuhkan suatu algoritma untuk berjalan (atau berapa banyak memori yang digunakannya), berdasarkan ukuran input. Misalnya, suatu algoritma dengan kompleksitas waktu berarti waktu berjalan meningkat secara linear seiring dengan ukuran input.
## 4. Hitung Big O dari Algoritma
### A. Kompleksitas waktu
Kompleksitas waktu adalah ukuran seberapa lama waktu yang dibutuhkan suatu algoritma untuk berjalan, berdasarkan ukuran input. Hal ini dinyatakan menggunakan notasi Big-O, yang memberikan perkiraan kasar waktu berjalan. Suatu algoritma dengan kompleksitas waktu yang lebih rendah umumnya akan lebih cepat daripada suatu algoritma dengan kompleksitas waktu yang lebih tinggi.

#### Contoh Komplesitas Waktu
Berikut adalah beberapa contoh bagaimana kompleksitas waktu yang berbeda diekspresikan menggunakan notasi Big-O:

- $O(1)$ = Waktu konstan. Waktu berjalan tidak bergantung pada ukuran input.
- $O(n)$ = Waktu linier. Waktu berjalan meningkat secara linier seiring dengan ukuran input.
- $O(n^2)$ = Waktu kuadrat. Waktu berjalan sebanding dengan kuadrat ukuran input.
- $O(logn)$ = Waktu logaritmik. Waktu berjalan meningkat secara logaritmik seiring dengan ukuran input.
- $O(2^n)$ = Waktu eksponensial. Waktu berjalan meningkat secara eksponensial dalam ukuran input.

#### Contoh Algoritma dan Kompleksitas Waktunya
1. Pencarian linier $O(n)$
```python
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
    return -1
```

Algoritma pencarian linier ini memiliki kompleksitas waktu $O(n)$, karena waktu berjalan berbanding lurus dengan ukuran input $n$. Jika ukuran input, pencarian linear akan memakan waktu n langkah untuk diselesaikan.

2. Pencarian biner  $O(logn)$
```python
def binary_search(arr, x):
    low = 0
    high = len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] < x:
            low = mid + 1
        elif arr[mid] > x:
            high = mid - 1
        else:
            return mid
    return -1
```

Algoritma pencarian biner ini memiliki kompleksitas waktu  $O(logn)$, karena waktu berjalan meningkat secara logaritmik dengan ukuran input. Jika ukuran input $n$, akan memakan waktu sekitar $log(n)$ langkah-langkah untuk menyelesaikan pencarian biner.

3. Sortir gelembung $O(n^2)$
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
```

Algoritma sort gelembung ini memiliki kompleksitas waktu $O(n^2)$, karena waktu berjalannya kuadratik dalam ukuran input. Jika ukuran input adalah $n$, maka akan dibutuhkan sekitar $n^2$ langkah untuk menyelesaikan bubble sort. 

4. Sortir Cepat $O(n * logn)$
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)
```
Implementasi quick sort ini memiliki kompleksitas waktu $O(logn)$, rata-rata. Dalam kasus terburuk, kompleksitas waktu adalah $O(n^2)$, jika pivot selalu merupakan elemen terkecil atau terbesar dalam array.

Algoritme quick sort bekerja dengan memilih elemen pivot dan membagi array menjadi tiga subarray: satu berisi elemen yang lebih kecil dari pivot, satu berisi elemen yang sama dengan pivot, dan satu berisi elemen yang lebih besar dari pivot. Kemudian, subarray kiri dan kanan diurutkan secara rekursif.

Kompleksitas waktu dari quick sort ditentukan oleh jumlah panggilan rekursif yang dilakukan. Setiap panggilan rekursif memproses sekitar $n/2$ elemen, jadi jumlah total panggilan rekursif kira-kira $log(n)$ Waktu berjalan setiap panggilan rekursif adalah $O(n)$, jadi total waktu berjalannya adalah $O(nlogn)$.

5. Urutan Fibonacci  $O(2^n)$ 
```python
def fibonacci(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n-1) + fibonacci(n-2)
```

Implementasi deret Fibonacci ini memiliki kompleksitas waktu $O(2^n)$, yang eksponensial dalam ukuran input. Hal ini karena setiap panggilan ke fibonacci(n) menghasilkan dua panggilan rekursif tambahan ke fibonacci(n-1) dan fibonacci(n-2).

Kompleksitas waktu algoritma ini ditentukan oleh jumlah panggilan rekursif yang dilakukan. Setiap panggilan rekursif memproses satu elemen, sehingga jumlah total panggilan rekursif kira-kira $2^n$ Waktu berjalan setiap panggilan rekursif adalah $O(1)$, jadi total waktu berjalannya adalah $O(2^n)$.

### B. Kompleksitas ruang
Kompleksitas ruang adalah ukuran seberapa banyak memori yang dibutuhkan suatu algoritma, berdasarkan ukuran input. Seperti kompleksitas waktu, kompleksitas ruang dinyatakan menggunakan notasi Big-O. Algoritma dengan kompleksitas ruang yang lebih rendah umumnya akan membutuhkan lebih sedikit memori daripada algoritma dengan kompleksitas ruang yang lebih tinggi.

#### Contoh Algoritma dan Kompleksitas Ruangnya
1. Pencarian linier $O(1)$
```python
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
    return -1
```
Algoritma pencarian linear ini memiliki kompleksitas ruang sebesar $O(1)$, karena hanya memerlukan sejumlah memori yang konstan, berapa pun ukuran inputnya. Algoritma ini membuat satu variabel (i) untuk menyimpan indeks loop, tetapi memori yang diperlukan untuk variabel ini bersifat konstan.

2. Deret Fibonacci $O(n)$
```python
def fibonacci(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n-1) + fibonacci(n-2)
```

Algoritma untuk menghitung elemen ke-n dari deret Fibonacci ini memiliki kompleksitas ruang sebesar $O(n)$, karena menggunakan rekursi dan tumpukan panggilan bertambah seiring ukuran input. Setiap panggilan rekursif memerlukan memori tambahan untuk menyimpan status fungsi, dan jumlah total memori yang diperlukan bertambah secara linear seiring ukuran input.

3. Urutkan gabungan $O(n)$
```python
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2
        left = arr[:mid]
        right = arr[mid:]

        merge_sort(left)
        merge_sort(right)

        i = j = k = 0

        while i < len(left) and j < len(right):
            if left[i] < right[j]:
                arr[k] = left[i]
                i += 1
            else:
                arr[k] = right[j]
                j += 1
            k += 1

        while i < len(left):
            arr[k] = left[i]
            i += 1
            k += 1

        while j < len(right):
            arr[k] = right[j]
            j += 1
            k += 1
```

Algoritma merge sort ini memiliki kompleksitas ruang sebesar $O(n)$, karena ia menciptakan dua array tambahan (kiri dan kanan) untuk menyimpan bagian kiri dan kanan input selama setiap panggilan rekursif. Memori yang dibutuhkan untuk menyimpan array ini meningkat secara linear seiring dengan ukuran input.

4. Sortir Cepat $O(logn)$ atau $O(n)$
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)
```

Algoritme quick sort bekerja dengan memilih elemen pivot dan membagi array menjadi tiga subarray: satu berisi elemen yang lebih kecil dari pivot, satu berisi elemen yang sama dengan pivot, dan satu berisi elemen yang lebih besar dari pivot. Kemudian, subarray kiri dan kanan diurutkan secara rekursif.

Pengurutan cepat memiliki kompleksitas ruang $O(logn)$, rata-rata. Dalam kasus terburuk, kompleksitas ruang adalah $O(n)$, jika pivot selalu merupakan elemen terkecil atau terbesar dalam array. Hal ini karena tumpukan panggilan bertambah seiring dengan jumlah panggilan rekursif, dan jumlah panggilan rekursif bersifat logaritmik dalam ukuran input.

5. Buat Matriks $O(n^2)$
```python
def create_matrix(n):
    matrix = []
    for i in range(n):
        matrix.append([0] * n)
    return matrix
```

Algoritma ini membuat matriks nxn yang diisi dengan angka nol. Algoritma ini melakukannya dengan membuat daftar baru berisi n angka nol untuk setiap baris matriks, dan menambahkan setiap baris ke matriks. Kompleksitas ruang dari algoritma ini adalah $O(n^2)$, karena ukuran matriks bertambah seiring dengan kuadrat ukuran input $(n)$. Memori yang dibutuhkan untuk menyimpan matriks meningkat sebanding dengan ukuran input.


## 5. Referensi
1. https://www.gramedia.com/literasi/pengertian-algoritma/#google_vignette
2. https://yuliana.lecturer.pens.ac.id/Struktur%20Data%20C/Prak%20SD%20-%20pdf/Praktikum%2011.pdf
3. https://revou.co/kosakata/pseudocode
4. https://www.designgurus.io/blog/big-o-algorithm-complexity
      
      
