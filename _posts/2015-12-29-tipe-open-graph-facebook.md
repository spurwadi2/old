---
layout: post
type: 
title: "Tipe Open Graph Facebook"
description: 
headline: 
modified: 
category: Webmaster
tags: [webmaster, html, facebook]
imagefeature: /feature/OGfacebook.png
imagecredit: script-tutorials.com
imagecreditlink: 
comments: true
mathjax: 
---

Open Graph Protocol adalah format meta tags yang berfungsi untuk menampilkan objek konten halaman website ke media social facebook. Meta tags Open Graph (og) ini ditempatkan pada header, tepatnya antara <head> dan </head> pada semua halaman website, baik itu halaman utama, kategori, tags, atau post. Dengan menggunakan meta tags ini, saat kita share atau berbagi link halaman website atau blog kita pada facebook, maka pada kolom status akan generate secara otomatis sesuai dengan data yang terdapat pada meta tags Open Graph. Untuk menampilkan format status tersebut sesuai dengan tema website atau blog kita, tentunya kita harus menggunakan Open Graph meta tags pada website dan berikut ini penjelasannya.

Nama Meta Tags Open Graph (Names URI Open Graph) Ada 7 format nama atau names URI yang berfungsi sebagai penanda pembuka penggunaan Open Graph yang ditempatkan pada html dengan menggunakan label prefix, yaitu default, music, video, article, book, profile dan website. Berikut ini kode html Name URI berdasarkan tipenya :

~~~ html
{% raw %}
<html prefix="og: http://ogp.me/ns#">
<html prefix="og: http://ogp.me/ns/music# ">
<html prefix="og: http://ogp.me/ns/video#">
<html prefix="og: http://ogp.me/ns/article#">
<html prefix="og: http://ogp.me/ns/book#">
<html prefix="og: http://ogp.me/ns/profile#">
<html prefix="og: http://ogp.me/ns/website#">
{% endraw %}
~~~

## Tipe Meta Tags Open Graph (Object Types Open Graph)

Ada 12 tipe meta tags open graph atau bahasa inggrisnya disebut sebagai Object Types Open Graph yang berfungsi sebagai objek data dari Names URI berdasarkan tipenya, yaitu

~~~ html
{% raw %}
<meta property="og:type" content="website" />
<meta property="og:type" content="music.song" />
<meta property="og:type" content="music.album" />
<meta property="og:type" content="music.playlist" />
<meta property="og:type" content="music.radio_station" />
<meta property="og:type" content="video.movie" />
<meta property="og:type" content="video.episode" />
<meta property="og:type" content="video.tv_show" />
<meta property="og:type" content="video.other" />
<meta property="og:type" content="article" />
<meta property="og:type" content="book" />
<meta property="og:type" content="profile" />
{% endraw %}
~~~

# Basic Meta Data Open Graph (Dasar)

Basic Meta Data Open Graph adalah meta tags dasar dari penggunaan Open Graph, yang terdiri dari title (judul), type (tipe), url (link) dan image (gambar). Untuk penggunaan kode meta tags dari Basic Meta Data adalah sebagai berikut :

~~~ html
{% raw %}
<meta property="og:title" content="Judul" />
<meta property="og:type" content="article" />
<meta property="og:url" content="http://contoh.com/opengraph/" />
<meta property="og:image" content="http://contoh.com/images/gambar.jpg" />
{% endraw %}
~~~

# Optional Meta Data Open Graph (Tambahan)

Optional Meta Data Open Graph adalah meta tags tambahan dari penggunaan Open Graph, yang terdiri dari description (deskripsi), determiner (kepala judul), locale (bahasa dan wilayah), locale alternate (alternatif bahasa dan wilayah), site name (nama website), audio dan video. Untuk penggunaan kode meta tags dari Optional Meta Data adalah sebagai berikut :

~~~ html
{% raw %}
<meta property="og:description" content="Deskripsi" />
<meta property="og:determiner" content="the" />
<meta property="og:locale" content="en_US" />
<meta property="og:locale:alternate" content="en_GB" />
<meta property="og:locale:alternate" content="id_ID" />
<meta property="og:site_name" content="Contoh.com" />
<meta property="og:audio" content="http://contoh.com/audio/lagu.mp3" />
<meta property="og:video" content="http://contoh.com/video/contoh-video.flv" />
{% endraw %}
~~~

# Penggunaan Open Graph Meta Tags

Jadi untuk penggunaan Open Graph Meta Tags dari penjelasan diatas adalah Names URI pada html, basic meta data dan optional meta data. Berikut ini adalah contoh penggunaan Open Graph Meta Tags hanya dengan menggunakan basic meta data dan optional meta data untuk tipe Artikel :

~~~ html
{% raw %}
<html prefix="og: http://ogp.me/ns/article#">
<head>
<title>Judul</title>
<meta property="og:title" content="Judul" />
<meta property="og:type" content="article" />
<meta property="og:site_name" content="contoh.com" />
<meta property="og:description" content="Deskripsi" />
<meta property="og:url" content="http://contoh.com/opengraph/" />
<meta property="og:image" content="http://contoh.com/images/gambar.jpg" />
<meta property="og:determiner" content="the" />
<meta property="og:locale" content="en_US" />
<meta property="og:locale:alternate" content="en_GB" />
<meta property="og:locale:alternate" content="id_ID" />
<meta property="og:audio" content="http://contoh.com/audio/lagu.mp3" />
<meta property="og:video" content="http://contoh.com/video/contoh-video.flv" />
</head>
<body></body>
</html>
{% endraw %}
~~~

## Struktur Properties Untuk Data Detail (Structured Properties)

Structured Properties adalah meta tags property open graph sebagai value data tambahan dari object atau tipe. Data value yang bisa ditambahkan sebagai data detail pada meta property adalah image, video, music, article, profile dan book.

# Image Structured Properties

Penggunaan Image Structured Properties berfungsi untuk memberikan data yang lebih detail untuk gambar pada open graph (og:image), yaitu menambahkan ukuran gambar seperti width dan height. Untuk contoh penggunaannya sbb :

~~~ html
{% raw %}
<meta property="og:image" content="http://contoh.com/gambar.jpg" />
<meta property="og:image:secure_url" content="https://secure.contoh.com/gambar.jpg" />
<meta property="og:image:type" content="image/jpeg" />
<meta property="og:image:width" content="620" />
<meta property="og:image:height" content="348" />
{% endraw %}
~~~

# Video Structured Properties

Penggunaan Video Structured Properties berfungsi untuk memberikan data yang lebih detail untuk video pada open graph (og:video). Untuk data yang ditampilkan dibagi 3 berdasarkan object types pada open graph, seperti og:video.movie, og:video.episode dan og:video.tv_show. Untuk contoh penggunaan video structured properties Open Graph adalah sbb :

Penggunaan type og:video.movie

~~~ html
{% raw %}
<meta property="og:video:actor" content="Nama Aktor Pada Video" />
<meta property="og:video:actor:role" content="Role Actor" />
<meta property="og:video:director" content="Nama Movie Director" />
<meta property="og:video:writer" content="Nama Penulis" />
<meta property="og:video:duration" content="Durasi Video dalam detik" />
<meta property="og:video:release_date" content="Tanggal Rilis Video" />
<meta property="og:video:tag" content="Video Tag" />
{% endraw %}
~~~

Penggunaan type og:video.episode dan og:video.tv_show

