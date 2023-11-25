Hai, Rekan CloudKilat pada kesempatan ini kami akan memberikan informasi tentang apa itu whois? cara instalasi di terminal linux dan fungsi grep pada perintah whois.

Untuk mempersingkat waktu, kita langsung saja pada point pertama apa itu whois? whois merupakan perintah atau protocol yang digunakan untuk mengakses basis data publik yang menyimpan informasi tentang kepemilikan atau registrasi sumber daya internet, seperti nama domain dan alamat IP. Dengan menggunakan whois, seseorang dapat mencari informasi tentang siapa yang memiliki atau mengelola suatu domain atau alamat IP, termasuk informasi kontak dan detail registrasi. Penting untuk dicatat bahwa beberapa penyedia domain atau organisasi mungkin membatasi akses ke informasi whois untuk melindungi privasi pengguna mereka.

## Instalasi WHOIS
1. Masuk ke terminal
2. Lakukan update repository dengan menjalankan perintah dibawah ini:

```
$ yum -y update (os turunan RHEL)
$ apt -y update (os turunan Ubuntu & Debian)
```

3. Setelah proses update selesai, dilanjutkan dengan instalasi whois dengan menjalankan perintah dibawah ini:

```
$ yum -y install whois (os turunan RHEL)
$ apt -y install whois (os turunan Ubuntu & Debian)
```

4. Berikut detail lampiran selama proses instalasi berlangsung hingga selesai dan siap digunakan:

![whois install](https://internal.s3-id-jkt-1.kilatstorage.id/KB/Install%20whois.png)

5. Berikut baris perintah untuk mendapatkan hasil data WHOIS:

```
$ whois nama-domaiin.tld
$ whois ip-public
```

## Implementasi fungsi grep pada perintah WHOIS
grep adalah utilitas baris perintah pada sistem operasi Unix dan sejumlah sistem operasi berbasis Unix (termasuk Linux) yang digunakan untuk mencari dan memfilter teks dalam file atau output dari perintah lainnya. Fungsi utama dari grep adalah mencocokkan pola teks di dalam suatu file atau output dan menampilkan baris yang sesuai dengan pola tersebut, untuk knowledge base kali ini kami berfokus pada fungsi grep untuk memfilter output dari perintah lain (WHOIS) dengan menggunakan pipa (|).

Implementasi fungsi grep pada perintah WHOIS ini diperlukan untuk mempermudah kita mengetahui informasi penting dari hasil whois yang bisanya menampilkan banyak informasi dan berikut contoh implementasi berserta hasil dari perintahnya:

1. Mengetahui Informasi Registrar Domain

```
$ whois nama-domaiin.tld |grep "Registrar" 
```

2. Mengetahui Informasi Status Domain

```
$ whois nama-domaiin.tld |grep "Status" 
```

3. Mengetahui Informasi Expired Date Domain

```
$ whois nama-domaiin.tld |grep "Exp" 
```

4. Mengetahui Informasi Nameserver Domain

```
$ whois nama-domaiin.tld |grep "Server" 
```

5. Berikut hasil dari pengaplikasiannya

![whois hasil](https://internal.s3-id-jkt-1.kilatstorage.id/KB/Hasil%20Whois.png)

