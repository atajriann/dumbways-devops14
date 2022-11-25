# Definisi Web Server
Web server merupakan sebuah sofware yang memberikan layanan berupa data. Berfungsi untuk menerima HTTP/HTTPS dari klien yang dikenal sebagai browser dan akan mengirimkan respon dalam berbentuk halaman web.
 
# Jalankan 2 VM
Disini saya akan membuat 2 V di 1 Virtual Box, VM pertama saya namakan Ubuntu-Server1 dan untuk VM kedua saya namakan Ubuntu-server

VM 1 (Install Nodejs)
![Screenshot (402)](https://user-images.githubusercontent.com/109257850/203879662-252ed264-7f5b-47d7-b699-8d61122bfe70.png)
![Screenshot (403)](https://user-images.githubusercontent.com/109257850/203880271-cc2a77c5-07d5-4a88-babf-fcfeb5968076.png)

VM 2  
![Screenshot (379)](https://user-images.githubusercontent.com/109257850/203689635-49520a86-6a68-4957-afa7-2073d7889ad2.png)
![Screenshot (380)](https://user-images.githubusercontent.com/109257850/203689642-6339c852-d835-43a6-bee1-d361540d4ec1.png)

# VM 1  
# dumbflix-frontend (appserver) -> git clone https://github.com/dumbwaysdev/dumbflix-frontend
![Screenshot (407)](https://user-images.githubusercontent.com/109257850/203880444-e536cc04-04db-466c-8bb5-33efa8dbd509.png)

Setelah git clone lalu masuk ke direktorinya dumbflix dan lalukan install npm untuk menginstall depedensi yang dilalukan
-> npm install
![Screenshot (409)](https://user-images.githubusercontent.com/109257850/203881879-ba758c60-4395-424d-83df-6846f0f4d0ba.png)

Lalu jalankan pm2 dengan perintah :
-> pm2 start npm --name "dumbflix-frontend" --start

![Screenshot (414)](https://user-images.githubusercontent.com/109257850/203884636-fe8759d4-cbc0-4fb5-80bb-ffe71cc96a7f.png)

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
 ![Screenshot (416)](https://user-images.githubusercontent.com/109257850/203886589-32939f70-4da1-48d5-8d2f-4505ca903cc0.png)

Lalu masukan IP dari virtual machine nginx, serta nama domain yang akan kita gunakan
 ![Screenshot (417)](https://user-images.githubusercontent.com/109257850/203886660-9a02d7b7-6e43-4acb-9e3c-140fa3909150.png)

# Membuat 2 konfigurasi load balance antara VM1 dan VM2
Install dan jalankan dumbflix di vm2

setelah itu kita perlu masuk ke dalam konfigurasi reverse proxy yang sudah kita buat sebelumnya
-> sudo nano /etc/nginx/ajaytajrian/ajaytajrian_proxy.conf

selanjutnya, tambahkan konfigurasi ke IP di vm kedua

upstream domain {
    server 192.168.0.11:3000;
    server 192.168.0.7:3000;
}
server {
    server_name ajaytajrian.xyz;

    location / {
             proxy_pass http://domain;
    }
}
 
![Screenshot (418)](https://user-images.githubusercontent.com/109257850/203890077-2bac310d-681f-490a-8744-78f995d692a7.png)

lalu lakukan cek syntak -> sudo nginx -t
lalu lakukan restart -> sudo systemctl restart nginx 
 

 
 
 
 
 
 
 
 
 
 
 
 
