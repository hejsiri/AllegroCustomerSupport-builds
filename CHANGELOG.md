# Changelog

## [2.1.102] - 2026-07-21

- Checkbox potwierdzenia w modalu „Bez odesłania” otrzymał standardowy styl Back Office: niebieskie wypełnienie i biały znacznik po zaznaczeniu.

## [2.1.101] - 2026-07-21

- Ujednolicono wygląd wszystkich czterech modali obsługi reklamacji: niebieska belka, nagłówek 26 px, wspólne odstępy i typografia treści 16 px.
- Oświadczenie „Potwierdzam, że rezygnuje…” ma teraz taki sam rozmiar jak pozostałe akapity i zwykłą, niepogrubioną grubość pisma.

## [2.1.100] - 2026-07-21

- Naprawiono migracje buildów Prestino 10–13, które przez niezgodne nazwy funkcji blokowały aktualizację instalacji ze starszych buildów.
- Proces budowania paczki sprawdza teraz automatycznie nazwę funkcji w każdym pliku migracji Prestino.

## [2.1.99] - 2026-07-21

- Naprawiono rozwijanie pola załącznika po wybraniu opcji „Załącz własną etykietę”, także gdy rozmowa reklamacyjna została wczytana dynamicznie.
- Obsługa nazwy wybranego pliku, pól wymaganych i liczników znaków działa teraz z poziomu głównego interfejsu modułu.

## [2.1.98] - 2026-07-21

- Treść modala „Zaplanuj odesłanie” została ujednolicona ze wzorem Allegro, wraz z pełnymi opisami metod oraz linkiem do informacji o etykiecie Allegro.

## [2.1.97] - 2026-07-21

- Modal rozpatrzenia reklamacji bez odesłania otrzymał standardową niebieską belkę akcentową u góry.

## [2.1.96] - 2026-07-21

- Powiększono tytuł „Rozpatrzenie reklamacji bez odesłania towaru” w oknie decyzji reklamacyjnej.

## [2.1.95] - 2026-07-21

- Przyciski „Bez odesłania” i „Zaplanuj odesłanie” w pierwszym kroku reklamacji otrzymały niebieski styl podstawowy.

## [2.1.94] - 2026-07-21

- Modal „Bez odesłania” otrzymał wskazany tytuł, opis skutków decyzji, informację o zapisie wiadomości w przebiegu reklamacji oraz pełne oświadczenie potwierdzające.
- Usunięto widoczne pole edycji wiadomości; wymagana wiadomość systemowa jest nadal przekazywana do Allegro wraz z decyzją.

## [2.1.93] - 2026-07-21

- Przycisk wyboru rozpatrzenia reklamacji bez zwrotu towaru otrzymał krótszą nazwę „Bez odesłania”.

## [2.1.92] - 2026-07-21

- Przycisk rozpoczynający wybór sposobu zwrotu reklamowanego towaru otrzymał nazwę „Zaplanuj odesłanie” zamiast „Wymagaj odesłania”.

## [2.1.91] - 2026-07-21

- Ustawienia modułu pokazują u góry taki sam alert licencji jak moduł pakowania: status pełnej wersji lub demo, termin aktualizacji oraz informację o bezterminowym działaniu modułu.
- Panel automatycznie sprawdza dostępność aktualizacji Prestino i pokazuje alert z przyciskiem bezpiecznej instalacji, gdy nowsza wersja jest dostępna.
- Alerty można zamknąć bez przeładowywania strony; brak połączenia z serwerem aktualizacji nie blokuje ustawień modułu.

## [2.1.90] - 2026-07-21

- Przywrócono właściwą linię numeracji `2.1.x`; poprzednie wydanie produkcyjne `2.1.78` odpowiadało funkcjonalnie dawnej wersji `0.2.179`.
- Wydanie konsoliduje wszystkie późniejsze zmiany robocze opisane jako `0.2.180–0.2.190`, bez utraty funkcji reklamacji, szablonów, cen produktów ani integracji z Prestino API.
- Numer `2.1.90` zachowuje końcówkę ostatniej wersji roboczej `0.2.190`; omyłkowo opublikowane wydanie porządkujące `2.1.79` zostało zastąpione przez `2.1.90`.
- Dodano migrację zbiorczą dla sklepów aktualizowanych bezpośrednio z `2.1.78` i `2.1.79` oraz zachowano ścieżkę aktualizacji z instalacji `0.2.189` i `0.2.190`.
- Aktualizacje korzystają z prywatnego API Prestino, serwerowej kontroli licencji i `updates_until`, kopii bezpieczeństwa, rollbacku oraz niezależnego buildu Prestino `4`.

> Wpisy `0.2.180–0.2.190` poniżej dokumentują wewnętrzną, omyłkowo kontynuowaną numerację po wydaniu `2.1.78`. Ich zawartość została oficjalnie włączona do `2.1.90`.

## [2.1.79] - 2026-07-21

- Krótkotrwałe wydanie przejściowe zastąpione tego samego dnia przez `2.1.90` w celu zachowania zgodności końcówki numeru z ostatnią wersją roboczą `0.2.190`.

## 0.2.190 - 2026-07-21

- Naprawiono sprawdzanie aktualizacji przez Prestino API w module Obsługi Klienta Allegro.
- Aktualizator pobiera teraz kontekst sklepu przez standardowy `Context::getContext()` zamiast wywoływać nieistniejącą metodę modułu `getContext()`.

## 0.2.189 - 2026-07-21

- Aktualizacje modułu są teraz sprawdzane i pobierane bezpośrednio z prywatnego API Prestino.
- Serwer Prestino weryfikuje licencję, domenę oraz termin dostępu do aktualizacji (`updates_until`).
- Przed instalacją aktualizacji moduł tworzy kopię bezpieczeństwa i automatycznie przywraca ją po błędzie.
- Dodano niezależny od wersji modułu numer buildu Prestino oraz obsługę migracji buildów.
- Zachowano ważność dotychczasowych licencji lokalnych; dostęp do nowych aktualizacji wymaga licencji wystawionej przez Prestino.

## [0.2.188] - 2026-07-21
- Rozwinięcie „Załącz własną etykietę” zawiera teraz strefę przeciągania lub wyboru pliku, nazwę wybranej etykiety oraz osobną wiadomość do kupującego.
- Rozwinięcie „Inna metoda odbioru” otrzymało dedykowane pole opisu odbioru zgodne z układem Allegro.
- Oba pola wiadomości mają limit i licznik 700 znaków, a serwer odczytuje treść wyłącznie z aktualnie wybranej metody.
- Uproszczono stopkę modalu: wysłanie następuje bez dodatkowego pola potwierdzenia, po wybraniu metody i uzupełnieniu wymaganych danych.

## [0.2.187] - 2026-07-21
- Modal „Zaplanuj odesłanie lub odbiór towaru” pokazuje opcje zgodne z przebiegiem reklamacji Allegro: informację o Allegro Smart, własną etykietę oraz inną metodę odbioru.
- Dodano wysyłanie własnej etykiety w formacie PDF lub obrazu do 2 MB przez oficjalny, dwuetapowy mechanizm załączników Allegro i wiadomość `RETURN_REQUIRED_SELLER_LABEL`.
- Dla innej metody odbioru formularz wymaga instrukcji dla kupującego i przekazuje ją jako `RETURN_REQUIRED_CUSTOM`.
- Pola formularza oraz przycisk wysyłania reagują na wybraną metodę, a niedostępna w publicznym API opcja Smart jest wyświetlana jako nieaktywna.

## [0.2.186] - 2026-07-21
- Dodano panel „Przebieg reklamacji” z osobnymi krokami decyzji o odesłaniu towaru i formalnego rozpatrzenia reklamacji.
- Sprzedający może przez API Allegro zdecydować o rozpatrzeniu bez odsyłania albo wymagać odesłania/udostępnienia towaru wraz z instrukcją dla kupującego.
- Dodano modal uznania reklamacji z wyborem naprawy, wymiany, zwrotu płatności lub częściowego zwrotu oraz modal odrzucenia z pełną listą powodów API Allegro i wymaganym uzasadnieniem.
- Operacje zmieniające przebieg i status reklamacji wymagają jawnego zatwierdzenia, są walidowane i zapisywane w logach modułu.

## [0.2.185] - 2026-07-21
- Jeśli historyczna pozycja zamówienia X13 zawiera tytuł, ale nie zawiera ceny, kwota reklamowanego produktu jest pobierana z odpowiadającej jej pozycji `order_detail` w PrestaShop.
- Dopasowanie lokalnej pozycji wykorzystuje sygnaturę oferty (`external.id`: ID produktu, referencję, EAN lub UPC), a dodatkowo powiązanie numeru oferty w tabeli X13.
- Kwota jest obliczana z historycznej ceny brutto właściwej pozycji i liczby reklamowanych sztuk; suma całego zamówienia nie jest używana.

