# Jarkom_Modul1_Lapres_T06

## Kelompok T06
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
Temukan paket dari web-web yang menggunakan basic authentication method!
Wireshark filter expression: `http.authbasic`
screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96061525-a8e32b80-0ebd-11eb-94eb-2eee925aaf73.png)

### Soal 5
Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

### Soal 6
Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
Wireshark filter expression: 'ftp-data'
Step Mencari file Answer.zip
- ctrl+f (display filter dichange ke regular expression) answer.zip
- find
- follow TCP Stream
- show and save data as 'RAW' 
- Save as dan beri nama "Answer.zip"
Step Mencari file zipkey.txt
- ctrl+f mecari .zip
- lalu menemukan zipkey.txt 
- follow tcp stream
- save as raw

Screenshot hasil:






