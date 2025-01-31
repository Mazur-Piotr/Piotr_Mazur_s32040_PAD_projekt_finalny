# Analiza cen ofertowych mieszkań w Warszawie

## Opis projektu

Projekt ma na celu analizę cen ofertowych mieszkań w Warszawie oraz opracowanie modelu, który pozwoli przewidywać, czy cena mieszkania jest przeszacowana, adekwatna, czy jest okazją na tle median cen rynkowych.

## Zawartość

- Zbieranie danych – Web scraping ofert sprzedaży mieszkań z serwisu Otodom.pl.
- Czyszczenie i eksploracja danych – Konwersja typów, usunięcie błędnych wartości, wstępna analiza statystyczna.
- Przygotowanie etykiet – Przypisanie etykiet na podstawie median cen transakcyjnych dla dzielnic Warszawy.
- Modelowanie – Użycie Drzewa Decyzyjnego do przewidywania klasy cenowej.
- Ewaluacja modelu – Analiza skuteczności predykcji za pomocą metryk klasyfikacyjnych i macierzy pomyłek.
- Wizualizacja wyników – Histogramy, wizualizacja drzewa decyzyjnego.

## Dane wejściowe

Dane pochodzą z serwisu Otodom.pl i zostały pobrane za pomocą web scraping.

Zebrane dane zawierają 1151 mieszkań opisanych przez 17 cech (np. powierzchnia, liczba pokoi, lokalizacja, rok budowy).
Dane są wzbogacone o medianę cen transakcyjnych dla danej dzielnicy, na podstawie której przypisano etykiety:
"Przeszacowana" – cena o 20% wyższa od mediany
"Adekwatna" – cena w przedziale ±20% mediany
"Okazja" – cena o 20% niższa od mediany

## Technologie

Python:

Pandas, NumPy – przetwarzanie danych

BeautifulSoup, Requests – web scraping

Scikit-learn – modelowanie (Drzewa Decyzyjne, GridSearchCV)

Matplotlib – wizualizacja

## Wyniki modelowania

### Najlepszy model: Drzewo Decyzyjne, optymalizowane GridSearchCV

Dokładność modelu: ok. 96% dla klasy „Przeszacowana”

Problem z klasą "Okazja" – niewielka liczba przykładów w zbiorze

## Wizualizacje

Histogramy rozkładu cen i cech mieszkań

Macierz pomyłek klasyfikacji

Wizualizacja drzewa decyzyjnego

## Uruchomienie

Zainstaluj wymagane biblioteki:
pip install requests beautifulsoup4 pandas scikit-learn matplotlib

Uruchom notebook.
Przeanalizuj zebrane dane, wytrenuj model i sprawdź jego skuteczność.

### Autor: Piotr Mazur s32040

Źródło danych: Otodom.pl | Podkluczyk.pl
