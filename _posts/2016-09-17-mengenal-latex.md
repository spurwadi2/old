---
layout: post
title: "Mengenal LaTex"
description: ""
headline: 
category: Education
tags: [education, computer, jekill]
imagefeature: 
imagecredit: 
imagecreditlink: 
comments: true
mathjax: true
---

Dalam dunia karya tulis ilmiah, Latex merupakan primadona. Banyak jurnal-jurnal ilmiah internasional yang mencantumkan syarat, article must be written in latex format, artikel wajib ditulis dalam format latex. Mulai jurnal ilmiah untuk disiplin ilmu alam sampai disiplin ilmu sosial.

Latex menjadi amat *powerful* ketika kita bekerja menggunakan banyak sekali formula matematika, banyak tabel dan banyak gambar. Sekali kita menulis artikel dengan latex, maka ketika tulisan yang sama ingin kita ubah menjadi format buku, ini akan mudah sekali dan mengasyikkan. Kita tidak perlu gelisah dengan persoalan bab, sub bab, daftar isi, atau daftar referensi. Kita juga tidak akan dipusingkan dengan penomoran rumus, tabel dan gambar. Pendek kata, Latex merupakan andalan kalau ingin menulis ilmiah.

Bagi banyak ilmuwan, seringkali penulisan dokumen menggunakan LaTeX merupakan keharusan. Tetapi penulisan dokumen menggunakan LaTeX seringkali menyebabkan dahi berkerut dibandingkan menggunakan pengolah kata komersil yang sudah ada. Seringkali muncul pertanyaan, kenapa LaTeX? Atau, apakah itu LaTeX?

## LaTex? ##

