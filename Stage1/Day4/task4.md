# Definisi Git
Git merupakan sebuah pengendali versi untuk mengelola versi source code program dengan menentukan baris serta kode yang akan ditambahkan atau diganti.
 
# Rubah IP address di PC kalian (tes menggunakan command ssh)
Bisa dengan menggunakan perintah berikut untuk mengganti IP.

sudo nano /etc/netplan/00-installer-config.yaml

![Screenshot (264)](https://user-images.githubusercontent.com/109257850/202496914-ea544f44-d7c6-46e5-95f2-c121fe13b7ec.png)
yang awalnya ip-nya 192.168.0.170/24 akan di ganti ke 192.168.0.171/24 lalu setelah itu bisa menjalankan perintah -> netplan apply untuk menerapkan perubahan IP nya.
![Screenshot (269)](https://user-images.githubusercontent.com/109257850/202497419-a3c89bf0-e1b6-4f6f-8fbf-24c2c0801485.png)
(hasil dari penggantian alamat ip berhasil dan bisa menjalankan ping google.com)
![Screenshot (270)](https://user-images.githubusercontent.com/109257850/202498135-ead383fe-6326-4385-90f7-f37b4290fc18.png)

Setelah itu akan test menggunakan test mengunakan ssh, gunakan perintah -> ssh (username)@(ip kalian).
Dibawah merupakan contoh jika berhasil menggunakan test ssh

![Screenshot (268)](https://user-images.githubusercontent.com/109257850/202499014-40b82da5-5511-4aee-aeae-8fc8618eb816.png)


# Hubungkan github ke server yang kita miliki. 

Bisa menggunakan perintah berikut untuk menghubungkan akun github:

git config --global user.name "your.github-user.name"
git config --global user.email "your.github-user.email"

![Screenshot (273)](https://user-images.githubusercontent.com/109257850/202591302-025c6b04-a0d5-4022-bf27-c907dd6470e4.png)

# Membuat 3 branch untuk repository 

Bisa menggunakan perintah berikut:

# 1. git branch
git branch <nama branch-nya>
 
![Screenshot (282)](https://user-images.githubusercontent.com/109257850/202596303-322354b0-1515-4094-a1d0-a01962efca2e.png)

 # 2. git checkout 
 Perintah ini adalah untuk berpindah branch 
 
 ![Screenshot (283)](https://user-images.githubusercontent.com/109257850/202596476-a35c0f5f-4d81-4880-aa1c-ad7b17af1134.png)

 # 3. git branch -m
Perintah diatas untuk membuat branch baru serta pindah kedalam branch tersebut

 ![Screenshot (285)](https://user-images.githubusercontent.com/109257850/202596689-bc3dac91-0c5a-446a-bf52-cbef91dcb051.png)
 ![Screenshot (286)](https://user-images.githubusercontent.com/109257850/202596910-959fa446-7e5c-4a7c-9650-c754dc12bb4f.png)
 
 ![Screenshot (290)](https://user-images.githubusercontent.com/109257850/202597589-285b7cab-66b7-472b-a565-3f7230c108fe.png)
git branch -a adalah untuk melihat list branch yang dimiliki

# 3 command git yang belum dijelaskan
 - Git log adalah perintah untuk melihat riwayat pada project
 - Git merge adalah suatu perintah untuk membuat branch yang bercabang menjadi satu kembali
 - Git diff memberitahu kita secara mendetail apa saja perubahan yang terjadi di antara dua titik referensi Git.









