## [0.2.184] - 2026-07-21
- Dodano obsługę starszego formatu pozycji zamówienia zapisywanego przez moduł X13 jako `lineItems.items`.
- Tytuł i kwota reklamowanego produktu są teraz pobierane z właściwej historycznej pozycji zamówienia także wtedy, gdy Allegro nie udostępnia już pełnych danych starego zamówienia przez API.
- Kwota nadal dotyczy wyłącznie pozycji dopasowanej do reklamowanej oferty, a nie całego zamówienia.

## [0.2.183] - 2026-07-21
- Panel zawsze pobiera pełne szczegóły wybranej reklamacji przed przygotowaniem gotowych odpowiedzi, zamiast korzystać wyłącznie ze skróconego wpisu z listy zgłoszeń.
- Dzięki pełnemu payloadowi reklamacji zmienne `{offer_title}` i `{claim_amount}` otrzymują identyfikator oferty potrzebny do dopasowania właściwej pozycji zamówienia Allegro.

## [0.2.182] - 2026-07-21
- Tytuł oferty w gotowej odmowie reklamacji jest pobierany dodatkowo bezpośrednio z oferty Allegro, a przy zamówieniu z jednym produktem także z pozycji lokalnego zamówienia PrestaShop.
- Usunięto podwójną kropkę po opisie wady przez normalizację końcowej interpunkcji zmiennej `{claim_reason_description}`.
- Kwota reklamacji jest liczona wyłącznie z ceny jednostkowej pozycji zamówienia Allegro dopasowanej po `offer.id` lub `offer.offerId` i liczby sztuk wskazanej w reklamacji.
- Usunięto fallback do całkowitej wartości zamówienia; przy braku jednoznacznego dopasowania kwota pozostaje pusta zamiast pokazywać sumę innych produktów.

## [0.2.181] - 2026-07-21
- Dodano zmienną `{offer_title}` uzupełnianą tytułem reklamowanej oferty Allegro.
- Gotowa odmowa reklamacji używa teraz sformułowania „dotyczącą produktu {offer_title}”; migracja zmienia wyłącznie ten fragment istniejącego szablonu.
- Uzupełnianie `{claim_amount}` korzysta dodatkowo z podsumowania płatności zamówienia Allegro i kwoty lokalnego zamówienia PrestaShop, gdy cena reklamowanej pozycji jest niedostępna.

## [0.2.180] - 2026-07-21
- Wbudowany aktualizator uruchamia teraz skrypty migracyjne przed zapisaniem nowej wersji modułu w bazie danych.
- Aktualizacja automatycznie dopisuje brakującą gotową odpowiedź „Odpowiedź na reklamację — odmowa” użytkownikom wersji `0.2.179`, bez nadpisywania istniejących szablonów.

## [2.1.78] - 2026-07-16

- Zmieniono schemat numeracji wersji modułu z linii `0.2.x` na `2.1.x`.
- Wydanie odpowiadało funkcjonalnie ówczesnej wersji `0.2.179` z 14 lipca 2026 r.

## [0.2.179] - 2026-07-21
- Dodano gotową odpowiedź odrzucającą reklamację, która uzupełnia dane zakupu, reklamacji, produktu, kwoty oraz opis wady bez nadpisywania istniejących szablonów.
- Dodano zmienne `{purchase_date}`, `{claim_submitted_date}`, `{claim_received_date}`, `{claim_reason}` i `{claim_reason_description}` wraz ze zgodnymi aliasami.
- Wynik diagnozy w gotowej odpowiedzi pozostaje oznaczony jako pole wymagające ręcznego uzupełnienia przed wysłaniem.

## [0.2.178] - 2026-07-14
- Naprawiono rozpoczynanie autoryzacji konta Allegro na sklepach, na których trasa frontowa `module/allegrocustomerservice/deviceauth` zwracała błąd 404.
- Żądania Device Flow są teraz obsługiwane przez chroniony kontroler ustawień w Back Office, bez ujawniania tokenu CRON w adresie autoryzacji.

## [0.2.177] - 2026-07-12
- Filtry wiadomości mają teraz tekst w spójnym, stonowanym kolorze oraz własne turkusowe checkboxy niezależne od systemowego stylu przeglądarki.
- Zaznaczony checkbox ma białą ikonę wyboru, a fokus otrzymał czytelne turkusowe podświetlenie.

## [0.2.176] - 2026-07-12
- Ujednolicono globalny odstęp między ikoną i tekstem we wszystkich przyciskach interfejsu modułu do 8 px.
- Reguła obejmuje ustawienia, wiadomości, dyskusje, reklamacje, zwroty oraz dynamiczne stany przycisku aktualizacji.

## [0.2.175] - 2026-07-12
- Wiadomości klientów powiązane z ofertą pokazują teraz miniaturę produktu obok numeru oferty.
- Miniatura jest rozwiązywana najpierw z produktu PrestaShop, następnie z danych oferty Allegro i zapisywana w cache według `offer_id`.

## [0.2.174] - 2026-07-12
- Nagłówek „Rozmowa z…” w sekcji wiadomości jest teraz linkiem otwierającym odpowiadający wątek w Centrum Wiadomości Allegro w nowej karcie.
- Link korzysta z bezpośredniej trasy Sales Center `/message-center/messages/thread/{threadId}`.

## [0.2.173] - 2026-07-12
- Zastąpiono nieaktualne README kompletną polską dokumentacją modułu: funkcje, instalacja, autoryzacja, wiadomości, zgłoszenia, zwroty, ustawienia, szablony, autoresponder, CRON, logi, licencja, aktualizacje, bezpieczeństwo i diagnostyka.

## [0.2.172] - 2026-07-12
- Opis funkcji „Włącz moduł” przeniesiono spod podpowiedzi po najechaniu bezpośrednio pod przełącznik, zgodnie z wyglądem pola trybu testowego.

## [0.2.171] - 2026-07-12
- Do etykiety „Włącz moduł” dodano podpowiedź wyjaśniającą, że przełącznik steruje automatycznym skanowaniem i odpowiedziami przez CRON, ale nie wyłącza panelu ani funkcji ręcznych.

## [0.2.170] - 2026-07-12
- Po wejściu do ustawień moduł automatycznie sprawdza dostępność aktualizacji i pokazuje wynik na głównym przycisku aktualizacji.
- Automatyczne sprawdzenie nie instaluje aktualizacji; instalacja nadal wymaga świadomego kliknięcia przycisku.

## [0.2.169] - 2026-07-12
- Zmniejszono wysokość pola adresu CRON i doklejonych przycisków z 52 do 42 px, bez zmiany wielkości tekstu oraz ikon.

## [0.2.168] - 2026-07-12
- Przycisk kopiowania adresu CRON jest domyślnie niebieski z białym tekstem i ikoną.
- Po skopiowaniu zielony stan „Skopiowano” zachowuje biały tekst i ikonę również po najechaniu oraz ustawieniu fokusu.

## [0.2.167] - 2026-07-12
- Pole adresu CRON i doklejone przyciski korzystają teraz z niezależnego układu flex zamiast konfliktującego `input-group` panelu administracyjnego.
- Wymuszono identyczną wysokość 52 px, wspólne obramowanie oraz pionowe wyśrodkowanie zawartości pola i przycisków.

## [0.2.166] - 2026-07-12
- Gotowe odpowiedzi są teraz prezentowane jako nieedytowalna lista ze statusem, nazwą i skróconym podglądem treści.
- Dodawanie i edycja gotowej odpowiedzi odbywają się we wspólnym oknie modalnym, a zapis jest wykonywany bezpośrednio z modala.
- Usuwanie wpisu wymaga potwierdzenia i od razu zapisuje zaktualizowaną listę.

## [0.2.165] - 2026-07-12
- Przycisk „Dodaj odpowiedź” w panelu gotowych odpowiedzi ma teraz niebieski styl głównej akcji.

## [0.2.164] - 2026-07-12
- Przycisk ręcznego uruchamiania skanowania ma teraz niebieski styl głównej akcji oraz ikonę odświeżania.

## [0.2.163] - 2026-07-12
- Panel gotowych odpowiedzi korzysta teraz z tej samej natywnej konstrukcji `panel` i nagłówka `h3` co pozostałe sekcje ustawień PrestaShop.
- Dodano ikony do nagłówków: gotowe odpowiedzi, informacje o module, reguły automatycznych odpowiedzi oraz ostatnie logi.

## [0.2.162] - 2026-07-12
- Usunięto konflikt nagłówka panelu gotowych odpowiedzi ze stylami `.panel h3` PrestaShop, który powodował nadmierną wysokość i pustą przestrzeń.
- Zagęszczono odstępy nagłówka, tabeli i stopki oraz zachowano czytelny układ mobilny.

## [0.2.161] - 2026-07-12
- Przyciski przy adresie CRON korzystają ponownie ze standardowego układu grupy pól Bootstrap i mają dokładnie tę samą wysokość co pole URL.

