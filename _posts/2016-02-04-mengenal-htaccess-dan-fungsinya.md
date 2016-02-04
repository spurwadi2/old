---
layout: post
title: "Mengenal .htaccess dan Fungsinya"
description:
headline: 
category: webmaster
tags: [webmaster, htaccess]
imagefeature: /feature/htaccess.png
imagecredit: allbloggingtips.com
imagecreditlink: 
comments: true
share: true
mathjax: 
---

File .htaccess adalah file konfigurasi yang disediakan oleh web server Apache, yang biasanya digunakan untuk mengubah pengaturan default dari Apache.

Kita ketahui bahwa sebagian besar web hosting di internet menggunakan Apache sebagai servernya sehingga bagi para pengelola web / webmaster sedikit banyak harus belajar tentang .htaccess agar kita bisa mengubah pengaturan default dari server.

File .htaccess merupakan file teks ASCII sederhana yang biasanya diletakkan dalam root direktori. File ini diharuskan dalam format ASCII dan bukan binary dan untuk file permission (atribut file) pada server hosting harus di set 644 (rw-r-r). Hal tersebut dimaksudkan agar server dapat mengakses file .htaccess, tapi mencegah user untuk mengakses file .htaccess dari browser mereka. File .htaccess yang diletakkan dalam root direktori dapat digunakan untuk mengubah konfigurasi dari subdirektori-subdirektori yang ada didalamnya, sehingga dalam satu website biasanya kita cukup untuk mempunyai 1 file .htaccess saja yang diletakkan dalam root direktori.

Kode perintah dalam file .htaccess harus ditempatkan dalam satu baris, jadi apabila kita membuat file .htaccessdengan menggunakan text editor seperti notepad maka kita harus mendisable fungsi word wrap (memotong baris) terlebih dahulu.

# KEGUNAAN FILE .HTACCESS #

<section id="table-of-contents" class="toc">
  <header>
    <h1>File .htaccess dapat digunakan antara lain untuk:</h1>
  </header>
<div id="drawer" markdown="1">
*  Auto generated table of contents
{:toc}
</div>
</section><!-- /#table-of-contents -->

## 1. CUSTOM HTTP ERROR ##

Pesan error pada sebuah website sangat penting karena bisa membantu para pengunjung dalam mengetahui apa yang sedang terjadi. Dengan htaccess kita dapat mengubah halaman error pada server, dengan mendefinisikan sesuai dengan keinginan kita sendiri. Contohnya yaitu pengalihan pesan sesuai fungsinya seperti berikut :

{% highlight html %}
{% raw %}
ErrorDocument 400 /errors/400.html ErrorDocument 401 /errors/401.html ErrorDocument 403 /errors/403.html ErrorDocument 404 /errors/404.html ErrorDocument 500 /errors/500.html
{% endraw %}
{% endhighlight %}

## 2. OVERRIDE SSI SETTINGS ##

Secara default, hanya halaman web yang mempunyai extensi .shtml yang bisa menjalankan server-side termasuk SSI di server. Dengan menggunakan .htaccess kita dapat mengubah setting default tersebut agar SSI bisa bekerja dengan format HTML.

Untuk mengubah pengaturan tersebut, kita dapat menambahkan kode berikut di file .htaccess

{% highlight html %}
{% raw %}
AddType text/html .html
AddHandler server-parsed .html
{% endraw %}
{% endhighlight %}

Jika kita menginginkan halaman yang berekstensi .html dan .htm untuk dapat menjalankan SSI, maka file .htaccessdapat ditambahkan kode berikut

{% highlight html %}
{% raw %}
AddType text/html .html
AddHandler server-parsed .html AddHandler server-parsed .htm
{% endraw %}
{% endhighlight %}

## 3. CHANGE DEFAULT HOME PAGE ##