~~~ html
{% raw %}
<meta property="og:video:actor" content="Nama Aktor Pada Video" />
<meta property="og:video:actor:role" content="Role Actor" />
<meta property="og:video:director" content="Nama Movie Director" />
<meta property="og:video:writer" content="Nama Penulis" />
<meta property="og:video:duration" content="Durasi Video dalam detik" />
<meta property="og:video:release_date" content="Tanggal Rilis Video" />
<meta property="og:video:tag" content="Video Tag" />
<meta property="og:video:series" content="Episode Video" />
{% endraw %}
~~~

# Music Structured Properties

Penggunaan Music Structured Properties berfungsi untuk memberikan data yang lebih detail untuk music pada open graph (og:music). Untuk data yang ditampilkan dibagi 4 berdasarkan object types pada open graph, seperti og:music.song, og:music.album, og:music.playlist dan og:music.radio_station. Untuk contoh penggunaan music structured properties Open Graph adalah sbb :

Penggunaan type og:music.song

~~~ html
{% raw %}
<meta property="og:music:duration" content="Durasi Musik Dalam Detik" />
<meta property="og:music:album" content="Nama Album dari Musik tsb" />
<meta property="og:music:album:disc" content="Disc Dari Musik tsb" />
<meta property="og:music:album:track" content="Track Dari Musik tsb" />
<meta property="og:music:musician" content="Nama Musisi" />
{% endraw %}
~~~

Penggunaan type og:music.album

~~~ html
{% raw %}
<meta property="og:music:song" content="Judul Lagu" />
<meta property="og:music:song:disc" content="Disk Dari Lagu tsb" />
<meta property="og:music:song:track" content="Track Dari Lagu tsb" />
<meta property="og:music:musician" content="Nama Musisi" />
<meta property="og:music:release_date" content="Tanggal Rilis Lagu" />
{% endraw %}
~~~

Penggunaan type og:music.playlist

~~~ html
{% raw %}
<meta property="og:music:song" content="Judul Lagu" />
<meta property="og:music:song:disc" content="Disk Dari Lagu tsb" />
<meta property="og:music:song:track" content="Track Dari Lagu tsb" />
<meta property="og:music:creator" content="Pembuat Playlist Lagu" />
Penggunaan type og:music.radio_station
<meta property="og:music:creator" content="Pembuat Playlist Lagu" />
{% endraw %}
~~~

# Article Structured Properties

Penggunaan Article Structured Properties berfungsi untuk memberikan data yang lebih detail untuk article pada open graph (og:article). Untuk contoh penggunaan article structured properties Open Graph adalah sbb :

~~~ html
{% raw %}
<meta property="og:article:published_time" content="Tanggal di Publikasikan" />
<meta property="og:article:modified_time" content="Tanggal di Modifikasi" />
<meta property="og:article:expiration_time" content="Tanggal Expired" />
<meta property="og:article:author" content="Nama Penulis" />
<meta property="og:article:section" content="Kategori Artikel" />
<meta property="og:article:tag" content="Tag Artikel" />
{% endraw %}
~~~

# Profile Structured Properties

Penggunaan Profile Structured Properties berfungsi untuk memberikan data yang lebih detail untuk article pada open graph (og:profile). Untuk contoh penggunaan profile structured properties Open Graph adalah sbb :

~~~ html
{% raw %}
<meta property="og:profile:first_name" content="Nama Depan" />
<meta property="og:profile:last_name" content="Nama Belakang" />
<meta property="og:profile:username" content="User Name" />
<meta property="og:profile:gender" content="Jenis Kelamin" />
{% endraw %}
~~~

# Book Structured Properties

Penggunaan Book Structured Properties berfungsi untuk memberikan data yang lebih detail untuk article pada open graph (og:book). Untuk contoh penggunaan book structured properties Open Graph adalah sbb :

~~~ html
{% raw %}
<meta property="og:book:author" content="Nama Penulis" />
<meta property="og:book:isbn" content="ISBN Buku" />
<meta property="og:book:release_date" content="Tanggal Rilis Buku" />
<meta property="og:book:tag" content="Tag Buku" />
{% endraw %}
~~~