## [0.2.160] - 2026-07-12
- Odpowiedź JSON zadania CRON zawiera teraz bezpieczne podsumowanie: liczbę sprawdzonych wątków, wiadomości klientów, dopasowań, wysłanych i testowych odpowiedzi, pominięć oraz błędów.
- Podsumowanie nie ujawnia treści wiadomości, danych klientów ani szczegółów zamówień.

## [0.2.159] - 2026-07-12
- Przyciski kopiowania i otwierania adresu CRON mają teraz pełną wysokość pola tekstowego oraz wyśrodkowane ikony i etykiety.

## [0.2.158] - 2026-07-12
- Dodano niezależny endpoint CRON-u w katalogu modułu, omijający niedziałający routing kontrolerów frontowych PrestaShop.
- Adres CRON-u w ustawieniach jest prezentowany w polu tekstowym z przyciskami kopiowania i otwierania w nowej karcie.

## [0.2.157] - 2026-07-12
- Odświeżono panel gotowych odpowiedzi: dodano spójny nagłówek, czytelne karty, podpowiedź zmiennych i responsywny układ mobilny.
- Adres CRON w ustawieniach korzysta teraz z bezpośredniej trasy `index.php`, niezależnej od przyjaznych adresów i prefiksu języka.

## [0.2.156] - 2026-07-10
- Wyrównano checkboxy filtrów wiadomości i ich etykiety w jednym wierszu.
- Etykiety `Nieprzeczytane` i `Wymaga odpowiedzi` mają normalną grubość tekstu niezależnie od stylów panelu administracyjnego.

## [0.2.155] - 2026-07-10
- Aktywne filtry wiadomości przeszukują po 80 wątków na każdą paczkę lazy load zamiast tylko 20, dzięki czemu odnajdują także starsze rozmowy wymagające odpowiedzi.
- Dodano twardy limit 400 skanowanych wątków oraz zachowano cache stanu ostatniej wiadomości, aby ograniczyć obciążenie API Allegro i panelu.

## [0.2.154] - 2026-07-10
- Filtry wiadomości uwzględniają kolejne paczki lazy load także wtedy, gdy pierwsza paczka zawiera zbyt mało wyników, aby lista miała pasek przewijania.
- Przy aktywnym filtrze krótka lista automatycznie pobiera jedną następną paczkę; dalsze paczki są pobierane przy przewijaniu lub ruchu kółkiem w dół, bez zapętlenia.

## [0.2.153] - 2026-07-10
- Dodano rzeczywisty mechanizm wykrywania wiadomości wymagających odpowiedzi na podstawie `author.isInterlocutor` najnowszej wiadomości w każdym wątku.
- Stan jest cache'owany względem `lastMessageDateTime`, dzięki czemu API jest ponownie sprawdzane dopiero po pojawieniu się nowej wiadomości.
- Wątki wymagające reakcji otrzymują oznaczenie `wymaga odpowiedzi`, a filtr `Bez mojej odpowiedzi` korzysta z tego samego stanu.

## [0.2.152] - 2026-07-10
- Tekst etykiet filtrów wiadomości używa normalnej grubości czcionki zamiast pogrubienia.

## [0.2.151] - 2026-07-10
- Powiększono tekst i checkboxy filtrów wiadomości oraz zwiększono odstępy i kontrast zaznaczenia dla lepszej czytelności.

## [0.2.150] - 2026-07-10
- Usunięto zapętlanie lazy load wiadomości przy aktywnych filtrach: kolejne paczki nie są już automatycznie pobierane przy starcie ani natychmiast po poprzedniej odpowiedzi.
- Następna paczka wątków jest pobierana dopiero po rzeczywistym przewinięciu listy do końca; przycisk pozostaje ręcznym fallbackiem.

## [0.2.149] - 2026-07-10
- Usunięto przycisk `Wyczyść` z filtrów wiadomości.
- Lista wiadomości pobiera początkowo 20 wątków, a kolejne paczki są dopisywane bez przeładowania widoku przez mechanizm lazy load.

## [0.2.148] - 2026-07-10
- Pusty wynik filtrowania wiadomości nie usuwa już listy, wyszukiwarki ani okna rozmowy; filtry można od razu wyłączyć.
- Filtr `Bez mojej odpowiedzi` obsługuje wątki, w których endpoint Allegro nie zwraca autora ostatniej wiadomości, używając statusu nieprzeczytania jako bezpiecznego fallbacku.

## [0.2.147] - 2026-07-10
- Filtry wiadomości `Nieprzeczytane` i `Bez mojej odpowiedzi` działają od razu po zaznaczeniu lub odznaczeniu, bez przycisku `Filtruj`.
- Poprawiono filtr `Bez mojej odpowiedzi`: sprawdza autora ostatniej wiadomości niezależnie od tego, czy wątek został już przeczytany.

## [0.2.146] - 2026-07-10
- Przeniesiono kompaktową wyszukiwarkę i filtry wiadomości bezpośrednio nad listę w lewej kolumnie.
- Pole `Szukaj odbiorcy` otrzymało neutralne atrybuty formularza blokujące sugestie haseł i autouzupełnianie menedżerów logowania.

## [0.2.145] - 2026-07-10
- Naprawiono odczyt cache miniaturek `Zwrotów towarów`: lista akceptuje teraz lokalne adresy zdjęć PrestaShop w formacie `/img/p/...`, które wcześniej były poprawnie używane w szczegółach, lecz odrzucane na liście.

## [0.2.144] - 2026-07-10
- Lista `Zwrotów towarów` zapisuje teraz w swoim cache dokładny URL zwracany przez ten sam resolver produktu, którego używają poprawne miniatury w szczegółach zwrotu.
- Podczas przygotowania listy wykorzystywany jest najpierw lokalnie zapisany checkout form, aby ograniczyć dodatkowe zapytania do Allegro.

## [0.2.143] - 2026-07-10
- Naprawiono puste miniatury na całej liście `Zwrotów towarów`: lista nie zależy już od niedziałającej trasy szczegółów zwrotu i korzysta z lekkiego resolvera `offerId + orderId`, który pobiera EAN z właściwej pozycji checkout formy.

## [0.2.142] - 2026-07-10
- Lista `Zwrotów towarów` używa teraz dokładnie tego samego resolvera pierwszego zwracanego produktu co poprawne miniatury w szczegółach zwrotu; wynik jest zapisywany w cache listy.

## [0.2.141] - 2026-07-10
- Przyspieszono ładowanie `Zwrotów towarów`: lista nie wykonuje już synchronicznie ciężkiego dopasowania każdej miniatury podczas generowania strony.
- Dodano osobny cache miniaturek zwrotów; pełne wyszukiwanie po EAN/historycznej pozycji jest wykonywane leniwie i jego poprawny wynik jest ponownie używany.

## [0.2.140] - 2026-07-10
- Ujednolicono miniaturę zaznaczonego `Zwrotu towarów` na liście z resolverem używanym w szczegółach produktu, aby poprawnie znalezione zdjęcie po EAN/historycznej pozycji nie znikało po zaznaczeniu zwrotu.

## [0.2.139] - 2026-07-10
- W modalu `Diagnostyka API zwrotu` dodano przycisk `Kopiuj JSON` z potwierdzeniem skopiowania i fallbackiem dla starszych przeglądarek.

## [0.2.138] - 2026-07-10
- Dla miniaturek `Zwrotów towarów` dodano fallback po historycznej pozycji powiązanego zamówienia PrestaShop, dopasowanej dokładnie po `offerId`; obsługuje to produkty, których EAN zmienił się po zakupie, również w zwrotach wielopozycyjnych.

## [0.2.137] - 2026-07-10
- Zastosowano dopasowanie po EAN-13 także do dużej miniatury produktu w szczegółach `Zwrotu towarów`, dzięki czemu używa ona tego samego zdjęcia PrestaShop co pozycja na liście.

## [0.2.136] - 2026-07-10
- Resolver miniatur zwrotów rozpoznaje teraz 13-cyfrowy EAN zapisany przez Allegro w `lineItems[].offer.external.id`, m.in. `5905997750783`, i wyszukuje po nim zdjęcie produktu lub kombinacji PrestaShop.

## [0.2.135] - 2026-07-10
- Przycisk `Decyzja zwrotowa` w sekcji zwrotów otrzymał niebieski styl głównej akcji.

## [0.2.134] - 2026-07-10
- W `Zwrotach towarów` miniatura jest dobierana priorytetowo po EAN-13 zwracanej pozycji, dopasowanym z danych zwrotu, pozycji checkout formy lub oferty Allegro do produktu/kombinacji PrestaShop.

## [0.2.133] - 2026-07-10
- Poprawiono brakujące miniatury wyłącznie w `Zwrotach towarów`: lista może teraz leniwie pobrać pełne szczegóły zwrotu i znaleźć zdjęcie po pozycji, ofercie, checkout formie lub powiązanym zamówieniu PrestaShop.

