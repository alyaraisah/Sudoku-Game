# Sudoku - B - 03

This repository is a final project (Java) from Object-Oriented Programming Class, Teknik Informatika Universitas Padjadjaran. 

[Challenge Guidelines](challenge-guideline.md)

## Credits
| NPM           | Name        |
| ------------- |---------------------|
| 140810200006  | Hali Putri Aisyah   |
| 140810200052  | Fasya Nurina Izzati |
| 140810200060  | Alya Raisa hidayat  |

## Change log
- **[Sprint Planning](changelog/sprint-planning.md) - (17 November 2021)** 
  -   Mencari referensi tentang permainan sudoku
  -   Scrum Meeting untuk berdiskusi dan membahas sprint backlog
 
- **[Sprint 1](changelog/sprint-1.md) - (17 - 23 November 2021)** 
   - Instalasi & Eksplorasi Gradle
   - Tampilan grid 9x9 dengan subgrid     
   - Implementasi dasar PBO            

- **[Sprint 2](changelog/sprint-2.md) - (24 - 30 November)** 
   - Tingkat Kesulitan
   - Tampilan String dan Clue          
   - Mengacak Angka              
   - Tampilan Tombol Restart 
   
- **[Sprint 3](changelog/sprint-3.md) - (01 - 07 Desember)** 
   - Set Angka yang tidak bisa diganti    
   - Cek Angka yang dimasukkan benar/salah 
   - Highlight grid yang bernilai sama
   - Perbaikan UI dan pembuatan Menu Bar 

## Running The App

1. Bukalah terminal pada text editor.
2. Lakukan cd file dari app -> src -> main -> java -> sudoku.
3. Compile program dengan menggunakan command "javac Sudoku.java".
4. Lalu, jalankan main dengan menggunakan command "java Sudoku".
5. Game sudah terbuka dan sip untuk dimainkan sesuai aturan yang sudah tertera pada button "Help -> Game Instructions".

## Classes Used

1. Class Puzzle, merupakan class untuk menginput serta mengacak angka yang ada pada sudoku
2. Class Sudoku, berfungsi untuk menampilkan tampilan game sudoku dan main class untuk menjalankan permainan sudoku

<img width="426" alt="Screen Shot 2021-12-08 at 07 57 14" src="https://user-images.githubusercontent.com/79495345/145129587-a583bd3b-3ea8-49e0-88e5-d4c272df1e11.png">

## Notable Assumption and Design App Details
- Tampilan grid berukuran 9x9 yang terdiri dari sub-grids 3x3
- Random Number bersifat Unik pada setiap baris, kolom, grid dan sub-grids
- Lakukan masking terhadap ubin tertentu (angka disembunyikan dan dijadikan text field)
- Ubin yang tidak dimasking bersifat read-only (angka didalamnya tidak bisa diubah)
- Cek apakah urutan tersebut dapat dipecahkan dengan aturan: Setiap angka yang didahului oleh angka yang lebih besar dianggap sebagai inversi, jumlah inversi dari puzzle harus genap.
- Buat listener untuk memproses input. Setiap inputan user akan dicek:
- Koordinat x dan y dimana inputan tersebut berada
- Apakah nilai yang dimasukan pada ubin sesuai dengan jawaban, jika sesuai maka background menjadi biru, jika tidak sesuai maka tulisan menjadi warna merah
- Highlight (background menjadi merah) ubin yang sudah berisi angka, jika dalam 1 baris, 1 kolom, atau 1 sub-grids berisi angka yang sama dengan inputan user
- Buat button “Reset/Restart” untuk mengacak ulang grid dan memulai game baru.
