# Jarkom_Modul3_Lapres_D09

- 05111840000058 Rafif Ridho
- 05111840000128 Muhammad Rivadhli Purnomo

<br>

#### 1. Membuat Topologi jaringan dengan 3 switch, 4 client, 1 router,  dan 3 server

![img1](/img/1-1.jpg)

* Setting Surabaya sebagai router dengan interface eth0, eth1, eth2, dan eth3

![img1](/img/1-2.jpg)

* Setting Malang dan Mojokerto sebagai server

![img1](/img/1-3.jpg)

![img1](/img/1-4.jpg)

* Setting Gresik, Tuban, Banyuwangi, dan Madiun sebagai client

![img1](/img/1-5.jpg)

![img1](/img/1-6.jpg)

![img1](/img/1-7.jpg)

![img1](/img/1-8.jpg)

#### 2. Surabaya sebagai DHCP Relay. Install isc dhcp relay pada Surabaya, lalu untuk settingan servernya diarahkan ke Tuban dan interfacenya adalah eth1, eth2, dan eth3.

![img1](/img/2-1.jpg)

* Pada interface tuban buat eth0

![img1](/img/2-2.jpg)

* Lalu subnetnya diarahkan ke ip router

#### 3. Client Gresik dan Sidoarjo yang berada pada subnet 1 disetting mendapat range ip dari 192.168.0.10 sampai 192.168.0.100 dan 192.168.0.110 sampai 192.168.0.200

![img1](/img/3-1.jpg)

#### 4. Sedangkan client Banyuwangi dan Madiun yang berada pada subnet 4 disetting mendapat range ip dari 192.168.1.50 sampai 192.168.1.70

![img1](/img/4-1.jpg)

* Lalu cek apaah masing-masing client telah mendapatkan IP setelah semua client di setting IP dinamis dari DHCP

![img1](/img/4-2.jpg)

![img1](/img/4-3.jpg)

![img1](/img/4-4.jpg)

![img1](/img/4-5.jpg)

#### 5. Cek apakah masing-masing client sudah mendapatkan DNS di resolv.conf

![img1](/img/5-1.jpg)

![img1](/img/5-2.jpg)

![img1](/img/5-3.jpg)

![img1](/img/5-4.jpg)

#### 6. Setting max lease time 300 detik untuk subnet 1 dan 600 detik untuk subnet 3

![img1](/img/6-1.jpg)

#### 7. Nyalakan proxy dengan IP Mojokerto, lalu membuat user authentication di /etc/squid/passwd

![img1](/img/7-1.jpg)

* Setelah membuat user authentication

![img1](/img/7-2.jpg)

#### 8. Mengsetting agar internet hanya bisa diakses pada Selasa-Rabu pukul 13:00 - 18:00 perlu membuat acl AVAILABLE_WORKING 

![img1](/img/8-1.jpg)

* Lalu di squid.conf, pada nomor 7 perlu ditambhakan auth_param yang diarahkan passwd yang telah dibuat. Tambahkan juga http_acces allow untuk AVAILABLE_WORKING, AVAILABEL_WORKING_1

![img1](/img/8-2.jpg)

#### 9 . Akses internet Selasa-Kamis 21:0 - 09:00

![img1](/img/8-1.jpg)

* Lalu di squid.conf, ambahkan juga http_acces allow untuk AVAILABLE_WORKING_2

![img1](/img/8-2.jpg)

#### 10. Tambahkan acl ban degann access deny untuk google.com dan arahkan ke monta.if.its.ac.id

![img1](/img/10-1.jpg)

* Saat mengakses google.com

![img1](/img/10-2.jpg)

