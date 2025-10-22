### Izmene v20251020-0754

• Izmenjen dijalog za dodavanje i izmenu izvora.
Omogućeno je selektivno prikazivanje sektora na sceni, sinhronizovano sa komandnim dugmićima za prikaz. Dodata su nova dugmad za pozicioniranje, prikaz i brisanje sektora, kao i dugmad za izbor paterna, otvaranje foldera sa paternima, pregled paterna i brisanje sistema.

• Omogućena selekcija sektora na sceni sa kontekst menijem (desni klik).
Na selektovani sektor moguće je primeniti opcije za pozicioniranje, uklanjanje iz prikaza na sceni i brisanje selektovanog sektora.
Sektori različitih operatora sada se prikazuju različitim bojama.
Omogućeno je podešavanje providnosti simbola sektora („trouglića“) preko Podešavanja → tab Prikaz → opis elementa „Simbol izvora površina [operator]“, izborom vrednosti u koloni Debljina linije.
Izbor vrednosti 0.25 / 0.5 / 0.75 / ≥1 podešava providnost (opacity) površine trouglića na 25% / 50% / 75% / 100%, respektivno. Veća vrednost znači manju providnost.

• Dodato dugme „Halo prikaz“ u toolbar glavnog prozora.
Kada je aktiviran, linije i tekst na sceni prikazuju se sa slojem druge, kontrastne boje ispod — čime se postiže bolja preglednost i vidljivost elemenata nad ortofoto podlogom.
Izbor „halo“ boje nalazi se u Podešavanja → tab Prikaz → opis elementa „Halo efekat“.
Preporučuje se da „halo“ boja bude kontrastna u odnosu na boje objekata i izvora — ako su boje tamne, „halo“ treba da bude svetla (najbolje bela), a ako su svetle, „halo“ treba da bude tamnija (najbolje crna).
Debljina „halo“ senke ispod linija i teksta podešava se izborom vrednosti u koloni Debljina linije u istom tabu.
Napomena: „Halo prikaz“ se ne čuva u projektnom Excel fajlu — to je privremena vizuelna opcija za prikaz na sceni i na plotovima rezultata proračuna.

• Rešen eksport PNG trenutnog prikaza na sceni — sada uključuje i legendu (ukoliko postoji, kao kod prikaza elevacija).

• Izmenjen prikaz elevacija (dupli klik na polje „Elevacije“ u dock-u Podaci o lokaciji).
Podešen je vektorski raster sa boljim kontrastom boja za prikaz pada terena, a oznake elevacija su prilagođene tako da budu vidljive i na manjim ortofoto snimcima i pri zoom-out prikazu.

• Optimizovan proračun elevacija za objekte i izvore — sada sa kraćim odzivom dijaloga pri dodavanju objekata.
Centralizovane su funkcije za izračunavanje elevacija iz keša (podatke sa Google Elevation API-ja program povlači samo prilikom kreiranja ili georeferenciranja ortofoto snimka).
Za objekte se uzima najniža tačka iz elevacionog grida koja pripada poligonu objekta; ako ni jedna tačka ne pripada poligonu, uzima se najniža od četiri najbliže tačke.
Za izvore — ako se izvor nalazi na objektu, koristi se elevacija objekta; u suprotnom, uzima se najbliža tačka iz elevacionog grida.

• Dodate opcije „Ažuriraj elevacije za sve izvore“ i „Ažuriraj elevacije za sve objekte“ (desni klik na tabele u dock-ovima).
Pošto je sada omogućen i ručni unos elevacija, ručno unete vrednosti ostaju sačuvane sve dok se ne uradi pojedinačno ažuriranje ili globalno ažuriranje koje povlači vrednosti iz keša i zamenjuje ručno unete.
Važno: zbog promene algoritma za proračun elevacija, preporučuje se da se po učitavanju starih projekata (kreiranih u ranijim verzijama programa) obavezno uradi ažuriranje elevacija za sve objekte i sve izvore.

• Omogućeno brisanje selektovanog objekta pomoću tastera Delete na tastaturi (uz iskačući prozor za potvrdu).

• Unapređena validacija oznaka objekata.
Sprečeno je dupliranje oznaka i brojeva objekata.
Ako se objekat obriše, broj obrisanog objekta dodeljuje se prvom sledećem novom objektu.
U slučaju pokušaja ručnog unosa oznake koja već postoji, program prikazuje upozorenje i automatski predlaže prvi slobodan broj.
Dodata je i validacija da svaki objekat mora imati numerički deo oznake.

• Podešen slajder „Transparentnost slojeva“ u dock-u Proračun.
Slajder direktno menja vidljivost ortofoto snimka od 0% do 100% — pri 0% ortofoto se ne vidi uopšte, a pri 100% je potpuno vidljiv (bez prozirnosti).
Vrednosti između se koriste u zavisnosti od specifične lokacije i kontrasta ortofoto snimka.
Slajder ne utiče na raster rezultata za zonu povećane osetljivosti (ZPO) — oni su uvek prikazani punom bojom, dok utiče na raster rezultata za javno područje (JP), ali komplementarno u odnosu na vidljivost ortofoto snimka.
Maksimalna providnost JP rastera ograničena je na 50%.
Na primer:

          - Slajder 0%   → Ortosnimak 0% (nevidljiv)  → ZPO raster 100% (neproziran) → JP raster 100%
          - Slajder 20%  → Ortosnimak 20%             → ZPO raster 100%               → JP raster 80%
          - Slajder 30%  → Ortosnimak 30%             → ZPO raster 100%               → JP raster 70%
          - Slajder 60%  → Ortosnimak 60%             → ZPO raster 100%               → JP raster 50% (donji limit)
          - Slajder 100% → Ortosnimak 100%            → ZPO raster 100%               → JP raster 50% (donji limit)


### Izmene v20251014-0048

• Dodato dugme za Eksport PNG trenutnog prikaza na sceni

• Izmena prikaza izvora na sceni (simbol sektora - trougao, unija kružnica za dislocirane sektore istog izvora, izbor dimenzije kružnica...)

• Obrisano polje ElTilt koje se ne koristi jer se električni tilt uzima iz antena paterna.

• Sređeni indeksi slojeva na nivou aplikacije čime je obezbeđen pravilan redosled slojeva.



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

•	Prikaz verzije iz version.txt u naslovu aplikacije (npr. v20251007-0802).

•	Auto-update: klijent proverava manifest.json sa GitHub Releases i, uz potvrdu korisnika, preuzima i primenjuje novi ZIP (korišćen pomoćni EMUpdater.exe).
