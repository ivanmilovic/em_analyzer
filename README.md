### Izmene v20251013-0127

• Generisanje fajlova svakog proračuna u poseban "batch" podfolder sa datumom i vremenom generisanja i izabranim faktorom refleksije (ukoliko je bez faktora slabljenja materijala upisuje sufiks "_no_att").

• Dodata legenda i opis svakog PNG plota



### Izmene v20251009-0248

• Ograničena dimenzija Google Map prozora na dimenziju scene, ispis dimenzije u zaglavlju i toolbar-u, podesiva Custom skala i strelica severa.

• Dijalog "Idi na lokaciju" pamti inicijalni unos koji ne prolazi validaciju i vraća ga na ispravku.

• Rešeno čuvanje pozicija oznaka objekata, izvora i strelice severa u projektnom excel fajlu i učitavanje iz excel-a.

• Podešeno čitanje glavne ikone programa kao ikone svih prozora i dijaloga.



### Izmene v20251007-0802

•	Desktop aplikacija, buildovana PyInstaller-om kao one-folder paket.

•	Učitavanje lokacija\map.html i prikaz mape unutar aplikacije.

•	Učitavanje šifarnika iz foldera podesavanja\ (CSV).

•	Prikaz verzije iz version.txt u naslovu aplikacije (npr. {{TAG}}).

•	Auto-update: klijent proverava manifest.json sa GitHub Releases i, uz potvrdu korisnika, preuzima i primenjuje novi ZIP (korišćen pomoćni EMUpdater.exe).
