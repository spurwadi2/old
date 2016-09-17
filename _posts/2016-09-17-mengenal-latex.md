---
layout: post
title: "Mengenal LaTeX"
description: "What You See Is What You Mean"
headline: 
category: Education
tags: [education, computer, jekill, latex]
imagefeature: feature/equation.jpg
imagecredit: 
imagecreditlink: 
comments: true
mathjax: true
---

Dalam dunia karya tulis ilmiah, Latex merupakan primadona. Banyak jurnal-jurnal ilmiah internasional yang mencantumkan syarat, *article must be written in latex format*, artikel wajib ditulis dalam format latex. Mulai jurnal ilmiah untuk disiplin ilmu alam sampai disiplin ilmu sosial.

Dalam dunia IT, paket Office yang berbasis WYSIWYG (*What You See is What You Get*) sudah menjadi standar industri dalam penggunaan di dunia akademisi, perkantoran, sekretariat, dan tata usaha. Microsoft Office, iWork, Libre Office dan Open Office adalah beberapa aplikasi standard untuk keperluan itu. Namun, dalam *scientific writing*, ternyata office WYSIWYG bukanlah satu-satunya opsi dalam menulis artikel ilmiah. Tersedia juga LaTeX untuk menunjang keperluan tersebut.

$$\rm\LaTeX$$ merupakan aplikasi penulisan dokumen yang berkualitas tinggi. Tidak seperti aplikasi office lain, aplikasi ini memiliki gaya penulisan script yang bersifat WYSIWYM (*What You See Is What You Mean*), yang mengedit struktur dalam sebuah dokumen untuk sebuah hasil yang dimaksud atau diinginkan.

Latex menjadi amat powerful ketika kita bekerja menggunakan banyak sekali formula matematika, banyak tabel dan banyak gambar. Sekali kita menulis artikel dengan latex, maka ketika tulisan yang sama ingin kita ubah menjadi format buku, ini akan mudah sekali dan mengasyikkan. Kita tidak perlu gelisah dengan persoalan bab, sub bab, daftar isi, atau daftar referensi. Kita juga tidak akan dipusingkan dengan penomoran rumus, tabel dan gambar. Pendek kata, Latex merupakan andalan kalau ingin menulis ilmiah.

Bagi banyak ilmuwan, seringkali penulisan dokumen menggunakan LaTeX merupakan keharusan. Tetapi penulisan dokumen menggunakan LaTeX seringkali menyebabkan dahi berkerut dibandingkan menggunakan pengolah kata komersil yang sudah ada. Seringkali muncul pertanyaan, kenapa LaTeX? Atau, apakah itu LaTeX?

## LaTex? ##

