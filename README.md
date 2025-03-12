# D17EvacSim
Symulacja tłumu to proces modelowania i analizowania zachowań grup ludzi lub innych jednostek (np. zwierząt, robotów) w różnych sytuacjach, takich jak ewakuacja, przemieszczanie się w zatłoczonych przestrzeniach, uczestnictwo w wydarzeniach masowych czy reakcje na zagrożenia. Celem symulacji jest zrozumienie, przewidywanie i optymalizacja zachowań tłumu w celu poprawy bezpieczeństwa, efektywności przemieszczania się lub planowania przestrzennego.

## Główne cechy symulacji tłumu:

### Modelowanie jednostek:

Każda osoba w tłumie jest reprezentowana jako indywidualna jednostka (agent) z własnymi cechami, takimi jak prędkość, cel, zachowanie i reakcje na otoczenie.

Jednostki mogą być modelowane jako autonomiczne podmioty, które podejmują decyzje na podstawie lokalnych informacji.

### Zachowania zbiorowe:

Symulacje tłumu uwzględniają interakcje między jednostkami, takie jak unikanie kolizji, podążanie za liderem, formowanie się grup czy reakcje na zagrożenia.

Zachowania te mogą być inspirowane naturą, np. modelem boidów (stada ptaków, ławice ryb), gdzie proste zasady prowadzą do złożonych, zsynchronizowanych ruchów.

### Środowisko:

Symulacje uwzględniają przestrzeń, w której porusza się tłum, np. budynki, stadiony, ulice czy tereny otwarte.
Ważnym elementem są przeszkody, wyjścia ewakuacyjne, wąskie gardła czy zmiany w otoczeniu (np. pożar, zawalenie się konstrukcji).

### Scenariusze:

Symulacje mogą obejmować różne scenariusze, takie jak ewakuacja w sytuacjach awaryjnych, przemieszczanie się podczas koncertów, meczów czy festiwali, a także codzienne przepływy ludzi w centrach handlowych lub na dworcach.


## Początki symulacji tłumu
Jednym z przełomowych podejść w tej dziedzinie jest model boidów (ang. boids), zaproponowany przez Craiga W. Reynoldsa w 1987 roku (_Flocks, Herds, and Schools:
A Distributed Behavioral Model_). Model ten symuluje zachowanie poszczególnych jednostek (np. ptaków, ryb), które działają niezależnie, ale ich interakcje prowadzą do złożonych, zsynchronizowanych ruchów grupy.

### Model Boidów
Model boidów opiera się na trzech podstawowych zasadach:

* Unikanie kolizji: Jednostki unikają zderzeń z sąsiadami.

* Dopasowanie prędkości: Jednostki dostosowują swoją prędkość do sąsiadów.

* Centrowanie grupy: Jednostki dążą do zbliżenia się do centrum grupy.

Te proste zasady, zastosowane do każdej jednostki, prowadzą do realistycznego zachowania grupy, takiego jak formowanie się stada, unikanie przeszkód czy synchronizacja ruchu.

Zastosowanie w symulacjach ewakuacji
Model boidów może być adaptowany do symulacji ewakuacji budynków, gdzie ludzie są traktowani jako jednostki dążące do wyjścia, unikające kolizji i dostosowujące swoje ruchy do innych. Kluczowe zalety tego podejścia to:

* Realizm: Zachowanie jednostek jest oparte na prostych zasadach, ale prowadzi do złożonych, naturalnych ruchów.

* Skalowalność: Model może być stosowany zarówno dla małych, jak i dużych grup.

* Elastyczność: Możliwość dodania dodatkowych zasad, takich jak reakcja na zagrożenia czy wpływ architektury budynku.

## Analiza wczesnych modeli

W 2004 roku pracownicy Uniwersytetu z Daleware będący członkami Centrum Badania Katastrof opublikowali analizę porównującą wybrane modele symulacji ewakuacji budynków (_A Critical Review of Emergency Evacuation Simulation Models_, Gabriel Santos, Benigno E. Aguirre). Badacze zauważyli również, że podejście do człowieka jako elementu ewakuacji zmieniało się na przestrzeni lat.