## [0.2.132] - 2026-07-10
- Dodano kompaktowy filtr nad listą wiadomości: wyszukiwanie po loginie odbiorcy oraz opcje `Nieprzeczytane` i `Bez mojej odpowiedzi`.

## [0.2.131] - 2026-07-10
- Usunięto zbędny podtytuł `Wątek Allegro` z nagłówka rozmowy w wiadomościach.

## [0.2.130] - 2026-07-10
- Usunięto szare tło avatarów na liście wiadomości; zdjęcie lub inicjał są wyświetlane na przezroczystym tle.

## [0.2.129] - 2026-07-10
- Nieodczytane wątki na liście wiadomości są wyróżniane pogrubionym loginem, datą i podglądem wiadomości bez względu na autora ostatniej odpowiedzi.

## [0.2.128] - 2026-07-10
- Dodano okrągłe avatary kupujących na liście wiadomości; moduł pokazuje zdjęcie profilowe zwrócone przez Allegro, a przy jego braku inicjał loginu.

## [0.2.127] - 2026-07-10
- Usunięto powtórzone wiersze `Zamówienie Allegro` i `Zamówienie w sklepie` z karty `Zamówienie i produkt`; dane pozostają widoczne w nagłówku reklamacji.

## [0.2.126] - 2026-07-10
- Przeniesiono kod kraju w danych dostawy na koniec wiersza z kodem pocztowym i miastem, np. `41-813 Zabrze PL`.

## [0.2.125] - 2026-07-10
- Uodporniono tłumaczenie `Not as described` na niewidoczne separatory oraz warianty ze spacjami, myślnikami i podkreśleniami zwracane przez Allegro.

## [0.2.124] - 2026-07-10
- Dodano polskie tłumaczenie powodu i tematu reklamacji `Not as described` jako `Produkt niezgodny z opisem`.

## [0.2.123] - 2026-07-10
- Miniatury reklamacji są teraz rozwiązywane bezpośrednio podczas renderowania listy z powiązanego zamówienia PrestaShop, bez uzależniania wszystkich obrazów od dodatkowego żądania lazy-load.

## [0.2.122] - 2026-07-10
- Poprawiono strukturę paczki instalacyjnej: katalog główny ZIP jest zgodny z techniczną nazwą modułu `allegrocustomerservice`.

## [0.2.121] - 2026-07-10
- Usunięto techniczny przycisk `DIAG` spod miniatur na listach reklamacji i dyskusji; diagnostyka miniatur nie jest już eksponowana w interfejsie obsługi klienta.
- Uzupełniono dobór miniatur reklamacji o bezpieczny fallback z powiązanego zamówienia PrestaShop, gdy Allegro nie zwraca pełnych identyfikatorów pozycji; odświeżono również klucze cache miniatur.

## [0.2.120] - 2026-06-11
- Dodano usuwanie starego pliku zgodności `allegroautoresponder.php` z katalogu modułu podczas aktualizacji.

## [0.2.119] - 2026-06-11
- Dodano skrypt aktualizacji PrestaShop, który usuwa z katalogu modułu pozostałości po wcześniejszych paczkach: `scripts/`, `tools/`, techniczny katalog `config/`, `.gitignore` oraz dokumenty automatyzacji release.

## [0.2.118] - 2026-06-11
- Oczyszczono paczkę instalacyjną z plików deweloperskich: `scripts/`, `config/`, `.gitignore` oraz dokumentów automatyzacji release.
- Aktualizator usuwa pozostałości po wcześniejszych paczkach z katalogu modułu, w tym stary generator licencji i skrypty release, bez dotykania lokalnego `license.php`.

## [0.2.117] - 2026-06-11
- Usunięto generator licencji z kodu i paczki modułu; płatny moduł zawiera wyłącznie walidację dostarczonego pliku `license.php`.
- README doprecyzowuje, że licencję generuje i dostarcza wydawca modułu, a nie instalacja klienta.

## [0.2.116] - 2026-06-11
- Dodano lokalną stronę WWW `tools/license-generator/` do wygodnego generowania i pobierania plików `license.php`.
- CLI i strona WWW korzystają ze wspólnej biblioteki generatora licencji, a katalog `tools/` jest pomijany przy budowaniu paczki modułu.

## [0.2.115] - 2026-06-11
- Dodano uniwersalny generator licencji `scripts/generate_license.php` dla modułów używających podpisanych kluczy w formacie CargoStockManager.
- Opisano generowanie `license.php` w README oraz dodano ignorowanie lokalnego `config/license_private.pem`.

## [0.2.114] - 2026-06-11
- Dodano licencjonowanie modułu w modelu CargoStockManager: podpisany klucz w `license.php`, weryfikacja przez `keys/license_public.pem`, sprawdzanie modułu, domeny i daty wygaśnięcia.
- Panel ustawień pokazuje dane licencji, a funkcje modułu, CRON i akcje administracyjne są blokowane, gdy licencja jest nieważna lub nieobecna.
- Aktualizator zachowuje lokalny plik `license.php` podczas instalacji nowej wersji.

## [0.2.113] - 2026-06-11
- Wyłączono sugestie haseł i autouzupełnianie Safari w polach wyszukiwania zgłoszeń oraz zwrotów.
- Pola wyszukiwania używają teraz typu `search` i neutralnych atrybutów autofill, żeby przeglądarka nie traktowała ich jak loginu.

## [0.2.112] - 2026-06-11
- Dodano wyszukiwarkę nad reklamacjami i dyskusjami, dopasowaną układem do filtrów zwrotów towarów.
- Wyszukiwanie zgłoszeń obejmuje m.in. numer zgłoszenia, zamówienie, ofertę, login kupującego, temat, status i dane z payloadu Allegro.

## [0.2.111] - 2026-06-09
- Poprawiono kody powodów zwrotu pieniędzy do wartości akceptowanych przez Allegro API: `PRODUCT_NOT_AVAILABLE`, `PAID_VALUE_TOO_LOW`, `OVERPAID`, `CANCELLED_BY_BUYER`, `NOT_COLLECTED`.
- Dodano mapowanie starych aliasów z formularza zwrotu pieniędzy na aktualne kody API, żeby uniknąć błędu 422 przy otwartym wcześniej formularzu.

## [0.2.110] - 2026-05-29
- Posprzątano runtime po migracji technicznej nazwy modułu: usunięto panel przenoszenia starego katalogu, automatyczne cleanupy legacy i ciche naprawiacze uruchamiane przy każdym wejściu do BO.
- Menu BO opiera się teraz wyłącznie na właściwych kontrolerach `AdminAllegroCustomerService*`, a upgrade tylko odświeża standardowe taby i hooki modułu.
- Usunięto stare mostki `AllegroAutoresponder*` oraz plik wejściowy `allegroautoresponder.php` z paczki instalacyjnej.

## [0.2.109] - 2026-05-29
- Naprawiono brak pozycji modułu w menu BO po migracji: instalacja i aktualizacja ponownie tworzą/naprawiają taby `AdminAllegroCustomerService*`, ustawiają `active`/`enabled` i odświeżają uprawnienia profilu.
- Dodano ciche samonaprawianie menu w hooku Back Office, żeby moduł odtworzył brakujące pozycje także po wcześniejszej niepełnej instalacji.

## [0.2.108] - 2026-05-29
- Naprawiono instalację po ręcznej migracji modułu na sklepach, gdzie część tabel powiązań modułu istnieje, ale nie ma kolumny `id_module`; cleanup starych wpisów sprawdza teraz kolumny każdej tabeli przed wykonaniem `DELETE`.

## [0.2.107] - 2026-05-29
- Naprawiono instalację po ręcznej migracji modułu, gdy tabela `hook_module_exceptions` w danej wersji PrestaShop nie ma kolumny `id_hook_module`; czyszczenie starych wpisów wykrywa teraz dostępne kolumny i używa właściwego wariantu zapytania.

## [0.2.106] - 2026-05-29
- Naprawiono błąd instalacji/porządkowania po migracji: sprawdzanie istnienia tabel nie używa już `Db::getValue('SHOW TABLES ...')`, bo PrestaShop dokleja tam `LIMIT 1`, czego MariaDB nie akceptuje dla `SHOW TABLES`.

## [0.2.105] - 2026-05-29
- Dodano automatyczne porządkowanie starych wpisów po ręcznej instalacji `allegrocustomerservice` obok dawnego modułu: osierocone taby `AdminAllegroAutoresponder*` są usuwane albo przepinane na nowe kontrolery, a stary wpis `module` jest czyszczony, gdy istnieje już nowy moduł.
- Naprawiono przypadek, w którym BO pokazywało `Kontroler AdminAllegroAutoresponderSettings jest niedostępny bądź uszkodzony` po zmianie nazwy katalogu starego modułu.

