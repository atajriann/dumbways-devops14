# Definisi DevOps?
DevOps merupakan gabungan dari dua kata yaitu Development dan Operation. Di mana kedua kata tersebut bermakna “Operasional Pengembang”. DevOps adalah sebuah culture dalam meningkatkan pengembangan, serta menjembatani antar tim development dan tim operations sehingga menyajikan aplikasi secara cepat. 
# Sebutkan dua life cycle DevOps & jelaskan definisinya?
Ada beberapa metode siklus hidup DevOps, di antaranya Plan, Develop, Build, Test, Deploy, Operate, Monitor. Disini akan menjelesankan defisini 2 dari yang disebutkan tadi.
- Plan -> Pada tahap perencanaan, proses identifikasi tujuan dan persyaratan untuk merancang dan mengembangkan perangkat lunak, selain itu ada kegitatan lain juga yaitu manajemen proyek, penjadwalan dan rencana perilisan.
- Monitor -> Monitor merupakan tahapan terakhir, biasanya aplikasi sudah di-deploy ke lingkungan production dengan sempurna sehingga bisa dinikmati oleh pengguna. Oleh karenanya, kita perlu memonitor aplikasi agar bisa mendeteksi error ataupun kejanggalan dengan cepat dan secara tanggap langsung memperbaikinya. 

# Instalasi Ubuntu Server
1. Setelah melakukan instalasi VMware, buka VMware anda dan klik dibagian "Create a New Virtual Machine"