Klasyczne badania nad paniką pokazły ewolucję rozumienia tego zjawiska. Wczesne teorie zakładały, że ludzie w sytuacjach kryzysowych tracą człowieczeństwo, ulegając strachowi i zachowując się jak zwierzęta. Późniejsze podejście, zaproponowane przez E. L. Quarantelliego (1957), postrzegało panikę jako aspołeczne zachowanie zbiorowe, w którym ludzie skupiają się wyłącznie na własnych potrzebach, ignorując innych. W latach 80. i 90. XX wieku prace Norrisa Johnsona i innych badaczy (Keating, 1982) obaliły te teorie, pokazując, że ludzie w sytuacjach zagrożenia nie tracą zdolności do racjonalnego działania, nie porzucają więzi społecznych i często ryzykują własne życie, aby pomóc innym (por. Helbing, Farkas i Vicsek, 2000; Chertkoff i Kushigian, 1999).

Założenie, że ludzie działają racjonalnie i normatywnie, ma istotne implikacje dla modelowania ewakuacji. Ruch ewakuacyjny nie jest jednokierunkowy, jak w przypadku stada lecz wielokierunkowy. Obejmuje to osoby wracające na miejsce ewakuacji, aby pomóc innym, ratować przyjaciół lub zabrać ważne przedmioty (Johnson, 1987; Johnson i in., 1994).

### Porównanie modeli
#### 1. Modele oparte na przepływie (Flow-Based Models)
* Przykład: EVACNET4

* Charakterystyka:
Modeluje ewakuację jako ciągły przepływ osób przez sieć węzłów (np. pokoje, korytarze, schody) i łuków (przejścia między węzłami).

Skupia się na fizycznych ograniczeniach, takich jak pojemność węzłów, czas przejścia przez łuki i przepustowość.

* Mocne strony:

Skutecznie oblicza optymalny czas ewakuacji przy uwzględnieniu fizycznych ograniczeń budynku.

Umożliwia analizę zagęszczenia i przepustowości w różnych częściach budynku.

* Słabe strony:

Brak uwzględnienia interakcji społecznych lub procesów grupowych.

Zakłada jednorodność agentów (osób ewakuujących się), co nie odzwierciedla różnic w zachowaniach indywidualnych.

Nie uwzględnia czynników psychospołecznych, takich jak panika czy współpraca.

#### 2. Modele oparte na automacie komórkowym (Cellular Automata)
* Przykład: EGRESS

* Charakterystyka:

Przestrzeń jest podzielona na dyskretne komórki, a ewakuacja jest symulowana jako ruch osób między komórkami.

Ruch osób jest określany przez rzut ważoną kostką, co odzwierciedla zmienność w zachowaniu.

* Mocne strony:

Umożliwia symulację ruchu osób w bardzo szczegółowy sposób, uwzględniając zagęszczenie i przepływ.

Może symulować wpływ substancji toksycznych lub dymu na ewakuację.

* Słabe strony:

Skupia się na indywidualnym ruchu, a nie na procesach społecznych.

Brakuje mechanizmów do symulacji interakcji między osobami ewakuującymi się.

Nie uwzględnia norm kulturowych dotyczących przestrzeni osobistej, które mogą się zmieniać w sytuacjach kryzysowych.

#### 3. Modele oparte na agentach (Agent-Based Models)
* Przykład: SIMULEX, EXIT89

* Charakterystyka:

Każdy agent (osoba) ma przypisane indywidualne atrybuty, takie jak prędkość chodzenia, wiek, płeć, które wpływają na jego zachowanie.

Umożliwia symulację indywidualnych decyzji i zachowań podczas ewakuacji.

* Mocne strony:

Uwzględnia różnice w zachowaniu osób, takie jak różnice w prędkości chodzenia czy reakcji na zagrożenie.

Pozwala na symulację bardziej realistycznych scenariuszy ewakuacji.

* Słabe strony:

Brakuje mechanizmów do symulacji interakcji społecznych na poziomie grupowym.

Nie uwzględnia procesów decyzyjnych grupowych, takich jak tworzenie norm emergentnych czy konflikty między grupami.

Skupia się na indywidualnych zachowaniach, co może prowadzić do pominięcia ważnych aspektów ewakuacji grupowej.

#### 4. Modele uwzględniające czynniki socjologiczne
* Przykład: EXODUS, FIRESCAP, Multi-Agent Simulation for Crisis Management (MASCM)

* Charakterystyka:

Wprowadzają bardziej zaawansowane mechanizmy symulacji zachowań społecznych, takie jak konflikty, współpraca, poszukiwanie informacji czy wpływ liderów.

Uwzględniają procesy decyzyjne oparte na normach społecznych i interakcjach między osobami.

