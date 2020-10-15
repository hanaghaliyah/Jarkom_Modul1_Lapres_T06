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
Wireshark filter expression: `ftp-data` <br>
Step Mencari file Answer.zip
- ctrl+f (display filter dichange ke regular expression) answer.zip
- find
- follow TCP Stream
- show and save data as 'RAW' 
- Save as dan beri nama "Answer.zip"
<br>Step Mencari file zipkey.txt
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