[$$\rm\LaTeX$$](https://id.wikipedia.org/wiki/LaTeX) [^1] adalah sebuah sistem untuk mempersiapkan dokumen (dilafalkan ‘*la-te(c)h*’, sama seperti saat kita mengeja kata *technology*), dengan LaTeX maka bisa dibuat suatu dokumen yang terbaca. Apakah itu berarti sama dengan pengolah kata komersil, sebutlah Microsoft Word? Atau yang gratis seperti Open Office? Kalau hanya sekedar ‘mengolah kata’, memang hanya itulah kesamaannya.

### Kenapa namanya LaTeX? ###

Etimologi LaTeX dimulai ketika Donald Knuth menciptakan TeX, sekitar tahun 1978, dari tiga huruf besar Yunani, *Tau*, *Epsilon* dan *Chi*, yang dalam bahasa inggris menjadi akar kata dari “*technical*” dan “*technique*”, ketika kemudian Leslie Lamport mengembangkan supaya TeX bisa lebih dipergunakan secara lebih sederhana, maka diperkenalkan LaTeX, mungkin agar bisa disesuaikan dengan namanya?

Ada 10 alasan kenapa LaTeX dipilih oleh para ilmuwan:

1. Keluaran TeX selalu yang terbaik, baik tulisan, gambar, rumus, format, tanpa bergantung pada peralatan tambahan, huruf tambahan. Baik untuk dokumen sederhana maupun dokumen yang rumit. Bayangkan menulis rumus dalam Microsft Words, yang harus bergantung pada Microsoft Equation, bagaimana jika rumusnya rumit-rumit, atau hurufnya besar kecil, sesuatu yang tidak muncul dalam tulisan sehari-hari? LaTeX juga menyediakan semua peralatan untuk membuat tabel, *cross-references*, *hyper-links*, yang bisa dilakukan dengan mudah. Karena kemudahan dan keunggulan dalam menuliskan rumus-rumus yang ajaib, maka TeX adalah pilihan terbaik untuk dokumen-dokumen ilmiah. Dan itu dilakukan menggunakan penulisan text standar saja.

2. LaTeX dan typesetting, LaTeX bisa mengatur simbol untuk variabel, berapa besar dan ruang yang dibutuhkan bagi notasi, superscript dan subscript, dsb. Bagan, flow chart, not balok, atau gambar rangkaian dapat dikerjakan dengan mudah. Bahkan dari penulisan standar bisa digunakan untuk menuliskan karakter-karakter bahasa di seluruh muka Bumi. Dengan demikian setiap dokumen dengan mudah mengikuti standar penulisan yang dibutuhkan, per se, tanpa harus berpusing-pusing mengatur format, setiap kali menulis.

3. LaTeX selalu cepat, karena untuk menulis dalam LaTeX bisa saja menggunakan text standard, maka menggunakan notepad pun bisa dilakukan, yang berarti mengirit ruang dan memori komputer.

4. LaTeX selalu stabil, sejak diperkenalkan, dipergunakan oleh jutaan orang, tidak pernah ada keluhan berarti, bahkan banyak yang membantu mengembangkannya. Stabil berarti LaTeX itu bekerja, dan akan terus bekerja, karena semakin banyak orang yang mempekerjakannya.

5. LaTeX itu luwes, setiap institusi, setiap jurnal punya gayanya sendiri, dan tidak hanya dalam ‘gaya’ yang ada di luarnya, tetapi juga dalam pengembangan engine-nya; tetapi terlepas semua pilihan yang dipergunakan, inti terdalam LaTeX itu selalu tetap sama.

6. Input yang selalu text. Dengan demikian, maka bekerja bisa dilakukan di komputer model apa saja, sistem operasi apa saja, dan untuk keperluan apa saja, jauh dari hanya sekedar pengolah-kata, tetapi bisa dikembangkan untuk basis data, atau keperluan yang memerlukan sumber daya yang besar, tetapi tidak boros.

7. Keluaran bisa berupa apa saja, dari sekedar untuk keperluan pencetakan, seperti pdf, ps, atau sekedar menampilkan seperti html, bahkan terbuka untuk pengembangan yang belum terpikirkan sebelumnya.

8. LaTeX itu gratis.

9. LaTeX itu bisa digunakan di mana saja, tanpa memandang sistem operasi, jenis komputer, atau jenis media.

10. LaTeX itu standar. Banyak penerbitan ilmiah dan Jurnal mempergunakan laTeX sebagai standar penyusunan dokumen.

## Menulis LaTeX ##

Dibanding pengolah kata standar yang bersifat WYSIWYG, bekerja dalam LaTeX lebih seperti membuat pemrograman, karena harus berurusan dengan kode-kode. Kode-kode ini harus di-*compile* agar memproduksi dokumen. Hal ini tidak berbeda dengan bahasa lain seperti C++ dan Java.

Tetapi LaTeX menjadi pilihan komunitas sains internasional karena kualitas yang dihasilkan, gratis, bisa dipergunakan semua jenis komputer, semua sistem operasi, dan bisa dipergukanakan untuk menampilkan hal-hal yang sulit dilakukan oleh pengolah kata standar.

Bagi yang belum pernah bekerja dengan LaTeX, mungkin bisa dibayangkan seperti menyusun dokumen untuk HTML, tetapi LaTeX sendiri jauh lebih dari sekedar itu saja.

Untuk menulis dokumen dengan LaTex ada beberapa aplikasi yang dibutuhkan:

- Kompiler : TexLive / Miktex (windows)
- Editor : TexMaker, Kile, TexWork
- Pemindai PDF : Okular, sumatra pdf, Foxit.

Semua aplikasi yang digunakan untuk menulis Latex merupakan aplikasi open source yang bebas pakai. Sehingga kita tidak perlu membeli lisensi untuk menggunakanya.

Selain itu, aplikasi tersebut adalah aplikasi yang dapat di gunakan di berbagai sistem operasi (cross platform). Sehingga memiliki portabilitas yang tinggi.

Selain itu, Latex juga mendukung penggunaan template. Template untuk artikel ilmiah, disertasi, bahkan presentasi (*beamer*) juga tersedia, dan kita hanya melakukan sedikit penyesuaian sebelum di-*compile*.

Dengan template akan membuat beban kerja dari penulis dapat dikurangi. Mengapa demikian? Karena dengan adanya template, penulis tidak perlu lagi mengatur dokumen yang dibuat. Artinya disain penulisan, bentuk huruf, dan dimensi kertas sudah diatur di template tersebut. Penulis tinggal memasukkan isi dari materi yang ingin ditulis.

## Reference Manager LaTeX ##

Nah, bagi yang terbiasa menggunakan aplikasi Office, kemungkinan pernah menggunakan *Reference Manager* (RefMan) seperti EndNote. Secara default, RefMan untuk LaTeX harus di-*coding*, dan di-*compile* juga, sama seperti dokumen utama.

BibTex adalah format standard untuk sitasi referensi dalam LaTex. Namun, kita tidak perlu khawatir untuk mengatur kode perintah, sebab sudah disediakan RefMan yang dapat membantu pekerjaan kita.

Beberapa RefMan yang umum digunakan untuk aplikasi Office, seperti Mendeley Desktop dan lainnya, dapat mengeksport citation ke dalam format BibTex. RefMan yang digunakan oleh penulis adalah JabRef, yang merupakan program Java, yang multiplatform.

JabRef memiliki fitur *automatic citation*, yang memungkinkan kita melakukan pencarian otomatis terhadap sitasi di database PubMed/Medline. Sehingga, sitasi dapat secara otomatis disimpan dalam format BibTex. Rasanya, dengan banyaknya opsi untuk RefMan, seharusnya sitasi dapat diatur dengan mudah, sesuai dengan selera kita.

## Contoh penulisan rumus matematika dengan $$\rm\LaTeX$$ ##

Nah, di poin inilah keunggulan LaTeX terlihat nyata dibandingkan aplikasi Office. Walaupun aplikasi Office juga memiliki *Equation Editor*, banyak yang berpendapat bahwa bagaimanapun LaTeX lebih superior untuk menangani rumus matematika.

Namun terlepas perdebatan mengenai superioritas masing-masing package, harus ditekankan bahwa Office dan LaTeX tidak seyogyanya dibandingkan secara *apple to apple*.

Dalam bidang studi yang tidak memerlukan banyak penggunaan rumus matematika, mungkin aplikasi Office sudah cukup untuk membantu. Sementara, jika bidang studi kita bersinggungan dengan sains dan teknologi, terutama *hard core computation*, Fisika dan Matematika Teoritis, rasanya LaTeX yang dapat lebih banyak berperan di sini.

Lalu bagaimana membuat rumus dalam LaTeX? Caranya tidak lebih sama dengan yang disebut di atas, yaitu menggunakan tag dan simbol yang kemudian di-*compile*. Namun, apakah sukar menulis rumus di LaTeX? Ternyata tidak demikian, karena front end GUI juga tersedia untuk penulisan rumus matematika.

Di MacOSX, untuk keperluan itu, tersedia LaTeXiT. Bahkan wikipedia menyediakan daftar lengkap mengenai rumus matematika LaTeX yang umum digunakan di sini. Tutorial dan Template rumus juga sangat banyak tersedia di web.

**The Lorenz Equations**

{% highlight css %}
{% raw %}
\begin{aligned}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{aligned}
{% endraw %}
{% endhighlight %}

kode di atas jika diterjemahkan maka akan menjadi

$$\begin{aligned}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{aligned}$$

**The Cauchy-Schwarz Inequality**

{% highlight css %}
{% raw %}
\left( \sum_{k=1}^n a_k b_k \right)^{\!\!2} \leq
 \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
{% endraw %}
{% endhighlight %}

menjadi

$$
\left( \sum_{k=1}^n a_k b_k \right)^{\!\!2} \leq
 \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
$$

**A Cross Product Formula**

{% highlight css %}
{% raw %}
  \mathbf{V}_1 \times \mathbf{V}_2 =
   \begin{vmatrix}
    \mathbf{i} & \mathbf{j} & \mathbf{k} \\
    \frac{\partial X}{\partial u} & \frac{\partial Y}{\partial u} & 0 \\
    \frac{\partial X}{\partial v} & \frac{\partial Y}{\partial v} & 0 \\
   \end{vmatrix}
{% endraw %}
{% endhighlight %}

$$
  \mathbf{V}_1 \times \mathbf{V}_2 =
   \begin{vmatrix}
    \mathbf{i} & \mathbf{j} & \mathbf{k} \\
    \frac{\partial X}{\partial u} & \frac{\partial Y}{\partial u} & 0 \\
    \frac{\partial X}{\partial v} & \frac{\partial Y}{\partial v} & 0 \\
   \end{vmatrix}
$$

**The probability of getting \(k\) heads when flipping \(n\) coins is:**

{% highlight css %}
{% raw %}
P(E) = {n \choose k} p^k (1-p)^{ n-k} 
{% endraw %}
{% endhighlight %}

$$P(E) = {n \choose k} p^k (1-p)^{ n-k} $$

**Isotop**

{% highlight css %}
{% raw %}
{^{14}_{7}N}
{% endraw %}
{% endhighlight %}

$${^{14}_{7}N}$$

**Persamaan Kimia**

{% highlight css %}
{% raw %}
{SO4^2- + Ba^2+ -> BaSO4}
{% endraw %}
{% endhighlight %}

$${SO4^2- + Ba^2+ -> BaSO4}$$

## LaTeX Bukan untuk Menggusur Office ##

Sebenarnya, Office dan LaTeX tidak bersaing dalam pasar yang sama. Kedua package tersebut memiliki niche sendiri, walau tentu saja, Office memiliki *niche* yang jauh lebih besar.

Submission artikel ke jurnal ilmiah umumnya juga diberikan opsi dalam format PDF. Tentu saja hal ini sangat welcome jika di-*compile* dengan LaTeX, selama kita juga menyediakan source code dan file gambar kepada penerbit.

Selain submission ke jurnal ilmiah, menulis skripsi/tesis/disertasi juga merupakan hal yang lumrah dilakukan dengan LaTeX.

Penulis sendiri pernah menulis tugas akhir dan publikasi ilmiah dengan Office dan LaTeX, dan menemukan bahwa kedua package tersebut memiliki kelebihan dan kelemahannya masing-masing.

Namun selama skill programming bukan masalah, LaTeX juga dapat dinikmati kemudahannya, seperti juga Office. Walaupun demikian, tidak ada masalah mana yang user lebih sukai.

Dalam konteks akademis, pemilihan penggunaan Office dan LaTeX adalah murni adalah kebijakan dari *Peer Group* riset yang bersangkutan. Oleh karena itu, hal ini bisa berbeda antara satu institusi, dengan yang lain, dan tidak bisa digeneralisir.

Sementara itu, di dunia bisnis/korporasi, tentu saja paket Microsoft Office merupakan standard de facto untuk aplikasi produktifitas.

Adapun jika pada akhirnya terpaksa juga Office dan LaTeX dibandingkan secara *apple to apple*, user akan untung juga. Aplikasi Office, seperti Libre, Neo dan Open Office, adalah aplikasi Open Source, sementara jelas LaTeX adalah Open Source.

Pada akhirnya, ‘*benchmarking*’ antara LaTeX dan Office, jika diletakkan dalam kacamata Open Source, selalu akan menguntungkan komunitas yang menggunakannya.


[^1]: [https://id.wikipedia.org/wiki/LaTeX](https://id.wikipedia.org/wiki/LaTeX)