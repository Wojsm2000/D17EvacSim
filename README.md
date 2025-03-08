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