## [0.2.104] - 2026-05-29
- Zabezpieczono główną klasę modułu, service’y, updater i kontrolery przed podwójnym załadowaniem, gdy PrestaShop widzi jednocześnie katalog `allegroautoresponder` i `allegrocustomerservice`.
- Poprawka usuwa fatal error `Cannot declare class AllegroCustomerService, because the name is already in use` podczas przejściowej migracji katalogu.

## [0.2.103] - 2026-05-29
- Dodano bezpieczny migrator katalogu modułu z `allegroautoresponder` do `allegrocustomerservice`: przenosi katalog FTP, aktualizuje wpis modułu w bazie, przestawia taby BO i poprawia zapisany URL OAuth.
- W ustawieniach pojawia się panel porządkowania tylko wtedy, gdy moduł działa jeszcze ze starej nazwy albo stary katalog nadal istnieje na FTP.

## [0.2.102] - 2026-05-29
- Naprawiono renderowanie konfiguracji po przejściu na `allegrocustomerservice`: szablon `configure.tpl` jest teraz szukany względem faktycznie załadowanego pliku wejściowego modułu, więc działa też po aktualizacji istniejącej instalacji ze starego katalogu.

## [0.2.101] - 2026-05-29
- Zmieniono techniczny identyfikator modułu z `allegroautoresponder` na `allegrocustomerservice`: główna klasa, plik modułu, namespace usług, kontrolery, linki frontowe, domeny tłumaczeń oraz paczka ZIP używają nowej nazwy.
- Dodano mostki kompatybilności dla starej nazwy modułu i starych kontrolerów, żeby aktualizacja istniejącej instalacji nie gubiła wejść BO ani endpointów frontowych podczas przejścia.
- Skrypt release buduje teraz paczkę instalacyjną z katalogiem `allegrocustomerservice/`; prefiksy konfiguracji `AAR_` i tabele `allegro_ar_*` pozostają bez zmian, żeby zachować dotychczasowe dane.

## [0.2.100] - 2026-05-29
- W nagłówku reklamacji podlinkowano numer zamówienia Allegro do Sales Center oraz referencję zamówienia sklepowego do widoku zamówienia w PrestaShop.
- Usunięto z prawej strony nagłówka reklamacji dodatkowe etykiety typu `Czat aktywny` i `Reklamacja ustawowa`, zostawiając sam status.
- Na liście reklamacji i dyskusji przeniesiono etykietę typu zgłoszenia oraz przycisk `DIAG` pod miniaturę produktu.

## [0.2.99] - 2026-05-28
- Dodano zmienną `{claim_product_name}` dla gotowych odpowiedzi, uzupełnianą nazwą reklamowanego produktu z pozycji zamówienia dopasowanej po `offer_id`.
- Dodano aliasy `{claimed_product_name}`, `{issue_product_name}` i `{product_name}` oraz pokazano nową zmienną w podpowiedzi sekcji gotowych odpowiedzi.

## [0.2.98] - 2026-05-28
- Dodano zmienne gotowych odpowiedzi dla kwoty reklamowanego produktu: `{claim_amount}`, `{claim_amount_value}`, `{claim_currency}`, `{claim_quantity}` i `{claim_unit_amount}`.
- Kwota reklamacji jest liczona z pozycji zamówienia Allegro dopasowanej po `offer_id`, z fallbackiem do lokalnie zapisanego checkout formu dla starszych zamówień.
- Formularz odpowiedzi po powiększeniu zachowuje przewinięcie wątku rozmowy i ma bardziej kompaktową wysokość przycisku `Wyślij`.

## [0.2.97] - 2026-05-28
- Ulepszono naprawę kodowania changeloga w panelu aktualizacji: parser rozdziela wpisy po liniach w trybie Unicode, co eliminuje rozbijanie polskich znaków podczas odczytu.
- Doprecyzowano opisy zmian, aby unikać prezentowania przykładowych sekwencji mojibake jako treści notki.

## [0.2.96] - 2026-05-28
- W formularzach odpowiedzi (wiadomości, dyskusje, reklamacje) dodano uchwyt z trzema kropkami do powiększania i zwijania pola wiadomości.
- Kliknięcie uchwytu przełącza tryb edytora bez utraty treści i utrzymuje wygodne fokusowanie kursora.

## [0.2.95] - 2026-05-28
- Naprawiono brakujące mapowanie uszkodzonej sekwencji dla litery `ż` w panelu aktualizacji, dzięki czemu opisy zmian poprawnie pokazują słowa typu `można` i `niezależnie`.
- Dodano fallback naprawy dla urwanych sekwencji CP1250 (np. końcówki wyrazu z uszkodzonym `ą`), żeby komunikaty aktualizacji nie gubiły polskich znaków.

## [0.2.94] - 2026-05-28
- Formularz odpowiedzi w dyskusjach i reklamacjach używa teraz ikony listy (hamburger) osadzonej w polu tekstowym zamiast osobnego przycisku `Gotowiec`.
- Dodano osobną sekcję `Gotowe odpowiedzi (ręczne)` w ustawieniach modułu, gdzie można tworzyć własne gotowce niezależnie od reguł automatycznych.
- Gotowe odpowiedzi obsługują teraz zmienne kontekstowe (m.in. `{orderdate}`, `{orderdatetime}`, `{claimdate}`, `{claimdatetime}`, `{order_id}`, `{offer_id}`, `{buyer_login}`), a podmiana działa zarówno przy wyborze gotowca, jak i przy wysyłce wiadomości.

## [0.2.93] - 2026-05-28
- Naprawiono kodowanie listy zmian w panelu aktualizacji: tekst z changeloga jest dodatkowo naprawiany dla typowych przekłamań Windows-1250/ISO-8859-2/Windows-1252.
- Odpowiedzi AJAX aktualizacji są zwracane jako UTF-8 z `JSON_UNESCAPED_UNICODE`, żeby polskie znaki nie zamieniały się w mojibake po stronie przeglądarki.

## [0.2.92] - 2026-05-28
- Miniatury reklamacji i dyskusji nie dopasowują już pozycji zamówienia po nazwie ani fuzzy-name; decyzja opiera się na identyfikatorach/EAN-ach, a brak trafienia w PrestaShop zostaje brakiem miniatury zamiast ryzyka pokazania innego produktu.
- Lookup po identyfikatorze PrestaShop normalizuje teraz spacje, myślniki i warianty EAN oraz sprawdza też `product_supplier.product_supplier_reference` i `cargostockmanager_product_logistics.module_model`.
- Cache miniatur przeniesiono na klucze `ps-v14`, żeby odciąć błędne wyniki zapisane przez dopasowanie po nazwie.

## [0.2.91] - 2026-05-28
- Dla reklamacji z pozycją checkout form pasującą po `offer_id` dopuszczono luźniejsze dopasowanie nazwy do `order_detail`, gdy EAN z oferty Allegro nie zgadza się już z EAN-em historycznej pozycji zamówienia PrestaShop.
- Cache miniatur przeniesiono na klucze `ps-v13`, żeby odciąć puste wyniki ze starszego progu dopasowania nazw.

## [0.2.90] - 2026-05-28
- Fallback miniatur dla niepełnych checkout formów sprawdza teraz także `/sale/product-offers/{offer_id}`, żeby wyciągnąć `external.id`/EAN oferty, gdy katalogowy `/sale/products/{product_id}` zwraca 404.
- Cache miniatur przeniesiono na klucze `ps-v12`, aby odciąć wyniki bez lookupu po ofercie produktowej.

## [0.2.89] - 2026-05-28
- Dodano bezpieczny fallback dla niepełnych zapisanych checkout formów: gdy pozycja reklamacji ma `offer_id`, ale lokalny checkout form nie ma tej pozycji, moduł próbuje pobrać identyfikatory produktu Allegro (`/sale/products/{product_id}`) i dopasować je do `order_detail` lub produktu PrestaShop.
- Diagnostyka miniatur pokazuje teraz lookup po produkcie Allegro oraz identyfikatory znalezione w payloadzie reklamacji/chatu.

## [0.2.88] - 2026-05-28
- Zaostrzono dobór miniatur reklamacji w zamówieniach wielopozycyjnych: jeśli reklamacja ma `offer_id`, a checkout form zawiera pozycje z innymi `offer_id`, moduł nie używa ich już jako fallbacku.
- Diagnostyka miniatur pokazuje teraz powód pominięcia fallbacku, gdy w zamówieniu Allegro nie ma pozycji pasującej do `offer_id` reklamacji.
- Cache miniatur przeniesiono na klucze `ps-v10`, żeby nie podawać wcześniej zapisanej miniatury z niepasującej pozycji.

## [0.2.87] - 2026-05-28
- Diagnostyka miniatur zwraca teraz JSON z nagłówkiem `application/json; charset=utf-8`, żeby polskie znaki nie wyświetlały się jako mojibake w przeglądarce.

