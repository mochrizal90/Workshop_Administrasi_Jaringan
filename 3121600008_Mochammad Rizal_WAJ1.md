# Laporan Workshop Administrasi Jaringan
Nama : Mochammad Rizal
NRP : 3121600008
Kelas :  2 D4 IT A

Laporan kali ini akan membahas tentang kernel, struktur direktori, perbedaan sudo dan su, jenis repository, dan perintah apt.


# 1. Identifikasi Kernel
Kernel adalah bagian inti dari sebuah sistem operasi yang bertanggung jawab untuk mengelola sumber daya komputer seperti CPU, memori, dan perangkat input/output. dan juga memungkinkan melakukan komunikasi antara perangkat keras dan perangkat lunak yang berjalan pada sistem operasi, serta menyediakan layanan seperti manajemen proses, manajemen memori, manajemen file, dan manajemen jaringan. Kernel juga bisa mengontrol akses ke sumber daya komputer dan memastikan bahwa perangkat lunak yang berjalan di atasnya tidak merusak sistem secara tidak sengaja atau sengaja.

Terdapat 2 perintah bash yang saya ketahui untuk melihat versi kernel, yaitu :

    uname -a
dan

    uname -r
untuk yang uname -a berguna untuk menampilkan informasi sistem secara lengkap, termasuk nama host, versi kernel, jenis arsitektur sistem, dan informasi sistem lainnya. Sedangkan untuk uname -r hanya akan menampilkan nomor versi kernel saja.

