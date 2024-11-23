---
title: Deretan dan Rekursif

---

# Deretan dan Rekursif

## A. Deretan (Sequence)

Deretan adalah suatu urutan atau susunan elemen atau objek yang disusun secara teratur berdasarkan suatu aturan tertentu. Elemen dalam deretan biasanya berupa angka, huruf, simbol, atau objek lainnya, dan urutannya dapat didasarkan pada pola, nilai, atau hubungan tertentu.

### 1. Definisi
Sebuah deretan adalah fungsi dari subset suatu himpunan bilangan bulat (biasanya $\mathbb{N}$ atau $\mathbb{P}$) ke sebuah himpunan $S$.

$$
\mathbb{N} = \{1, 2, 3, 4, \dots\} \\
S \text{ misalnya } \{2, 4, 6, 8, \dots\}, \{\frac{1}{3}, \frac{1}{5}, \frac{1}{7}, \dots\}, \text{ dsb.}
$$

### 2. Notasi Deretan
Notasi deretan dinyatakan sebagai $\{a_n\}$.

### 3. Contoh Formula Deretan

$$
\begin{aligned}
    a_n &= 2n \\
    a_n &= \frac{1}{n} \\
    a_n &= 7 - 3n
\end{aligned}
$$

### 4. Contoh Deretan Bilangan

- Deretan bilangan ganjil: $1, 3, 5, 7, \dots$
- Deretan bilangan genap: $2, 4, 6, 8, \dots$
- Deretan bilangan dalam deret aritmetika: $3, 6, 9, 12, \dots$
- Deretan bilangan kuadrat: $1, 4, 9, 16, 25, \dots$ (dinyatakan dengan $a_n = n^2$)
- Deretan bilangan kubik: $1, 8, 27, 64, 125, \dots$ (dinyatakan dengan $a_n = n^3$)
- Deretan bilangan Fibonacci: $0, 1, 1, 2, 3, 5, 8, 13, \dots$ (dinyatakan dengan $a_0 = 0, a_1 = 1$, dan $a_n = a_{n-1} + a_{n-2}$ untuk $n \geq 2$)

### 5. Penjelasan dan Contoh Deret

#### a. Deret Aritmetika
Deret aritmetika adalah deretan bilangan di mana selisih antara dua suku berturutan selalu konstan.

Rumus suku ke-$n$:
$$
a_n = a_1 + (n-1)d
$$
Contoh: $2, 5, 8, 11, \dots$, dengan $a_1 = 2$ dan $d = 3$.

#### b. Deret Geometri
Deret geometri adalah deretan bilangan di mana rasio antara dua suku berturutan selalu konstan.

Rumus suku ke-$n$:
$$
a_n = a_1 \cdot r^{n-1}
$$
Contoh: $3, 6, 12, 24, \dots$, dengan $a_1 = 3$ dan $r = 2$.

#### c. Deret Bilangan Kuadrat
Deretan ini terdiri dari bilangan yang merupakan kuadrat sempurna.

Rumus suku ke-$n$:
$$
a_n = n^2
$$
Contoh: $1, 4, 9, 16, 25, \dots$.

#### d. Deret Bilangan Kubik
Deretan ini terdiri dari bilangan yang merupakan kubik sempurna.

Rumus suku ke-$n$:
$$
a_n = n^3
$$
Contoh: $1, 8, 27, 64, 125, \dots$.

#### e. Deret Fibonacci
Deret ini didefinisikan secara rekursif, dengan dua suku pertama adalah $0$ dan $1$, dan setiap suku berikutnya adalah jumlah dari dua suku sebelumnya.

Rumus:
$$
a_0 = 0, \quad a_1 = 1, \quad a_n = a_{n-1} + a_{n-2} \quad (n \geq 2)
$$
Contoh: $0, 1, 1, 2, 3, 5, 8, 13, \dots$.

### 6. String

String adalah deretan berhingga karakter berbentuk $a_1a_2a_3a_4\dots a_n$. Panjang string $S$ adalah jumlah karakter di dalam string tersebut.

#### Contoh

- "informatika" adalah string dengan panjang 11 karakter.
- "10100101" adalah string biner dengan panjang 8 bit.

String kosong dilambangkan dengan $\lambda$, panjangnya $= 0$.

## B. Penjumlahan Deretan

Jumlah deret
$$a_m, a_{m+1}, a_{m+2}, ..., a_n$$
adalah
$$a_m + a_{m+1} + a_{m+2} + ... + a_n$$
atau dalam notasi sigma:
$$\sum_{k=m}^{n} a_k$$
di mana:
* $k$ adalah indeks penjumlahan,
* $m$ adalah batas bawah penjumlahan,
* $n$ adalah batas atas penjumlahan.

**Contoh 2: Berapa nilai** $\sum_{k=1}^{5}k^2$?

**Jawaban:**

$$\sum_{k=1}^{5}k^2 = 1^2 + 2^2 + 3^2 + 4^2 + 5^2 = 1 + 4 + 9 + 16 + 25 = 55$$

