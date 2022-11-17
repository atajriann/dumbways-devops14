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















