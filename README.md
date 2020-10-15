# Jarkom_Modul1_Lapres_T06
Kelompok T06
1. Hana Ghaliyah Azhar  (05311840000032)
2. Azmi                 (05311840000047)

## Display Filter
### Soal 1
Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

### Soal 2
Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

### Soal 3
Cari username dan password ketika login di "ppid.dpr.go.id"!

### Soal 4
Temukan paket dari web-web yang menggunakan basic authentication method! <br>
Wireshark filter expression: `http.authbasic` <br>
screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96061525-a8e32b80-0ebd-11eb-94eb-2eee925aaf73.png)

### Soal 5
Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

### Soal 6
Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut). <br>
#### Pembahasan
Wireshark filter expression: `ftp-data` <br>
Step Mencari file Answer.zip
- ctrl+f (display filter dichange ke regular expression) answer.zip
- find
- follow TCP Stream
- show and save data as 'RAW' 
- Save as dan beri nama "Answer.zip" <br>

Step Mencari file zipkey.txt
- ctrl+f mecari zipkey
- lalu menemukan zipkey.txt 
- follow tcp stream
- show and save data as `raw`

Screenshot hasil: <br>
![image](https://user-images.githubusercontent.com/26424136/96062496-01b3c380-0ec0-11eb-838d-37106e2d0efa.png) <br>
Isi File Zipkey.txt<br>
Password : `hey997400323051` <br>
![image](https://user-images.githubusercontent.com/26424136/96062512-109a7600-0ec0-11eb-9bbe-d960447bc059.png)<br>
File "Open This.pdf"<br>
![image](https://user-images.githubusercontent.com/26424136/96062295-8520e500-0ebf-11eb-84ae-8e9dcb46712b.png)

### Soal 7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
#### Pembahasan
##### Wireshark filter expression: `ftp-data contains Yes.pdf`

##### Screenshot hasil: 
![image](https://user-images.githubusercontent.com/26424136/96069184-df25a880-0ec7-11eb-9041-9393fd95955a.png)

### Soal 8
Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
#### Pembahasan
##### Wireshark filter expression: `ftp.request.command == "RETR" && ip.addr == 198.246.117.106`

##### Screenshot hasil:

### Soal 9
Cari username dan password ketika login FTP pada localhost!

### Soal 10
Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46" 

## Capture Filter
### Soal 11
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
#### Pembahasan
##### Wireshark filter expression: `port 21`
- Menyalakan filezila
- Pilih adapter loopback pada wireshark
##### Screenshot hasil:


### Soal 12
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
#### Pembahasan
##### Wireshark filter expression: `src port 80`
##### Screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96070938-5a3c8e00-0ecb-11eb-92e6-a2f1bbb6d676.png)

### Soal 13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
#### Pembahasan
##### Wireshark filter expression: `dst port 443`
##### Screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96071087-a091ed00-0ecb-11eb-8382-096a0339ce9a.png)

### Soal 14
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
#### Pembahasan
##### Wireshark filter expression: `src host 192.168.0.109`
##### Screenshot hasil:
Buka Cmd dan gunakan perintah `ipconfig`. IP laptop kita adalah `192.168.0.109` <br>
![image](https://user-images.githubusercontent.com/26424136/96071253-e77fe280-0ecb-11eb-9675-c4f0005c45ec.png) <br>
Paket yang berasal dari `192.168.0.109` <br>
![image](https://user-images.githubusercontent.com/26424136/96071298-05e5de00-0ecc-11eb-81f0-6a6070e35ce4.png) <br>

### Soal 15
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
#### Pembahasan
##### Wireshark filter expression: `dst host monta.if.its.ac.id`
##### Screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96071593-af2cd400-0ecc-11eb-95c3-65c25bbdcd7c.png)