![uname](https://user-images.githubusercontent.com/126677063/223571452-f92a544e-bb44-4dd7-aafa-96e739153862.png)
Pada gambar di atas, terlihat bahwa ubuntu saya memiliki versi kernel 5.15.0-60-generic.

<br/>

# 2. Identifikasi Directory Structure

![direktori](https://user-images.githubusercontent.com/126677063/223571472-59b32993-eae9-47d4-b32e-6cf2e0d3d650.png)

Berikut penjelasan dari beberapa struktur direktori yang saya temukan :
1. **/bin** : berfungsi untuk eksekutabel tabel file (semua user bisa melakukannya).
2. **/sbin** : berfungsi untuk eksekutabel tabel file (super user bisa melakukannya).
3. **/root** : menyimpan file konfigurasi, skrip shell, dll yang berkaitan dengan pengguna root.
4. **/usr** : berfungsi untuk menyimpan program dan data. 
5. **/opt** : berisi untuk aplikasi aplikasi optional.
6. **/etc** : berisi file konfigurasi sistem dan aplikasi.
7. **/lib** : berisi library yang dibutuhkan oleh program yang terinstal di sistem.
8. **/temp** : berfungsi untuk menyimpan data / file sementara (temporary files).
9.  **/var** : berisi file yang sering berubah, seperti log sistem.

<br/>

# 3. Identifikasi Perbedaan **su** dengan **sudo**
**su** dan **sudo** adalah dua perintah pada sistem operasi Linux yang digunakan untuk mendapatkan akses root atau superuser (pengguna dengan hak akses tertinggi) dalam terminal. Kedua perintah ini dapat berguna dalam situasi di mana pengguna memerlukan akses root untuk menjalankan perintah tertentu, seperti memperbarui sistem atau menginstal perangkat lunak.

**su** ("**switch user**") adalah suatu perintah yang memungkinkan pengguna untuk beralih ke akun pengguna lain, termasuk akun root, dan menjalankan perintah sebagai akun tersebut. Perintah **su** memerlukan kata sandi akun yang akan diakses.

**sudo** ("**superuser DO**") adalah suatu perintah yang memungkinkan pengguna biasa untuk menjalankan perintah sebagai root atau pengguna lain dengan hak akses yang lebih tinggi. Perintah "sudo" memerlukan masukan kata sandi pengguna untuk memastikan bahwa pengguna yang meminta hak akses tambahan memiliki hak akses yang sah. Setelah kata sandi yang benar dimasukkan, perintah yang dijalankan dijalankan dengan hak akses **superuser**.

    sudo su
![](https://user-images.githubusercontent.com/126677063/223571470-cc23e60f-3df0-4f04-90fc-22639bbc05e6.png)

    sudo su -
![](https://user-images.githubusercontent.com/126677063/223571465-13fdd40b-0909-4328-b03b-d9cd09b37488.png)

<br/>

# 4. Identifikasi Jenis Repository
    nano /etc/apt/sources.list
![](https://user-images.githubusercontent.com/126677063/223571458-977da2d5-a7b8-4174-9665-fc3392ec6f18.png)

Berikut maksud dari isi file sources.list :
- **deb http://archive.ubuntu.com/ubuntu/ focal main restricted** : repository utama yang berisi paket-paket utama yang didukung oleh Ubuntu, baik untuk sistem inti (main) maupun untuk driver perangkat keras terbatas (restricted) dari Ubuntu 20.04 LTS.

- **deb http://archive.ubuntu.com/ubuntu/ focal-updates main restricted** : ini adalah repository untuk sumber perangkat lunak (repository) yang digunakan untuk memperbarui paket baik untuk sistem inti (main) maupun untuk driver perangkat keras terbatas (restricted) dari Ubuntu 20.04 LTS.

- **deb http://archive.ubuntu.com/ubuntu/ focal universe** : ini adalah repository yang sumber perangkat lunak bebas dan terbuka yang digunakan untuk menginstal dan memperbarui paket pada sistem operasi Ubuntu.

- **deb http://archive.ubuntu.com/ubuntu/ focal-updates universe** : ini adalah repositori yang berisi pembaruan-pembaruan dari paket-paket yang telah dirilis sebelumnya di komponen universe yang berisi paket-paket perangkat lunak bebas dan terbuka, yang tidak termasuk dalam repositori utama Ubuntu.

- **deb http://archive.ubuntu.com/ubuntu/ focal multiverse** : komponen tambahan dalam repository Ubuntu yang berisi paket-paket perangkat lunak yang tidak sepenuhnya bebas dan memerlukan dukungan teknis tambahan. Paket-paket ini dapat mengandung kode-kode sumber tertutup, lisensi tidak bebas, atau fitur-fitur yang dibatasi penggunaannya.

- **deb http://archive.ubuntu.com/ubuntu/ focal-updates multiverse** : ini adalah repositori yang berisi pembaruan-pembaruan dari paket-paket yang telah dirilis sebelumnya di komponen multiverse yang berisi paket-paket perangkat lunak yang tidak sepenuhnya bebas dan memerlukan dukungan teknis tambahan.

- **deb http://archive.ubuntu.com/ubuntu/ focal-backports main restricted universe multiverse** : ini adalah repositori yang berisi versi terbaru dari paket-paket perangkat lunak yang telah dirilis sebelumnya dalam komponen "main", "restricted", "universe", dan "multiverse". Repositori ini dirancang untuk menyediakan pembaruan yang lebih baru dari paket-paket perangkat lunak yang terdapat dalam versi Ubuntu saat ini, yang mungkin belum tersedia di repositori standar Ubuntu.

- **deb http://security.ubuntu.com/ubuntu/ focal-security main multiverse** : ini adalah Repositori ini menyediakan pembaruan keamanan untuk paket-paket perangkat lunak yang telah dirilis sebelumnya dalam komponen "main" dan "multiverse".

<br/>

# 5. Identifikasi Perintah **apt**

- **apt list** = menampilkan daftar paket yang sudah terinstall
- **apt update** = memperbarui daftar paket yang tersedia di repository
- **apt install** = menginstal paket baru
- **apt remove** = menghapus paket yang sudah terisntall
- **apt autoremove** = Menghapus semua paket yang tidak dibutuhkan secara otomatis
- **apt search** = mencari dalam deskripsi paket
- **apt show** = menampilkan informasi detail paket
- **apt upgrade** = memperbarui daftar paket yang ada di repository
- **apt full-upgrade** = memperbarui sistem dengan menghapus/menginstal/memperbarui paket