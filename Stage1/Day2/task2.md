# Perbedaan antara IP private & public?
IP public adalah alamat IP yang digunakan dalam jaringan global Internet. Sedangkan untuk IP private adalah alamat IP yang digunakan dalam jaringan local dan tidak bisa diakses dari jaringan internet secara langsung.

# Perbedaan antara IP dinamis & statis?

Perbedaan antara IP Statis dan Dinamis terletak pada durasi alamat IP yang ditetapkan. IP statis adalah alamat IP yang ditetapkan secara manual ke suatu perangkat untuk jangka waktu yang lama. Tentunya berbeda dengan IP dinamis, alamat IP Dinamis sering berubah setiap kali pada saat si pengguna melakukan boot pada mesinnya, dan secara otomatis akan ditetapkan.

# Install web server Apache2 secara manual 

Sebelum menginstall Apacha2 atau apapun itu, diharuskan untuk menjalankan commands "apt-update" terlebih dahulu supaya semuanya up to date.

Selanjutnya anda bisa menjalan perintah dibawah ini untuk install  
sudo apt-get install apache2 

Lalu akan akan di akan muncul seperti gambar dibawah ini 

![Screenshot (200)](https://user-images.githubusercontent.com/109257850/202212795-e800af0a-aa12-4ec6-bf44-406c8014b51f.png)

Lalu jalankan perintah dibawah ini untuk install Apache2
sudo apt install apache2

![Screenshot (201)](https://user-images.githubusercontent.com/109257850/202213292-96d8ab44-8f39-4556-8949-cc4c35bd1311.png)
(Tampilan saya seperti diatas karena sebelumnya udah terinstal Apache2 nya" dan tentunya berbeda bila anda belum install Apache2 nya juga)

Jika sudah selesai, bisa gunakan perintah cek status apache2 nya dengan menggunakan:
sudo systemctl status apache2

![Screenshot (203)](https://user-images.githubusercontent.com/109257850/202216289-65bbb796-547b-4cc3-95d9-610b86ef6195.png)

Bila sudah seperti gambar diatas, lalu anda ketik "localhost" di browser anda ntah itu google atau microsoft edge, jika keluar gammbar di bawah tandanya anda berhasil deploy web servernya.

![Screenshot (204)](https://user-images.githubusercontent.com/109257850/202228095-2a954fc1-4edc-4af6-b76d-4a27bd33ceda.png)








































