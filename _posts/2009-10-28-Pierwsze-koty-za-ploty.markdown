---
layout: post
title: Pierwsze koty za płoty
---

# {{page.title}}

##Że jakie ToDo?!
Nie stworzyłem listy kontaktów postanowiłem się pobawić i zrobić coś co od dawna zamierzałem.
Napisałem prosty organizer. Projekt dostępny jest na githubie w dwóch wersjach:<br />

*	master - wersja, kórej używam. ma wrzucony authlogic by nikt z zewnątrz nie wszedl. Sama encja użytkownik nie jest do niczego 
wykorzystywana.<br />

*	[as](http://github.com/dogrizz/ToDo/tree/as) - wersja pod nasze zajęcia z wykorzystanym paperclip-em assetPackager-em itp.

[Tutaj](http://gen2.org:3752) dostepna jest wersja as do przeklikania.
##Pierwszy wynik
Pierwszy test YSlow-a przeszedł z oceną 96 minusy za brak kompresji nagłówków i braku czasu ich wygaśnięcia.

##Instalowanie layoutu
Instalacja gema install-theme przeszła bezproblemowo. Schody zaczęły się przy samym instalowaniu tematu.
Po dłuzyszym grzebaniu w końcu zrozumiałem co z czym i jak i powstało sobie polecenie:

	install_theme . ~/Downloads/beta "#page:text" --partial "menu://div[@id='nav']/text()" --partial "sidebar://div[@id='sidebar']"

Kilka dodatkowych przeróbek css i mamy ładną strone.

##PaperClip
Zamiast gravatarów dorzuciłem do projektu PaperClipa. Dlaczego?
Nie miałem gdzie gravatarów użyć...

Postanowiłem dodać do projektów logo. W modelu projektu pojawiła się linijka

	has_attached_file :logo, :styles => { :medium => "300x300>", :thumb => "15x15>" }

Trzeba było dodać do projektu odpowiednie kolumny:
{% highlight ruby %}
class AddLogoColumnsToProject < ActiveRecord::Migration
  def self.up
    add_column :projects, :logo_file_name,    :string
    add_column :projects, :logo_content_type, :string
    add_column :projects, :logo_file_size,    :integer
    add_column :projects, :logo_updated_at,   :datetime
  end

  def self.down
    remove_column :projects, :logo_file_name
    remove_column :projects, :logo_content_type
    remove_column :projects, :logo_file_size
    remove_column :projects, :logo_updated_at
  end
end
{% endhighlight %}

Kilka zmian w widokach:
w new.html.erb
{% highlight html %}
	<%= f.label :icon %>
	<%= f.file_field :logo %>
{% endhighlight %}
W show i index dość podobne 5 linijek

{% highlight html %}
<% unless @project.logo_file_name.blank? %>
    <%= image_tag @project.logo.url %><!-- vel @project.logo.url(:thumb) -->
  <% else %>
		None
  <% end %>
{% endhighlight %}

I śmiga ^^.

##Druga Ocena
Ocena na tym etapie conajmniej mnie zaskoczyla. YSlow ocenił stronę na zaledwie 76 pkt.
Brakuje czasu wygaśnięcia nagłówków, kompresji nagłówków i javascript znalazł się w nagłówkach.

##AssetPackager
Nad samą instalacją rozpisywał się nie będe po prostu zastosowałem się do [tego](http://github.com/sbecker/asset_packager)
Co ważne to znaczna poprawa wyniku: 87 pkt. Pewnie jakby projekt został odpalony w trybie produkcyjnym byłoby więcej.

##Wnioski
Ruby on Rails jest fajne!
Dawno nie miałem tyle fun-u z programowania. Projekt rzecz jasna jest jeszcze niedopracowany. Będę miał zajęcie na długie zimowe wieczory ;)