* Mocne strony:

EXODUS: Zawiera wiele atrybutów społeczno-psychologicznych, takich jak wiek, płeć, prędkość biegu, a także możliwość wykonywania zadań przed ewakuacją (np. szukanie dziecka).

FIRESCAP: Symuluje procesy decyzyjne oparte na normach społecznych i roli liderów w sytuacjach kryzysowych.

MASCM: Uwzględnia rolę liderów i ich wpływ na zmianę trasy ewakuacji w zależności od sytuacji.

* Słabe strony:

EXODUS: Brakuje mechanizmów do symulacji złożonych interakcji społecznych na poziomie mikro, takich jak tworzenie norm emergentnych.

FIRESCAP: Nie uwzględnia wpływu toksyczności na wybór trasy ewakuacji.

MASCM: Brakuje mechanizmów do symulacji procesów wyboru liderów w sytuacjach, gdy nie ma oficjalnych liderów.

#### 5. Modele oparte na aktywności (Activity-Based Models)
* Przykład: EXODUS (częściowo)

* Charakterystyka:

Uwzględniają, że osoby ewakuujące się mogą wykonywać różne zadania przed ewakuacją, np. szukanie przedmiotów, pomoc innym.

* Mocne strony:

Bardziej realistycznie odzwierciedlają zachowania osób w sytuacjach kryzysowych.

Umożliwiają symulację zadań, które mogą opóźnić ewakuację.

* Słabe strony:

Brakuje mechanizmów do symulacji złożonych interakcji społecznych, takich jak tworzenie norm emergentnych czy konflikty między grupami.


## Różne metody zbierania danych  
Badanie z 2022 roku autorstwa Liu C., Liu Z. i Chai Y. (_Review of Virtual Simulation of Crowd Motion for Urban Emergency Management_) również podejmowało tematykę porównań już co prawda bardziej nowoczesnych modeli lecz co ciekawsze sposoby zberania danych do symulacji zachowań tłumów w sytuacjach zagrożenia. Badacze wyszczególnili trzy główne metody.

### 1. **Monitorowanie wideo**  
- **Zalety**:  
  - Automatyczne zbieranie danych, długi czas rejestracji.  
  - Integracja z urządzeniami IoT.  
- **Wady**:  
  - Niska jakość danych, brak możliwości prognozowania.  
- **Przykład**: Algorytm Zhao et al. (2018) z klasteryzacją hierarchiczną.  

### 2. **Ćwiczenia ewakuacyjne**  
- **Zalety**:  
  - Realizm scenariuszy, zbieranie danych czasowo-przestrzennych.  
- **Wady**:  
  - Wysokie koszty, trudności w śledzeniu uczestników.  
- **Przykład**: Eksperyment Haghani i Sarvi (2019).  

### 3. **Filmowanie dronami (UAV)**  
- **Zalety**:  
  - Niski koszt, wysokiej jakości dane, elastyczność w dużych przestrzeniach.  
- **Wady**:  
  - Ograniczony czas lotu, niedojrzałość technologii.  

#### Porównanie metod:  
| Metoda           | Koszt    | Jakość danych | Skala scenariusza |  
|------------------|----------|---------------|-------------------|  
| Monitorowanie    | Średni   | Niska         | Mała              |  
| Ćwiczenia        | Wysoki   | Wysoka        | Mała              |  
| Drony            | Niski    | Wysoka        | Duża              |  


## Podsumowanie dostępnej literatury z 2020 r.
Artykuł autorstwa S. Yang et al z 2020 roku "A review on crowd simulation and modeling" podsumowuje dostępne ówcześnie podejścia do modelowania i symulacji tłumów zarówno w kontekście zastosowania wizualnych efektów w multimediach, jak i urbanistyki oraz ewakuacji w sytuacjach awaryjnych.

### 1. Główne kategorie modeli symulacji tłumów
a) Modele mikroskopowe:

* oparte na regułach (Rule-based)
      
* oparte na sile (Force-based)
      
* oparte na prędkości (Velocity-based)
      
* agentowe (Agent-based)
      
* oparte na widzeniu (Vision-based)
      
b) Modele makroskopowe

* Modele continuum (Continuum models)
  
* Dynamika zbiorcza (Aggregate dynamics)
  
* oparte na polu potencjału (Potential field-based)

c) Modele mezoskopowe

* Dynamiczne zachowania grupowe (Dynamic group behavior)
  
