---
layout: post
title: "Disleksia"
description: Anak disleksia hanya kehilangan huruf, bukan masa depan.
headline: 
category: Education
tags: [education, javascript]
imagefeature: feature/dyslexia.jpg
comments: true
share: true
mathjax: 
---

Apa kesamaan antara Alexander Graham Bell, Albert Einstein, dan Leonardo da Vinci? Selain sama-sama merupakan salah satu figur paling terkenal dalam sejarah dan ilmu pengetahuan, mereka semua juga sama-sama menunjukkan tanda-tanda menderita disleksia[^1].

<figure>
	<a href="https://fivezol.files.wordpress.com/2009/09/people-with-disleksia-problem1.jpg"><img src="https://fivezol.files.wordpress.com/2009/09/people-with-disleksia-problem1.jpg"></a>
</figure>

Banyak orang yang menganggap bahwa disleksia dapat memengaruhi tingkat inteligensi atau kecerdasan penderitanya, tapi anggapan ini tidaklah benar. Anak dengan tingkat kecerdasan baik rendah maupun tinggi, bisa menderita disleksia. Disleksia adalah sebuah gangguan dalam perkembangan baca-tulis yang umumnya terjadi pada anak menginjak usia 7 hingga 8 tahun[^2].



[^1]: [https://www.docdoc.com/id/id/info/condition/disleksia](https://www.docdoc.com/id/id/info/condition/disleksia)
[^2]: [https://id.wikipedia.org/wiki/Disleksia](https://id.wikipedia.org/wiki/Disleksia)




<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>
<script type="text/javascript">

"use strict";

$(function(){

	var getTextNodesIn = function(el) {
	    return $(el).find(":not(iframe,script)").addBack().contents().filter(function() {
	        return this.nodeType == 3;
	    });
	};

	// var textNodes = getTextNodesIn($("p, h1, h2, h3"));
	var textNodes = getTextNodesIn($("*"));



	function isLetter(char) {
		return /^[\d]$/.test(char);
	}


	var wordsInTextNodes = [];
	for (var i = 0; i < textNodes.length; i++) {
		var node = textNodes[i];

		var words = []

		var re = /\w+/g;
		var match;
		while ((match = re.exec(node.nodeValue)) != null) {

			var word = match[0];
			var position = match.index;

			words.push({
				length: word.length,
				position: position
			});
		}

		wordsInTextNodes[i] = words;
	};


	function messUpWords () {

		for (var i = 0; i < textNodes.length; i++) {

			var node = textNodes[i];

			for (var j = 0; j < wordsInTextNodes[i].length; j++) {

				// Only change a tenth of the words each round.
				if (Math.random() > 1/10) {

					continue;
				}

				var wordMeta = wordsInTextNodes[i][j];

				var word = node.nodeValue.slice(wordMeta.position, wordMeta.position + wordMeta.length);
				var before = node.nodeValue.slice(0, wordMeta.position);
				var after  = node.nodeValue.slice(wordMeta.position + wordMeta.length);

				node.nodeValue = before + messUpWord(word) + after;
			};
		};
	}

	function messUpWord (word) {

		if (word.length < 3) {

			return word;
		}

		return word[0] + messUpMessyPart(word.slice(1, -1)) + word[word.length - 1];
	}

	function messUpMessyPart (messyPart) {

		if (messyPart.length < 2) {

			return messyPart;
		}

		var a, b;
		while (!(a < b)) {

			a = getRandomInt(0, messyPart.length - 1);
			b = getRandomInt(0, messyPart.length - 1);
		}

		return messyPart.slice(0, a) + messyPart[b] + messyPart.slice(a+1, b) + messyPart[a] + messyPart.slice(b+1);
	}

	// From https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random
	function getRandomInt(min, max) {
		
		return Math.floor(Math.random() * (max - min + 1) + min);
	}


	setInterval(messUpWords, 50);
});


</script>
