﻿1. **Kernel**

**Kernel** merupakan program komputer yang menjadi inti dari sebuah sistem operasi komputer, dengan kontrol terhadap segala hal atas sistem tersebut. Pada kebanyakan sistem, kernel merupakan salah satu dari program yang dijalankan dalam urutan pertama saat komputer dinyalakan. Kernel menangani fungsi-fungsi selanjutnya atas proses penyiapan komputer dari sejak komputer dinyalakan seperti menangani layanan input/output dari program lain, menerjemahkanya ke dalam instruksi-instruksi untuk dieksekusi oleh prosesor. Kernel juga menangani perangkat kerja lain seperti memori, papan ketik, tetikus, monitor, printer, speaker, serta perangkat-perangkat lainnya.

Karena akses terhadap perangkat keras terbatas, sedangkan ada lebih dari satu program yang harus dilayani dalam waktu yang bersamaan, maka kernel juga bertugas untuk mengatur kapan dan berapa lama suatu program dapat menggunakan satu bagian perangkat keras tersebut. Hal tersebut dinamakan sebagai multiplexing.

Akses kepada perangkat keras secara langsung merupakan masalah yang kompleks, oleh karena itu kernel biasanya mengimplementasikan sekumpulan abstraksi hardware. Abstraksi-abstraksi tersebut merupakan sebuah cara untuk menyembunyikan kompleksitas, dan memungkinkan akses kepada perangkat keras menjadi mudah dan seragam. Sehingga abstraksi pada akhirnya memudahkan pekerjaan programer.

Pada dasarnya, untuk menjalankan sebuah komputer tidak harus menggunakan kernel sistem operasi. Sebuah program dapat saja langsung dijalankan oleh komputer, yaitu saat sebuah program komputer akan digunakan tanpa bantuan abstraksi perangkat keras atau bantuan sistem operasi. Teknik ini umumnya digunakan oleh komputer-komputer generasi awal, sehingga bila ingin berpindah dari satu program ke program lain, pengguna harus mereset dan menjalankan kembali program-program tersebut.

Para arsitek sistem operasi mengembangkan kernel sistem operasi yang pada akhirnya terbagi menjadi empat bagian yang secara desain berbeda, sebagai berikut:

- **Kernel monolitik**. Kernel monolitik mengintegrasikan banyak fungsi di dalam kernel dan menyediakan lapisan abstraksi perangkat keras secara penuh terhadap perangkat keras yang berada di bawah sistem operasi.
- **Mikrokernel**. Mikrokernel menyediakan sedikit saja dari abstraksi perangkat keras dan menggunakan aplikasi yang berjalan di atasnya—yang disebut dengan server—untuk melakukan beberapa fungsionalitas lainnya.
- **Kernel hibrida**. Kernel hibrida adalah pendekatan desain microkernel yang dimodifikasi. Pada hybrid kernel, terdapat beberapa tambahan kode di dalam ruangan kernel untuk meningkatkan performanya.
- **Eksokernel**. Eksokernel menyediakan hardware abstraction secara minimal, sehingga program dapat mengakses hardware secara langsung. Dalam pendekatan desain exokernel, library yang dimiliki oleh sistem operasi dapat melakukan abstraksi yang mirip dengan abstraksi yang dilakukan dalam desain kernel monolitik.



1. **Directory in Linux**

**General Files** – Ini juga disebut file biasa. Ini mungkin berupa gambar, video, program, atau file teks sederhana. Jenis file ini bisa dalam format ASCII atau Biner. Ini adalah file yang paling umum digunakan dalam sistem Linux.

**Directory Files** – Jenis file ini adalah gudang untuk jenis file lainnya. Ini mungkin file direktori di dalam direktori (subdirektori).

**Device Files** – Dalam sistem operasi mirip Windows, perangkat seperti CD-ROM, dan hard drive direpresentasikan sebagai huruf drive seperti F:G:H sedangkan di perangkat sistem Linux direpresentasikan sebagai file. Seperti misalnya /dev/sda1, /dev/sda2 dan seterusnya.

**Ini adalah direktori tingkat atas umum yang terkait dengan direktori root:**

/bin – binary or executable programs.

/etc – system configuration files.

/home – home directory. It is the default current directory.

/opt – optional or third-party software.

/tmp – temporary space, typically cleared on reboot.

/usr – User related programs.

/var – log files.

**Beberapa direktori lain di sistem Linux:**

/boot- Ini berisi semua file dan folder informasi terkait boot seperti conf, grub, dll.

/dev – Ini adalah lokasi file perangkat seperti dev/sda1, dev/sda2, dll.

/lib – Ini berisi modul kernel dan pustaka bersama.

