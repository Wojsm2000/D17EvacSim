# Software
## Cromosim
W moim odczuciu najlepszy z trzech bibliotek/programów, które udało mi się uruchomić. Niewątpliwym plusem jest to, że sam twórca pisze na swojej stronie (https://www.cromosim.fr/), że od wersji **2.X** :

Main new features of the Release 2.X of cromosim (mainly concerning microscopic crowd modeling):

* addition of a Destination class allowing to use a more elaborate color code: a door can be represented by a red line, another by a yellow line, etc …

* possibility of having several elements of the Domain class. It is for example possible to define a domain per floor.

* possibility of having several possible destinations for people and chaining them

* **possibility of defining stairs**, thanks to the Destination class

* during the initialization of groups of people, their radius and speed of movement can be defined with probability laws (normal or uniform). They are also assigned an initial destination

Zdaje mi się, że jest to biblioteka dość złożona, chyba najbardziej złożona z trzech które udało mi się uruchomić ale daje największe możliwości. DUŻYM plusem jest to, że kod jest pisany w Pythonie.

## Vadere

Vadere to w zasadzie trochę JDK, trochę taki wyklikiwacz symulacji i chyba jest najprostszym narzędziem ale ma jedną ogromną wadę. Wiesza się niemiłosienie i w losowych momentach. Ma też problemy optymalizacyjne. Nawet przykładowe symulacje dawane przez twórców nie odpalają się w pełni ( małe symulacje działają, duże nie, Vadere się wiesza). Zdaje się, że istnieje możliwość budowy klatek schodowych ale nie mogłem znaleźć przykładu stworzonego przez twórców gdzie schody są używane a jakaś próba ich implementacji wieszała program. 


## JuPedSim

Biblioteka ta w moim odczuciu wygląda trochę jak demo wersja **Cromosim'u**. Podstawowe elementy jak poruszanie się agentów , czy własna budowa pokoi jest zaimplemntowana ale nie udało mi się znaleźć informacji o klatkach schodowych więc pozostaje mi (nam) tylko założyć, że nie ma tam takiej możliwości po prostu. Do tego dość uboga dokumentacja mało co tłumacząca to duży minus w stosunku do Cromosimu.
