# UKŁAD DYSKRETNY NE555
Układ przedstawia Przerzutnik Ne555 W dyskretnej formie. Projekt jest na zaliczenie z konstrukcji urządzeń elektronicznych
## Wstęp (abstract)
Chip tak uniwersalny, że był używany we wszystkim, od zabawek po statki kosmiczne. Układ, który może działać jako oscylator, wyzwalacz impulsowy, sterownik PWM, syrena/alarm, detektor światła lub ciemności i wiele innych. Jest to najpopularniejszy układ scalony wszech czasów, który istnieje od 1971 roku i obecnie sprzedaje się na ponad 1 miliard rocznie.
## Dlaczego został zbudowany ?
1. Żeby się nauczyć:
Nauka może być dla niektórych przerażająca, ale ten projekt nauczył mnie wiele o komparatorach i obwodach analogowych, a także wielu podstaw zegara 555. Zegar 555 łączy w sobie zarówno układ cyfrowy jak i analogowy i podczas gdy układ cyfrowy przejmuje kontrolę nad nim, analogowy jest nadal ważny.
2. Aby zrozumieć:
Zegar 555 jest bardzo wszechstronnym i użytecznym układem. Dlatego jest on najczęściej produkowanym układem numer 1. Jest on używany bardzo często, więc ważne jest, aby zrozumieć jak to działa. Teraz możesz przeczytać o nim lub nawet zobaczyć symulację, ale nic nie jest tak dobre, jak w rzeczywistości zrobić to samemu.
3. To jest zabawa:
Jeśli lubisz pracować z elektroniką, zwłaszcza z płytkami prototypowymi, to powinien to być zabawny mały projekt. Przełamiesz czarną plastikową barierę, która stoi pomiędzy tobą a twoimi układami scalonymi i zobaczysz układ w całej jego okazałości (prawie, zrobienie własnego tranzystora może być trudne)!

## Założenia (funkcjonalne i konstrukcyjne)


<p align=middle>
    <img src="https://www.circuitstoday.com/wp-content/uploads/2009/09/555-IC-Timer-Block-Diagram.jpg">
</p>


Na pierwszym obrazku widzimy, że są dwa komparatory, jeden na spuście i jeden na sworzniu progowym. Widzimy też, że są one podłączone do dzielnika napięcia. Jedno wejście komparatora Threshold jest na 2/3 Vcc, a jedno wejście komparatora Trigger jest na 1/3 Vcc. Wyjścia komparatorów prowadzą do klapki. Choć na obrazie nie ma tego napisu, to jednak jest to japonka SR. W flip flopie znajduje się stopień wyjściowy, który prowadzi do pina wyjściowego i tranzystora sterującego rozładowaniem, czyli podstawowych części zegara 555.

To jest podstawowa teoria działania:
Gdy napięcie wyzwalania spadnie poniżej 1/3 Vcc (napięcie odniesienia) komparator ustawia klapkę, która ściąga wyjście wysoko i wyłącza rozładowanie. Gdy próg wychyla się powyżej 2/3 Vcc (napięcie referencyjne) komparator resetuje klapkę, która ściąga wyjście nisko i wyłącza wyładowanie. Ta podstawowa operacja pozwala na pracę zegara 555 na różne sposoby w różnych konfiguracjach.


Układ klapki jest dość interesujący. Dużo się dzieje, jeśli chodzi o to, co jest tylko japonką SR z drugim resetem siły. To może być zrobione z 3 tranzystorami, więc wyrzuciłem ten układ i zrobiłem swój własny.

Sterownik wyjściowy jest dość prosty. Składa się z dwóch tranzystorów, z sygnałem do jednego odwróconego tak, że kiedy jeden jest włączony, drugi jest wyłączony. Dzięki temu wyjście może pracować w trybie push-pull. Oznacza to, że wyjście może być źródłem prądu, wyjście jest zwarte do Vcc, kiedy jest wysokie i tonie, wyjście jest zwarte do masy, kiedy jest niskie. 

## Opis części sprzętowej

Cały projekt został wykonany w programie Eagle natomiast po testach, płytka soatała zlecoa firmie JLPcb

### Schemat układu dyskretnego:

<p align=middle>
    <img src="https://github.com/olszes291/NE555/blob/main/sch_discrete.jpg">
</p>

### Płytka układu dyskretnego:

<p align=middle>
    <img src="https://github.com/olszes291/NE555/blob/main/brd_discrete.jpg">
</p>

Pianino wykonałem i zleciłem w takiej samej Formie:
### Schemat pianina:

<p align=middle>
    <img src="https://github.com/olszes291/NE555/blob/main/schPIANO.jpg">
</p>

### Płytka pianina:

<p align=middle>
    <img src="https://github.com/olszes291/NE555/blob/main/brd_PIANO.jpg">
</p>

## Uruchomienie i testy

Jako ukad testowy przygotowaem małe pianino któe współpracuje z układem NE555 i 

## WNIOSKI