* Interaktywne formowanie grup (Interactive group formation)
  
* Tłumy społeczno-psychologiczne (Social Psychological crowds)

### Modele mikroskopowe (zwane też bottom-up) 
Skupiają się na zachowaniach i cechach poszczególnych poszczególnych osób. W tym podejściu ludzie traktowani są jako dyskretne obiekty, na których zachowanie wpływają ich otoczenie i sąsiedzi. Autorzy dużo uwagi poświecają kwestii unikania kolizji między obiektami.

Do najważniejszych modeli w tej kategorii należą:
* Social Force Model (SFM) Helbinga et al. z 2000 r. opisujący mechanizmy i dynamikę spanikowanego tłumu, próbującego się ewakuować. To pierwszy model, w którym fizyczne kryteria wykorzystane zostały do opisu mikroskopowego zbiorowiska ludzi. Na zachowanie poszczególnych osób w modelu wpływają zarówno czynniki społeczno-psychologiczne i fizyczne.  
* High-density autonomous crowds (HiDAC) model Pelechano et al. z 2007 r. (model agentowy)  
* Wagoum et al. proposed an efficient crowd simulation for evacuation assistant integrated with cellular automata 


###  Modele makroskopowe
* tłumy są traktowane jako jednolity, ciągły byt, a ich ruch jest determinowany przez pola potencjału (potential fields) lub dynamikę płynów. Planowanie ścieżek tłumu oraz unikanie kolizji są zarządzane przez globalny solver. Modele te nie skupiają się na szczegółowych interakcjach, przez co każdy wirtualny agent nie uwzględnia interakcji na poziomie indywidualnym między sobą a środowiskiem.  
* wykorzystywane głównie do efektów wizualnych dużych zbiorowisk ludzkich

### Modele mezoskopowe (symulacje grupowe) 
* Simulation of small social group behaviors in emergency evacuation R. Xie et al. 2016 - model dynamic group behavior  
* Social Psychological crowds nawiązują do teorii cech charakteru i zaraźliwości społecznej emocji
* Wykorzystywane są różne modele cech osobowości i emocji, takie jak OCEAN, PEN, OCC (Ortony, Clore, Collins), PAD (Pleasure Arousal Dominance)
* Model ESCAPES zawiera cztery kluczowe cechy (typ agenta, emocje, informacje, interakcje) w celu symulacji zjawisk psychologicznych w sytuacjach ewakuacji.
(e.g. People forget theirentrance, First-time visitors, Heightened emotions, Herding behavior, Pre-evacuation delay, Families gather before exiting, Authorities calm people)
* M. Xu et al. Crowd behavior simulation with emotional contagion in unexpected multihazard situations(2019)
* Y. Mao et al. Emotion-based diversity crowd behavior simulation in public emergency (2018)
* Y. Mao et al. Personality trait and group emotion contagion based crowd simulation for emergency evacuation (2018) 
* G. Zhang, D. Lu, H. Liu, Strategies to utilize the positive emotional contagion optimally in crowd evacuation (2018)

### Ewaluacja modeli
* W celu ewaluacji i porówniania różnych modeli konieczne jest ujednolicenie kryteriów, co może być problematyczne dla różnych rodzajów modeli.
* Autorzy review proponują ocenę umiejętności danego modeli symulowania dynamiki zachowań grupowych (zjawisk emergentnych), jak i realistycznych zachowań w skali mikro

### Podsumowanie - autorzy zalecają:
* gromadzenie większej ilości rzeczywistych danych
* zastosowanie metod uczenia maszynowego z nadzorem i bez w celu modelowania odpowiednich zachowań
* integrację wiedzy z zakresu psychologii społecznej w celu stworzenia bardziej ogólnych i realistycznych modeli m.in ewakuacji w sytuacjach awaryjnych
* branie pod uwagę złożoności obliczeniowej modeli
* stwierdzają również, że wykorzystanie głębokiego uczenia i obliczania równoległego jest wykonalne.


## Artykuł "Agent-Based Modelling and Simulation for evacuation of people from a building in case of fire" Selain Kasereka et al. z 2018 r.

### Opis modelu

Autorzy badania stworzyli model oparty na inteligentnych agentach w celu symulacji ewakuacji supermarketu w razie wystąpienia pożaru.

Wyszczególnili cztery rodzaje agentów:
* osoby ewakuujące sie (evacuees)
* ogień
* dym
* alarm przeciwpożarowy

