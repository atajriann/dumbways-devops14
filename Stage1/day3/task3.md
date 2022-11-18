# Perbandingan antara Monolith & Microservices
Arsitektur monolith atau monolitik adalah menempatkan berbagai komponen (seperti authentication service, order service, account service, dll) di satu unit yang sama karena disimpan di satu unit yang sama dan saling berkaitan, bila satu komponen mengalami error, kemungkinan besar komponen yang lain akan terkendala.
Jika monolitik adalah sebuah arsitektur aplikasi secara kesatuan atau tunggal, maka microservices adalah sebaliknya. Microservices terbagi menjadi unit pecahan yang lebih kecil dan spesifik. Setiap unitnya terpisah dan memiliki sistem beserta database. Seandainya terjadi kendala di satu unit, kemungkinan unit lainnya tidak ikut mengalami error.

# Make Simple Application

Di sini saya akan menggunakan Node.js, Golang, dan Python sebagai dasar dari pembuatan simple application.

# Deploy alplikasi ways-hub-frontend (Node.js)
Saya akan mendeploy sebuah aplikasi yang sudah tersedia di link github berikut: https://github.com/dumbwaysdev/wayshub-frontend

Sekarang saya akan berinteraksi dengan konsol ini. Dengannya, kita akan melakukan banyak hal. Pertama, mari kita clone (salin/unduh) repositori GitHub yang diperlukan terlebih dahulu. Jalankan perintah berikut ini.
git clone https://github.com/dumbwaysdev/wayshub-frontend.git

