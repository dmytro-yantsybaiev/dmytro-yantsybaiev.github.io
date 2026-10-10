---
title: Polityka prywatności
lang: pl
permalink: /diff-for-gitlab/pl/privacy/
---

*English version: [Privacy Policy](../../privacy/)*

# Diff for GitLab — Polityka prywatności

**Data wejścia w życie:** 10 października 2026 r.

Niniejsza polityka wyjaśnia, co aplikacja na iOS **Diff for GitLab™** („Aplikacja”) robi z Twoimi danymi. Jest to niezależna aplikacja, niepowiązana z GitLab Inc. ani przez nią niepopierana, niesponsorowana i niezatwierdzona. GITLAB jest znakiem towarowym GitLab Inc. w Stanach Zjednoczonych oraz innych krajach i regionach. Aplikację tworzy i udostępnia Dmytro Yantsybaiev, twórca oprogramowania prowadzący działalność w Krakowie („ja”), który jest administratorem danych w zakresie przetwarzania wymienionego w tabeli poniżej. Dane kontaktowe znajdują się w sekcji 12.

## Podsumowanie

- Twój token GitLab jest przechowywany wyłącznie w pęku kluczy (Keychain) Twojego urządzenia i wysyłany wyłącznie do serwera GitLab, na którym się logujesz. Nigdy do mnie nie trafia.
- Twój kod, merge requesty, pipeline’y i inne treści z GitLab są przesyłane wyłącznie między Twoim urządzeniem a Twoim serwerem GitLab. Nie mam do nich dostępu.
- Zakupy obsługuje Apple. Nigdy nie widzę Twoich danych płatniczych.
- Aplikacja niczego mi nie wysyła. Łączy się wyłącznie z Twoim serwerem GitLab i z Apple. Strony z dokumentami prawnymi otwierane z Aplikacji, takie jak ta, wczytują się z GitHub Pages (sekcja 10).
- Brak reklam, brak śledzenia w innych aplikacjach i witrynach, brak sprzedaży lub udostępniania danych brokerom danych.

Dane z sekcji 1 są przetwarzane przez Aplikację na Twoim urządzeniu i pozostają pod Twoją kontrolą; nigdy ich nie otrzymuję. Pisanie do mnie jest dobrowolne. Do korzystania z Aplikacji potrzebny jest token GitLab, ale nigdy do mnie nie trafia. Nie podejmuję wobec Ciebie zautomatyzowanych decyzji i nie stosuję profilowania.

| Przetwarzanie | Podstawa prawna | Odbiorcy | Okres przechowywania |
|---|---|---|---|
| Sprawdzanie Twojej subskrypcji (sekcja 4) | Wykonanie umowy, art. 6 ust. 1 lit. b rozporządzenia (UE) 2016/679 („RODO”) | Apple (odrębny administrator) | Dopóki Aplikacja jest zainstalowana |
| Wiadomości e-mail, które do mnie wysyłasz (sekcja 6) | Prawnie uzasadniony interes polegający na udzieleniu Ci odpowiedzi, art. 6 ust. 1 lit. f RODO; wykonanie umowy, art. 6 ust. 1 lit. b RODO, gdy wiadomość dotyczy Twojej subskrypcji | Google (Gmail) | 24 miesiące od ostatniej wiadomości |
| Wszystko, co znajduje się na Twoim urządzeniu (sekcja 1) | Wykonanie umowy, art. 6 ust. 1 lit. b RODO, w celu dostarczenia Aplikacji, z której korzystasz; w przypadku imion, nazwisk i awatarów innych osób prawnie uzasadniony interes, art. 6 ust. 1 lit. f RODO | Wyłącznie Twój serwer GitLab (sekcja 2); nigdy ja | Token, konta, pamięć podręczna i ostatnie elementy: do wylogowania (nieużywane wpisy pamięci podręcznej po 30 dniach). Pozostałe ustawienia: przypisane do konta – do wylogowania z niego, reszta – do usunięcia Aplikacji |
| Raporty o awariach i statystyki użycia od Apple (sekcja 5) | Prawnie uzasadniony interes polegający na usuwaniu błędów, art. 6 ust. 1 lit. f RODO | Ja, za pośrednictwem Apple | Pobrane przeze mnie kopie: do usunięcia błędu; oryginały Apple przechowuje według własnych zasad |

## 1. Dane przechowywane na Twoim urządzeniu

Wszystkie poniższe dane pozostają na Twoim urządzeniu, chyba że dalsza sekcja stanowi inaczej.