artinya bahwa file .htaccess dapat digunakan untuk mengubah nama default halaman depan web. Agar user bisa mengakses website kita hanya dengan nama domain saja (http://www.nama_web.com) tanpa harus menulis nama file secara jelas (http:www.nama_web.com/file.html), kita harus mempunyai file index di root direktori. Nama file yang bisa diterima antara lain index.html, index.htm, index.cgi, index.php dll. Pastikan bahwa file tsb bernama index.*

Ada tingkatan dalam pemberian nama tersebut. Jika kita punya index.cgi & index.html di root direktori maka server akan menampilkan index.cgi karena .cgi memiliki tingkatan yang lebih tinggi daripada .html

Dengan .htaccess, kita bisa mendefinisikan file index tambahan atau bisa juga mengubah urutan tingkatannya. Untuk mendefinisikan mainpage.html sebagai halaman index, kita dapat menambahkan kode berikut ke file.htaccess

{% highlight html %}
{% raw %}
DirectoryIndex mainpage.html
{% endraw %}
{% endhighlight %}

Hal ini akan membuat server mencari file bernama mainpage.html. Jika server menemukannya maka server akan menampilkannya. Tapi bila tidak, maka server akan menampilkan error 404 Missing Page

Untuk mengubah urutan tingkatan, kita dapat memasukkan perintah DirectoryIndex dengan nama-nama file dalam satu baris. Urutan penulisan file tersebut menentukan urutan tingkatan, contohnya:

{% highlight html %}
{% raw %}
DirectoryIndex mainpage.html index.cgi index.php index.html
{% endraw %}
{% endhighlight %}

## 4. ENABLE DIRECTORY BROWSING ##

Untuk alasan keamanan, server Apache biasanya telah menghilangkan default setting yang memungkinkan directory indexing. Opsi inilah yang memungkinkan isi dari direktori untuk ditampilkan di browser jika direktori tersebut tidak mempunyai halaman index.

Contohnya, jika kita memasukkan sebuah URL yang tidak mempunyai halaman index seperti misalnya http://domainanda.com/images/, maka browser akan menampilkan daftar images di dalam direktori tersebut

## 5. BLOCK USERS FROM ACCESSING YOUR WEB SITE ##

Jika kita menginginkan mem-blok access untuk beberapa user, dimana kita mengetahui IP / domainname yang digunakannya, kita dapat menambahkan kode berikut :

{% highlight html %}
{% raw %}
order deny,allow
deny from 123.456.789.000
deny from 456.78.90.
deny from .aol.com
allow from all
{% endraw %}
{% endhighlight %}

Pada contoh di atas, user dg IP 123.456.789.000 akan diblok. Semua user antara 456.78.90.000 sampai 456.78.90.999 akan diblok. Dan semua user yang berasal dari AOL.com akan diblok. Jika mereka mencoba mengakses website kita, maka akan tampil error 403 Forbidden (You do not have permission to access this site)

## 6. REDIRECT VISITORS TO A NEW PAGE OR DIRECTORY ##

Misalkan kita membuat ulang seluruh website kita, me-rename halaman & direktori. Maka pengunjung halaman lama akan mendapat error 404 File Not Found. Masalah tersebut dapat diatasi dengan melakukan redirect dari halaman lama ke halaman yang baru. Contohnya bila halaman lama kita adalah oldpage.html dan halaman baru adalah newpage.html maka perintahnya adalah:

{% highlight html %}
{% raw %}
Redirect permanent /oldpage.html http://www.mydomain.com/newpage.htm
{% endraw %}
{% endhighlight %}

Jika kita me-rename (mengganti nama) direktori, maka perintahnya adalah:

{% highlight html %}
{% raw %}
Redirect permanent /olddirectory http://www.mydomain.com/newdirect
{% endraw %}
{% endhighlight %}

Perhatikan bahwa nama direktori yang lama ditulis dengan relative path, sementara yang baru ditulis dengan URLabsolut

## 7. PREVENT HOT LINKING AND BANDWIDTH LEECHING ##

Untuk mencegah orang lain me-link secara langsung ke direktori image anda dari website mereka, biasanya ada orang mengambil gambar dari website kita, tapi tetap menggunakan link diserver host kita, ini tentu akan merugikan bagi kita karena dapat mengurangi bandwith di hosting kita, untuk mengatasi hal ini kita dapat menambahkan kode berikut:

{% highlight html %}
{% raw %}
RewriteEngine on
RewriteCond %{HTTP_REFERER} !^$ RewriteCond %{HTTP_REFERER} !^http://(www.)?namadomain.com/.*$ [NC]
RewriteRule .(gif|jpg)$ - [F]
{% endraw %}
{% endhighlight %}

Perintah tersebut akan membuat direktori image hanya bisa diakses bila user sedang mengakses www.namadomain.com

Jika kita merasa jengkel, kita bisa membuat sebuah image alternatif bila direktori image di-link oleh orang lain. Contohnya kita membuat image alternatif dengan nama nogambar.gif yang bertuliskan: Gambar dr web lain kunjungi http://namadomain.com untuk melihat gambar sebenarnya. Maka kita dapat menambahkan kode berikut:

{% highlight html %}
{% raw %}
RewriteEngine on
RewriteCond %{HTTP_REFERER} !^$ RewriteCond %{HTTP_REFERER} !^http://(www.)?mydomain.com/.*$ [NC]
RewriteRule .(gif|jpg)$ http://www.mydomain.com/dontsteal.gif [R,L]
{% endraw %}
{% endhighlight %}

## 8. PREVENT VIEWING OF .HTACCESS OR OTHER FILES ##

Untuk mencegah user mengakses file .htaccess, ketikkan perintah:

{% highlight html %}
{% raw %}
order allow,deny deny from all
{% endraw %}
{% endhighlight %}

## 9. REWRITING URLS ##

Agar kita dapat melakukan pengaturan pada permalink kita agar lebih SEO friendly kita dapat menambahkan kode berikut ini:

{% highlight html %}
{% raw %}
RewriteEngine On
RewriteBase /
RewriteCond %{REQUEST_FILENAME} !-f RewriteCond %{REQUEST_FILENAME} !-d RewriteRule . /index.php [L]
{% endraw %}
{% endhighlight %}

## 10. MIME TYPES ##

Memerintahkan server untuk mengenali jenis file-file yang belum didaftarkan dalam sistem server. Contohnya :

{% highlight html %}
{% raw %}
AddType application/octet-stream .doc .xls .pdf
{% endraw %}
{% endhighlight %}

## 11. CACHE CONTROL ##

htaccess bisa mengendalikan caching pada web browser sehingga dapat mengurangi penggunaan bandwidth atau aktivitas yang ada didalam server. Contohnya :

{% highlight html %}
{% raw %}
# 480 weeks Header set Cache-Control "max-age=290304000, public" # 2 DAYS Header set Cache-Control "max-age=172800, public, must-revalidate" # 2 HOURS Header set Cache-Control "max-age=7200, must-revalidate"
{% endraw %}
{% endhighlight %}

Dari beberapa kegunaan dari file .htaccess diatas, kita dapat kembangkan sesuai dengan kebutuhan kita.