![Screenshot (126)](https://user-images.githubusercontent.com/109257850/201922788-3609bd42-33f3-4798-8f3d-d7bb0f420a38.png)

2. Setelah itu akan muncul halaman seperti gambar dibawah. Disini pilih saja di bagian use ISO image, lanjut klik di bagian browse lalu cari lokasi file ISO ubuntu server yang sudah di download sebelumnya lalu dan klik next

![Screenshot (127)](https://user-images.githubusercontent.com/109257850/201923447-68c992e9-6fc2-4c2e-86d1-de05113dbb47.png)

3. Lalu pada bagian "Guest Operating System" pilih saja Linux dan versi Ubuntu 64-bit, klik next

![Screenshot (167)](https://user-images.githubusercontent.com/109257850/201925025-f9d91dc8-aa1c-4a07-88d6-a43a8a1735b8.png)

4. Selanjutnya adalah menentukan lokasi dimana virtual machine akan disimpan.

![Screenshot (168)](https://user-images.githubusercontent.com/109257850/201926981-86f30f17-279b-4a5e-8f39-9482ab573ded.png)

5. Setelah itu atur size disk yang ingin digunakan. Disini sebagai contoh saya menggunakan 20GB. Disini ada 2 pilihan yaitu Store Disk as a single file dan Split virtual disk into multiple files. Pilih lah "Split virtual disk into multiple files" untuk mengkostumasasi storage nya.

![Screenshot (169)](https://user-images.githubusercontent.com/109257850/201927309-63505d1f-4eb7-4839-aaa9-63ebc206d4d3.png)

6. Lalu disini saya akan mengkostumasi hardware untuk server yang dibuat, tekan saja di bagian "Customize Hardware".

![Screenshot (170)](https://user-images.githubusercontent.com/109257850/201928053-08fa3aad-c646-4ab6-a256-f0758fee772f.png)

7. Disini ada beberapa pilihan untuk melakukan kustomasasi seperti Memory, Processors dan Network adapter

Keterangan: Memory berfungsi untuk penyimpanan data yang ingin digunakan untuk Virtual Machine yang ingin dibuat. Disini pilih gunakan saja defaultnya yaitu sebesar 4Gb tetapi misalkan merasa kurang boleh untuk menaikkannya sesuai keinginan. Processors adalah salah satu komponen penting untuk Virtual Machine yang ingin dibangun, serta berfungsi untuk memproses data dan mengontrol sistem yang ada pada Virtual Machine. Disini saya menggunakan defaultnya saja yaitu sebesar 2 core. Network adapter berfungsi untuk menghubungkan komputer ke jaringan. 

![Screenshot (171)](https://user-images.githubusercontent.com/109257850/201928881-259be7a7-87ea-4c53-a317-12cf57f55944.png)

8. Jika sudah selesai untuk mengatur memory dan processor, selanjutnya pergi ke bagian Network Adapter. Setelah itu ubah dari defaultnya yaitu NAT menjadi Bridge.
Keterangan: kalau menggunakan NAT nantinya server yang dibuat ini akan mendapatkan IP yang sudah di sediakan oleh Virtual Machine, kalau Menggunakan Bridge nantinya server yang dibuat akan mendapatkan IP dari internet yang sedang gunakan.

Jika sudah bisa langsung klik saja close.

![Screenshot (172)](https://user-images.githubusercontent.com/109257850/201929170-c4b9875a-2a97-4194-bf71-fa96b9fd8651.png)

9. Setelah di setting seperti yang disebutkan diatas, lalu tekan saja di bagian "Close", lalu lanjutkan dengan klik "Finish" setelah beres klik "Close".

![Screenshot (173)](https://user-images.githubusercontent.com/109257850/201929919-e88a921f-3389-4ffd-9bdb-1d675fa000b0.png)

10. Lalu klik "Play virtual machine" untuk menjalankan.

![Screenshot (174)](https://user-images.githubusercontent.com/109257850/201930184-63272c69-1ee9-46e6-9c16-385fd965c499.png)

11. Tunggu beberapa saat, lalu anda akan diarahkan ke halaman instalasi ubuntu server. Setelah muncul halaman seperti gambar dibawah, pilih saja "Try or Install Ubuntu Server"

![Screenshot (175)](https://user-images.githubusercontent.com/109257850/201930432-78fc6dfd-9883-49d8-9062-b32efddc4cee.png)

12. Setelah itu anda akan diarahkan kehalaman selanjutnya untuk mimilih bahasa yang digunakan untuk menginstall ubuntu server, pilih saja "English" lalu tekan enter

![Screenshot (136)](https://user-images.githubusercontent.com/109257850/201931130-b3c81ebf-63ac-4936-b931-5594cabf9680.png)

13. Dihalaman selanjutnya langsung klik enter saja untuk men-skip step ini

![Screenshot (176)](https://user-images.githubusercontent.com/109257850/201931484-dcb8c195-7c94-4410-8be9-786fb3374c74.png)

14. Selanjutnya pilih "Ubuntu Server" lalu klik enter

![Screenshot (137)](https://user-images.githubusercontent.com/109257850/201931638-80455c42-3d3d-4a0e-9e98-851b18c59d07.png)

15. Selanjutnya kita akan ubah konfigurasinya dari yang awalnya itu DHCPv4 menjadi Static.

Keterangan: DHCP (Dynamic Host Protocol Configuration) : Alamat IP yang dapat berubah-ubah pada perangkat yang tersambung setiap kali terhubung kembali pada jaringan tersebut (otomatis). Static : Alamat IP tidak berubah-ubah dari yang telah diberikan oleh adminisitrator (setting manual).

16. Pilih di bagian ens33, setelah itu pada bagian "IPv4 Method" ubah dari yang awalnya automatic menjadi manual. Setelah itu masukan detail IP pada form yang tersedia (kalian bisa masukan saja IP yang sudah tertera di bagian DHCPv4). Jika sudah langsung saja Save.

Keterangan: Subnet : Istilah teknologi Informasi yang membedakan Network ID dan Host ID atau sebagai penentu porsi Network ID dan Host ID pada deretan kode biner Address : Alamat IP yang akan digunakan untuk Virtual Machine yang akan kalian buat. (kalian dapat mengisi bagian ini dengan IP yang sudah ada di bagian DHCP) Gateway : Perangkat komputer yang berfungsi untuk mengkoneksikan sebuah Jaringan komputer terhadap satu jaringan komputer yang lain. Name servers : Dibagian Name servers ini kalian cukup memasukkan IP DNS dari google supaya dapat terhubung dengan browser. Setelah itu klik save

![Screenshot (177)](https://user-images.githubusercontent.com/109257850/201933838-05f3b47f-f39f-4b1d-9aec-e36065b940a9.png)

17. Jika konfigurasi sudah selesai maka akan ada perubahan di bagian DHCPv4 tadi menjadi static.

18. Pada bagian ini skip saja dengan klik enter

![Screenshot (178)](https://user-images.githubusercontent.com/109257850/201934168-0eafdfbf-3c64-4cb6-851e-e89026c6f8b7.png)

19. Pada bagian ini lansung skip saja klik enter

![Screenshot (179)](https://user-images.githubusercontent.com/109257850/201934329-38011b0c-0feb-4de4-902d-88f1e505a58e.png)

20. Disini saya akan memilih bagian Custom storage layout, jika memilih "Custom storage layout" saya bisa membuat 2 buah partisi, jika sudah dipilih setelah itu langsung saja klik done.

![Screenshot (180)](https://user-images.githubusercontent.com/109257850/201934646-d237dfdb-e01c-4653-9531-6ff0e13a1437.png)

21. Selanjutnya disini saya akan membuat 2 buah partisi untuk root dan swap. Langsung pilih saja di bagian "Free Space" lalu pilih di bagian "Add GPT Partition". Untuk kapasitasnya bisa disamakan saja dengan gambar dibawah (kecuali untuk swap, kalian bisa setting semau kalian apabila merasa kurang).

Keterangan : root adalah tempat dimana sistem kita itu ter-install. swap adalah suatu memory cadangan yang akan digunakan untuk server kita apabila memory utama sudah penuh.

![Screenshot (181)](https://user-images.githubusercontent.com/109257850/201936088-c78037ec-80ef-4e35-9ffd-7a4a0f41780c.png)

![Screenshot (182)](https://user-images.githubusercontent.com/109257850/201936132-3cb60912-1735-44b5-bc4c-b121aeb83272.png)

![Screenshot (184)](https://user-images.githubusercontent.com/109257850/201936209-0d34b780-3543-45cd-a109-520dce5ca267.png)

22. Jika sudah, disini saya sudah berhasil membuat 2 partisi untuk root dan swap. Lalu langsung saja klik "Done" dan klik "continue" untuk lanjut ke step berikutnya.

![Screenshot (186)](https://user-images.githubusercontent.com/109257850/201936541-c8256eeb-d5e6-4827-9f09-4dd405a0dc12.png)

23. Selanjutnya masukan informasi seperti nama, username dan password untuk server yang dibuat. Jika sudah klik "Done".

![Screenshot (187)](https://user-images.githubusercontent.com/109257850/201936811-a3e6c130-f26a-48cc-b36c-46667087815c.png)

24. Pada tahap ini, instalasi ubuntu server sudah sampai akhir. Tunggu saja proses instalasi sampai selesai jika sudah selesai langsung klik "Reboot Now".

![Screenshot (188)](https://user-images.githubusercontent.com/109257850/201938634-e84bc037-4410-46e5-8b07-4ab540a60799.png)

![Screenshot (189)](https://user-images.githubusercontent.com/109257850/201941881-1112640f-83df-478d-ac1d-528e2607c048.png)

25. Jika tahapan instalasi sudah selesai. Masukkan id beserta password yang sudah di set-up sebelumnya, Jika sudah maka anda telah berhasil melakukan instalasi ubuntu server.

 ![Screenshot (190)](https://user-images.githubusercontent.com/109257850/201943380-e878bcaf-d615-45dd-a059-cabeee6fc47a.png)

26. 



















