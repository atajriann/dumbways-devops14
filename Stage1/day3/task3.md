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
npm install
2. Jalankan project
npm run start

Selanjutnya, pasang Node.js versi 16, dengan perintah berikut:
nvm install 16 

![Screenshot (211)](https://user-images.githubusercontent.com/109257850/202325745-e0bf3774-7fcb-4137-a14f-45cd0ebeb445.png)
(Tampilannya seperti ini karena sebelumnya di laptop saya sudah terinstall nvm-nya)
Catatan: Pastikan Node.js berhasil terpasang dengan mengeksekusi perintah node -v.

Berhasil. Node.js berhasil terpasang. Kini Anda bisa menjalankan web server. Pastikan Anda berada di dalam folder wayshub-frontend. Jika belum, silakan masuk ke foldernya dengan perintah berikut: cd wayshub-frontend/.

Instal beberapa dependencies yang dibutuhkan oleh web server Node.js dengan menjalankan perintah ini: npm install.

Lanjut, jalankan web server dengan perintah berikut: npm run start.

![Screenshot (213)](https://user-images.githubusercontent.com/109257850/202327151-4cd74830-6f52-45c7-b6c6-5334724a41c1.png)





























