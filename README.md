# Jarkom_Modul1_Lapres_T06
<b> Laporan Resmi Praktikum Jaringan Komputer </b> <br>
Kelompok T06
1. Hana Ghaliyah Azhar  (05311840000032)
2. Azmi                 (05311840000047)

## Display Filter
Memilah paket yang akan ditampilkan dari kumpulan paket yang sudah ditangkap.
<br>

### Soal 1
Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
#### Pembahasan
##### Wireshark filter expression: `http.host == testing.mekanis.me`
##### Screenshot hasil:
Dapat dilihat webserver yang digunakan pada <b>testing.mekanis.me</b> adalah `Server: nginx/1.14.0 (Ubuntu)` <br>
![image](https://user-images.githubusercontent.com/26424136/96079850-fe303480-0edf-11eb-8a48-51e3263945cd.png)
<br>

### Soal 2
Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
#### Pembahasan
1. Pilih File -> Export Objects -> HTTP
![Screenshot (135)](https://user-images.githubusercontent.com/26424136/96080225-cd043400-0ee0-11eb-9727-a438efef1b30.png)
2. Lalu cari gambar <b>Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg</b> pada `Text Filter`, Lalu <b>save as</b> dengan format `.jpg`
![Screenshot (136)](https://user-images.githubusercontent.com/26424136/96080229-cf668e00-0ee0-11eb-9efd-ae1a65147df1.png)
3. Buka Gambar
![Screenshot (137)](https://user-images.githubusercontent.com/26424136/96080230-cfff2480-0ee0-11eb-87c6-4bb1d0d7f80c.png)
<br>

### Soal 3
Cari username dan password ketika login di "ppid.dpr.go.id"!
#### Pembahasan
##### Wireshark filter expression: `http.host == ppid.dpr.go.id && http.request.method == POST`
##### Screenshot hasil:
Pada `HTML Form URL Encode`, kita dapat menemukan username dan password.
- Username: `10pemuda`
- Password: `guncangdunia` <br>
![image](https://user-images.githubusercontent.com/26424136/96081724-2752c400-0ee4-11eb-891b-aae006dc1fcd.png)
<br>

### Soal 4
Temukan paket dari web-web yang menggunakan basic authentication method! <br>
#### Pembahasan
##### Wireshark filter expression: `http.authbasic` <br>
##### Screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96061525-a8e32b80-0ebd-11eb-94eb-2eee925aaf73.png)
<br>

### Soal 5
Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng! 
#### Pembahasan
##### Wireshark filter expression: `http.host == aku.pengen.pw` <br>
##### screenshot hasil:
1. Pada Authorization dibagian Credentials terdapat username `kakakgamtenk` dan password `hartatahtabermuda` untuk login di <b>aku.pengen.pw</b> 
![image](https://user-images.githubusercontent.com/26424136/96083326-2c654280-0ee7-11eb-90c9-1e38666a2d6c.png)
2. Login dengan username dan password yang telah diperoleh. Berikut Tampilan web setelah kita berhasil login.
![image](https://user-images.githubusercontent.com/26424136/96083497-73533800-0ee7-11eb-9167-3e23613c0bac.png)
<br>

### Soal 6
Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut). <br>
#### Pembahasan
##### Wireshark filter expression: `ftp-data` <br>
##### Screenshot hasil: <br>
1. Mencari file Answer.zip
- ctrl+f (display filter dichange ke regular expression) answer.zip
- find
- follow TCP Stream
- show and save data as 'RAW' 
- Save as dan beri nama "Answer.zip" <br>
![image](https://user-images.githubusercontent.com/26424136/96062496-01b3c380-0ec0-11eb-838d-37106e2d0efa.png) <br>
2. Mencari file zipkey.txt
- ctrl+f mecari zipkey
- lalu menemukan zipkey.txt 
- follow tcp stream
- show and save data as `raw` <br>
Isi File Zipkey.txt berupa Password : `hey997400323051` <br>
![image](https://user-images.githubusercontent.com/26424136/96062512-109a7600-0ec0-11eb-9bbe-d960447bc059.png)<br>
3. File "Open This.pdf"<br>
![image](https://user-images.githubusercontent.com/26424136/96062295-8520e500-0ebf-11eb-84ae-8e9dcb46712b.png)
<br>

### Soal 7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
#### Pembahasan
##### Wireshark filter expression: `ftp-data contains Yes.pdf`
##### Screenshot hasil: 
1. Setelah menemukan paketnya, klik Follow Tcp Stream
![Screenshot (131)](https://user-images.githubusercontent.com/26424136/96079008-ec4d9200-0edd-11eb-900a-78a50c1efebe.png)
2. Show and save data as `RAW`, lalu gunakan format `.zip` pada file tersebut
![Screenshot (133)](https://user-images.githubusercontent.com/26424136/96079014-ee175580-0edd-11eb-9a38-5dddaf7edce4.png)
3. Extract file tersebut dan buka file `Yes.pdf` yang ada didalamnya.
![Screenshot (134)](https://user-images.githubusercontent.com/26424136/96079017-eeafec00-0edd-11eb-8a3d-a56fbec3f201.png)
<br>

### Soal 8
Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
#### Pembahasan
##### Wireshark filter expression: 
- Filter untuk Mencari IP Microsoft yaitu `ftp contains Microsoft`
- Filter untuk mencari objek yaitu `ftp.request.command == "RETR" && ip.addr == 198.246.117.106` 
##### Screenshot hasil:
1. Mencari IP Microsoft.
![image](https://user-images.githubusercontent.com/26424136/96101272-7ce89a00-0eff-11eb-8e28-b29e714650d9.png)
2. Objek telah ditemukan (File yang ditemukan ialah <b>readme</b>). 
![image](https://user-images.githubusercontent.com/26424136/96101410-9f7ab300-0eff-11eb-9b5f-72df82f24a1e.png)
<br>

### Soal 9
Cari username dan password ketika login FTP pada localhost!
#### Pembahasan
##### Wireshark filter expression: `ftp.request.command == USER || ftp.request.command == PASS`
##### Screenshot hasil:
User: `dhana` dan Pass: `dhana123` <br>
![image](https://user-images.githubusercontent.com/26424136/96077426-fa011880-0ed9-11eb-97e2-0ccad712c34a.png)
<br>

### Soal 10
Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46" 
#### Pembahasan
1. ctrl + f (display filter dichange ke Hex Value)
2. Find `25 50 44 46`
3. Setelah menemukan paketnya, Pilih Follow TCP Stream
4. Show and save data as `raw`
5. Save as dengan format `pdf`

##### Screenshot hasil:
1. Paket telah ditemukan <br>
![image](https://user-images.githubusercontent.com/26424136/96077865-16518500-0edb-11eb-957b-187f0c643f4f.png)
2. Pada Follow TCP Stream, Show and save data as `RAW`. Kemudian save as dengan format `.pdf`
![image](https://user-images.githubusercontent.com/26424136/96087940-ddbba680-0eee-11eb-8ee1-e8b2ef3704d1.png)
3. Buka file tersebut <br>
![image](https://user-images.githubusercontent.com/26424136/96088346-810cbb80-0eef-11eb-882b-9b3ec919054a.png)
<br>

## Capture Filter
Memilah paket yang akan ditangkap (captured). Paket yang tidak memenuhi kriteria dibiarkan lewat tanpa ditangkap.
<br>

### Soal 11
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
#### Pembahasan
##### Wireshark filter expression: `port 21`
- Menyalakan filezila (agar port 21 bisa terdeteksi)
- Pilih adapter loopback pada wireshark
##### Screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96077231-70e9e180-0ed9-11eb-93e5-508b252036f3.png)
<br>

### Soal 12
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
#### Pembahasan
##### Wireshark filter expression: `src port 80`
##### Screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96070938-5a3c8e00-0ecb-11eb-92e6-a2f1bbb6d676.png)
<br>

### Soal 13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
#### Pembahasan
##### Wireshark filter expression: `dst port 443`
##### Screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96071087-a091ed00-0ecb-11eb-8382-096a0339ce9a.png)
<br>

### Soal 14
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
#### Pembahasan
##### Wireshark filter expression: `src host 192.168.0.109`
##### Screenshot hasil:
Buka Cmd dan gunakan perintah `ipconfig`. IP laptop kita adalah `192.168.0.109` <br>
![image](https://user-images.githubusercontent.com/26424136/96071253-e77fe280-0ecb-11eb-9675-c4f0005c45ec.png) <br>
Paket yang berasal dari `192.168.0.109` <br>
![image](https://user-images.githubusercontent.com/26424136/96071298-05e5de00-0ecc-11eb-81f0-6a6070e35ce4.png) <br>
<br>

### Soal 15
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
#### Pembahasan
##### Wireshark filter expression: `dst host monta.if.its.ac.id`
##### Screenshot hasil:
![image](https://user-images.githubusercontent.com/26424136/96071593-af2cd400-0ecc-11eb-95c3-65c25bbdcd7c.png)
