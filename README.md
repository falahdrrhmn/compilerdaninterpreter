# PERBEDAAN ANTARA COMPILER DAN INTERPRETER

<div id="top"></div>

<!-- GETTING STARTED -->

## Compiler

- Compiler adalah program yang menerjemahkan seluruh kode program dari bahasa pemrograman tingkat tinggi ke dalam kode objek atau kode mesin yang dapat dieksekusi oleh komputer.
- Compiler melakukan analisis sintaksis dan analisis semantik terhadap kode sumber untuk memastikan kebenaran sintaks dan penggunaan tipe data yang tepat.
- Proses kompilasi biasanya terdiri dari beberapa tahap, seperti analisis, optimasi, dan generasi kode objek.
- Setelah kompilasi selesai, hasil akhirnya adalah file eksekusi yang dapat dieksekusi secara langsung oleh komputer tanpa memerlukan keberadaan compiler.

## Interpreter

- Interpreter adalah program yang membaca, menganalisis, dan menjalankan kode program satu baris atau satu instruksi pada satu waktu.
- Interpreter menerjemahkan dan menjalankan kode program secara langsung tanpa memerlukan tahap kompilasi terlebih dahulu.
- Interpreter membaca kode program baris per baris atau instruksi per instruksi, menerjemahkan instruksi tersebut menjadi kode mesin, dan langsung menjalankannya.
- Proses interpretasi terjadi saat program dijalankan, sehingga perubahan pada kode program dapat langsung dilihat hasilnya tanpa perlu melakukan kompilasi ulang.

## Perbedaan antara Compiler dan Interpreter

1. Tahapan: Compiler melakukan proses kompilasi yang melibatkan analisis, optimasi, dan generasi kode objek, sementara interpreter langsung menerjemahkan dan menjalankan kode program tanpa tahap kompilasi.
2. Eksekusi: Compiler menghasilkan file eksekusi yang dapat dieksekusi tanpa compiler, sedangkan interpreter membaca dan menjalankan kode program langsung saat program dijalankan.
3. Performa: Kode yang telah dikompilasi cenderung berjalan lebih cepat karena telah diterjemahkan menjadi kode mesin, sementara program yang dieksekusi oleh interpreter biasanya lebih lambat karena perlu menerjemahkan instruksi pada saat eksekusi.
4. Debugging: Karena interpreter membaca kode program per baris, debugging dapat dilakukan dengan mudah karena setiap baris bisa dianalisis secara langsung, sedangkan pada compiler, debugging bisa sedikit lebih rumit karena memerlukan pemahaman lebih lanjut tentang kesalahan yang muncul saat kompilasi.

## Penggunaan pada Bahasa Pemrograman

Banyak bahasa pemrograman menggunakan kompilasi, seperti C, C++, Java, dan Go. Contoh bahasa pemrograman yang menggunakan interpreter adalah Python, JavaScript, dan Ruby.

## Alur Kerja Compiler

1. Analisis Sintaksis: Compiler membaca kode sumber dan memeriksa struktur sintaksisnya. Jika ada kesalahan sintaksis, compiler menghasilkan pesan kesalahan.
2. Analisis Semantik: Compiler menganalisis makna dan penggunaan kata-kata serta instruksi dalam program. Compiler memastikan kebenaran tipe data, pemanggilan fungsi, dan struktur program sesuai dengan aturan bahasa pemrograman.
3. Optimasi: Compiler melakukan optimasi kode untuk meningkatkan performa atau mengurangi ukuran kode. Ini melibatkan pengurangan redundansi, penggabungan instruksi, dan penghilangan kode yang tidak terpakai.
4. Generasi Kode Objek: Setelah tahap analisis dan optimasi selesai, compiler menghasilkan kode objek atau kode mesin yang sesuai dengan arsitektur target komputer. Kode objek ini tidak dapat dijalankan langsung, tetapi merupakan representasi dari kode program dalam bentuk bahasa mesin yang dapat dieksekusi.
5. Linking: Jika program terdiri dari beberapa file atau menggunakan pustaka eksternal, compiler melakukan proses linking untuk menggabungkan kode objek dengan kode objek lainnya dan pustaka yang diperlukan. Hasil akhirnya adalah file eksekusi yang dapat dieksekusi secara langsung oleh komputer.

## Alur Kerja Interpreter