Każdy z rodzajów agentów miał przyporządkowane możliwe stany, percepcje (na co zwraca uwagę w otoczeniu), działanie (pojedyncze) i zachowanie warunkowe ("kiedy coś się dzieje, powinien zrobić to").

Wyszczególnione zostały założenia początkowe, dotyczące poszczególnych agentów. Jako model nawigacji użyto algorytmu najkrótszej drogi (Dijkstra).

Do stworzenia modelu wykorzystali platformę GAMA i język  zorientowany agentowo programowownia GAML (GAma Modeling Language).

### Symulacja - parametry

Określone zostały cztery parametry służące do oceny kazdego scenariusza ewakuacji:
* Liczba osób, która bezpiecznie opuściła budynek
* Liczba ofiar
* Średnia energia osób, które opuściły budynek
* Średni czas potrzebny na ewakuację

Przeprowadzono symulacje z różnymi parametrami dotyczącymi rozprzestrzeniania się ognia i dymu, prędkości ludzi, liczby wyjść ewakuacyjnych i innych. Dla każdego zestawu parametrów przeprowadzono po 100 symulacji, a wyniki uśredniono.

### Symulacja - wyniki i podsumowanie

Zmiana parametrów miały znaczący wpływ na uzyskane wyniki. Największy wpływ na liczbę ofiar miała prędkość i zasięg ognia i dymu oraz liczba wyjść ewakuacyjnych.

Wedługg autorów badania ich model jest na tyle ogólny, że może być stosowany również do symulacji ewakuacji innych bydunków użyteczności publicznej. Zwracają jednak uwagę na ograniczenia ich modelu - nie wzięto pod uwagę cech psychofizycznych pojedynczych osób ani złożonych interakcji społecznych podczas ewakuacji.

## Badanie przeglądające wspólczesną literaturę

Praca Gayani P.D.P. Senanayake, Minh Kieu, Yang Zou, Kim Dirks (_Agent-based simulation for pedestrian evacuation: A systematic literature review_, 2024) przeprowadza systematyczny przegląd literatury dotyczącej modelowania ewakuacji pieszych z wykorzystaniem modeli opartych na agentach (ABM – Agent-Based Models). Autorzy analizują 134 badania z lat 2013–2023, aby ocenić obecny stan wiedzy, metodologie, praktyki walidacyjne oraz wyzwania związane z symulacjami ewakuacji. 

### Główne postępy w symulacji ewakuacji

* Integracja czynników behawioralnych: W ostatnich latach nastąpił znaczący postęp w modelowaniu zachowań pieszych podczas ewakuacji. Modele ABM coraz częściej uwzględniają czynniki psychologiczne, socjologiczne, demograficzne i środowiskowe, co pozwala na bardziej realistyczne symulacje.

* Zastosowanie zaawansowanych technik obliczeniowych: Wykorzystanie technik uczenia maszynowego (ML), takich jak uczenie ze wzmocnieniem (RL) czy sieci neuronowe (NN), pozwala na lepsze modelowanie adaptacyjnych zachowań agentów. Techniki te umożliwiają agentom uczenie się na podstawie doświadczeń i dostosowywanie się do dynamicznych warunków ewakuacji.

* Hybrydowe podejścia do modelowania: Coraz częściej stosowane są hybrydowe modele, które łączą ABM z innymi technikami, takimi jak automaty komórkowe (CA) czy modele sił społecznych (Social Force Models), co zwiększa realizm symulacji.

### Wnioski badaczy 

Mimo postępujących ulepszeń modeli autorzy pracy zwracają uwagę na małą elastyczość i brak empirycznego uzasadnienia modeli. Stosowane architektury i modele choć różnią się od siebie, często opierają się na uproszczonych regułach. Badacze widzą również problem w ogrniczeniu wydajności obliczeniowej oraz brak danych walidujących. Techniki walidacji opierały się głównie na ograniczonych eksperymentach w świecie rzeczywistym i osądzie ekspertów. Autorzy postulują również interdyscyplinarne podejście do tego rodzaju badań. Współpraca między naukowcami zajmującymi się modelowaniem, psychologią, naukami społecznymi i informatyką jest według nich kluczowa dla rozwoju bardziej realistycznych i użytecznych modeli ewakuacji. W przyszłości według autorów należy dążyć do standaryzacji metod walidacyjnych oraz udostępniania modeli i danych, aby umożliwić ich reprodukcję i porównanie.