/lost+found – Digunakan untuk menemukan bit yang dipulihkan dari file yang rusak.

/media – Ini berisi subdirektori tempat perangkat media penghapusan dimasukkan.

/mnt – Ini berisi direktori pemasangan sementara untuk memasang sistem file.

/proc - Ini adalah sistem file virtual dan pseudo untuk berisi info tentang proses yang berjalan dengan ID proses atau PID tertentu.

/run – Ini menyimpan data runtime yang mudah menguap.

/sbin – program yang dapat dieksekusi biner untuk administrator.

/srv – Ini berisi file khusus server dan terkait server.

/sys – Ini adalah sistem file virtual untuk distribusi Linux modern untuk menyimpan dan memungkinkan modifikasi perangkat yang terhubung ke sistem.



1. **Perbedaan SU dengan SUDO**

**SU** – adalah super user dan dikhususkan untuk anakan ubuntu dan perintah ini termasuk perintah command-line. Dengan menjalankan perintah ini, user akan diminta untuk login sebagai root, user dapat dengan mudah menjalankan semua perintah, tanpa dibatasi oleh apapun.

**SUDO** – adalah program yang terdapat di linux yang digunakan untuk menjalankan perintah yang membutuhkan akses dari akun root. Sudo hanya dapat digunakan oleh user yang sudah terdaftar di file /etc/sudoers. Pada saat dijalankan sudo akan meminta password user yang menjalankan sudo tersebut, tetapi bisa juga dibuat untuk meminta password root atau tanpa password sama sekali. Secara default password yang dimasukkan tadi akan disimpan selama 15 menit dan 15 menit kedepan anda akan diminta memasukan password lagi.



1. **Repositori Linux**

**Repositori Linux** adalah lokasi penyimpanan tempat sistem Anda mengambil dan menginstal pembaruan dan aplikasi OS. Setiap repositori adalah kumpulan perangkat lunak yang di-host di server jauh dan dimaksudkan untuk digunakan untuk menginstal dan memperbarui paket perangkat lunak pada sistem Linux. Ketika Anda menjalankan perintah seperti “sudo apt update” atau “sudo apt upgrade”, Anda mungkin menarik informasi paket dan memperbarui paket dari sejumlah repositori.

- **Main** – perangkat lunak sumber terbuka yang didukung secara resmi. Canonical memberikan dukungan resmi untuk paket-paket ini. Setiap paket perangkat lunak sumber terbuka yang disertakan dalam instalasi default disertakan bersama dengan beberapa paket penting lainnya.
- **Restricted** – yang didukung secara resmi, perangkat lunak sumber tertutup – mis., Driver perangkat keras – didukung selama rilis.
- **Universe** – dikelola komunitas, sumber terbuka. Mayoritas perangkat lunak Ubuntu berasal dari repositori ini. Canonical tidak memberikan dukungan atau pembaruan resmi.
- **Multiverse** – perangkat lunak yang tidak didukung, sumber tertutup, dan terbebani paten.



1. **Perintah APT**

Dalam linux digunakan untuk menginstal, memperbarui, menghapus dan mengelola paket di distro linux yang berbasis debian. Perintah ini harus digunakan dengan menggunakan sudo karena memerlukan hak akses khusus. Ada beberapa yang bisa dilakukan apt

**- Mengupdate indeks package**

Ini digunakan dengan melakukan perintah sudo apt update, yang mana fungsinya indeks paket yang berada dilinux. Pada dasarnya linux menyimpan indeks package di semacam database dimana untuk mengupdate harus di update indeksnya

**- Mengupgrade indeks package**

Perintah ini dilakukan untuk mengupgarde versi package menjadi yang terbaru. Cara penulisannya dengan sudo apt upgrade, jika tidak dispesifikan package nya maka akan menupgrade banyak/semua package yang ready untuk diupgrade. Contoh yang menspesifikan package sudo apt upgrade firefox.

**- Menginstall package**

Salah satu perintah penting lainnya adalah menginstall package dengan sudo apt install <nama package> maka akan mendownload package dari repository. Bisa juga langsung menggunakan file .deb caranya sudo apt install /file/package.deb.

**- Menghapus package**

Untuk menguninstal paket dengan menggunakan apt, gunakan perintah berikut :

sudo apt remove package\_name Kita juga dapat menentukan beberapa paket untuk di uninstall. Perintah remove akan menghapus instalasi paket yang diberikan tetapi mungkin meninggalkan beberapa file konfigurasi. Jika Anda ingin menghapus paket termasuk semua file konfigurasi gunakan perintah purge alih-alih remove sudo apt purge package\_name