| Dane | Gdzie | Szczegóły |
|---|---|---|
| Token dostępu GitLab (osobisty token dostępu lub tokeny OAuth) | Pęk kluczy iOS (Keychain) | Przechowywany z klasą ochrony „dostępny po odblokowaniu, tylko na tym urządzeniu”. Nie jest synchronizowany z Pękiem kluczy iCloud ani przywracany na innym urządzeniu z kopii zapasowej. Usuwany po wylogowaniu. |
| Lista kont | Ustawienia Aplikacji | Dla każdego konta: nazwa użytkownika, adres serwera GitLab, metoda logowania oraz, w przypadku OAuth, identyfikator aplikacji. Potrzebne do wyświetlania Twoich kont i przełączania się między nimi. |
| Pamięć podręczna odpowiedzi GitLab do pracy offline | Folder pamięci podręcznej Aplikacji | Odpowiedzi z Twojego serwera GitLab (na przykład listy merge requestów i zmiany w kodzie), dzięki którym ekrany otwierają się od razu i działają offline. Chronione do pierwszego odblokowania urządzenia po ponownym uruchomieniu, ograniczone do 200 MB; wpisy nieużywane przez 30 dni są usuwane, a iOS może wyczyścić folder przy braku miejsca. Czyszczone po wylogowaniu z konta. |
| Ostatnie wyszukiwania i ostatnio przeglądane projekty | Ustawienia Aplikacji | Przechowywane osobno dla każdego konta i czyszczone po wylogowaniu z tego konta. |
| Ustawienia | Ustawienia Aplikacji | Rozmiar tekstu kodu, ustawienie znaczników czasu w logach zadań, ostatnio wpisany adres samodzielnie hostowanego serwera, stan sekcji ekranu głównego, informacja, które wskazówki zostały już wyświetlone, oraz, w przypadku konta na starszym serwerze GitLab, wersja tego serwera, aby Aplikacja mogła wyświetlić uproszczony ekran główny. Elementy przypisane do konta są czyszczone po wylogowaniu z tego konta. |

Usunięcie Aplikacji usuwa pamięć podręczną i ustawienia. iOS nie gwarantuje, że elementy pęku kluczy zostaną usunięte razem z aplikacją, dlatego najpierw się wyloguj, co usuwa token, albo unieważnij token w GitLab.

## 2. Dane wysyłane do Twojego serwera GitLab

Aplikacja jest klientem GitLab. Każde jej żądanie trafia do serwera GitLab, na którym się logujesz, wyłącznie przez HTTPS, wraz z Twoim tokenem, aby GitLab mógł działać w Twoim imieniu. Obejmuje to odczytywanie merge requestów, zmian w kodzie, pipeline’ów, logów zadań, projektów i plików oraz działania wykonywane przez dotknięcie elementu sterującego, na przykład zatwierdzanie merge requestu lub cofanie zatwierdzenia, scalanie lub rebase, komentowanie lub rozwiązywanie wątku, ponawianie, anulowanie lub uruchamianie pipeline’u albo zadania oraz oznaczanie projektu gwiazdką.

- Awatary osób są wczytywane wyłącznie z Twojego serwera GitLab, nigdy z Gravatara ani innej zewnętrznej usługi z obrazami. Awatary projektów nie są wczytywane.
- Gdy wpisujesz adres samodzielnie hostowanego serwera, Aplikacja wysyła żądania bez danych uwierzytelniających do `/api/v4/user` pod tym adresem oraz, w razie potrzeby, pod adresem głównym tego samego hosta, aby przed poproszeniem o token potwierdzić, że jest to serwer GitLab.
- Aplikacja odrzuca pliki cookie od Twojego serwera GitLab. Odpowiedzi sieciowe są przechowywane wyłącznie w pamięci operacyjnej, nigdy nie są zapisywane na dysku i są usuwane po wylogowaniu lub zamknięciu Aplikacji. Jedyną kopią przechowywaną na urządzeniu jest własna pamięć podręczna Aplikacji (sekcja 1).
- Po otwarciu wyszukiwania Aplikacja pyta iOS, czy schowek zawiera link, bez odczytywania jego treści, aby móc wyświetlić przycisk Wklej. Treść schowka jest odczytywana dopiero po dotknięciu przycisku Wklej i nie jest przechowywana.

To, co Twój serwer GitLab robi z tymi żądaniami, określa polityka prywatności GitLab Inc. (w przypadku gitlab.com) albo organizacja prowadząca Twoją samodzielnie hostowaną instancję; są one odrębnymi administratorami tych danych. Nie mam do nich dostępu.

