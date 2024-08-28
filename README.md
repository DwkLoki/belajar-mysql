# Belajar MySQL
Repo ini berisi rangkuman belajar salah satu aplikasi RDBMS yaitu MySQL. Mulai dari penginstalan, menjalankan mysql server dan mysql client hingga mempelajari berbagai query yg ada pada SQL.

# Pendahuluan
Apa itu mysql? jawaban super singkatnya adalah mysql merupakan salah satu **'aplikasi database'** yang ada saat ini. Defenisi database sendiri adalah sebuah kumpulan data yang **'terorganisasi'**. Data tidak harus berada di komputer, masih banyak kantor/perusahaan yang menyimpan catatan absen, penjualan serta laporan bulanan menggunakan kertas. Jika data-data ini dikelompokkan dan disusun menggunakan sebuah cara tertentu, itu juga sudah bisa dikatakan sebagai database.

Namun menyimpan data di kertas punya banyak kelemahan seperti mudah tercecer, sobek dan mungkin kalo jumlahnya sudah banyak akan butuh tempat yg besar juga. Di era digital sekarang ini, orang-orang mulai menyimpan data di komputer atau di internet. Contoh salah satu cara yg paling sering kita lihat untuk menyimpan/mengelola data di komputer adalah dengan menggunakan aplikasi spreadsheet seperti Microsoft Excel. 

kalo di ranah pemrograman, aplikasi database yg digunakan untuk menyimpan dan mengelola data bukan lagi excel melainkan mysql. Alasannya aplikasi seperti MySQL bisa digabung dengan bahasa pemrograman. Bahasa pemrograman ini nantinya berfungsi untuk membuat interface atau tampilan aplikasi, sedangkan datanya disimpan ke dalam MySQL. Intinya aplikasi seperti mysql ini secara khusus diciptakan sebagai aplikasi pengelola data di bidang pemrograman. that's it.

**Tambahan:** database model adalah teori dasar seputar bagaimana data itu akan disimpan, disusun, dan dimanipulasi dalam sebuah sistem database. Dalam teori database, banyak cara yang dikembangkan untuk menyimpan data di komputer, mulai dari flat model, hierarchical model, network model, relational model, hingga object oriented model. MySQL merupakan salah satu aplikasi RDBMS (*Relational Database Management System*). Pengertian sederhana dari RDBMS adalah: aplikasi database yang menggunakan prinsip relasional (relational model). Beberapa contoh lain aplikasi RDBMS: mariaDB, postgreSQL dan Oracle.

# Instalasi MySQL
Untuk mulai mempelajari mysql, tools yg kita butuhkan adalah **mysql server** dan **mysql client**. ada 2 opsi untuk mendapatkan kedua tools tersebut.
1. Instal XAMPP atau, 
2. Instal MySQL saja.

Jika tujuannya adalah mempelajari web programming maka pilihan yg pas adalah instal XAMPP karena di dalamnya terdapat semua aplikasi yg kita butuhkan dalam web development termasuk mysql. Jika hanya butuh mempelajari mysql saja, maka cukup instal mysql saja.

Di sini saya hanya ingin mempelajari mysql, maka saya hanya perlu mendownload aplikasi mysql saja. Kunjungi website resmi mysql kemudian cari mysql installer atau klik link berikut: [mysql installer](https://dev.mysql.com/downloads/) untuk mendownload aplikasi mysql.

Setelah terdownload, instal aplikasinya seperti biasa. Jika terdapat pilihan ***windows service*** pada saat instalasi, sebaiknya dinonaktifkan. ***windows service*** adalah fitur pada sistem operasi windows untuk menjalankan sebuah aplikasi secara otomatis saat komputer dinyalakan.

# Menjalankan mysql server dan mysql client
Setelah proses instalasi mysql, secara default terdapat 2 folder baru:
1. C:\Program Files\MySQL\MySQL Server 8.0 (di sinilah terdapat aplikasi mysql server dan mysql client)
2. C:\ProgramData\MySQL\MySQL Server 8.0 (berisi seluruh file database dan tabel yang ada di dalam MySQL)

## Menjalankan MySQL Server
Untuk menjalankan MySQL server, kita harus mengakses file mysqld.exe yang berada di folder bin. Buka aplikasi terminal, kalo di windows ada cmd. kemudian ketik alamat file mysqld.exe 
> C:\Program Files\MySQL\MySQL Server 8.0\bin\mysqld.exe

Cara memastikan apakah mysql server sdh berjalan, bisa dengan mengeceknya di task manager. Untuk menghentikan mysqld.exe, cara yang paling praktis adalah dari task manager juga. Di dalam tab Processes cari mysqld.exe, klik kanan, kemudian pilih End task.

## Menjalankan MySQL Client
MySQL client digunakan untuk berkomunikasi dengan MySQL server. MySQL client hadir dengan berbagai bentuk. Ada yang diakses dari cmd, berbasis web, maupun yang berbasis aplikasi desktop.

Untuk menjalankan MySQL Client, caranya mirip seperti menjalankan MySQL server, hanya saja kali ini yang diakses adalah file bin\mysql.exe
> C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql -h localhost -u root -prahasia  

Karena localhost adalah nilai default dari host (-h), perintah diatas boleh disingkat:
> C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql -u root -prahasia

Apabila MySQL server berada di komputer lain yang beralamat IP 10.12.254.14, maka perintahnya menjadi:
> C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql -h 10.12.254.14 -u root -prahasia

Dalam perintah diatas, password untuk user langsung tertulis dan mudah untuk dilihat. Agar lebih aman (dari orang yang mengintip password di belakang anda), bisa menggunakan perintah alternatif:
> C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql -u root -p

Untuk keluar dari MySQL client, ketik perintah: exit.
