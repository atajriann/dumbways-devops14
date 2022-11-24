# Definisi Web Server
Web server merupakan sebuah sofware yang memberikan layanan berupa data. Berfungsi untuk menerima HTTP/HTTPS dari klien yang dikenal sebagai browser dan akan mengirimkan respon dalam berbentuk halaman web.
 
# Jalankan 2 VM
Disini saya akan membuat 2 VM, VM pertama saya membuatnya di wsl dan untuk VM kedua saya membuanya di virtual box.

VM 1 
![Screenshot (377)](https://user-images.githubusercontent.com/109257850/203689540-4f586f54-f2d8-4269-b923-f6989ed3c5b6.png)
![Screenshot (378)](https://user-images.githubusercontent.com/109257850/203689567-e899b7c0-1565-436a-9532-cdded2f2cbbf.png)

VM 2  
![Screenshot (379)](https://user-images.githubusercontent.com/109257850/203689635-49520a86-6a68-4957-afa7-2073d7889ad2.png)
![Screenshot (380)](https://user-images.githubusercontent.com/109257850/203689642-6339c852-d835-43a6-bee1-d361540d4ec1.png)

# VM 1  
# dumbflix-frontend (appserver)
![Screenshot (382)](https://user-images.githubusercontent.com/109257850/203690105-09c6d2d6-137a-4378-b142-f2f4a74e2816.png)

PM2 
![Screenshot (381)](https://user-images.githubusercontent.com/109257850/203690152-8e20884b-8b34-4b49-a296-9a7f34f1550c.png)

lalu setting firewall nya agar dapat di akses di pc utama
-> ufw enable
-> ufw allow 3000
![Screenshot (388)](https://user-images.githubusercontent.com/109257850/203693259-56aa9e03-b5dd-4814-8fbe-eee22a571da4.png)




#VM 2
Jalankan nginx: - sudo systemctl enable nginx
                - sudo systemctl start nginx
 
![Screenshot (384)](https://user-images.githubusercontent.com/109257850/203694939-bccc5858-0995-4878-9c34-c42e2283ad24.png)
![Screenshot (380)](https://user-images.githubusercontent.com/109257850/203690267-e8f9c333-d45d-4782-b62a-d4989c5c9808.png)

Lalu cek di browser dengan memasuk ip kita yang ada di virtualbox

Contoh kalau sudah berhasil 
![Screenshot (389)](https://user-images.githubusercontent.com/109257850/203695586-27daf638-e309-4730-a6c2-c57b96ab3621.png)

Lanjut, kita akan menkofigurasi reverse proxy 
Masuk ke direktori nginx dengan perintah:
- cd /etc/nginx  
- sudo mkdir ajaytajrian (membuat direktori)
- cd ajaytajrian (masuk kedirektori ajaytajrian) 
- sudo nano my.reverse-proxy.conf (buat file)
- lalu masukan konfigurasi dibawah ini:

server {
    server_name ajaytajrian.xyz;
    
    location / {
             proxy_pass http://172.19.29.245:3000;
    }
}
 
 Sesuaikan server_name dengan nama domain yang ingin anda pakai lalu sesuaikan proxy_pass dengan IP pada virtual machine pertama
 
 
Setelah di save kembali ke direktori /etc/nginx -> cd ..
 
Lalu -> sudo nano nginx.conf
 ![Screenshot (391)](https://user-images.githubusercontent.com/109257850/203715732-e51ae0eb-5fe3-42d6-845e-575fa8563f5e.png)

Selanjutanya pergi ke bagian *include*, setelah itu masukan lokasi file konfigurasi yang tadi dibuat
 ![Screenshot (390)](https://user-images.githubusercontent.com/109257850/203716031-c0d5c3bc-66ea-4924-ae8b-a28b12b47389.png)

INFO:
/*; menandakan file nginx.conf akan membaca seluruh file yang berada di dalam directory dumbways
 
 
Beberapa proses tadi adalah cara untuk membuat reverse proxy untuk aplikasi kita, kemudian pastikan untuk melakukan pengecekan konfigurasi dengan menjalankan
perintah :
 -> sudo nginx -t
 ![Screenshot (392)](https://user-images.githubusercontent.com/109257850/203716611-bb62f7a0-1509-410b-abec-39bb29ed33f8.png)

 Jika sudah kita tinggal melukukan restart/reload nginx kita
 -> sudo systemctl restart nginx
 
 Sekarang kita perlu setting virtual host nya, untuk os window file nya ada: ->> c:\Windows\System32\Drivers\etc\hosts
 
 Lalu masukan IP dari virtual machine nginx, serta nama domain yang akan kita gunakan
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
