# EMAnalyzer

Desktop aplikacija za proracun elektromagnetnih polja i procenu uticaja na zivotnu sredinu.

## Struktura projekta

- `main.py`: ulazna tacka aplikacije i startup orkestracija
- `gui/`: Qt prozori, dockovi i splash/update UI
- `lokacija/`: rad sa lokacijom, elevacijom i map prikazom
- `izvori/`: modeli i UI za izvore polja
- `objekti/`: modeli i UI za objekte i spratove
- `proracun/`: proracunska logika i eksport/interop pomocni moduli
- `rezultati/`: prikaz i obrada rezultata
- `funkcije/`: zajednicke pomocne funkcije
- `utils/`: konfiguracija, licenca, update i startup helperi
- `tests/`: automatizovani testovi
- `tools/`: pomocne PowerShell skripte za build, update i test pokretanja
