# PRAKTIKUM MODUL 1 JARINGAN KOMPUTER 2023

## No. 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 

b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 

c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

### Cara Pengerjaan
Melakukan pencarian dan pengecekan terhadap aktifitas yang dilakukan satu persatu hingga mendapatkan yang sesuai pada aktifitas mengunggah file c75-GrabThePhisher.zip. Pada proses request untuk menjawab poin A & B, dan response untuk poin C & D

[![Screenshot-96.png](https://i.postimg.cc/pLdDt7LN/Screenshot-96.png)](https://postimg.cc/rKvd1f4g)

[![Screenshot-97.png](https://i.postimg.cc/2ydzjhDq/Screenshot-97.png)](https://postimg.cc/4HdCBKnZ)

sehingga didapatkan flag

[![image.png](https://i.postimg.cc/dVp40k2t/image.png)](https://postimg.cc/gxyvS0tf)

## No. 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

### Cara Pengerjaan

Filter packet HTTP lalu klik kanan pada salah satu packet HTTP kemudian pilih follow >> HTTP Stream

[![Screenshot-90.png](https://i.postimg.cc/027qqwLx/Screenshot-90.png)](https://postimg.cc/xcjZvcfF)

Kemudian akan tampil sebagai berikut dan terlihat server yang digunakan adalah gunicorn

[![Screenshot-91.png](https://i.postimg.cc/LsF5pP4M/Screenshot-91.png)](https://postimg.cc/PCKTbP86)

Sehingga didapatkan flag berikut :

[![image.png][url=https://ibb.co/Z8L78X7][img]https://i.ibb.co/0MDvM2v/image.png[/img][/url]

## No. 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

b. Protokol layer transport apa yang digunakan?

### Cara Pengerjaan

Filter packet dengan mengetikkan ip.addr == 239.255.255.250 && udp.port == 3702 sehingga didapatkan capture paket sesuai dengan permintaan soal kemudian dihitung dan didapatkan 21 paket

[![Screenshot-92.png](https://i.postimg.cc/hv1XGbsm/Screenshot-92.png)](https://postimg.cc/4HnfLcr4)

Lalu cari informasi protocol dan didapat UDP

[![Screenshot-93.png](https://i.postimg.cc/W4x8mTvn/Screenshot-93.png)](https://postimg.cc/CZHbSydB)

Sehingga didapat flag sebagai berikut:

[![image.png](https://i.postimg.cc/fW13wyv5/image.png)](https://postimg.cc/Dmdf62Hb)

## No. 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?

### Cara Pengerjaan

Buka paketnya lalu cari paket di nomor 130 kemudian cari informasi dibagian frame bawah pada User diagram protocol dan didapat Checksum:0x18e5

[![Screenshot-94.png](https://i.postimg.cc/43T89XQT/Screenshot-94.png)](https://postimg.cc/pmqYNbS0)

sehingga didapatkan flag nya 



## No. 5
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.

a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

b. Port berapakah pada server yang digunakan untuk service SMTP?

c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

### Cara Pengerjaan

[![Screenshot-98.png](https://i.postimg.cc/DZ6YMzXC/Screenshot-98.png)](https://postimg.cc/njskspT7)

## No. 6
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

### Cara Pengerjaan
Cek packet yang ke 7812, source address nya adalah 104.18.14.101.

![6packet](https://github.com/wahyuandhikarizaldi/Jarkom-Modul-1-IT06-2023/assets/113814423/2f02bf97-21da-4908-8b76-2753bd9d0aff)

Sesuai dengan hint yang diberikan, substitusikan dengan a1z26 cipher, rentang huruf A-R, 1-18, dan berjumlah 6 huruf. Maka source address nya akan menjadi:

10.4.18.14.10.1 = JDRNJA

Inputkan jawabannya ke terminal, lalu didapatkan flag.

![image](https://github.com/wahyuandhikarizaldi/Jarkom-Modul-1-IT06-2023/assets/113814423/8b7d39b0-ddc3-4259-bcaf-f7a282fb6fac)


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

![image](https://github.com/wahyuandhikarizaldi/Jarkom-Modul-1-IT06-2023/assets/113814423/75d5da7f-ec80-4ad1-ac34-c62beb9e24a4)

Terdapat 6 packet yang menuju IP 184.87.193.88. Input jawaban ke server, lalu didapatkan flag.

![image](https://github.com/wahyuandhikarizaldi/Jarkom-Modul-1-IT06-2023/assets/113814423/ea02a328-9488-4001-810b-f0b52aff9242)

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

![image](https://github.com/wahyuandhikarizaldi/Jarkom-Modul-1-IT06-2023/assets/113814423/cd815e70-37ad-4f19-bd0d-04aca898c233)


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

![image](https://github.com/wahyuandhikarizaldi/Jarkom-Modul-1-IT06-2023/assets/113814423/757a990a-b40c-41aa-813a-5c84a48196a1)

```bash
Here is your flag: Jarkom2023{y3s_its_SjOkQjRmQmS_qu3ry1ng}
```

## No. 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet.

### Cara Pengerjaan

Analisis pcap nya di wireshark, cari kredensial yang benar.
Filter pcap nya dengan ``telnet``

![image](https://github.com/wahyuandhikarizaldi/Jarkom-Modul-1-IT06-2023/assets/113814423/3d669417-0bf9-4cd6-ab9e-efd543577cc6)


Didapatkan beberapa packet yang mengandung kredensial. Inputkan satu persatu ke server sebagai jawaban, lalu didapatkan kredensial yang benar yaitu ``dhafin:kesayangannyak0k0``.

![image](https://github.com/wahyuandhikarizaldi/Jarkom-Modul-1-IT06-2023/assets/113814423/d4d0f7d4-c329-4507-b2bb-f27b3153e388)


```bash
Here is your flag: Jarkom2023{t3lnet_is_BA57yyBz7A7xB35Cx_N0tSecu2e}
```

