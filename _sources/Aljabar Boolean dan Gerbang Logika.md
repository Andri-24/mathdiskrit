---
title: Aljabar Boolean dan Gerbang Logika

---

# Aljabar Boolean dan Gerbang Logika

## 1. Aljabar Boolean

### A. Definisi Aljabar Boolean
Aljabar Boolean terdiri dari dua operator yaitu operator biner dan operator uner
#### Operator Biner
Aljabar Boolean memiliki dua operator biner:
Penjumlahan (+): Digunakan untuk operasi disjungsi (OR).
Perkalian (⋅): Digunakan untuk operasi konjungsi (AND).
#### Operator Uner
Komplemen (’): Digunakan untuk menghasilkan nilai yang berlawanan dari suatu elemen. Misalnya, jika a = 1, maka a’ = 0, dan sebaliknya.

### B.  Aksioma-Aksioma
Disebut aljabar Boolean jika untuk setiap $a, b, c \in B$ berlaku aksioma-aksioma atau postulat Huntington berikut:

1. **Closure:** $a + b \in B$ dan $a \cdot b \in B$.
2. **Identitas:** $a + 0 = a$ dan $a \cdot 1 = a$.
3. **Komutatif:** $a + b = b + a$ dan $a \cdot b = b \cdot a$.
4. **Distributif:** $a \cdot (b + c) = (a \cdot b) + (a \cdot c)$ dan $a + (b \cdot c) = (a + b) \cdot (a + c)$.
5. **Komplemen:** Untuk setiap $a \in B$, terdapat elemen unik $a' \in B$ sehingga $a + a' = 1$ dan $a \cdot a' = 0$.

### C. Aljabar Dua Nilai
Aljabar Boolean dua-nilai:
- B = {0, 1}
- operator biner, + dan ⋅
- operator uner, ’
- Kaidah untuk operator biner dan operator uner:

#### Tabel Operasi AND ($a \cdot b$)

| $a$ | $b$ | $a \cdot b$ |
|-----|-----|-------------|
| 0   | 0   | 0           |
| 0   | 1   | 0           |
| 1   | 0   | 0           |
| 1   | 1   | 1           |

#### Tabel Operasi OR ($a + b$)

| $a$ | $b$ | $a + b$ |
|-----|-----|---------|
| 0   | 0   | 0       |
| 0   | 1   | 1       |
| 1   | 0   | 1       |
| 1   | 1   | 1       |

#### Tabel Komplement ($a'$)

| $a$ | $a'$ |
|-----|------|
| 0   | 1    |
| 1   | 0    |

### D. Hukum-Hukum Aljabar Boolean

| No. | Hukum                               | Pernyataan                                    |
|-----|-------------------------------------|-----------------------------------------------|
| 1   | **Hukum Identitas**                | $a + 0 = a$ **dan** $a \cdot 1 = a$          |
| 2   | **Hukum Idempoten**                | $a + a = a$ **dan** $a \cdot a = a$          |
| 3   | **Hukum Komplemen**                | $a + a' = 1$ **dan** $a \cdot a' = 0$        |
| 4   | **Hukum Dominansi**                | $a \cdot 0 = 0$ **dan** $a + 1 = 1$          |
| 5   | **Hukum Involusi**                 | $(a')' = a$                                  |
| 6   | **Hukum Penyerapan**               | $a + ab = a$ **dan** $a(a + b) = a$         |
| 7   | **Hukum Komutatif**                | $a + b = b + a$ **dan** $ab = ba$           |
| 8   | **Hukum Asosiatif**                | $a + (b + c) = (a + b) + c$ **dan** $a(bc) = (ab)c$ |
| 9   | **Hukum Distributif**              | $a + (bc) = (a + b)(a + c)$ **dan** $a(b + c) = ab + ac$ |
| 10  | **Hukum De Morgan**                | $(a + b)' = a'b'$ **dan** $(ab)' = a' + b'$ |
| 11  | **Hukum 0/1**                      | $0' = 1$ **dan** $1' = 0$                   |

## 2. Gerbang Logika
### A. Definisi Gerbang Logika
- Gerbang merupakan rangkaian dengan satu atau lebih sinyal masukan, tetapi hanya menghasilkan satu sinyal keluaran. 
- Gerbang dinyatakan dengan dua keadaan :
1. Tegangan tinggi / logika tinggi / high logic / logika 1
2. Tegangan rendah / logika rendah / low logic / logika 0
- Rangkaian digital dirancang dengan menggunakan Aljabar Boole, penemunya George Boole.

#### Gerbang Logika Dasar

![image](https://hackmd.io/_uploads/BkEI5HFyye.png)

#### Gerbang Logika Lain

![image](https://hackmd.io/_uploads/r1qq9rKkkl.png)

![image](https://hackmd.io/_uploads/HyO3qHY1Jg.png)

#### Contoh

![image](https://hackmd.io/_uploads/B11EsBFyJg.png)

![image](https://hackmd.io/_uploads/SJmYsHYkkx.png)


## 3. Referensi
1. https://irma.lecturer.pens.ac.id/Matematika%20Diskrit/Aljabar%20Boolean.pdf
2. https://repository.unikom.ac.id/46068/1/gerbang-logika-dan-aljabar-boole.ppt


