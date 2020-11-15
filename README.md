# Jarkom_Modul2_Lapres_D11
Lapres praktikum jarkom modul 2 kelompok D11

Anggota Kelompok:
- M. Farras Pangestu - 05111840000134
- Rasyid Ridlo W. - 05111840000135

## Nomor 1 : Pertama kita harus membuat domain dengan mengisikan konfigurasi untuk semerud11.pw di MALANG 
  
   <img src="https://github.com/RsydRidloo/Jarkom_Modul2_Lapres_D11/blob/main/Foto/1a.PNG" >
   
   - Buat folder semeru di dalam /etc/bind
   - Copykan file db.local pada path /etc/bind ke dalam folder semeru

        *buat baru dan ubah namanya menjadi semerud11.pw*

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
  - 
  
   
   
   

   
   
   
   