## [0.2.86] - 2026-05-28
- Dodano fallback dla starych checkout formów bez EAN/sygnatur: po znalezieniu zamówienia PrestaShop moduł dopasowuje pozycję po podobieństwie nazwy z Allegro do `order_detail.product_name`, a dla zamówień z jednym produktem używa tej jednej pozycji.
- Odświeżono klucze cache miniatur, żeby nie mieszać wyników ze starszą logiką.

## [0.2.85] - 2026-05-28
- Uproszczono zapytania SQL wybierające obraz produktu PrestaShop zgodnie z CargoStockManager: najpierw `MIN(product_attribute_image.id_image)`, potem cover z `image`, potem najniższe `id_image`, bez ręcznego `LIMIT` w `Db::getValue()`.

## [0.2.84] - 2026-05-28
- Miniatury PrestaShop budują teraz bezpośredni legacy URL `/img/p/.../{id_image}-small_default.jpg`, zgodny z realnymi adresami obrazów w sklepie.
- Diagnostyka miniatur pokazuje `legacy_url`, żeby łatwo porównać wygenerowany adres z adresem pliku w PrestaShop.

## [0.2.83] - 2026-05-28
- Naprawiono budowanie URL miniatur PrestaShop: moduł używa teraz formatu `id_product-id_image`, szuka `link_rewrite` z fallbackiem poza bieżącym sklepem/językiem i pokazuje szczegóły wyboru obrazu w diagnostyce.
- Dopasowanie EAN/reference/SKU w PrestaShop ignoruje przypadkowe spacje w polach produktu, kombinacji i szczegółów zamówienia.

## [0.2.82] - 2026-05-28
- Miniatury dyskusji i reklamacji są teraz strict PrestaShop: nie zapisują ani nie zwracają obrazu z Allegro jako finalnego fallbacku.
- Lookup miniatur po `checkout_form_id` sprawdza też powiązane zamówienie PrestaShop i jego `order_detail`, w tym `product_ean13`, `product_reference`, `product_supplier_reference`, `product_upc` oraz `product_attribute_id`.
- Diagnostyka miniatur pokazuje wynik dopasowania po szczegółach zamówienia PrestaShop oraz ignorowany URL Allegro, jeśli Allegro go zwróciło.

## [0.2.81] - 2026-05-28
- Diagnostyka miniatur pokazuje `module_version` i `thumbnail_logic_version`, aby łatwo potwierdzić wersję faktycznie zainstalowaną w sklepie.
- Usunięto z klienta API przestarzałą metodę `GET /sale/offers/{id}`, żeby żaden fallback ani diagnostyka nie mogły już wywołać zablokowanego endpointu Allegro.

## [0.2.80] - 2026-05-28
- Usunięto przestarzałe wywołania Allegro `GET /sale/offers/{id}` z diagnostyki i fallbacku miniatur, aby nie pokazywać mylącego komunikatu `ACCESS_DENIED`.
- Diagnostyka dopasowania sygnatury PrestaShop pokazuje teraz jawnie `source: not_found` oraz sprawdzane pola, gdy EAN/reference/SKU nie pasuje do produktu ani kombinacji.

## [0.2.79] - 2026-05-28
- Reklamacje i dyskusje preferują miniaturę z PrestaShop po sygnaturze pozycji zamówienia przed każdym URL-em obrazu z Allegro.
- Cache miniatur zgłoszeń przeniesiono na klucze `order-v5`, aby odciąć wcześniejsze wpisy zapisane z URL-ami Allegro.

## [0.2.78] - 2026-05-28
- Diagnostyka miniatur pokazuje sygnaturę pozycji zamówienia Allegro (`offer.external.id`) oraz wszystkie kandydaty identyfikatorów używane do dopasowania produktu.
- Miniatury zgłoszeń próbują teraz użyć sygnatury z pozycji zamówienia do znalezienia obrazu produktu lub kombinacji w PrestaShop po EAN/reference/SKU, zanim przejdą do obrazu z oferty Allegro.
- Dopasowanie wielopozycyjnych zamówień nie przeskakuje już na inną pozycję, gdy zgłoszenie ma znane `offer_id`.
- Cache miniatur zgłoszeń przeniesiono na klucze `order-v4`, aby preferować nowy wynik z PrestaShop po sygnaturze.

## [0.2.77] - 2026-05-28
- Miniatury zgłoszeń używają zamówienia Allegro do wyboru właściwej pozycji, a gdy `checkout_form.lineItems` nie zawiera obrazów, dociągają miniaturę z oferty/produktu Allegro dla tej pozycji.
- Cache miniatur zgłoszeń przeniesiono na klucze `order-v3`, aby ominąć wcześniejsze puste lub błędne wyniki.

## [0.2.76] - 2026-05-28
- Diagnostyka miniatur zgłoszeń jest teraz widoczna w panelu jako przycisk `diag` przy miniaturze oraz jako lista linków w konsoli przeglądarki.

## [0.2.75] - 2026-05-28
- Dodano diagnostykę miniatur zgłoszeń w endpointcie `thumbnail`, pokazującą identyfikatory z dyskusji, chat, cache, pobranie `checkout_form` i znalezione obrazy w pozycjach zamówienia Allegro.
- Gdy miniatura zgłoszenia nie załaduje się w przeglądarce, moduł loguje w konsoli link diagnostyczny i wynik diagnostyki JSON.

## [0.2.74] - 2026-05-28
- Miniatury dyskusji i reklamacji korzystają sztywno z obrazów w zamówieniu Allegro (`checkout_form_id` / `lineItems`), z proxy dla chronionych URL-i API Allegro i bez fallbacku do produktów PrestaShop.

## [0.2.73] - 2026-05-28
- Gdy `checkout_form_id` pozwala ustalić ofertę, miniatura zgłoszenia jest pobierana z obrazu oferty Allegro zamiast z mapowania produktu PrestaShop.

## [0.2.72] - 2026-05-28
- Miniatury dyskusji i reklamacji są pobierane najpierw z pozycji zamówienia Allegro (`checkout_form_id` + `offer_id`), czyli z tego samego źródła co poprawne miniatury w zamówieniu.

## [0.2.71] - 2026-05-28
- Przebudowano resolver miniatur zgłoszeń: `checkout_form_id` mapuje zamówienie PrestaShop, a `offer_id` wybiera konkretną pozycję po referencji, EAN/GTIN, SKU, nazwie lub zapisanym payloadzie checkout form.

## [0.2.70] - 2026-05-28
- Miniatury zgłoszeń z gotowym `checkout_form_id` szukają teraz bezpośrednio lokalnego zamówienia PrestaShop przed wywołaniami API Allegro.

## [0.2.69] - 2026-05-28
- Lazy loader miniatur zgłoszeń używa teraz chatu do znalezienia zamówienia PrestaShop, gdy lista Allegro zawiera tylko `issue_id`.

## [0.2.68] - 2026-05-28
- Miniatury dyskusji i reklamacji opierają się wyłącznie na produktach PrestaShop, bez fallbacku do obrazów Allegro.

## [0.2.67] - 2026-05-28
- Zabezpieczono lokalne zapytania miniatur PrestaShop, aby błąd SQL fallbacku nie blokował pobierania danych Allegro.

## [0.2.66] - 2026-05-28
- Ustawiono miniatury PrestaShop jako pierwsze źródło w zgłoszeniach i zwrotach, z Allegro tylko jako fallbackiem.

## [0.2.65] - 2026-05-28
- Przywrócono szersze szukanie miniatur dla dyskusji, a blokadę katalogu produktów Allegro ograniczono do reklamacji.

## [0.2.64] - 2026-05-28
- Twardo odcięto katalogowe `productSet.product.images` dla miniatur reklamacji i dyskusji oraz przeniesiono cache zgłoszeń na nowe klucze bez starych wpisów po ofercie.

## [0.2.63] - 2026-05-28
- Miniatury reklamacji i dyskusji z `issue_id` nie korzystają już z katalogu produktów Allegro; loader dociąga chat zgłoszenia i szuka miniatury po zamówieniu lub ofercie z `relatesTo`.

## [0.2.62] - 2026-05-28
- Poprawiono formatowanie tekstu w modalu odmowy zwrotu pieniędzy: mniejsze nagłówki, ciaśniejsze odstępy i czytelniejsze opcje wyboru.

## [0.2.61] - 2026-05-28
- Miniatury reklamacji preferuja obraz z zamowienia lub oferty; katalog produktu Allegro jest uzywany dopiero jako ostatni fallback i nie nadpisuje cache zgłoszenia.

## [0.2.60] - 2026-05-28
- Lista zwrotow uzywa miniatury z pelnych szczegolow zaznaczonego zwrotu, aby miniatura po lewej byla taka sama jak w panelu szczegolow.

## [0.2.59] - 2026-05-28
- Fixed Polish characters in update changelog rendering by repairing UTF-8 mojibake before sending update notes to the browser.

## [0.2.58] - 2026-05-28
- Odfiltrowano adresy `api.allegro.pl` z miniatur produktów, aby przeglądarka nie ładowała chronionych zasobów API i nie pokazywała błędu `unauthorized`.

