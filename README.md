# Tugas Sistem Operasi 1

**Nama**: Firas Rasendriya Athaillah  
**NRP**: 3124500042  
**Kelas**: D3 IT B  

## Konversi Bilangan

### 1. Bilangan Biner dan Heksadesimal
- **Bilangan biner** adalah bilangan yang berbasis **dua (2)**.
- **Bilangan heksadesimal** adalah bilangan yang berbasis **enam belas (16)**.

### 2. Konversi Desimal ke Biner
#### 1234₁₀ → ?
```
1234 : 2 = 617 sisa 0
 617 : 2 = 308 sisa 1
 308 : 2 = 154 sisa 0
 154 : 2 =  77 sisa 0
  77 : 2 =  38 sisa 1
  38 : 2 =  19 sisa 0
  19 : 2 =   9 sisa 1
   9 : 2 =   4 sisa 1
   4 : 2 =   2 sisa 0
   2 : 2 =   1 sisa 0
   1 : 2 =   0 sisa 1
```
**Jawaban**: `10011010010₂`

#### 5670₁₀ → ?
```
5670 : 2 = 2835 sisa 0
2835 : 2 = 1417 sisa 1
1417 : 2 =  708 sisa 1
 708 : 2 =  354 sisa 0
 354 : 2 =  177 sisa 0
 177 : 2 =   88 sisa 1
  88 : 2 =   44 sisa 0
  44 : 2 =   22 sisa 0
  22 : 2 =   11 sisa 0
  11 : 2 =    5 sisa 1
   5 : 2 =    2 sisa 1
   2 : 2 =    1 sisa 0
   1 : 2 =    0 sisa 1
```
**Jawaban**: `1011000100110₂`

### 3. Konversi Biner ke Desimal
#### 10101010₂ → ?
```
1 × 2⁷ = 128
0 × 2⁶ =  0
1 × 2⁵ = 32
0 × 2⁴ =  0
1 × 2³ =  8
0 × 2² =  0
1 × 2¹ =  2
0 × 2⁰ =  0
```
**Jawaban**: `170₁₀`

#### 01010101₂ → ?
```
0 × 2⁷ =  0
1 × 2⁶ =  0
0 × 2⁵ =  0
1 × 2⁴ = 16
0 × 2³ =  0
1 × 2² =  4
0 × 2¹ =  0
1 × 2⁰ =  1
```
**Jawaban**: `85₁₀`

### 4. Konversi Biner ke Oktal
#### 101011111001₂ → ?
```
101 = 5
011 = 3
111 = 7
001 = 1
```
**Jawaban**: `5371₈`

### 5. Konversi Oktal ke Biner
#### 2170₈ → ?
```
2 = 010
1 = 001
7 = 111
0 = 000
```
**Jawaban**: `010001111000₂`

### 6. Konversi Desimal ke Heksadesimal
#### 1780₁₀ → ?
```
1780 : 16 = 111 sisa 4
 111 : 16 =  6 sisa 15 (F)
   6 : 16 =  0 sisa 6
```
**Jawaban**: `06F4₁₆`

### 7. Konversi Heksadesimal ke Desimal
#### ABCD₁₆ → ?
```
A = 16³ × 10 = 40960
B = 16² × 11 = 2816
C = 16¹ × 12 = 192
D = 16⁰ × 13 = 13
```
**Jawaban**: `43981₁₀`

### 8. Konversi Pecahan Desimal ke Biner
#### 0.3125₁₀ → ?
```
0.3125 × 2 = 0.625 sisa 0
0.625 × 2 = 1.25  sisa 1
0.25  × 2 = 0.5   sisa 0
0.5   × 2 = 1.0   sisa 1
```
**Jawaban**: `0.0101₂`

### 9. Konversi Desimal ke BCD
#### 1987₁₀ → ?
```
1 = 0001
9 = 1001
8 = 1000
7 = 0111
```
**Jawaban**: `0001 1001 1000 0111`

### 10. Konversi ASCII
#### Karakter "A" ke ASCII
```
A = 65₁₀ → 41₁₆
```
**Jawaban**: `41₁₆`

### 11. Positif atau Negatif dalam Biner
#### 01111111₂ → ?
```
0 × 2⁷ = 0
1 × 2⁶ = 64
1 × 2⁵ = 32
1 × 2⁴ = 16
1 × 2³ =  8
1 × 2² =  4
1 × 2¹ =  2
1 × 2⁰ =  1
```
**Jawaban**: `127 (Positif)`

---

Format Markdown ini membuat isi tugas lebih rapi dan mudah dibaca!

