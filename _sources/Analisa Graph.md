---
title: Analisa Graph

---

# Analisa Graph
## A. Social Network Analysis
Social Network Analysis merupakan bidang kajian yang mengekplorasitentang hubungan manusia dengan menggunakan teori graf. Implementasi Social Network Analysis dapat menjelaskan relasi atau hubungan antar aktor melalui visualisasi berbentuk graf. Relasi dalam analisis jaringan sosial dapat diproses dalam bentuk perhitungan yang disebut centrality dalam sebuah jaringan sosial sesuai dengan posisi masing-masing aktor di dalam struktur jaringan tersebut

![image](https://hackmd.io/_uploads/r1VbYk_MJe.png)

**Social network** 
*terdapat node yang mewakili 
orang atau individu atau aktor. 
Relasi  antar objek  dapat dinyatakan dengan link 
atau edges yang terjadi antara aktor tersebut 
Social network terdiri dari banyak aktor 
yang mempunyai relasi satu sama lain hingga
membentuk peta jaringan sosial yang dinyatakan dengan 
graph*


![image](https://hackmd.io/_uploads/BkKwKkuzkg.png)

1. Tidak semua node dalam jaringan adalah penting  (aktor)
2. Mencari node yang paling penting dalam suatu jaringan
3. Centrality adalah penentuan aktor menggunakan ukuran pada Social Network Centrality dalam teori graf dan social network .Dibagi menjadi empat jenis, 
- Degree Centrality, 
- Betweeness Centrality, 
- Closeness Centrality 
- Eigenvector Centrality

## B. Jenis-Jenis Centrality

### 1. Degree Centrality
Degree centrality adalah jumlah koneksi (*edges*) yang terhubung pada suatu simpul (*node*). Semakin tinggi derajat koneksi sebuah node, semakin penting posisinya dalam jaringan. Rumus degree centrality adalah:

$C_D(v) = \text{degree}(v)$

Normalisasi untuk degree centrality adalah:

$C_D^\text{norm}(v) = \frac{\text{degree}(v)}{n-1}$

di mana $n$ adalah jumlah total simpul dalam graf.

### 2. Closeness Centrality
Closeness centrality mengukur kedekatan rata-rata satu simpul ke simpul lainnya dalam jaringan. Simpul dengan closeness yang tinggi dapat menyebarkan informasi lebih cepat. Rumusnya:

$C_C(v) = \frac{1}{\sum_{u \neq v} d(u, v)}$

Normalisasi untuk closeness centrality adalah:

$C_C^\text{norm}(v) = \frac{n-1}{\sum_{u \neq v} d(u, v)}$

di mana $d(u, v)$ adalah jarak terpendek antara simpul $u$ dan $v$, dan $n$ adalah jumlah total simpul dalam graf.

### 3. Betweenness Centrality
Betweenness centrality mengukur seberapa sering sebuah simpul menjadi perantara dalam jalur terpendek antara dua simpul lain. Rumus:

$C_B(v) = \sum_{s \neq v \neq t} \frac{\sigma_{st}(v)}{\sigma_{st}}$

Normalisasi untuk betweenness centrality adalah:

$C_B^\text{norm}(v) = \frac{C_B(v)}{(n-1)(n-2)/2}$

di mana:
- $\sigma_{st}$ adalah jumlah jalur terpendek antara $s$ dan $t$,
- $\sigma_{st}(v)$ adalah jumlah jalur tersebut yang melalui $v$,
- $n$ adalah jumlah total simpul dalam graf.

### 4. Eigenvector Centrality
Eigenvector centrality mengukur pentingnya sebuah simpul berdasarkan koneksi dengan simpul lain yang juga penting. Rumusnya berbasis eigenvector dari matriks adjensi $A$:

$Ax = \lambda x$

di mana:
- $A$ adalah matriks adjensi graf,
- $x$ adalah eigenvector yang menunjukkan centrality dari simpul,
- $\lambda$ adalah nilai eigen terbesar.

Normalisasi untuk eigenvector centrality dilakukan dengan membagi setiap komponen $x_i$ dengan norma total eigenvector $x$:

$C_E^\text{norm}(v_i) = \frac{x_i}{\sum_{j=1}^n x_j}$

di mana $x_i$ adalah nilai eigenvector untuk simpul $i$, dan $\sum_{j=1}^n x_j$ adalah total nilai eigenvector.

---

Semua ukuran di atas digunakan untuk menganalisis jaringan sosial dan mengidentifikasi simpul yang paling signifikan dalam penyebaran informasi atau fungsi jaringan lainnya.

