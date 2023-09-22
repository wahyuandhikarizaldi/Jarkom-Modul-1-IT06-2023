# PRAKTIKUM MODUL 1 JARINGAN KOMPUTER 2023

## No. 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 

b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 

c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?



## No. 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!


## No. 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

b. Protokol layer transport apa yang digunakan?


## No. 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?


## No. 5
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.

a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

b. Port berapakah pada server yang digunakan untuk service SMTP?

c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

## No. 6
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

### Cara Pengerjaan
Cek packet yang ke 7812, source address nya adalah 104.18.14.101.

(ss packet)


Sesuai dengan hint yang diberikan, substitusikan dengan a1z26 cipher, rentang huruf A-R, 1-18, dan berjumlah 6 huruf. Maka source address nya akan menjadi:

10.4.18.14.10.1 = JDRNJA

Inputkan jawabannya ke terminal, lalu didapatkan flag.

(ss terminal)

```bash
Here is your flag: Jarkom2023{h3h3_ctf_d1k1t_a0T35XQ1309B7YI4HEkx}
```


## No. 7
Berapa jumlah packet yang menuju IP 184.87.193.88?

### Cara Pengerjaan

Filter packet yang menuju IP 184.87.193.88 dengan mengunakan kueri:

```bash
ip.addr == 184.87.193.88
``` 

(ss packet)

Terdapat 6 packet yang menuju IP 184.87.193.88. Input jawaban ke server, lalu didapatkan flag.

(ss terminal)
```bash
Here is your flag: Jarkom2023{4uKBiU1L6RF966HkFj_4n0th3r_f1lt3ring}
```

## No. 8 
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

### Cara Pengerjaan

Kueri yang digunakan adalah:
```bash
tcp.dstport == 80 || udp.dstport == 80
``` 

Kueri ini untuk memfilter packet yang destination port nya 80, baik melalui protokol TCP atau UDP.


Inputkan kuerinya sebagai jawaban ke server, lalu didapatkan flag.

(ss terminal)

```bash
Here is your flag: Jarkom2023{qu3ryyyyying_661602_EkAuEtBiNzQ_15_fun}
```

## No. 9
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

### Cara Pengerjaan

Kueri yang digunakan adalah:
```bash
ip.src == 10.51.40.1 && ip.dst != 10.39.55.34
``` 

Kueri ini untuk memfilter packet yang berasal dari ip 10.51.40.1, dan tidak menuju ip 10.39.55.34

Inputkan kuerinya sebagai jawaban ke server, lalu didapatkan flag.

(ss terminal)

```bash
Here is your flag: Jarkom2023{y3s_its_SjOkQjRmQmS_qu3ry1ng}
```

## No. 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet.

### Cara Pengerjaan

Analisis pcap nya di wireshark, cari kredensial yang benar.
Filter pcap nya dengan ``telnet``

(ss packet)

Didapatkan beberapa packet yang mengandung kredensial. Inputkan satu persatu ke server sebagai jawaban, lalu didapatkan kredensial yang benar yaitu ``dhafin:kesayangannyak0k0``.

(ss terminal)

```bash
Here is your flag: Jarkom2023{t3lnet_is_BA57yyBz7A7xB35Cx_N0tSecu2e}
```

