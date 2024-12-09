---
title: 'Probabilitas Diskret  '

---

# Probabilitas Diskret dan Probabilitas Bayesian

## A. Pengantar
Naive Bayes adalah algoritma pembelajaran mesin untuk klasifikasi berdasarkan **Teorema Bayes**. Ia menggunakan asumsi "naif" bahwa semua fitur bersifat independen.

Dalam artikel ini, kita membahas cara kerja **Naive Bayes Diskret** menggunakan dua fitur diskret: 
- **Suhu ($X_1$)**: rendah, sedang, tinggi.
- **Angin ($X_2$)**: lemah, normal, kuat.

Target kita, **Pantai ($B$)**, memiliki nilai boolean: $true$ (pergi ke pantai) atau $false$ (tidak pergi).

## B. Rumus Dasar
Teorema Bayes memungkinkan kita menghitung probabilitas posterior berdasarkan probabilitas sebelumnya:
$$
P(E \mid C) = \frac{P(C \mid E) \cdot P(E)}{P(C)}
$$

Untuk kasus kita:
- **$E$**: Keputusan ($B$) - $true/false$.
- **$C$**: Kondisi fitur - $(X_1, X_2)$.

Probabilitas posterior menjadi:
$$
P(B \mid X_1, X_2) = \frac{P(X_1, X_2 \mid B) \cdot P(B)}{P(X_1, X_2)}
$$

## C. Asumsi Independensi
Asumsi independensi fitur memungkinkan kita menyederhanakan perhitungan:
$$
P(X_1, X_2 \mid B) = P(X_1 \mid B) \cdot P(X_2 \mid B)
$$
$$
P(X_1, X_2) = P(X_1) \cdot P(X_2)
$$

Sehingga rumus akhir menjadi:
$$
P(B \mid X_1, X_2) = \frac{P(X_1 \mid B) \cdot P(X_2 \mid B) \cdot P(B)}{P(X_1) \cdot P(X_2)}
$$

## D. Contoh Perhitungan
### Data:

![Screenshot 2024-12-09 102607](https://hackmd.io/_uploads/ryN_XJENJx.png)

- Sampel: 5 data $(X_1, X_2, B)$.
- Prior Probabilitas:
  $$
  P(B = T) = \frac{3}{5} = 0.6, \quad P(B = F) = \frac{2}{5} = 0.4
  $$

- Likelihood untuk $B = T$:
  $$
  P(X_1 = M, X_2 = W \mid B = T) = P(X_1 = M \mid B = T) \cdot P(X_2 = W \mid B = T)
  $$

- Probabilitas Marginal:
  $$
  P(X_1 = M, X_2 = W) = P(X_1 = M) \cdot P(X_2 = W)
  $$

### Prediksi:
Bandingkan posterior untuk $B = T$ dan $B = F$. Pilih yang lebih besar.

## Kesimpulan
Naive Bayes memberikan cara sederhana namun kuat untuk klasifikasi berdasarkan probabilitas, meskipun dengan asumsi independensi fitur.

## Referensi
https://tvovalentin.medium.com/the-math-behind-a-discrete-naive-bayes-classifier-abdc86e1cbf3

