---
layout: post
title:  "Mam słabą pamięć i mój Dreamcast też"
date:   2023-06-14
categories: elektronika
---
To miało być łatwe, zresztą jak zwykle... 
Byłem w maju na retro giełdzie. Szukałem padów do Saturna i być może jeszcze pomniejszych pierdół. skończyło się na kupnie kolejnej konsoli...
Wypatrzyłem Dreamcasta w kompletnym zestawie. Stan był niezły i cena też, żona pobłogosławiła, jakieś 3 godziny moralniaka i byłem już szczęśliwym posiadaczem ostatniej konsoli Segi.

![mój Dreamcast](/assets/images/dreamcast/console.jpg)
*mój Dreamcast*

Wróciliśmy do domu na wieczór, dzieci ogarnięte do spania, można podłączyć. Konsola tymczasowo na podłogę, przewód zasilający, przewód A/V i power on.
Ciemno... No ładnie. Nie to wyjście w telewizorze? Nie, to jest to... hmm ale chyba coś widzę na ekranie, szczególnie że sygnał jakiś musi być podawany inaczej TV zgłasza brak sygnału. Ok restart konsoli, faktycznie coś tam majaczy, może przewód A/V jest walnięty? Grzebię przy wyjściu na gorąco, coś tam się pojawia. Wyłączam konsolę, sprawdzam gniazdo i wtyk przewodu. Coś tam niby do poprawienia jest. Poprawiam paluchem bo przecie nie mam izopropanolu pod ręką. Wciskam, odpalam, lepiej!
Jeszcze obraz jest lekko przygaszony jakby luma nie dochodziła `(TODO: ZWERYFIKOWAĆ CZY O LUME CHODZI)`. Wpinam jeszcze ze 2 razy i jest, obraz wyraźny i kolorowy. Zanotować, sprawdzić czy gniazdo A/V ma dobre połączenie z PCB. Pierwsza naprawa Dreamcasta za mną, fuck yeah!

W czasie tej krótkiej serii ponownych włączeń konsoli zauważyłem że Dreamcast za każdym razem prosi o podanie czasu systemowego. W zasadzie każda konsola od czasów 6 generacji (a w przypadku Segi już od czasów Saturna) jest wyposażona w jakąś baterię w celu utrzymania modułu RTC. Konsola swoje lata ma, więc postanowiłem że ktoregoś dnia ją rozłożę i wymienię baterię. Pozostało sprawdzić co to za bateria i jak się do niej dobrać i tu pierwszy zonk. Zamiast standardowych ogniw typu CR2032, inżynierzy umieścili na stałe zalutowany akumulator ML2020. Ze względu na koszt samego akumulatora i fakt że jest w stanie podtrzymać zegar przez ok. 20 dni, a nie jest to konsola którą często będę uruchamiać, zostałem przy pomyśle wlutowania koszyczka na CR2032 tak, aby łatwo można było wymieniać ogniwo w przysżłości.
Szczęśliwie w necie jest mnóstwo poradników jak to zrobić, wraz z zablokowaniem przesyłu prądu który pierwotnie miał ładować akumulator. `(TODO: określić czy podawać link)`

![akumulator ML2020](/assets/images/dreamcast/battery.jpg)
*akumulator ML2020*

Mija kilka dni, przyszedł zamówiony koszyczek na baterię i dioda schottky'ego. Nooo to teraz pójdzie już szybko. Rozkręcamy konsolę, wyjmujemy zasilacz, odpinamy i wykręcamy płytkę od kontrolerów na której umieszczony akumulator i zabieramy się do rozlutowania go. Już nie pamiętam kiedy udało mi się odlutować element z taką łatwością, ale to stary sprzęt, cyna dobrej jakości, łatwo połączyła się z tą moją, znak czasów. Potem dolutowałem koszyczek (to był mały błąd, ale o tym za chwilę) i już miałem połowę roboty za sobą. Pozostało odlutować jedną nożkę rezystora obok koszyczka i pomiędzy nóżkę opornika, a otworem po niej, wlutować diodę Schottky'iego w kierunku zaporowym tak, aby do baterii niedopływał prąd. Zrobione, prościzna, lecimy sprawdzić.

![płytka od kontrolerów z zamontowanym koszykiem wraz z diodą schottky'iego](/assets/images/dreamcast/controller_board.jpg)
*płytka od kontrolerów z zamontowanym koszykiem wraz z diodą schottky'iego*

Z powrotem na dole domu (swoją drogą potrzebuję sobie przygotować stanowisko do sprawdzania konsol na górze), podłączam konsolę, włącza się (to już 50% sukcesu), obraz i prośba o podanie czasu. Pewny siebie od razu podaję aktualną datę i czas, konsola wchodzi do menu głównego, resetuję, obraz i pojawia się prośba o podanie czasu... Niedobrze. Od razu wyłączam sprzęt i odpinam z sieci. W głowie kołuje mi się co mogło pójść nie tak. Jako pierwsze sprawdzam napięcie na baterii. Piękne 3V, to nie to. Wyjąłem baterię, podłączyłem konsolę i sprawdziłem napięcie na koszyczku od baterii. Trochę ponad 3V... to ja już wiem co zrobiłem. Wlutowałem diodę w kierunku przewodzącym, brawo. Dalsza historia jest już prosta. Zrezygnowany porażkami tamtego wieczora (a nie był to jedyny fuckup, ale o tym kiedy indziej), odłożyłem konsolę na kilka dni, poczym wlutowałem już diodę w prawidłowym kierunku. Tym razem konsola już prawidłowo pamiętała czas po wyłączeniu zasilania i nie sprawiała więcej problemów.

Pora na moje refleksje wynikające z powyższego epizodu:
 - Potrzebuje stanowiska do testów urządzeń w mojej pracowni
 - Nie majstrować przy urządzeniach na gorąco. Kiedyś będę płakać z tego powodu.
 - To o czym zawsze zapominam, mianowicie lutować najpierw małe elementy, następnie większe
 - Źle wlutowana dioda wynikała z tego że na zdjęciu w poradniku rezystor przy baterii był pochylony w drugą stronę i bezmyślnie przylutowałem do wolnej nóżki. Błąd nowicjusza który niepowinien mi się już przytrafiać. 

Póki co aktualny stan Dreamcasta mnie zadowala, ale mam już plany co do kolejnych projektów i modyfikacji.

Dzięki, BNB

-------------------