**Contoh 3: Batas bawah sumasi kadangkala perlu digeser agar dapat dijumlahkan dengan sumasi lain yang memiliki batas bawah berbeda.** Pada contoh 2 di atas batas bawah digeser dari 1 menjadi 0, akibatnya:

$$\sum_{k=1}^{5}k^2 = \sum_{k=0}^{4}(k+1)^2$$

**Contoh 4: Sumasi dapat dipecah dengan membagi dua indeksnya, misalnya**

$$\sum_{k=1}^{100}k^2 = \sum_{k=1}^{49}k^2 + \sum_{k=50}^{100}k^2$$


**Contoh 5: Hitung nilai** $\sum_{k=50}^{100}k^2$

**Jawaban:**

$$\sum_{k=1}^{100}k^2 = \sum_{k=1}^{49}k^2 + \sum_{k=50}^{100}k^2$$

Oleh karena itu, 
$$\sum_{k=50}^{100}k^2 = \sum_{k=1}^{100}k^2 - \sum_{k=1}^{49}k^2$$

**Gunakan rumus:** $\sum_{k=1}^{n}k^2 = \frac{n(n+1)(2n+1)}{6}$

Maka,
$$\sum_{k=50}^{100}k^2 = \frac{100(101)(201)}{6} - \frac{49(50)(99)}{6} = 338350 - 40425 = 297925$$


## C. Sumasi Ganda

Di dalam algoritma, kita perlu menghitung berapa kali suatu operasi tertentu dilakukan di dalam sebuah kalang bersarang (nested loop). Penjumlahan semua operasi di dalam kalang bersarang dinyatakan dalam bentuk sumasi ganda.

Contoh: $\sum_{i=1}^{4}\sum_{j=1}^{3}ij$

Untuk menghitung sumasi ganda, mula-mula ekspansi sumasi terdalam, lalu dilanjutkan dengan sumasi terluar:

$$\sum_{i=1}^{4}\sum_{j=1}^{3}ij=\sum_{i=1}^{4}(i+2i+3i)=\sum_{i=1}^{4}6i=6+12+18+24=60$$

**Contoh penggunaan:** Berapa kali operasi + dilakukan di dalam algoritma di bawah ini?
```
x = 0
for j = 1 to 10 do
   for k = 1 to j do
       x = x + 2
   end for
end for
```

**Penyelesaian:**

Operasi + terdapat di dalam pernyataan x = x + 2.
Operasi ini dilakukan satu kali pada setiap pengulangan.
Jumlah seluruh operasi + adalah:

$$t = \sum_{j=1}^{10} \sum_{k=1}^{j} 1$$
$$= \sum_{j=1}^{10} (1+1+...+1 \text{ sebanyak } j \text{ kali})$$
$$= \sum_{j=1}^{10} j$$
$$= \frac{10(10+1)}{2} = 55$$

### Latihan Soal

1. **Tentukan nilai** $\sum_{k=1}^{8}2^k + \sum_{k=2}^{8}(-3)^k$

   Untuk menyelesaikan soal ini, kita dapat langsung menghitung setiap sumasi:
   $$\sum_{k=1}^{8}2^k = 2^1 + 2^2 + ... + 2^8 = 254$$
   $$\sum_{k=2}^{8}(-3)^k = (-3)^2 + (-3)^3 + ... + (-3)^8 = 1640$$
   Jadi, nilai totalnya adalah: 
   $$254 + 1640 = 1894$$

2. **Tentukan nilai** $\sum_{i=0}^{2}\sum_{j=0}^{3}(2i+3j)$

   Kita akan menghitung sumasi dalam terlebih dahulu, lalu sumasi luar:
   $$\sum_{i=0}^{2}\sum_{j=0}^{3}(2i+3j) = \sum_{i=0}^{2}[(2i+0) + (2i+3) + (2i+6) + (2i+9)]$$
   $$= \sum_{i=0}^{2}(8i+18) = (8*0+18) + (8*1+18) + (8*2+18) = 90$$

