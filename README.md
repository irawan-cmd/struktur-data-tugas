# struktur-data-tugas-25-3-26
## Soal 1

Integer (bilangan bulat) diimplementasikan dan dimanipulasi di tingkat hardware, yang memungkinkan operasi yang cepat. Namun hardware tidak mendukung nilai integer tak terbatas. Misalnya, pada arsitektur 32-bit, integer dibatasi pada rentang -2.147.483.648 hingga 2.147.483.647. Jika menggunakan arsitektur 64-bit, rentangnya menjadi -9.223.372.036.854.775.808 hingga 9.223.372.036.854.775.807. Tapi bagaimana jika kita butuh lebih dari 19 digit untuk merepresentasikan sebuah nilai integer?

Untuk menyediakan integer yang tidak bergantung pada platform dan mendukung integer lebih dari 19 digit, Python mengimplementasikan tipe integer-nya secara software. Artinya, penyimpanan dan semua operasi yang bisa dilakukan pada nilai-nilai tersebut ditangani oleh instruksi program, bukan oleh hardware. Kita mendefinisikan **Big Integer ADT** (Tipe Data Abstrak) di bawah ini yang bisa digunakan untuk menyimpan dan memanipulasi nilai integer berukuran berapa pun, seperti tipe `int` bawaan Python.

**Method-method yang harus dibuat:**

- `BigInteger(initValue = "0")` → Membuat big integer baru yang diinisialisasi dengan nilai integer dari string yang diberikan
- `toString()` → Mengembalikan representasi string dari big integer
- `comparable(other)` → Membandingkan big integer ini dengan big integer `other` untuk menentukan urutan logisnya. Perbandingan bisa dilakukan dengan operator: `<`, `<=`, `>`, `>=`, `==`, `!=`
- `arithmetic(rhsInt)` → Mengembalikan objek BigInteger baru hasil dari operasi aritmatika pada `self` dan `rhsInt`. Operasi yang bisa dilakukan: `+` `-` `*` `//` `%` `**`
- `bitwise-ops(rhsInt)` → Mengembalikan objek BigInteger baru hasil dari operasi bitwise pada `self` dan `rhsInt`. Operasi yang bisa dilakukan: `|` `&` `^` `<<` `>>`

**Pertanyaan:**

**(a)** Implementasikan Big Integer ADT menggunakan **singly linked list** di mana setiap digit dari nilai integer disimpan dalam node terpisah. Node-node harus diurutkan dari digit yang paling tidak signifikan (paling kecil) ke yang paling besar. Contohnya, linked list di bawah ini merepresentasikan nilai integer 45.839:

```
head → [9] → [8] → [3] → [5] → [4]
```
*(angka 45839 disimpan terbalik: 9, 8, 3, 5, 4)*

**(b)** Implementasikan Big Integer ADT menggunakan **Python list** untuk menyimpan digit-digit individual dari sebuah integer.

---

## Soal 2

Modifikasi implementasi Big Integer ADT dari soal sebelumnya dengan menambahkan **operator kombinasi assignment** yang bisa dilakukan pada big integer `self` dan `rhsInt`. Izinkan operasi-operasi berikut:

| Operator | Arti |
|---|---|
| `+=` | tambah lalu simpan |
| `-=` | kurang lalu simpan |
| `*=` | kali lalu simpan |
| `//=` | bagi bulat lalu simpan |
| `%=` | modulo lalu simpan |
| `**=` | pangkat lalu simpan |
| `<<=` | geser bit kiri lalu simpan |
| `>>=` | geser bit kanan lalu simpan |
| `\|=` | bitwise OR lalu simpan |
| `&=` | bitwise AND lalu simpan |
| `^=` | bitwise XOR lalu simpan |
