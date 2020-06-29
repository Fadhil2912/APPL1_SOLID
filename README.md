# APPL1_SOLID_Exercises
Latihan mengimplementasikan SOLID design dalam pemrograman OOP

### 1.StreamProgress 
Tujuan dari program ini adalah supaya bisa bekerja dengan beberapa macam stream. Strategi untuk menyelesaikan ini adalah dengan menggunakan OCP (Open-Closed Principle). Caranya adalah dengan membuat interface IStreamable yang memiliki abstract method Length dan abstract method Bytes. Kemudian selanjutnya membuat class File dan Music yang mengimplementasikan IStreamable.

### 2. GraphicsEditor
Tujuan dari program ini adalah supaya Graphic Editor dapat menggambar segala macam bentuk tanpa melakukan pengecekan kembali dengan menggunakan conditional if-else. Cara nya adalah dengan menggunakan strategi yang sama. yaitu OCP (Open-Closed Principle). Pertama-tama kita membuat interface IShape yang memiliki method Drow(). Setiap class model shape pada program ini mengimplementasikan interface IShape. Setelah itu class GraphicEditor dimana method nya menggunakan parameter bertipe IShape sehingga setiap class yang mengimplementasikan interface IShape bisa digambar dengan method yang sama oleh class GraphicEditor tanpa mengubah class lagi ketika ada model shape class yang baru.

### 3. Detail Printer
Tujuan dari program ini adalah membuat Detail Printer yang hanya membutuhkan print detail dari seluruh employee tanpa meminta lagi jenis employee nya. Penyelesaian masalah ini sama dengan yang sebelumnya, yaitu dengan menggunakan OCP juga. Cara nya adalah dengan membuat class Employee menjadi superclass yang hanya menyimpan atribut List of Employee sehingga setiap class yang menwariskan class employee akan melakukan override method toString untuk merepresentasikan jenis employee dan kemudian memasang DetailsPrinter untuk memiliki parameter Employee. Dengan demikian, DetailsPrinter dapat mencetak detail untuk setiap employee tanpa mengetahui jenis employee tersebut.

### 4. Recharge Problem
Program ini dibuat sehingga class Robot mengimplementasikan interface IRechargeable dan extends terhadap class worker secara bersamaan. Permasalahan ini dapat diatasi dengan menggunakan strategi ISP (Interface Segregation Principle). ISP adalah metode pemisahan interface ke bagian yang lebih kecil dan spesifik. Pada permasalahan ini, ISP diterapkan pada pemisahan antara interface ISleeper dan interface IRechargeable yang berturut-turut memiliki class yang mengimplementasikannya, yaitu class Employee dan class Robot (Keduanya extends terhadap class worker). 

### 5. Security Door
Solusi permasalahan ini sama dengan sebelumnya, yaitu dengan menggunakan prinsip ISP (Interface Segregation Principle). Kita bisa membuat class baru yaitu ScannerUI yang mengimplementasikan semua method di dalam ISecurityUI kemudian kita membuat class KeyCardCheck dan PinCodeCheck memiliki parameter tipe ISecurityUI sehingga kita dapat menggunakan ScannerUI sebagai argumen untuk kelas tersebut. Kemudian kita dapat membuat class SecurityManager yang memiliki tipe parameter KeyCardCheck dan PinCodeCheck.  