## 3. Logowanie przez OAuth

Jeśli wybierzesz „Sign in with GitLab”, Aplikacja otworzy GitLab w systemowym oknie logowania iOS. Logujesz się na stronach GitLab; Aplikacja nigdy nie widzi Twojego hasła do GitLab. Przy pierwszym logowaniu na danym serwerze i przy ponownej autoryzacji konta okno to współdzieli pliki cookie z Safari, więc GitLab może utrzymać Twoją sesję w swoim serwisie w Safari; wylogowanie z Aplikacji nie wylogowuje Cię tam. Gdy dodajesz kolejne konto na tym samym serwerze, okno nie współdzieli plików cookie, dzięki czemu możesz zalogować się jako inna osoba. Aplikacja prosi o zakres `api` w GitLab, a tokeny są wymieniane bezpośrednio między Twoim urządzeniem a Twoim serwerem GitLab z użyciem PKCE. Żaden mój serwer nie uczestniczy w tym procesie.

W przypadku gitlab.com aplikacja OAuth, z której korzysta Aplikacja, jest zarejestrowana na moim koncie GitLab; ta rejestracja nie daje mi dostępu do Twojego konta ani tokenów. W przypadku serwerów hostowanych samodzielnie aplikację rejestruje administrator Twojej instancji. W każdej chwili możesz cofnąć Aplikacji dostęp na stronach ustawień GitLab „Applications” lub „Access Tokens”.

## 4. Zakupy

Subskrypcje są sprzedawane przez system zakupów w aplikacji Apple. Apple jest odrębnym administratorem w zakresie zakupu i Twojego Konta Apple: przetwarza płatność i przechowuje Twoje dane płatnicze, imię i nazwisko oraz dane konta. Od Apple Aplikacja otrzymuje wyłącznie podpisane informacje o transakcji: produkt, jego status, daty odnowienia lub wygaśnięcia oraz identyfikatory transakcji Apple, które nie pozwalają mi Cię zidentyfikować. Do samego zakupu ma zastosowanie polityka prywatności Apple. Aplikacja wykorzystuje te informacje wyłącznie na Twoim urządzeniu, aby odblokować swoje funkcje; nie są one do mnie wysyłane. Apple przekazuje mi raporty sprzedaży i subskrypcji, które nie pozwalają Cię zidentyfikować.

## 5. Bez śledzenia i bez reklam

Aplikacja nie śledzi Cię w aplikacjach i witrynach innych firm, nie wyświetla reklam i nie sprzedaje ani nie udostępnia Twoich danych brokerom danych. Dlatego nie prosi o zgodę w ramach przejrzystości śledzenia przez aplikacje (App Tracking Transparency), a jej manifest prywatności nie deklaruje śledzenia ani zbierania danych.

Etykieta prywatności Aplikacji w App Store to **Dane nie są zbierane** (Data Not Collected).

Jeśli w ustawieniach prywatności urządzenia włączono *Udostępniaj deweloperom* (Share With App Developers), Apple może przekazywać mi raporty o awariach i zbiorcze statystyki użycia Aplikacji. Jest to funkcja Apple, sterowana w ustawieniach iOS, a nie przez Aplikację. Apple nie przekazuje mi wraz z nimi Twojej tożsamości. Wykorzystuję je do usuwania błędów na podstawie mojego prawnie uzasadnionego interesu (art. 6 ust. 1 lit. f RODO), a pobrane przeze mnie kopie przechowuję do usunięcia błędu; oryginały Apple przechowuje według własnych zasad. W każdej chwili możesz to zatrzymać, wyłączając *Udostępniaj deweloperom*.

## 6. Wiadomości e-mail, które do mnie wysyłasz

Jeśli napiszesz do mnie, przechowuję Twój adres i wiadomość, aby Ci odpowiedzieć i zachować zapis korespondencji. Poczta jest obsługiwana przez Google (Gmail), który działa jako odrębny administrator na podstawie Polityki prywatności Google, i może być przetwarzana w Stanach Zjednoczonych przez Google LLC, certyfikowaną w ramach Ram ochrony danych UE–USA (EU–U.S. Data Privacy Framework) i ich rozszerzenia dla Zjednoczonego Królestwa. Wątki korespondencji usuwam 24 miesiące po ostatniej wiadomości, a dłużej tylko wtedy, gdy są mi potrzebne do ustalenia, dochodzenia lub obrony roszczeń, i tylko do czasu ich rozstrzygnięcia. Są to jedyne dane, które mogłyby pozwolić mi Cię zidentyfikować.