[LaTeX](https://id.wikipedia.org/wiki/LaTeX) [^1] adalah sebuah sistem untuk mempersiapkan dokumen (dilafalkan ‘*la-te(c)h*’, sama seperti saat kita mengeja kata *technology*, bukan latex), dengan LaTeX maka bisa dibuat suatu dokumen yang terbaca. Apakah itu berarti sama dengan pengolah kata komersil, sebutlah Microsoft Word(TM)? Atau yang gratis seperti Open Office? Kalau hanya sekedar ‘mengolah kata’, memang hanya itulah kesamaannya.

Kenapa namanya LaTeX? Etimologi LaTeX dimulai ketika Donald Knuth menciptakan TeX, sekitar tahun 1978, dari tiga huruf besar Yunani, Tau, Epsilon dan Chi, yang dalam bahasa inggris menjadi akar kata dari “*technical*” dan “*technique*”, ketika kemudian Leslie Lamport mengembangkan supaya TeX bisa lebih dipergunakan secara lebih sederhana, maka diperkenalkan LaTeX, mungkin agar bisa disesuaikan dengan namanya?

## Kode-kode ##

Dibanding pengolah kata standar yang bersifat WYSIWYG (*What You See is What You Get*), bekerja dalam LaTeX lebih seperti membuat pemrograman, karena harus berurusan dengan kode-kode, tetapi LaTeX menjadi pilihan komunitas sains internasional karena kualitas yang dihasilkan, gratis, bisa dipergunakan semua jenis komputer, semua sistem operasi, dan bisa dipergukanakan untuk menampilkan hal-hal yang sulit dilakukan oleh pengolah kata standar.

Bagi yang belum pernah bekerja dengan LaTeX, mungkin bisa dibayangkan seperti menyusun dokumen untuk HTML, tetapi LaTeX sendiri jauh lebih dari sekedar itu saja.

Ada 10 alasan kenapa LaTeX dipilih oleh para ilmuwan:

1. Keluaran TeX selalu yang terbaik, baik tulisan, gambar, rumus, format, tanpa bergantung pada peralatan tambahan, huruf tambahan. Baik untuk dokumen sederhana maupun dokumen yang rumit. Bayangkan menulis rumus dalam Microsft Words(TM), yang harus bergantung pada Microsoft Equation(TM), bagaimana jika rumusnya rumit-rumit, atau hurufnya besar kecil, sesuatu yang tidak muncul dalam tulisan sehari-hari? LaTeX juga menyediakan semua peralatan untuk membuat tabel, cross-references, hyper-links, yang bisa dilakukan dengan mudah. Karena kemudahan dan keunggulan dalam menuliskan rumus-rumus yang ajaib, maka TeX adalah pilihan terbaik untuk dokumen-dokumen ilmiah. Dan itu dilakukan menggunakan penulisan text standar saja.

2. LaTeX dan typesetting, LaTeX bisa mengatur simbol untuk variabel, berapa besar dan ruang yang dibutuhkan bagi notasi, superscript dan subscript, dsb. Bagan, flow chart, not balok, atau gambar rangkaian dapat dikerjakan dengan mudah. Bahkan dari penulisan standar bisa digunakan untuk menuliskan karakter-karakter bahasa di seluruh muka Bumi. Dengan demikian setiap dokumen dengan mudah mengikuti standar penulisan yang dibutuhkan, per se, tanpa harus berpusing-pusing mengatur format, setiap kali menulis.

3. LaTeX selalu cepat, karena untuk menulis dalam LaTeX bisa saja menggunakan text standard, maka menggunakan notepad pun bisa dilakukan, yang berarti mengirit ruang dan memori komputer.

4. LaTeX selalu stabil, sejak diperkenalkan, dipergunakan oleh jutaan orang, tidak pernah ada keluhan berarti, bahkan banyak yang membantu mengembangkannya. Stabil berarti LaTeX itu bekerja, dan akan terus bekerja, karena semakin banyak orang yang mempekerjakannya.

5. LaTeX itu luwes, setiap institusi, setiap jurnal punya gayanya sendiri, dan tidak hanya dalam ‘gaya’ yang ada di luarnya, tetapi juga dalam pengembangan engine-nya; tetapi terlepas semua pilihan yang dipergunakan, inti terdalam LaTeX itu selalu tetap sama.

6. Input yang selalu text. Dengan demikian, maka bekerja bisa dilakukan di komputer model apa saja, sistem operasi apa saja, dan untuk keperluan apa saja, jauh dari hanya sekedar pengolah-kata, tetapi bisa dikembangkan untuk basis data, atau keperluan yang memerlukan sumber daya yang besar, tetapi tidak boros.

7. Keluaran bisa berupa apa saja, dari sekedar untuk keperluan pencetakan, seperti pdf, ps, atau sekedar menampilkan seperti html, bahkan terbuka untuk pengembangan yang belum terpikirkan sebelumnya.

8. LaTeX itu gratis.

9. LaTeX itu bisa digunakan di mana saja, tanpa memandang sistem operasi, jenis komputer, atau jenis media.

10. LaTeX itu standar. Banyak penerbitan ilmiah dan Jurnal mempergunakan laTeX sebagai standar penyusunan dokumen.

## Contoh penulisan rumus matematika dengan LaTeX ##

**The Lorenz Equations**

{% raw %}
\begin{aligned}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{aligned}
{% raw %}

$$\begin{aligned}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{aligned}$$

**The Cauchy-Schwarz Inequality**

$$
\left( \sum_{k=1}^n a_k b_k \right)^{\!\!2} \leq
 \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
$$

**A Cross Product Formula**

$$
  \mathbf{V}_1 \times \mathbf{V}_2 =
   \begin{vmatrix}
    \mathbf{i} & \mathbf{j} & \mathbf{k} \\
    \frac{\partial X}{\partial u} & \frac{\partial Y}{\partial u} & 0 \\
    \frac{\partial X}{\partial v} & \frac{\partial Y}{\partial v} & 0 \\
   \end{vmatrix}
$$

**The probability of getting \(k\) heads when flipping \(n\) coins is:**

$$P(E) = {n \choose k} p^k (1-p)^{ n-k} $$

[^1]: [https://id.wikipedia.org/wiki/LaTeX](https://id.wikipedia.org/wiki/LaTeX)