1. Analisis dan Parsing: Interpreter membaca kode program dan melakukan analisis sintaksis. Kemudian, interpreter memecah kode program menjadi struktur data yang dapat diproses lebih lanjut.
2. Menerjemahkan dan Menjalankan Instruksi: Interpreter menerjemahkan dan menjalankan instruksi kode program satu per satu secara berurutan. Interpreter membaca instruksi, menerjemahkannya menjadi instruksi yang dapat dieksekusi oleh komputer, dan menjalankannya.
3. Iterasi: Setelah menjalankan satu instruksi, interpreter melanjutkan ke instruksi berikutnya, dan proses ini berlanjut hingga seluruh kode program selesai dieksekusi.
4. Error Handling: Jika interpreter menemui kesalahan saat menjalankan instruksi, ia menghasilkan pesan kesalahan dan berhenti eksekusi.
5. Debugging dan Eksekusi Interaktif: Interpreter memungkinkan proses debugging dan eksekusi interaktif yang memungkinkan pengguna untuk memeriksa dan memodifikasi variabel, menjalankan potongan kode secara terpisah, atau melakukan langkah demi langkah dalam eksekusi program.

<br>
<br>

# NGECOMPILE C++ MENGGUNAKAN TERMINAL

tutorial untuk membuat program Hello World sederhana dalam bahasa C++ dan melakukan kompilasi menggunakan terminal:

1. Buka editor teks atau IDE favoritmu dan buat file baru dengan ekstensi `.cpp`, misalnya `hello.cpp`.

2. Tulis kode program Hello World berikut ini di dalam file `hello.cpp`:

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

Kode di atas menggunakan header `<iostream>` untuk mengakses fungsi `cout` yang digunakan untuk mencetak pesan di layar.

3. Simpan file `hello.cpp`.

4. Buka terminal atau command prompt di komputermu.

5. Pindah ke direktori tempat kamu menyimpan file `hello.cpp` menggunakan perintah `cd`.

6. Jalankan perintah berikut ini untuk melakukan kompilasi file `hello.cpp` menggunakan `gcc` (GNU Compiler Collection):

```bash
g++ hello.cpp -o hello
```

- `g++` adalah perintah untuk menjalankan compiler C++ dari GCC.
- `hello.cpp` adalah nama file sumber yang akan dikompilasi.
- `-o hello` digunakan untuk menentukan nama file output atau file hasil kompilasi. Dalam contoh ini, file output disebut `hello`.

7. Jika kompilasi berhasil, perintah tersebut akan menghasilkan file eksekusi dengan nama `hello`.

8. Jalankan program Hello World yang telah dikompilasi dengan perintah:

```bash
./hello
```

9. Jika semuanya berjalan dengan baik, kamu akan melihat pesan "Hello, World!" dicetak di terminal.

Itu adalah langkah-langkah untuk membuat program Hello World sederhana dalam bahasa C++ dan melakukan kompilasi menggunakan terminal. 

Alur kerja kompilasi C++ melibatkan:
1. Preprocessing: Preprocessor (`cpp`) mengambil file sumber C++ dan memproses direktif preprocessor seperti `#include` dan `#define`.
2. Compilation: Compiler C++ (`g++`) mengambil hasil dari preprocessing dan menerjemahkannya menjadi kode objek dalam bahasa mesin.
3. Linking: Jika program C++ menggunakan pustaka eksternal atau file objek lainnya, linker (`ld`) menggabungkan file objek tersebut dan menghasilkan file eksekusi yang dapat dieksekusi.

```
Lenovo@DESKTOP-9EO0J5L MINGW64 /d/cppp badas
$ g++ hello.cpp -o setelahcompile

Lenovo@DESKTOP-9EO0J5L MINGW64 /d/cppp badas
$ ls
hello.cpp  setelahcompile.exe*

Lenovo@DESKTOP-9EO0J5L MINGW64 /d/cppp badas
$ ./setelahcompile.exe

Hello, World!
```

<br>
<br>

<div align="center">
  <a href="#list">(Back to List)</a>
  ·
  <a href="#top">(Back to Top)</a>
</div>

<br>
<br>

<div align="center">
    Follow me!<br>
    <a href="https://bit.ly/3Qcg3s4">LinkedIn</a>
    ·
    <a href="https://bit.ly/3oRMMaA">Instagram</a>
    ·
    <a href="https://bit.ly/3zqrTrP">Youtube</a>
</div>
