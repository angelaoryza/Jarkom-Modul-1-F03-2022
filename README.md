# Jarkom-Modul-1-F03-2022

## Anggota Kelompok dan Kontribusi
   1. Angela Oryza Prabowo (5025201022)
      - Menulis laporan resmi dan membantu menambahkan penjelasan
   2. Helmi Taqiyuddin (5025201152)
      - Mengerjakan nomor 7, 8, 9, dan 10
   3. Naufal Fabian Wibowo (05111940000223)
      - Mengerjakan nomor 1, 2, 3, 4, 5, 6 , dan 7

## Cara Pengerjaan
1. Web server yang digunakan pada monta.if.its.ac.id adalah **Nginx** <br>
    <picture>
     <img alt="Screenshoot hasil No 1." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/1.png">
    </picture>
    >	**Informasi web server pada website monta.if.its.ac.id dapat diketahui dengan tahap sebagai berikut :**
    >	1. Melakukan filter capture  untuk semua paket yang berasal dan diterima oleh internet yang diakses perangkat
    >   2.	Membuka web monta.if.its.ac.id sehingga paket dari website tersebut dapat ditangkap oleh wireshark
    >   3.	Untuk mengetahui servernya, kita dapat memilih menu “Analyze” kemudian “Follow” dan memilih “TCP Stream”
    >   4.	Referensi : https://www.wireshark.org/docs/wsug_html_chunked/ChAdvFollowStreamSection.html 

2. Judul TA yang dibuka oleh Ishaq adalah **Evaluasi unjuk kerja User Space Filesystem (FUSE)** <br>
    <picture>
     <img alt="Screenshoot hasil No 2." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/2.png">
    </picture>
    >   Untuk soal nomor 2, perlu menggunakan bantuan file dari folder *resource*. Ketika file tersebut dibuka, maka akan muncul paket-paket apa saja yang                    sudah di*capture*. Setelah itu dilakukan filter yang hanya menampilkan string bernama "detailTopik" (`http.request.uri contains "detailTopik"`). Wireshark akan menampilkan alamat url http yang mengandung string “detailTopik”. Maka setelah itu, kita tinggal mengikuti alamat tersebut di peramban setelah alamat monta.if.its.ac.id 
    
3. Filter sehingga wireshark hanya menampilkan paket yang menuju port 80 adalah menggunakan fitur **Display** dengan syntax **tcp.dstport == 80**
    <picture>
     <img alt="Screenshoot hasil No 3." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/3.png">
    </picture>
    >   File pcapng sudah berisi paket paket yang dicapture, sehingga kita tidak perlu lagi melakukan capture lagi. Untuk mendapatkan paket yang menuju port 80, maka kita bisa menggunakan fitur **display** dengan sintaks `tcp.dstport == 80`. Karena hanya ingin menampilkan paket yang menuju port tertentu, maka digunakan sintaks `dst`
    
4. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21 adalah menggunakan fitur **Capture** dengan syntax **tcp.srcport == 21**
    <picture>
     <img alt="Screenshoot hasil No 4." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/4.png">
    </picture>
    >   File pcapng sudah berisi paket paket yang dicapture, sehingga kita tidak perlu lagi melakukan capture lagi. Untuk mengambil paket yang berasal dari port 21, maka kita bisa menggunakan fitur **capture** dengan sintaks `tcp.srcport == 21`. Karena hanya ingin mengambil paket yang berasal dari port tertentu, maka digunakan sintaks `src`
    
5. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443 adalah menggunakan fitur **Capture** dengan syntax **tcp.srcport == 443**
    <picture>
     <img alt="Screenshoot hasil No 5." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/5.png">
    </picture>
    >   File pcapng sudah berisi paket paket yang dicapture, sehingga kita tidak perlu lagi melakukan capture lagi. Untuk mengambil paket yang berasal dari port 443, maka kita bisa menggunakan fitur **capture** dengan sintaks `tcp.srcport == 443`. Karena hanya ingin mengambil paket yang berasal dari port tertentu, maka digunakan sintaks `src`
   
6. Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id adalah menggunakan fitur **Display** dengan syntax **tcp contains "lipi.go.id"**
    <picture>
     <img alt="Screenshoot hasil No 6." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/6.png">
    </picture>
    >   File pcapng sudah berisi paket paket yang dicapture, sehingga kita tidak perlu lagi melakukan capture lagi. Untuk mendapatkan paket yang berasal dari website lipi.go.id, maka kita bisa menggunakan fitur **display** dengan sintaks `tcp contains "lipi.go.id"`
    
7. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kami adalah menggunakan fitur **Capture** dengan syntax **src host ip address**
   1. Angela Oryza Prabowo (`src host 192.168.1.4`)
    <picture>
     <img alt="Screenshoot hasil No 6." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/7-1.png">
    </picture>
    
   2. Naufal Fabian W (`src host 192.168.0.103`)
    <picture>
     <img alt="Screenshoot hasil No 6." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/7-2.png">
    </picture>
    
   3. Helmi Taqiyuddin (`src host 192.168.1.2`)
    <picture>
     <img alt="Screenshoot hasil No 6." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/7-3.png">
    </picture>
    
    >   Untuk menngambil paket yang berasal dari IP Address kita, kita perlu mencari tahu IP Address dari koneksi masing masing terlebih dahulu. Setelah mendapatkannya, maka kita tinggal menggunakan fitur **capture** dari wireshark untuk mengambil paket-paket yang hanya berasal dari IP Address kita dengan sintaks `src host IP Address`
    
8.  <br>
    <picture>
     <img alt="Screenshoot hasil No 6." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/8.png">
    </picture>
    
    >   Karena protokol dengan keandalan yang tinggi adalah TCP, maka paket yang perlu kita filter adalah paket dengan **protokol TCP**. Setelah itu, kita tinggal menggunakan menu `Analyze -> Follow -> TCP Stream` dan mencari percakapan sebagai bukti contekan
    
9.  <br>
    <picture>
     <img alt="Screenshoot hasil No 6." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/9.png">
    </picture>
    
    >   - Untuk menyimpan file yang dijadikan contekan, kita perlu menggunakan filter dengan sintaks  `tcp.srcport==9002`. Sintaks ini digunakan untuk menangkap paket dari **port 9002** yang merupakan port dimana contekan tersebut diberikan berdasarkan hasil percakapan mereka. Setelah menemukan paket-paket yang berasal dari port 9002, kita membaca salah satu paket dengan mengubahnya ke RAW karena file tersebut sudah sempat dienkripsi ke salted. Setelah itu disimpan dengan nama `F03.des3.`
	>   - Untuk mengubahnya ke file flag.txt, maka digunakan CLI dengan command **openssl des3 -d salt -in F03.des3 -out flag.txt -k nakano.**
    
10. <br>
    <picture>
     <img alt="Screenshoot hasil No 6." src="https://github.com/angelaoryza/Jarkom-Modul-1-F03-2022/blob/main/src/10.png">
    </picture>
    
    >   - Password nakano didapatkan dari clue di percakapan rahasia mereka
	>   - Isi dari file flag.txt itu sendiri adalah **JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}**
    
    
## Kendala
1. Praktikum bertabrakan dengan supporteran Dies Natalis Basket Putri FTEIC vs FTK
2. Kesulitan mencari clue untuk password decrypt file ke flag.txt
3. Tidak pernah mengetahui cara decryp file salt ke txt sebelumnya
