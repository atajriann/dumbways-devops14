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
Cat
- Buat file script nya
- Di baris pertama kita ketikan "#! /env/usr/env bash" untuk bisa menjalankan script
- lalu ketikan seperti gambar dibawah: 
![Screenshot (339)](https://user-images.githubusercontent.com/109257850/203336487-6279c417-c9b5-4af1-8bb5-02c4d15e8b5a.png)
![Screenshot (340)](https://user-images.githubusercontent.com/109257850/203336506-4b40ad0f-f441-41d7-a2f4-682c1faf332a.png)
 
Grep
![Screenshot (344)](https://user-images.githubusercontent.com/109257850/203339108-d3089b21-d12f-47eb-9405-d1b56b3d4e8b.png)
![Screenshot (345)](https://user-images.githubusercontent.com/109257850/203339121-6af57e87-e564-4e9d-b942-d2cb097f67de.png)

Echo
![Screenshot (346)](https://user-images.githubusercontent.com/109257850/203339612-c0d3ccc7-b333-4729-91fa-bf80ee451ba1.png)
![Screenshot (347)](https://user-images.githubusercontent.com/109257850/203339676-53ab3f68-0722-496d-bcb0-35add583b4b7.png)

Sort
![Screenshot (342)](https://user-images.githubusercontent.com/109257850/203338321-f6db30db-e2e2-476e-810a-e76812a5c84d.png)
![Screenshot (343)](https://user-images.githubusercontent.com/109257850/203338335-c882e2c5-0a12-42f3-bc14-24a4caad827b.png)

Mengganti text 'Dumbways' ke 'Bootcamp'

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


































