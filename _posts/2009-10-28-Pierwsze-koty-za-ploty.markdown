---
layout: post
title: Pierwsze koty za płoty
---

# {{page.title}}

##Pierwszy wynik
Pierwszy test YSlow-a przeszedł z oceną 96 minusy za brak kompresji nagłówków i braku czasu ich wygaśnięcia.

##Instalowanie layoutu
Instalacja gema install-theme przeszła bezproblemowo. Schody zaczęły się przy samym instalowaniu tematu.
Po dłuzyszym grzebaniu w końcu zrozumiałem co z czym i jak i powstało sobie polecenie:

	install_theme . ~/Downloads/beta "#page:text" --partial "menu://div[@id='nav']/text()" --partial "sidebar://div[@id='sidebar']"

Kilka dodatkowych css przeróbek i mamy ładną strone.

##GitHubbed!
Projekt trafił na github-a. Postepy w rozwoju aplikacji można śledzić <a href="http://github.com/dogrizz/ToDo">tu</a>
