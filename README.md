# agataubezpiecza.pl — kod strony

Statyczna strona (czysty HTML/CSS/JS, bez frameworków i bez procesu budowania).
Gotowa do wgrania bezpośrednio na GitHub Pages.

## Struktura plików

```
index.html                   Strona główna
o-mnie.html                  O mnie
oferta.html                  Oferta / usługi
opinie.html                  Opinie klientów
faq.html                     Najczęściej zadawane pytania
kontakt.html                 Kontakt (telefon + e-mail, bez formularza)
polityka-prywatnosci.html    Polityka prywatności (RODO)
404.html                     Niestandardowa strona błędu
robots.txt                   Zasady dla robotów wyszukiwarek
sitemap.xml                  Mapa strony dla wyszukiwarek
CNAME                        Domena własna dla GitHub Pages
assets/css/style.css         Cały system stylów (kolory, typografia, komponenty)
assets/js/nav.js             Rozwijanie menu mobilnego (bez śledzenia, bez cookies)
assets/fonts/                Czcionki Fraunces i Work Sans (self-hosted, open source, OFL)
assets/img/favicon.svg       Ikona strony
```

## Jak wdrożyć (bez SSH — przez przeglądarkę)

1. Wejdź na swoje repozytorium na GitHub (`agataubezpiecza`).
2. Kliknij **Add file → Upload files**.
3. Przeciągnij i upuść **całą zawartość** tego folderu (nie sam folder — jego zawartość, żeby `index.html` znalazł się w głównym katalogu repozytorium).
4. Zatwierdź commit (przycisk **Commit changes**).
5. W ustawieniach repozytorium: **Settings → Pages** — upewnij się, że custom domain to `agataubezpiecza.pl` i że opcja "Enforce HTTPS" jest włączona (może się pojawić dopiero po kilku minutach od wgrania pliku CNAME).

## Co trzeba uzupełnić przed publikacją

Poniższe miejsca w kodzie są oznaczone jako **do uzupełnienia** — strona zadziała bez tego, ale nie powinna iść na żywo, dopóki tego nie zmienisz:

- [ ] **Numer telefonu** — obecnie placeholder `+48 XXX XXX XXX` / `tel:+48000000000` w: `index.html`, `o-mnie.html`, `oferta.html`, `opinie.html`, `faq.html`, `kontakt.html`, `polityka-prywatnosci.html`, `404.html` (stopka).
- [ ] **Adres e-mail** — obecnie sugerowany `kontakt@agataubezpiecza.pl`. Sprawdź, czy ta skrzynka istnieje i działa (masz hosting e-mail na home.pl).
- [ ] **Liczba lat doświadczenia i liczba klientów** — pasek zaufania na stronie głównej (`index.html`, sekcja `trust-bar`), oznaczone jako `[X] lat` i `[XX]+`.
- [ ] **Historia / o mnie** — `o-mnie.html`, akapity w nawiasach kwadratowych.
- [ ] **Prawdziwe opinie klientów** — `opinie.html` i skrócona wersja w `index.html`. Każda opinia oznaczona jest etykietą „Przykładowa opinia — do zamiany"; usuń tę etykietę przy prawdziwych opiniach.
- [ ] **Polityka prywatności** — `polityka-prywatnosci.html`: data publikacji, pełne dane rejestrowe firmy (NIP/REGON jeśli dotyczy), okres przechowywania danych. **Zalecana konsultacja z prawnikiem przed publikacją** — branża ubezpieczeniowa jest regulowana.
- [ ] **Zdjęcia** — obecnie miejsca na zdjęcia to stylizowane placeholdery (bez prawdziwej fotografii). Podmień je, gdy będziesz mieć gotowe zdjęcia.

## Edycja FAQ i opinii

Oba pliki (`faq.html`, `opinie.html`) mają w kodzie komentarz z instrukcją "jak dodać / zmienić / usunąć" —
wystarczy skopiować/wkleić/usunąć cały blok jednego pytania lub jednej opinii.

## Uwagi techniczne

- Brak plików cookie, brak Google Analytics, brak zewnętrznych skryptów śledzących.
- Brak formularza kontaktowego — kontakt wyłącznie przez `tel:` i `mailto:`.
- Czcionki (Fraunces, Work Sans) są hostowane lokalnie w `assets/fonts/` — żadne zapytania do Google Fonts nie są wysyłane.
- Strona jest w pełni statyczna — nie wymaga PHP, bazy danych ani procesu budowania.
