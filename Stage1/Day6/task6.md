# Perbedaan antara Shell dan BASH
Shell adalah sebuah penerjemah command line yang menerjemah yang ditulis oleh pengguna di terminal, ke dalam tindakan sistem yang dijalankan, yang juga dapat secara otomatis dijalankan dalam program yang disebut Shell Scripting. Sedangkan BASH (Bourne Again Shell) adalah jenis dari shell. Fungsinya kurang lebih sama. Bash adalah sripting pemrograman kumpulan perintah menggunakan script yang ditulis ke dalam bash shell, sehingga nantinya dapat dieksekusi oleh sistem operasi. 

# BASH script update dan upgrade server
1. Buat file script nya di text editor, kali ini saya membuatnya di text editor nano dengan nama "task2.sh"
- Di baris pertama kita ketikan "#! /env/usr/env bash" untuk bisa menjalankan script.
- Lalu ketikan sudo apt update && sudo apt upgrade
- Setelah selesai ubah dulu permission file nya agar bisa di execution
- Lalu jalankan filenya dengan perintah -> ./task2.sh
![Screenshot (333)](https://user-images.githubusercontent.com/109257850/203273406-ffacf11c-9d96-42fd-a7fd-acf17d42f3ef.png)
![Screenshot (334)](https://user-images.githubusercontent.com/109257850/203275648-b1a03dc2-4b59-47dc-bee5-8def4e81a507.png)

# BASH script untuk memberi akses ke port 22,80,443
- Buat file nya sama seperti tugas di atas
- Di baris pertama kita ketikan "#! /env/usr/env bash" untuk bisa menjalankan script
- Lalu ketikan : - sudo ufw allow 22
                 - sudo ufw allow 80
                 - sudo ufw allow 443
![Screenshot (335)](https://user-images.githubusercontent.com/109257850/203328714-c292ad46-e5c7-4cad-b080-496ffd75e6f8.png)
![Screenshot (336)](https://user-images.githubusercontent.com/109257850/203329021-d92ec897-8ff6-48da-b2b8-1c6ef5740558.png)
![Screenshot (337)](https://user-images.githubusercontent.com/109257850/203329064-9c5f43b5-bedb-42cb-9c8e-5ddcca4096d8.png)

# Text Manipulation 
Cat:
- Buat file script nya
- Di baris pertama kita ketikan "#! /env/usr/env bash" untuk bisa menjalankan script
- lalu ketikan seperti gambar dibawah: 
![Screenshot (339)](https://user-images.githubusercontent.com/109257850/203336487-6279c417-c9b5-4af1-8bb5-02c4d15e8b5a.png)
![Screenshot (340)](https://user-images.githubusercontent.com/109257850/203336506-4b40ad0f-f441-41d7-a2f4-682c1faf332a.png)
 
Grep:
![Screenshot (344)](https://user-images.githubusercontent.com/109257850/203339108-d3089b21-d12f-47eb-9405-d1b56b3d4e8b.png)
![Screenshot (345)](https://user-images.githubusercontent.com/109257850/203339121-6af57e87-e564-4e9d-b942-d2cb097f67de.png)

Echo:

![Screenshot (346)](https://user-images.githubusercontent.com/109257850/203339612-c0d3ccc7-b333-4729-91fa-bf80ee451ba1.png)
![Screenshot (347)](https://user-images.githubusercontent.com/109257850/203339676-53ab3f68-0722-496d-bcb0-35add583b4b7.png)

Sort:

![Screenshot (342)](https://user-images.githubusercontent.com/109257850/203338321-f6db30db-e2e2-476e-810a-e76812a5c84d.png)
![Screenshot (343)](https://user-images.githubusercontent.com/109257850/203338335-c882e2c5-0a12-42f3-bc14-24a4caad827b.png)

Mengganti text 'Dumbways' ke 'Bootcamp'
1. pertama buat filenya dan isikan "bonjour dumbays" di file dumwbays.txt
![Screenshot (372)](https://user-images.githubusercontent.com/109257850/203485485-ab5cd548-df13-4afe-ae4b-8ef5890c018f.png)

lalu buat file nano lagi dengan nama <bebas>, kali ini saya menamainya dengan -> nano dumbwaysv2.sh
lanjut masukan perintah berikut: - #!bin/bash
                                 - sed -i 's/nama_awal/nama_yang_ingin_diganti/g' 
![Screenshot (370)](https://user-images.githubusercontent.com/109257850/203485744-0d41a011-f426-4810-b314-6b538924c075.png)
Hasilnya dibawah ini:
![Screenshot (371)](https://user-images.githubusercontent.com/109257850/203485809-b8771632-2615-47d9-8ef0-fe1298af2639.png)

# Contoh Penggunaan Monitoring 
Monitoring adalah aktivitas untuk melihat kinerja sistem secara realtime. Berikut ini adalah beberapa perintah yang dapat kita gunakan untuk memonitoring sebuah server.

# 1. htop
htop merupakan perintah untuk memonitoring sistem, kita dapat melihat penggunaan memory, cpu, swap. Ketikkan perintah htop diterminal untuk membukanya, jika htop belum terinstall maka install dulu menggunakan perintah -> sudo apt install htop -y

Buka htop dengan mengetikan htop di terminal
![Screenshot (349)](https://user-images.githubusercontent.com/109257850/203342978-14621053-4c76-4b41-b36c-13af894bab19.png)
![Screenshot (348)](https://user-images.githubusercontent.com/109257850/203343060-488ed884-7b9e-495b-be2d-099b070f4cb9.png)

Keterangan :

- CPU adalah berapa jumlah core yang kita miliki.
- Mem adalah total penggunaan memory.
- Swp adalah Memory cadangan.
- Tasks adalah aplikasi yang sedang berjalan di server.
- Load average adalah rata-rata aplikasi yang berjalan.
- Uptime adalah berapa lama server kita hidup.
- PID adalah nomor proses id setiap proses yang berjalan di linux.
- VIRT adalah memory yang terpakai.
- Command adalah perintah apa yang sedang di jalankan.

# 2. nmon
Untuk instalasi nmon bisa menggunakan perintah -> sudo apt install nmon
![Screenshot (352)](https://user-images.githubusercontent.com/109257850/203455611-cd47d2f6-5f98-4cd9-9815-e0a55101e53a.png)
![Screenshot (353)](https://user-images.githubusercontent.com/109257850/203455621-4ca15b02-da12-4d6d-9e90-456ecddc2fcc.png)

Lalu untuk menjalankannya ketikkan nmon diterminal
![Screenshot (354)](https://user-images.githubusercontent.com/109257850/203455881-f4df1b5b-c16a-4928-8287-00cb37c1fa2e.png)

Keterangan : Kita dapat memilih ingin memonitoring apa saja, Disini kita coba saja untuk menampilkan beberapa saja.

- c adalah CPU
- m adalah Memory
- d adalah Disk
- n adalah network

# 3. lsof
Lsof merupakan singkatan list open files, berfungsi untuk melihat seluruh file yang terbuka berdasarkan proses aktif yang berjalan di sistem.

![Screenshot (363)](https://user-images.githubusercontent.com/109257850/203479883-3a813dcd-949b-45d5-ae63-5bb7845d590d.png)

# 4. ps
ps -f -u <your-user> 
  
![Screenshot (364)](https://user-images.githubusercontent.com/109257850/203480405-6f6c7e82-7e39-470e-9f4a-22fb4b63bf40.png)

# Buat script instalasi node version manager menggunakan BASH
  
![Screenshot (374)](https://user-images.githubusercontent.com/109257850/203678654-e1ec6f39-e1aa-4382-b4c7-8df2d66ac9ca.png)

![Screenshot (376)](https://user-images.githubusercontent.com/109257850/203678687-34fb92d2-201b-45e0-862b-59eac70c89e4.png)
