## [0.2.57] - 2026-05-28
- Ukryto natywną ikonkę uszkodzonego obrazka na liście dyskusji i reklamacji: każdy błąd ładowania miniatury przełącza teraz widok na placeholder modułu.

## [0.2.56] - 2026-05-28
- Poprawiono miniatury produktów w reklamacjach: lazy loader miniatur potrafi dociągnąć szczegóły zgłoszenia po `issue_id`, gdy lista Allegro nie zawiera identyfikatorów oferty lub zamówienia.

## [0.2.55] - 2026-05-28
- Ujednolicono kolor etykiety statusu `W toku` z etykietą `Dyskusja` na liście dyskusji.

## [0.2.54] - 2026-05-28
- Poprawiono miniatury produktów na liście dyskusji: moduł wyszukuje identyfikatory oferty, produktu i zamówienia także w zagnieżdżonych danych Allegro oraz zapisuje miniaturę pod wszystkimi dostępnymi kluczami cache.

## [0.2.53] - 2026-05-28
- Ukryto listę uprawnień tokena Allegro w ustawieniach modułu, pozostawiając informacje o połączonym koncie i ważności tokena.

## [0.2.52] - 2026-05-27
- Poprawiono wygląd panelu informacji o module: metadane są pokazane w kafelkach, pasek aktualizacji jest czytelniejszy, a lista zmian ma kompaktowy biały box zamiast dużego niebieskiego alertu.

## [0.2.51] - 2026-05-27
- Dodano bezpieczny górny odstęp panelu rozmów i reklamacji, aby sticky nagłówek PrestaShop nie ucinał pierwszego elementu listy ani nagłówka zgłoszenia.

## [0.2.50] - 2026-05-27
- Zbliżono mechanizm aktualizacji do CargoStockManager: panel aktualizacji pokazuje changelog dostępnej wersji, updater pobiera zakres zmian z `CHANGELOG.md`, a skrypt release zapisuje lokalny manifest wersjonowany i kopię changeloga.

## [0.2.49] - 2026-05-27
- Zmieniono nazewnictwo widoczne w module z autorespondera na `AllegroCustomerSupport` / `Obsługa Klienta Allegro`, pozostawiając techniczny identyfikator modułu bez zmian dla kompatybilności aktualizacji.

## [0.2.48] - 2026-05-27
- Poprawiono przewijanie panelu dyskusji/reklamacji: wewnętrzne listy nie przestawiają już wysokości całego widoku, a formularz odpowiedzi nie nakłada się jako osobna warstwa.

## [0.2.47] - 2026-05-27
- Dodano tłumaczenia angielskich powodów dyskusji dotyczących odmowy przyjęcia zwrotu przez sprzedającego.

## [0.2.46] - 2026-05-27
- Zmieniono nazwę modułu i głównej pozycji menu na `Obsługa Klienta Allegro`.

## [0.2.45] - 2026-05-27
- Dodano wybór gotowej wiadomości z aktywnych reguł autorespondera jako dropup obok przycisku wysyłki.

## [0.2.44] - 2026-05-27
- Ujednolicono kolory tytułów w timeline: wszystkie wykonane kroki mają niebieski kolor, nie tylko krok aktywny.

## [0.2.43] - 2026-05-27
- Zwiększono czytelność meta nagłówka zwrotu (`Zamówienie Allegro` / `Zamówienie w sklepie`) do 14px oraz pokazano powody zwrotu pieniędzy jako listę widoczną od razu (radio), bez listy rozwijanej.

## [0.2.42] - 2026-05-27
- Formularz odmowy zwrotu w modalu otrzymał dokładnie żądaną listę powodów (z opisami) oraz pole komentarza na dole, z mapowaniem do kodów API Allegro.

## [0.2.41] - 2026-05-27
- Dodano formularz `Odmowa zwrotu pieniędzy` w modalu i ujednolicono jego wygląd ze stylem modułu/PrestaShop.

## [0.2.40] - 2026-05-27
- Formularz zwrotu pieniędzy przeniesiono do modala i dodano wymagane pole `Powód zwrotu pieniędzy` zgodne z powodami Allegro.

## [0.2.39] - 2026-05-27
- Delikatnie poszerzono kolumnę `Zwrot środków` i zablokowano łamanie numeru konta bankowego na dwie linie.

## [0.2.38] - 2026-05-27
- Poprawiono status `COMMISSION_REFUND_CLAIMED`: nie oznacza już `Zwrot prowizji` ani `Zwrot wpłaty`; krok prowizji domyka się wyłącznie przy `COMMISSION_REFUNDED`.

## [0.2.37] - 2026-05-27
- Poprawiono wyznaczanie dat `Zwrot wpłaty` i `Zwrot prowizji`: gdy brakuje ich w szczegółach zwrotu, moduł używa danych rekordu zwrotu z listy (`statusChangedAt`/`updatedAt`) jako fallbacku.

## [0.2.36] - 2026-05-27
- Zmniejszono mniej więcej o połowę odstęp między etykietą menu a czerwoną plakietką licznika.

## [0.2.35] - 2026-05-27
- Ustawiono `Ustawienia` na końcu podmenu modułu i dodano czerwoną plakietkę z liczbą zwrotów do obsłużenia przy pozycji `Zwroty towarów`.

## [0.2.34] - 2026-05-27
- Usunięto fałszywe daty `Zwrot wpłaty` wyciągane z płatności oryginalnego zamówienia przy zwrotach, które nie zostały jeszcze zrefundowane.

## [0.2.33] - 2026-05-27
- Dla zwrotów bez przewoźnika i numeru przesyłki pole `Metoda dostawy` pokazuje teraz `Wysyłka własna`.

## [0.2.32] - 2026-05-27
- Poprawiono wykrywanie `Wysyłka własna`, aby opierało się na braku przewoźnika, numeru przesyłki i trackingu w danych zwrotu.

## [0.2.31] - 2026-05-27
- Dodano skrócony timeline dla `Wysyłka własna`, bez kroków transportowych między zgłoszeniem a zwrotem wpłaty.

## [0.2.30] - 2026-05-27
- Przeniesiono etykietę `FAKTURA` / `BEZ FAKTURY` z nagłówka do sekcji `Dane kupującego` i zmniejszono ją do rozmiaru tekstowego.

## [0.2.29] - 2026-05-27
- Dane kupującego w zwrocie pobierane są priorytetowo z zamówienia Allegro, a w nagłówku dodano etykietę `FAKTURA` / `BEZ FAKTURY`.

## [0.2.28] - 2026-05-27
- Podlinkowano `Zamówienie w sklepie` w nagłówku zwrotu do widoku zamówienia PrestaShop.

## [0.2.27] - 2026-05-27
- Uproszczono wyszukiwarkę zwrotów do jednego pola bez wyboru typu i dodano szerokie wyszukiwanie po numerach, przesyłkach, telefonach i danych kupującego.

## [0.2.26] - 2026-05-27
- Zmieniono tytuł podstrony zwrotów z `Zwroty` na `Zwroty towarów`.

## [0.2.25] - 2026-05-27
- Zmieniono nazwę pozycji menu `Zwroty` na `Zwroty towarów`.

## [0.2.24] - 2026-05-27
- Uproszczono meta nagłówka zwrotu do `Zamówienie Allegro` i `Zamówienie w sklepie`, bez loginu i daty.

## [0.2.23] - 2026-05-27
- Dodano login kupującego w sekcji `Dane kupującego` dla zwrotów.

## [0.2.22] - 2026-05-27
- Przycisk `Śledź na stronie przewoźnika` przełączono na domyślny styl `btn-primary` z BO zamiast własnego koloru.

## [0.2.21] - 2026-05-27
- Usunięto z listy zwrotów nick, numer zwrotu i numer zamówienia oraz przestano ucinać tytuły produktów.

## [0.2.20] - 2026-05-27
- Dodano w nagłówku zwrotu linkowane zamówienie Allegro oraz numer zamówienia PrestaShop obok linku do zwrotu.

## [0.2.19] - 2026-05-27
- Zmieniono link do zwrotu w Allegro Sales Center na wyszukiwanie po numerze zwrotu z parametrami `page`, `limit`, `from` i `search`.

## [0.2.18] - 2026-05-26
- Przeniesiono sumę `Razem` z sekcji `Zwrot środków` do dolnego panelu obok przycisku `Decyzja zwrotowa`.

## [0.2.17] - 2026-05-26
- Zmieniono przycisk zewnętrznego trackingu na `Śledź na stronie przewoźnika` i nadano mu niebieski styl.

## [0.2.16] - 2026-05-26
- Zwężono jeszcze bardziej okno modala trackingu.

## [0.2.15] - 2026-05-26
- Ułożono nagłówek modala trackingu tak, aby tytuł z numerem był po lewej, a przycisk zamknięcia po prawej.