3. **Tentukan nilai** $\sum_{i=0}^{3}\sum_{j=0}^{2}i$

   Perhatikan bahwa nilai `i` tidak bergantung pada `j`. Kita bisa keluarkan `i` dari sumasi dalam:
   $$\sum_{i=0}^{3}\sum_{j=0}^{2}i = \sum_{i=0}^{3}i \cdot \sum_{j=0}^{2} 1$$
   $$\sum_{j=0}^{2} 1 = 3` (karena kita menjumlahkan 1 sebanyak 3 kali)
   Jadi, 
\sum_{i=0}^{3}\sum_{j=0}^{2}i = 3 \cdot \sum_{i=0}^{3} i = 3 \cdot (0+1+2+3) = 18$$

**Jawaban:**

1. Nilai dari $\sum_{k=1}^{8}2^k + \sum_{k=2}^{8}(-3)^k$ adalah **1894**.
2. Nilai dari $\sum_{i=0}^{2}\sum_{j=0}^{3}(2i+3j)$ adalah **90**.
3. Nilai dari $\sum_{i=0}^{3}\sum_{j=0}^{2}i$ adalah **18**.

## D. Rekursif

Sebuah objek dikatakan **rekursif** jika ia didefinisikan dalam terminologi dirinya sendiri. Proses mendefinisikan objek dalam terminologi dirinya sendiri disebut **rekursi (recursion)**.

### a. Fungsi Rekursif

Fungsi rekursif didefinisikan oleh dua bagian:

1. **Basis**: Bagian yang berisi nilai fungsi yang terdefinisi secara eksplisit. Basis juga menghentikan rekursif.
2. **Rekurens**: Bagian yang mendefinisikan fungsi dalam terminologi dirinya sendiri. Rekurens berisi kaidah untuk menemukan nilai fungsi pada suatu input dari nilai lainnya pada input yang lebih kecil.

### Contoh

Misalkan fungsi $f$ didefinisikan secara rekursif sebagai berikut:

$$
    f(n) = 2f(n-1) + 4 \quad \text{dengan } f(0) = 3.
$$

Hitung $f(4)$:

$$
\begin{aligned}
    f(4) &= 2f(3) + 4 \\
         &= 2(2f(2) + 4) + 4 \\
         &= 2(2(2f(1) + 4) + 4) + 4 \\
         &= 2(2(2(2f(0) + 4) + 4) + 4) + 4 \\
         &= 108.
\end{aligned}
$$

### b. Faktorial

Misalkan $f(n) = n!$, maka:

$$
\begin{aligned}
    5! &= 5 \times 4 \times 3 \times 2 \times 1 \\
       &= 120.
\end{aligned}
$$

### Algoritma Faktorial

```plaintext
function Faktorial(n : integer) → integer {
  if n = 0 then
    return 1   {basis}
  else
    return n * Faktorial(n-1) {rekurens}
}
```


## E. Tugas Pembuktian

![image](https://hackmd.io/_uploads/ByvWcTk7ke.png)

### Pembuktian Rumus-Rumus Penjumlahan (Summation Formula)

#### 1. Rumus $\sum_{k=0}^n ar^k = \frac{ar^{n+1} - a}{r-1}, \ r \neq 1$
**Pembuktian:**

$$
S = \sum_{k=0}^n ar^k \\
  = a + ar + ar^2 + \cdots + ar^n.
$$
Kalikan kedua sisi dengan $r$:

$$
rS = ar + ar^2 + ar^3 + \cdots + ar^{n+1}.
$$
Kurangkan persamaan pertama dari yang kedua:

$$
S - rS = a - ar^{n+1} \\
S(1-r) = a(1-r^{n+1}) \\
S = \frac{ar^{n+1} - a}{r-1}, \quad r \neq 1.
$$

#### 2. Rumus $\sum_{k=1}^n k = \frac{n(n+1)}{2}$
**Pembuktian:**

$$
S = \sum_{k=1}^n k \\
  = 1 + 2 + 3 + \cdots + n.
$$
Tuliskan kembali urutan secara terbalik:

$$
S = n + (n-1) + (n-2) + \cdots + 1.
$$
Jumlahkan dua barisan:

$$
2S = (1+n) + (2+(n-1)) + (3+(n-2)) + \cdots + (n+1).
$$
Setiap pasangan menghasilkan $n+1$, dan terdapat $n$ pasangan. Maka:

$$
2S = n(n+1) \\
S = \frac{n(n+1)}{2}.
$$

#### 3. Rumus $\sum_{k=1}^n k^2 = \frac{n(n+1)(2n+1)}{6}$
**Pembuktian (Induksi Matematika):**
- **Basis Induksi:** Untuk $n=1$,

$$
\sum_{k=1}^1 k^2 = 1^2 = 1 \\
\frac{1(1+1)(2\cdot 1 + 1)}{6} = \frac{1 \cdot 2 \cdot 3}{6} = 1.
$$
Maka, rumus benar untuk $n=1$.

- **Hipotesis Induksi:** Misalkan rumus benar untuk $n=m$, yaitu:

$$
\sum_{k=1}^m k^2 = \frac{m(m+1)(2m+1)}{6}.
$$

- **Langkah Induksi:** Buktikan untuk $n=m+1$:

$$
\sum_{k=1}^{m+1} k^2 = \sum_{k=1}^m k^2 + (m+1)^2 \\
= \frac{m(m+1)(2m+1)}{6} + (m+1)^2.
$$
Faktorkan $m+1$:

$$
\frac{m(m+1)(2m+1)}{6} + (m+1)^2 = \frac{(m+1)\left[m(2m+1) + 6(m+1)\right]}{6} \\
= \frac{(m+1)(2m^2 + 7m + 6)}{6} \\
= \frac{(m+1)(m+2)(2m+3)}{6}.
$$
Maka, rumus benar untuk $n=m+1$.

Oleh karena itu, rumus terbukti benar untuk semua $n \geq 1$. 
