# Szablon jekyll-bloga 

Dostosowany do konfiguracji serwera *Sigma* szablon bloga.
Statyczne strony bloga generujemy za pomocą programu *jekyll*.


## Instalacja

Klikamy w ikonkę **fork** i natępnie klonujemy sforkowanego bloga
na swoje konto na serwerze *Sigma*. Klona umieszczamy w katalogu
*public_git*, który musimy wcześniej utworzyć.

Cała procedura może wyglądać tak:

<pre>mkdir -p ~/public_git/
cd ~/public_git/
git clone git@github.com:twój login na <b>githubie</b>⟩/jblog.git sp
</pre>

gdzie nazwa katalogu *sp* to skrót (modulo polskie literki)
od nazwy wykładu „Środowiska programisty”.
Równie dobrze może być ustawiona inna nazwa.


## Jak zacząć?

Wpisy do bloga umieszczamy w katalogu `_posts`.
Nazwy plików z postami tworzymy według schematu:

    rok-miesiąc-dzień-tytuł.markdown

na przykład:

    2009-06-12-jekyll-howto.markdown

Po napisaniu posta generujemy statyczną wersję bloga wykonując z
katalogu z blogiem, czyli z katalogu **~/public_git/sp/** polecenie:

    jekyll ~/public_html/sp

jeśli nie chcemy wpisywac za kazdym razem calego polecenia modyfikujemy
plik deploy.sh i od tej pory wystarczy że będąc w folderze z projektem użyjemy

    ./deploy.sh

Skrypt zrzuci do tła automatyczną aktualizacje. Czyli jeśli jakieś pliki zostaną zmienione bądź dodane zmiany zostaną zastosowane do wersji wyswietlanej.
Po wykonaniu polecenia blog jest dostępny pod URI:

<pre>http://sigma.ug.edu.pl/~⟨twój login na <b>sigmie</b>⟩/sp/
</pre>

## Kończymy instalację

W *jBlogu* jest kilka napisów, które należy wymienić na swoje,
na przykład, w pliku *index.html* znajdziemy:

    title: dzmitrow blog

w plikach *_layouts/default.html* i :*_layouts/index.html*

    <meta name="author" content="Dominik Zmitrowicz" />.
    ...
 
w pliku *atom.xml*:

    <title>dzmitrow blog</title>
    <link href="http://sigma.ug.edu.pl/~dzmitrow/atom.xml" rel="self"/>
    ...

