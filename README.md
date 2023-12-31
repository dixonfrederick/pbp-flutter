# Covid Information App

[![pipeline status](https://gitlab.com/dixonfrederick/pbp-flutter/badges/main/pipeline.svg)](https://gitlab.com/dixonfrederick/pbp-flutter/-/commits/main)

# PBP D Kelompok 9
- Dixon Frederick - 2006597840
- Anindya Sasriya Ibrahim - 2006597714
- Paskalis Abhista Bagaskara Y - 2006597733
- M Margaretha Stella Kalyanaduhita T - 2006597815
- Muhammad Abdurahman Basyah - 2006597241
- Muhammad Arkan Fauzan - 2006597380
- Al Ghifari Enerza Sentanu - 2006596825

## Link Download APK: 
https://drive.google.com/file/d/1luM7ld1A4No4IuZ8SqOPSara6Bsllscj/view?usp=sharing

## Cerita Modul dan Implementasi Web Service
Kami akan membuat suatu aplikasi yang berisi informasi yang valid seputar Covid-19, dengan tujuan untuk mengedukasi para pengguna. Aplikasi ini akan berisi hal-hal yang perlu dilakukan atau dihindari di masa pandemi, data kasus Covid-19, informasi vaksinasi, dan hal-hal terkait lainnya.
Modul yang akan diimplementasikan pada aplikasi ini akan merujuk pada modul-modul pada situs [Covid App](http://covid-information-app.herokuapp.com/) yang telah kami buat sebelumnya, yaitu sebagai berikut:
1. **Authorization & Authentication** <br>
Modul ini akan memberikan akun kepada pengguna yang mendaftar pada situs [Covid App](http://covid-information-app.herokuapp.com/) dan data yang disimpan akan terhubung ke _database_ yang ada pada Django. Semua yang telah diintegrasikan di situs akan diimplementasikan ke dalam bentuk _mobile app_ seperti _profile page, login page,_ dan _registration page_.
2. **Home & Info seputar Covid-19** <br>
Halaman utama pada aplikasi, yang juga berisi informasi seputar Covid-19 yang dapat langsung dilihat oleh pengguna.
3. **Data kasus Covid-19** <br>
Berisi update data jumlah kasus Covid-19 (positif, sembuh, meninggal), baik secara nasional, maupun pada berbagai daerah di Indonesia.
4. **Info terkait vaksin** <br>
Sama seperti fungsinya pada situs [Covid App](http://covid-information-app.herokuapp.com/), modul ini akan menampilkan banyaknya jumlah orang yang sudah melaksanakan vaksinasi baik vaksinasi pertama maupun kedua berdasarkan kategorinya(data yang terlibat bukan merupakan data yang sebenarnya). Modul ini juga akan melakukan _request_ kedalam _database_ Django sehingga nantinya data yang ditampilkan dapat seragam dengan data yang berada pada situs [Covid App](http://covid-information-app.herokuapp.com/).
5. **Indeks kewaspadaan tiap daerah** <br>
Modul ini akan menampilkan indeks kewaspadaan dengan beberapa kategori, seperti yang telah diimplementasikan pada situs [Covid App](http://covid-information-app.herokuapp.com/), melalui iframe yang pada flutter, dapat ditampilkan dengan WebView atau [InAppWebView](https://newbedev.com/flutter-loading-an-iframe-from-webview). Data iframe yang akan ditampilkan tersebut diambil dengan metode GET pada _database_ views Django, yang akan mengembalikan sebuah JsonResponse berupa data nama dan source iframe. Untuk pengguna berupa admin, maka akan dapat menambahkan nama dan source untuk kategori indeks lainnya.
6. **Rujukan rumah sakit** <br>
Modul berfungsi sama seperti pada situs [Covid App](http://covid-information-app.herokuapp.com/), menampilkan daftar rumah sakit rujukan yang merupakan objek model pada database Django. Jika pengguna merupakan admin, bisa menambah rumah sakit rujukan.
7. **Forum Discussion** <br>
Modul ini adalah implementasi forum diskusi seputar Covid-19, yang dapat diisi oleh User (pengguna yang sudah login).

Manfaat yang ingin kami berikan untuk masyarakat dari aplikasi ini adalah memberikan informasi yang akurat terkait Covid-19, sehingga diharapkan dapat membantu dalam mengedukasi dan meningkatkan kewaspadaan masyarakat terhadap Covid-19 serta menekan peningkatan kasus Covid-19 di Indonesia.

Persona
- Guest Mode: dapat melihat informasi yang ada, tetapi tidak dapat bergabung ataupun mem-posting pada forum discussion.
- User: dapat melihat seluruh informasi yang ada pada website, serta dapat bergabung dalam forum discussion dan dapat mem-posting dalam forum discussion, namun tidak dapat menghapus postingan pada forum discussion.
- Administrator: dapat menghapus postingan yang sudah di-post pada forum discussion.