## [0.2.14] - 2026-05-26
- Poprawiono polskie znaki w tłumaczeniach statusów trackingu w modalu przesyłki.

## [0.2.13] - 2026-05-26
- Przeniesiono przycisk `Pokaż API` pod timeline statusów zwrotu.

## [0.2.12] - 2026-05-26
- Zwężono okno modala trackingu, aby lepiej pasowało do szerokości historii przesyłki.

## [0.2.11] - 2026-05-26
- Nagłówek modala trackingu pokazuje teraz tytuł, numer przesyłki i przewoźnika w jednym wierszu.

## [0.2.10] - 2026-05-26
- Dodano polskie tłumaczenia trackingu i wyrenderowano historię w modalu w tym samym stylu co timeline zwrotu.

## [0.2.9] - 2026-05-26
- Dla `INPOST` numer `waybill` również otwiera modal z trackingiem z API, z przyciskiem do strony przewoźnika.

## [0.2.8] - 2026-05-26
- Dla przesyłek `ALLEGRO` preferowany jest allegrowy numer `waybill` jako główne źródło trackingu i linkowania.

## [0.2.7] - 2026-05-26
- Modal trackingu działa teraz tylko dla przesyłek `ALLEGRO`, a pozostali przewoźnicy otwierają zewnętrzne śledzenie.

## [0.2.6] - 2026-05-26
- Numer przesyłki w zwrocie otwiera teraz modal z historią trackingu z API, z fallbackiem do zewnętrznego śledzenia.

## [0.2.5] - 2026-05-26
- Tracking zwrotu próbuje teraz zarówno par `transportingCarrierId + transportingWaybill`, jak i `carrierId + waybill`, a `ALLEGRO` linkuje do publicznego śledzenia Allegro Delivery.

## [0.2.4] - 2026-05-26
- Diagnostykę API zwrotu przeniesiono z widoku szczegółów do modala otwieranego przyciskiem `Pokaż API`.

## [0.2.3] - 2026-05-26
- `Nadany` może teraz być wyliczany z pierwszego `IN_TRANSIT` w historii trackingu, jeśli po nim pojawiały się `PENDING`.

## [0.2.2] - 2026-05-26
- Timeline zwrotu koloruje teraz tylko kroki z realnymi datami zamiast zakładać wykonanie po samym statusie końcowym.

## [0.2.1] - 2026-05-26
- Dodano link diagnostyczny przy timeline zwrotu i podgląd surowej odpowiedzi API dla wybranego zwrotu.

## [0.2.0] - 2026-05-26
- Usunięto fallback `PENDING` dla kroku `Nadany`, żeby nie udawać nadania przy samym zgłoszeniu zwrotu.

## [0.1.200] - 2026-05-26
- Ograniczono wykrywanie dat `Nadany` do rzeczywistych historii statusu i trackingu, bez kopiowania z pierwszej przesyłki.

## [0.1.199] - 2026-05-26
- Poszerzono wykrywanie dat statusów w timeline zwrotu i dodano bezpieczny fallback tylko dla aktywnego kroku.

## [0.1.198] - 2026-05-26
- Usunięto kopiowanie dat na kroki bez własnego statusu w timeline zwrotu.

## [0.1.197] - 2026-05-26
- Dodano biały odstęp także przy szarych punktach timeline'u zwrotu.

## [0.1.196] - 2026-05-26
- Dopięto fallback dat w timeline zwrotu i dodano obramowanie punktu, aby linia odcinała się od markera.

## [0.1.195] - 2026-05-26
- Ujednolicono kolor aktywnego punktu timeline'u i kolorowanie linii między wykonanymi krokami zwrotu.

## [0.1.194] - 2026-05-26
- Uaktywniono zlecanie zwrotu pieniędzy z poziomu decyzji zwrotowej Allegro.

## [0.1.193] - 2026-05-26
- Poprawiono menu "Decyzja zwrotowa", aby otwierało się nad przyciskiem w dolnym panelu.

## [0.1.192] - 2026-05-26
- Poprawiono wykrywanie imienia i nazwiska kupującego, format telefonu oraz linki śledzenia do stron przewoźników.

## [0.1.191] - 2026-05-26
- Poprawiono wygląd pionowego timeline'u zwrotu oraz wykrywanie dat zwrotu wpłaty i prowizji.

## [0.1.190] - 2026-05-26
- Poprawiono dane kupującego, linkowanie e-maila i numeru śledzenia oraz miniatury produktów w widoku zwrotu.

## [0.1.189] - 2026-05-26
- Dodano czytelne tłumaczenie powodu zwrotu `NONE` oraz dodatkowe pola opisu powodu zwrotu.

## [0.1.188] - 2026-05-26
- Uproszczono szczegóły zwrotu do najważniejszych danych: produkty, status, kupujący, dostawa, adres zwrotu, zwrot środków i suma.

## [0.1.187] - 2026-05-26
- Poprawiono zapamiętywanie filtrów zwrotów przy przechodzeniu między pozycjami, odświeżaniu i paginacji.

## [0.1.186] - 2026-05-26
- Poprawiono link do zwrotu w Allegro Sales Center, aby używał bezpośredniej ścieżki po id zwrotu.

## [0.1.185] - 2026-05-26
- Zmieniono menu "Decyzja zwrotowa" na standardowy styl przycisku i dropdownu PrestaShop.

## [0.1.184] - 2026-05-26
- Uzupełniono timeline zwrotu o daty z historii śledzenia przesyłki zwrotnej.

## [0.1.183] - 2026-05-26
- Dodano przycisk "Decyzja zwrotowa" z menu decyzji w szczegółach zwrotu.

## [0.1.182] - 2026-05-26
- Dodano poziomy timeline statusu zwrotu w szczegółach zwrotu.

## [0.1.181] - 2026-05-26
- Uporządkowano pasek filtrów w zakładce "Zwroty".
- Dodano domyślny filtr daty zwrotów z ostatnich 90 dni oraz wybór zakresu dat.

## [0.1.180] - 2026-05-26
- Dodano zakładkę "Zwroty" z listą, filtrami i szczegółami zwrotów klienckich Allegro.
- Dodano obsługę odmowy zwrotu przez API Allegro.

## [0.1.179] - 2026-05-14
- Wymuszono odświeżenie zakładek modułu i nazwę "Reklamacje" w menu BO po aktualizacji.

## [0.1.178] - 2026-05-14
- Dodano preloader rozmowy przy przełączaniu pozycji na listach wiadomości, dyskusji i reklamacji.
- Usunięto efekt przygaszenia okna rozmowy podczas ładowania kolejnej pozycji.

## [0.1.177] - 2026-05-13
- Rozdzielono widoki menu: "Dyskusje" pokazują tylko dyskusje, a "Reklamacje" tylko reklamacje.

## [0.1.176] - 2026-05-13
- Zmieniono etykietę pozycji menu "Reklamacje i dyskusje" na "Reklamacje".

## [0.1.175] - 2026-05-13
- Naprawiono błąd odpowiedzi AJAX przy sprawdzaniu aktualizacji modułu.

## [0.1.174] - 2026-05-13
- Poprawiono rozwijanie i aktywny stan menu modułu w Back Office.
- Ustawienia modułu renderują się teraz przez własny kontroler menu zamiast przekierowania do listy modułów.

## [0.1.173] - 2026-05-13
- Poprawiono AJAX ręcznego sprawdzania aktualizacji w konfiguracji modułu.
- Przeniesiono panel informacji o module nad ustawienia ogólne.

## [0.1.172] - 2026-05-13
- Zmieniono działanie ręcznego sprawdzania aktualizacji na AJAX-owy mechanizm jak w Cargo Stock Manager.
- Ten sam przycisk po wykryciu dostępnej wersji przełącza się w instalację aktualizacji.

## [0.1.171] - 2026-05-13
- Dopasowano rozmiar tekstu i przycisków w panelu informacji o module do reszty konfiguracji.

## [0.1.170] - 2026-05-13
- Przebudowano panel aktualizacji na widok "Informacje o module" w stylu Cargo Stock Manager.
- Dodano wybór kanału aktualizacji i przycisk zapisu bezpośrednio przed ręcznym sprawdzaniem aktualizacji.

## [0.1.169] - 2026-05-13
- Dodano awaryjne pobieranie manifestu aktualizacji przez GitHub API.
- Doprecyzowano komunikaty błędów sprawdzania aktualizacji.

## [0.1.168] - 2026-05-13
- Poprawiono wyrównanie kontrolek w panelu aktualizacji modułu.
- Ujednolicono rozmiar tekstu w bloku statusu połączenia konta Allegro.

## [0.1.167] - 2026-05-13
- Dodano podpisany mechanizm aktualizacji modułu przez publiczne repo buildów.
- Dodano panel sprawdzania i instalowania aktualizacji w konfiguracji modułu.
- Dodano konfigurację prywatnego repo źródłowego i publicznego repo buildów.
