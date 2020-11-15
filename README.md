# Jarkom_Modul2_Lapres_D11
Lapres praktikum jarkom modul 2 kelompok D11

Anggota Kelompok:
- M. Farras Pangestu - 05111840000134
- Rasyid Ridlo W. - 05111840000135

## Nomor 1 : Pertama kita harus membuat domain dengan mengisikan konfigurasi untuk semerud11.pw di MALANG 
  
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/1a.PNG" >
   
   - Buat folder semeru di dalam /etc/bind
   - Copykan file db.local pada path /etc/bind ke dalam folder semeru

         buat baru dan ubah namanya menjadi semerud11.pw

   - lalu buka file semerud11.pw dan setting seperti gambar berikut
   
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/2a.PNG" >
   
   - Setelah kita *service bind9 restart* , lalu kita tes
   
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/1c.PNG" >
  
## Nomor 2 :  Selanjutnya kita akan membuat alias

  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/2a.PNG" >
  
  - Setelah itu kita tes dengan cara ping www.semerud11.pw
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/2b.PNG">
  
## Nomor 3 : Setelah itu kita membuat subdomain

  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/3a.PNG">
  
  - Setelah itu kita tes dengan cara ping penanjakan.semerud11.pw
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/3b.PNG" >
  
## Nomor 4 : Setelah itu kita membuat reverse domain

  - Setting file /etc/bind/named.conf.local
  
  - Lalu tambahkan konfigurasi zone seperti gambar berikut
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/4a.PNG" >
  
  - Copykan file db.local pada path /etc/bind ke dalam folder jarkom
  

         yang baru saja dibuat dan ubah namanya menjadi 79.151.10.in-addr.arpa

   - Setting file 79.151.10.in-addr.arpa menjadi seperti gambar di bawah ini
   
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/4b.PNG" >
   
   - Setelah selesai lalu kita restart Malang dan coba pada gresik 
   
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/4c.PNG" >
   
## Nomor 5 : Setelah itu kita membuat DNS Server Slave

   - Setting file pada /etc/bind/named.conf.local sebagai berikut
   
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/5a.PNG" >
   
   - Setting file pada /etc/bind/named.conf.local di MOJOKERTO sebegai berikut
   
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/5b.PNG" >
   
   - Setelah selesai lalu matikan malang dengan cara *service bind9 stop*
   
   - Lalu kita tes pada gresik sebagai berikut
   
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/5c.PNG" >

## Nomor 6 : Setelah itu kita membuat subdomain di delagasikan ke MOJOKERTO dan mengarah ke PROBOLINGGO

  - Setting file pada /etc/bind/semeru/semerud11.pw untuk menambah subdomain baru
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/6a.PNG" >
  
  - Lalu setting file pada /etc/bind/named.conf.options dan comment dnssec-validation auto, dan tambahkan baris tersebut di MALANG
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/6b.PNG" >
  
  - Lalu setting file pada /etc/bind/named.conf.options dan comment dnssec-validation auto, dan tambahkan baris tersebut di MOJOKERTO
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/6confmojo.PNG" >
  
  - Kemudian buat direktori dengan nama delegasi lalu copy db.local ke direktori gunung.semerud11.pw

  - Kemudian setting file gunung.semerud11.pw menjadi seperti dibawah ini
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/6d.PNG" >
  
  - Lalu kita tes pada gresik sebagai berikut
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/6e.PNG" >
  
## Nomor 7 : Setelah itu kita membuat subdomain naik.gunung.semerud11.pw

  - Setting file pada /etc/bind/delegasi/gunung.semerud11.pw untuk menambah subdomain baru
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/7a.PNG" >

  - Lalu kita tes pada gresik sebagai berikut
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/7b.PNG" >
  
## Nomor 8 : Setelah itu kita mengatur webserver untuk Domain semerud11.pw
  
  - Dengan menambahkan ServerName dan DocumentRoot pada *nano /etc/apache2/sites-available/semerud11.pw*
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/8a.PNG" >
  
  - Lalu untuk melihat hasilnya dapat diakses dengan browser semerud11.pw
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/8b.PNG" >
  
## Nomor 9 : Setelah itu kita menghilangkan index.php

  - Aktifkan *a2enmod rewrite*
  
  - Lalu untuk semerub02.pw, AllowOverride diganti All
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/9a.PNG" >
  
  - Lalu edit file .htaccess dan isikan seperti berikut
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/9b.PNG" >
  
  - Lalu untuk melihat hasilnya tinggal di coba untuk semerud11.pw/home
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/9c.PNG" >
  
## Nomor 10 : Setelah itu kita mensetting penanjakan.semerud11.pw

  - Ekstrak file ke folder /var/www/penanjakan.semerud11.pw 
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/10a.PNG" >
  
  - Lalu tambahkan ServerName dan DocumentRoot dengan penanjakan.semerud11.pw pada *nano /etc/apache2/sites-available/penanjakan.semerud11.pw*
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/10b.PNG" >
  
  - Lalu aktifkan a2ensite penanjakan
  - Hasilnya jika dibuka penanjakan.semerud11.pw
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/10c.PNG" >
  
## Nomor 11 : Listing pada /public tanpa public/*

  - Tambahkan Option +Indexes untuk directory penanjakan.semerud11.pw/public dan tambahkan Option -Indexes untuk directory penanjakan.semerud11.pw/public/*
  
  <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/11a.PNG" >
  
  - Hasilnya saat mengakses penanjakan.semerud11.pw/public/
  
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/11b.PNG" >
  
  - Hasilnya saat mengakses penanjakan.semerud11.pw/public/images/
  
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/11c.PNG" >



## Nomor 12 : Setelah itu kita mensetting penanjakan.semerud11.pw


## Nomor 13 : Setelah itu kita mensetting penanjakan.semerud11.pw


## Nomor 14 : Setelah itu kita mensetting penanjakan.semerud11.pw


## Nomor 15 : Setelah itu kita mensetting penanjakan.semerud11.pw


## Nomor 16 : Setelah itu kita mensetting penanjakan.semerud11.pw


## Nomor 17 : Setelah itu kita mensetting penanjakan.semerud11.pw



  
   
   
   

   
   
   
   
