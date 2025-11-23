# Blue-Team---Cloud-Security-Final-Project
Cloud Security
Cloud Security – Final Project (Blue Team)
Opis projektu

Celem projektu było przeprowadzenie dochodzenia bezpieczeństwa w chmurze AWS, w oparciu o udostępnione klucze dostępu. Zadanie odzwierciedla realną pracę Blue Team/SOC Analyst podczas incydentów związanych z ujawnieniem danych uwierzytelniających w środowisku chmurowym.

Projekt obejmował analizę kluczy, identyfikację użytkowników, ocenę możliwych nadużyć oraz uzyskanie dostępu do zasobów S3 w celu wykrycia wycieku danych.

Zakres prac w projekcie
1. Konfiguracja środowiska dochodzeniowego

-Skonfigurowano środowisko AWS CLI przy użyciu dostarczonych kluczy dostępu.

-Przygotowano środowisko analityczne do wykonywania zapytań AWS CLI i enumeracji.

-Przeprowadzono ocenę ryzyka związanego z ujawnieniem kluczy użytych podczas testu.

2. Analiza bezpieczeństwa ujawnionych kluczy dostępu

W projekcie przeanalizowano zagrożenia wynikające z ekspozycji kluczy AWS, w tym:

-Nieautoryzowany dostęp: możliwość przejęcia zasobów przez osoby trzecie.

-Ryzyko finansowe: nieuprawnione generowanie zasobów, co może prowadzić do dużych kosztów.

-Naruszenie bezpieczeństwa danych: dostęp do bucketów S3 z poufnymi plikami.

-Ryzyko prawne: potencjalne naruszenia RODO i innych regulacji.


3. Identyfikacja użytkowników AWS

Za pomocą dostarczonych kluczy przeprowadzono enumerację:

-identyfikację właściciela kluczy (użytkownik Ben),

-wyszukanie pozostałych użytkowników w koncie AWS,

-sprawdzenie ich uprawnień i potencjalnego wpływu na bezpieczeństwo środowiska.

4. Analiza S3 i dostęp do poufnych danych

W ramach dochodzenia wykonano:

-wylistowanie wszystkich bucketów S3 dostępnych z użyciem klucza,

-analizę ich zawartości w poszukiwaniu poufnych plików,

-pobranie wrażliwego dokumentu z zasobnika S3 do dalszej inspekcji,

-potwierdzenie, że dane mogły zostać skompromitowane.

To symuluje realny incydent wycieku danych w środowisku chmurowym.

5. Wnioski i rekomendacje Blue Team

W podsumowaniu opracowano działania naprawcze:

-natychmiastowa rotacja i dezaktywacja ujawnionych kluczy,

-audyt pozostałych użytkowników i ich dostępów,

-wdrożenie monitoringu i alertów wykrywających podejrzane aktywności,

-przegląd polityk IAM oraz ograniczeń dostępu do bucketów S3,

-wdrożenie zasad zarządzania kluczami (KMS, rotacja, polityki minimalnych uprawnień).

Efekt końcowy projektu

Projekt umożliwił praktyczne przećwiczenie Blue Teamowych działań w środowisku chmurowym AWS, obejmujących:

-analizę incydentu związanego z wyciekiem kluczy,

-identyfikację użytkowników i ich uprawnień,

-enumerację zasobów AWS,

-wykrywanie i analizę wrażliwych plików w S3,

-formułowanie rekomendacji dotyczących poprawy bezpieczeństwa,

-zrozumienie ryzyk związanych z błędnym zarządzaniem kluczami dostępu.

Projekt odzwierciedla praktyczne zadania wykonywane w rolach:
