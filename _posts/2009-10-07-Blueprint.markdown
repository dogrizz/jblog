---
layout: post
title: BluePrint
---

# {{page.title}}

##Co to
<p>
<b>Framework css</b> majacy skrócić czas tworzenia aplikacji.<br />
Zawiera <b>zestaw zdefiniowanych klas css</b>, dzięki którym nasza aplikacja będzie wyglądała tak samo na wszystkich przegladarkach (także resetuje domyślne style przeglądarki!).<br />
Najwazniejsza jego cechą jest <b>siatka</b>, na której tworzymy aplikacje. Siatka ta to domyślnie 24 kolumny na 950px. <br />
By ustawić odpowiednią szerokość używamy klas span-*, które wyznaczają szerokość tego obiektu na stronie.<br/>
</p>
<p>
	Przykladowa strona składająca się z nagłówka, menu, bloku zawartosci i stopki:
	{% highlight html %}
	<div class="container showgrid">
		<div class="span-24 clear" id="naglowek">
			<h1>Div Naglowka</h1>
		</div>
		<div class="span-4" id="navi">
			<b class="prepend-1">Menu</b>
			<ul>
				<li>Pozycja 1</li>
				<li>Pozycja 2</li>
				<li>Pozycja 3</li>
				<li>Pozycja 4</li>
				<li>Pozycja 5</li>
				<li>Pozycja 6</li>
			</ul>
		</div>
		<div class="span-15 last" id="content">
			<p>
				Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
			</p>
		</div>
		<div class="span-5 small prepend-10 clear" id="stopka">
			&copy; Dogrizz
		</div>
	</div>
	{% endhighlight %}
	Co w praktyce wygląda <a href="http://sigma.ug.edu.pl/~dzmitrow/bpexample">tak.</a>
</p>

##Wnioski
<ul>
	<li>Dobra baza do budowania strony.</li>
	<li>JBlogg jest stworzony w oparciu o BluePrint.</li>
	<li>Proste w użyciu.</li>
</ul>

##Linki o które się potknąłem
<ul>
    <li><a href="http://www.blueprintcss.org/">Oficjalna strona</a></li>
    <li><a href="http://groups.google.com/group/blueprintcss/browse_thread/thread/f95b05c988565d69/6819b9983eb0024f">Grupa dyskusyjna zajmujaca sie BluePrint-em</a></li>
    <li><a href="http://rubyonrailswin.wordpress.com/2008/07/02/blueprint-css-template/">HowTo i krotki opis</a></li>
</ul>

##Wyniki walidacji:
<p>
    <a href="http://validator.w3.org/check?uri=referer"><img src="http://www.w3.org/Icons/valid-xhtml10-blue" alt="Valid XHTML 1.0 Strict" height="31" width="88" /></a>
</p>
<p>
    Plik css pozostawiam jak jest nigdy nie wiadomo co sie przyda. Moze mnie natchnie coć, rzuce się z zapałem i przerobie bloga bardziej pod siebie.
</p>
<p>
<a href="http://jigsaw.w3.org/css-validator/check/referer"><img style="border:0;width:88px;height:31px" src="http://jigsaw.w3.org/css-validator/images/vcss-blue" alt="Poprawny CSS!" /></a>
</p>