## 7. Bezpieczeństwo

- Akceptowane są wyłącznie adresy serwerów HTTPS. Certyfikaty weryfikuje iOS; serwer hostowany samodzielnie z prywatnym urzędem certyfikacji wymaga zainstalowania na urządzeniu profilu konfiguracyjnego.
- Tokeny są chronione przez pęk kluczy iOS i można je odczytać tylko wtedy, gdy urządzenie jest odblokowane.
- Dane GitLab w pamięci podręcznej są chronione przez szyfrowanie plików iOS do pierwszego odblokowania urządzenia po ponownym uruchomieniu.

Żadna metoda przechowywania ani przesyłania danych nie jest w pełni bezpieczna. Jeśli uważasz, że Twój token mógł zostać ujawniony, unieważnij go w GitLab.

## 8. Dzieci

Aplikacja jest narzędziem dla programistów posiadających konto GitLab i nie jest skierowana do dzieci.

## 9. Twoje prawa

Na podstawie RODO i podobnych przepisów możesz mieć prawo dostępu do danych osobowych, ich sprostowania lub usunięcia, ograniczenia przetwarzania, wniesienia sprzeciwu, przenoszenia danych oraz wniesienia skargi do organu nadzorczego.

Jedyne dane osobowe, które posiadam i które mogłyby Cię zidentyfikować, to wiadomości e-mail, które do mnie wysyłasz (sekcja 6). Aby skorzystać z któregokolwiek z tych praw w odniesieniu do nich, napisz do mnie. Dane, które pozostają na Twoim urządzeniu, nigdy do mnie nie trafiają: kontrolujesz je, wylogowując się lub usuwając Aplikację.

**Prawo do wniesienia sprzeciwu.** Jeśli opieram się na prawnie uzasadnionym interesie (odpowiedź na Twoją wiadomość lub raporty o awariach), możesz w każdej chwili wnieść sprzeciw, pisząc do mnie, a ja zaprzestanę przetwarzania, chyba że wykażę istnienie ważnych prawnie uzasadnionych podstaw, które są nadrzędne wobec Twoich interesów, praw i wolności, albo dane są mi potrzebne do ustalenia, dochodzenia lub obrony roszczeń. Raporty o awariach możesz też w każdej chwili zatrzymać, wyłączając *Udostępniaj deweloperom*.

Możesz wnieść skargę do organu nadzorczego w kraju, w którym mieszkasz lub pracujesz. Organem nadzorczym właściwym dla mnie jest Prezes Urzędu Ochrony Danych Osobowych (uodo.gov.pl).

Dane przechowywane przez Twojego dostawcę GitLab lub przez Apple podlegają ich politykom; w sprawie tych danych kontaktuj się bezpośrednio z nimi.

## 10. Podmioty trzecie

| Podmiot | Rola |
|---|---|
| GitLab Inc. (gitlab.com) lub operator Twojej samodzielnie hostowanej instancji | Odrębny administrator: otrzymuje każde żądanie, które Aplikacja wysyła w Twoim imieniu, i decyduje o Twoich danych w GitLab |
| Apple Inc. | Odrębny administrator w zakresie zakupów w aplikacji, subskrypcji i Twojego Konta Apple; dystrybuuje Aplikację |
| Google (Gmail; Google LLC w Stanach Zjednoczonych) | Odrębny administrator: obsługuje moją pocztę, w tym wiadomości, które do mnie wysyłasz (sekcja 6) |
| GitHub Inc. | Hostuje tę stronę w GitHub Pages; GitHub może rejestrować adresy IP odwiedzających zgodnie z własnym oświadczeniem o prywatności |

Nie udostępniam Twoich danych nikomu innemu, chyba że wymaga tego prawo.

## 11. Zmiany

Mogę aktualizować tę politykę wraz ze zmianami w Aplikacji. Aktualna wersja jest zawsze dostępna pod tym adresem wraz z datą wejścia w życie.

## 12. Kontakt

Dmytro Yantsybaiev, Kraków, Polska  
E-mail: d.yantsybaiev@gmail.com

Pełne dane mojej działalności (adres, telefon, NIP) znajdują się w [Warunkach korzystania](../terms/#14-kontakt).

Polityka prywatności jest dostępna w języku polskim i angielskim; obie wersje mają tę samą treść.
