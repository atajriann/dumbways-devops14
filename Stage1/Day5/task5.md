# Definisi CI/CD
Continuous integration (CI) adalah pengintegrasian kode ke dalam repositori kode kemudian menjalankan pengujian secara otomatis, cepat, dan sering. Sedangkan Continous Delivery/Deployment adalah sebuah praktik yang dilakukan setelah proses CI selesai dan seluruh kode berhasil terintegrasi, sehingga aplikasi bisa dibangun lalu dirilis secara otomatis.

# Fork repoitory Dumbflix 
Fork adalah sebuah proses menyalin repository dari akun orang lain atau organisasi ke akun kita sendiri.
Pertama kalian bisa masuk ke link (https://github.com/dumbwaysdev/dumbflix-frontend) tersebut lalu lakukan fork. Setelah lakukan fork sekarang kita akan mendeploy apliakasi-nya di Cloudflare.

# Deploy aplikasi Dumbflix di Cloudflare Pages
1. Pertama masuk ke web Cloudflare dan lalukan login bila sudah mempunyai akun atau sign up bila belum mempunyai akun.
Disini saya lalukan login karena sudah mempunyai akun

![Screenshot (301)](https://user-images.githubusercontent.com/109257850/202968175-0d0b10c2-e5e2-4f6b-a546-35e028e306cf.png)

2. Setelah login lalu masuk ke option "Pages" lalu klik "Create a project" untuk membuat project

![Screenshot (302)](https://user-images.githubusercontent.com/109257850/202968313-58c5cdb3-e3d5-4951-8cf8-252b5a6848f4.png)

3. Selanjutnya Tekan bagian Connect to GitHub, supaya repository di github kita terdeteksi ke Cloudflare Pages

![Screenshot (303)](https://user-images.githubusercontent.com/109257850/202969127-8bb48429-184a-4248-9647-67b6ac9e7063.png)
![Screenshot (304)](https://user-images.githubusercontent.com/109257850/202969147-91ebc777-0189-4d1e-a081-8c6957666fe1.png)

4. Bila anda memiliki beberapa akun pilih akun yang sesuai. Misalkan saya menggunakan akun pribadi yang bernama atajriann dan pilih satu repository.
![Screenshot (305)](https://user-images.githubusercontent.com/109257850/202969411-cc0b3a9b-b285-476b-9538-47e68a26f6dd.png)

5. Jika sudah kalian dapat memilih semua repository maupun salah satu repository saja. Dalam hal ini kita hanya menghubungkan cloudflare pages ke salah satu repository saja.
![Screenshot (306)](https://user-images.githubusercontent.com/109257850/202969511-c8ffad5e-51ab-4344-8dbc-6ca9b04e3ae3.png)

6. Kemudian akan menampilkan halaman berikut, dan bisa klik begin setup untuk proses konfigurasinya.
![Screenshot (307)](https://user-images.githubusercontent.com/109257850/202969768-078d1d0f-08c7-42f6-9e70-bee15d54a807.png)

7. Pastikan untuk mengisi nama dan branch yang digunakan, kemudian pada bagian build settings pilih framework yang digunakan kemudian pastikan untuk memasukkan build commandnya. Jika sudah sesuai langsung saja klik Save and Deploy.
![Screenshot (310)](https://user-images.githubusercontent.com/109257850/202970425-d3958db5-7803-49ab-b8c4-dec002cac847.png)
![Screenshot (311)](https://user-images.githubusercontent.com/109257850/202970437-ef64eddd-e857-4399-a7a3-cb546fb8083e.png)

8. Setelah itu kita tunggu saja sampai proses build selesai.
![Screenshot (312)](https://user-images.githubusercontent.com/109257850/202970622-1ac2ddb4-ef18-439e-975f-b635e6e3c5d5.png)

9. Jika proses build berhasil maka akan terlihat seperti berikut.
![Screenshot (313)](https://user-images.githubusercontent.com/109257850/202971053-f4fd3871-7698-4c80-acc5-6a891d6e1d8e.png)

10. Sekarang kita coba akses aplikasi yang sudah kita deploy menggunakan cloudflare ini dengan url yang ada di sebelah Domains (lihat bagian production).
![Screenshot (314)](https://user-images.githubusercontent.com/109257850/202971282-c659eaf9-9526-4782-b831-96926bd13977.png)

11. Dan inilah hasilnya website yang telah berhasil dijalankan ke server Cloudflare Pages.
![Screenshot (315)](https://user-images.githubusercontent.com/109257850/202971463-8be41468-12b7-4509-8c9e-782db3a021de.png)

# Update Code 
Sekarang akan mencoba mempraktekkan bagaimana cara kerja dari CI/CD, setiap ada perubahan code maka code tersebut akan dikirimkan ke server Cloudflare Pages.

- Sekarang kita akan mencoba untuk melakukan perubahan code pada bagian title, Kita coba ubah pada bagian <title> ... </title>, dimaksudkan untuk mengetahui apakah proses CI/CD berhasil atau tidak.

![Screenshot (316)](https://user-images.githubusercontent.com/109257850/202972094-0d4c5353-27d9-4514-b0c9-eb79444eb08c.png)

- Selanjutnya kita coba lihat di Cloudflare pages kita, disini Cloudflare secara otomatis melakukan build ulang, kenapa? karena sebelumnya kita sudah melakukan suatu perubahan di bagian title tadi. Selanjutnya kita tunggu saja sampai proses build selesai.
![Screenshot (318)](https://user-images.githubusercontent.com/109257850/202972319-9f543d16-8de6-43c3-b50f-5ac7c295f359.png)

- Jika sudah selesai dan proses build telah berhasil, maka akan berubah seperti di bawah ini. Pada bagian title yang sebelumnya Dumbflix - Fadhil Darma Putera Z telah menjadi Dumbflix - Arsena Tajrian


