![Screenshot (209)](https://user-images.githubusercontent.com/109257850/202324495-62f90409-4d08-4aa4-823c-085fb3e65753.png)

Lalu masuk ke folder yang kita clone dari github tadi, bisa dengan perintah berikut:
cd wayshub-frontend

![Screenshot (210)](https://user-images.githubusercontent.com/109257850/202324820-2b0745e0-dc02-4890-ab73-771b83bef8f4.png)

Langkah pertama saya akan menginstal engine-nya terlebih dahulu. Untuk instalasi bisa menggunakan perintah dibawah ini:

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

![Screenshot (206)](https://user-images.githubusercontent.com/109257850/202322729-cd34f0d2-0963-4f70-8aed-2d39c999bb43.png)

keterangan: disini saya menggunakan nvm 
nvm merupakan singkatan dari Node Version Manager. nvm adalah sebuah program yang akan membantu kita untuk menggunakan lebih dari satu versi Nodejs di dalam satu komputer.

Untuk menjalankan project ini, pastikan npm sudah terinstall pada komputer/laptop kalian
Tata cara menjalankan project:

1. Install node modules
 -> npm install
2. Jalankan project
 -> npm run start

Selanjutnya, pasang Node.js versi 16, dengan perintah berikut:
nvm install 16 

![Screenshot (211)](https://user-images.githubusercontent.com/109257850/202325745-e0bf3774-7fcb-4137-a14f-45cd0ebeb445.png)
(Tampilannya seperti ini karena sebelumnya di laptop saya sudah terinstall nvm-nya)
Catatan: Pastikan Node.js berhasil terpasang dengan mengeksekusi perintah node -v.

Berhasil. Node.js berhasil terpasang. Kini Anda bisa menjalankan web server. Pastikan Anda berada di dalam folder wayshub-frontend. Jika belum, silakan masuk ke foldernya dengan perintah berikut: cd wayshub-frontend/.

Instal beberapa dependencies yang dibutuhkan oleh web server Node.js dengan menjalankan perintah ini: npm install.

Lanjut, jalankan web server dengan perintah berikut: npm run start.

![Screenshot (213)](https://user-images.githubusercontent.com/109257850/202327151-4cd74830-6f52-45c7-b6c6-5334724a41c1.png)

![Screenshot (234)](https://user-images.githubusercontent.com/109257850/202449787-67eea679-55d5-4fa9-b64b-942f3d0b0c9c.png)

![Screenshot (235)](https://user-images.githubusercontent.com/109257850/202449885-1bd63f99-576f-4b13-80e9-67e1825a706b.png)

![Screenshot (236)](https://user-images.githubusercontent.com/109257850/202449899-18130379-26a9-4dd4-a315-d672e3867321.png)

Jika sudah seperti gambar diatas, tandanya berhasil mendeploy sebuah aplikasi.

# Konfigurasi dengan PM2 
Apa itu PM2? PM2 adalah sebuah manajer proses dan bisa juga melakukan monitoring pada project yang kita buat, supaya aplikasi tetap berjalan jika terminal kita tertutp makan gunakanlah PM2.

Pertama untuk menjalankan PM2, bisa lalukan install terlebih dahulu secara global dengan perintah dibawah ini:
sudo npm install pm2 -g atau npm install pm2 -g 
setalah terinstall lalu cek dengan perintah: sudo pm2 atau pm2. Jika muncul gambar dibawah ini, tandanya sudah berhasil menginstall PM2

![Screenshot (239)](https://user-images.githubusercontent.com/109257850/202459749-13cb15d9-3b10-4b10-bf5c-07b485f9a378.png)
![Screenshot (240)](https://user-images.githubusercontent.com/109257850/202459818-a698d4b8-2817-4501-9331-d6e73e71be14.png)

Setelah PM2 berhasil terinstall, silahkan masuk ke direktori aplikasi wayshub-frontend yang tadi dijalankan, untuk menjalan pm2 di aplikasi tersebut bisa gunakan perintah: 
pm2 start wayshub-frontend

![Screenshot (242)](https://user-images.githubusercontent.com/109257850/202461327-e49588ef-cd61-4532-ad9b-dd7cb26d4e53.png)

Dengan PM2 kita bisa melakukan monitoring dengan perintah berikut:
pm2 monit

![Screenshot (244)](https://user-images.githubusercontent.com/109257850/202462248-068b162b-8ecd-4b09-aca1-293a3fe17081.png)

# Golang
Pertama bisa install terlebih dahulu engine-nya. Untuk instalasi bisa menggunakan beberapa perintah dibawah ini:
wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su

![Screenshot (246)](https://user-images.githubusercontent.com/109257850/202466443-2e7c05ab-c0ee-4554-afd7-3b93ef31652d.png)

rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit

![Screenshot (247)](https://user-images.githubusercontent.com/109257850/202466814-f45834dd-cc5a-4f70-bb40-be76be066a63.png)

Langsung masukan perintah path go pada .bashrc

sudo nano .bashrc

![Screenshot (248)](https://user-images.githubusercontent.com/109257850/202467487-0381f615-9511-4a1b-a686-9e80c0c7858f.png)

Lalu tambahkan path command dibawah ini dibagian paling bawah dari .bashrc
export PATH=$PATH:/usr/local/go/bin

![Screenshot (250)](https://user-images.githubusercontent.com/109257850/202468805-4b8c32b3-632c-4906-b0f4-a45f22736a87.png)

Jika sudah sekarang dapat verifikasi go dengan cara berikut:
go version

![Screenshot (251)](https://user-images.githubusercontent.com/109257850/202470343-0d28afc9-39b2-4b3c-98d2-5817c2741b04.png)

Sekarang kita akan membuat aplikasi sederhana menggunakan go. Bisa menggunakan perintah berikut:
nano index.go

lalu masukan script dibawah ini:
package main

import "fmt"

func main() {
    fmt.Println("Hai, nama saya Ajay Tajrian!")
}

![Screenshot (252)](https://user-images.githubusercontent.com/109257850/202472233-8999e5a9-2753-4501-9117-659bb298ebf1.png)

sekarang bisa jalankan aplikasi go dengan perintah berikut:
go run index.go

![Screenshot (254)](https://user-images.githubusercontent.com/109257850/202472566-678f3379-7730-4d32-b1ce-939f6dc29ea7.png)

# Python
Pertama-tama kita harus install terlebih dahulu Pyhton3. Untuk instalasi ikuti beberapa perintah di bawah ini:
sudo apt update; sudo apt upgrade

Python3 sudah ada secara default, untuk melakukan pengecekan jalankan perintah berikut:
python3 -V

![Screenshot (257)](https://user-images.githubusercontent.com/109257850/202478489-06991118-6bf3-4194-8f2c-52df88d5496b.png)

Sekarang kita install package manager dari python3. Kalian dapat menggunakan perintah berikut ini:
sudo apt install python3-pip

![Screenshot (258)](https://user-images.githubusercontent.com/109257850/202479358-42f7ad78-a9c2-4811-a53d-51d494c7d803.png)

lalu jalankan perintah -> pip install flask

![Screenshot (259)](https://user-images.githubusercontent.com/109257850/202479862-16c90ce2-e576-4f71-83de-76548bba9b38.png)

PIP adalah sebuah package management system yang biasa digunakan untuk mengatur dan menginstall package yang berisi modul-modul Python. PIP digunakan untuk menginstall Flask karena Flask ditulis dan dikembangkan dengan bahasa dan modul-modul pemrograman Python. Dengan menggunakan PIP, semua hal yang dibutuhkan untuk instalasi Flask akan diunduh dan dipasang dalam satu perintah.

- Sekarang kita akan membuat aplikasi sederhana menggunakan Python3.
- Bisa buat terlebih dahulu file dengan nama index.py. Lewat perintah dibawah ini:
nano index.py

![Screenshot (260)](https://user-images.githubusercontent.com/109257850/202480844-8256782b-6bdb-4ba1-8699-732fd58c89f8.png)

Jika sudah sekarang jalankan aplikasi dengan menggunakan perintah berikut ini:
python3 index.py

![Screenshot (262)](https://user-images.githubusercontent.com/109257850/202481210-4eb605e8-402b-4598-ab2a-c2ab24053a47.png)

Sekarang coba akses web browser kalian setelah itu coba akses dengan localhost:5000

![Screenshot (261)](https://user-images.githubusercontent.com/109257850/202481376-6de2cfb3-acf6-4672-b238-cd7f7af3f509.png)

# Konfigurasi PM2 Python

Tidak perlu menginstall lagi, cukup jalankan perintah dibawah ini untuk mengkonfigurasi Golang dengan PM2
pm2 start server.go

![Screenshot (263)](https://user-images.githubusercontent.com/109257850/202485702-30a16ff1-1588-4f2f-994a-7f8a9e37dee7.png)

# Jalankan localtunnel untuk aplikasi no 1 (wayshub-frontend)

![Screenshot (272)](https://user-images.githubusercontent.com/109257850/202508197-51c45af4-dafe-4b05-85cf-30ebd7554156.png)












