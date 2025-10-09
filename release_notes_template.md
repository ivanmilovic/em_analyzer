### **EM Analyzer {{TAG}} - Testerski build**

Status: Pre-release (ograničen krug testera)
Cilj: Validacija osnovne funkcionalnosti aplikacije, procesa buildovanja i mehanizma automatskog update-a.
________________________________________

### Šta testirati (prioriteti)
1.	Pokretanje bez konzolnog prozora; proveri da je verzija u naslovu {{TAG}}.
2.	Učitavanje i prikaz lokacija\map.html i kreiranje projekta
3.	Unos ulaznih podatka, učitavanje šifarnika iz 'podesavanja' i pravilno punjenje UI elemenata.
4.	Stabilnost osnovnih tokova (bez crash-a).
5.	Verifikacija metode proračuna E-polja i faktora izloženosti
6.	Verifikacija rezultata proračuna (tabelarni i grafički rezultati)
7.	Auto-update scenario (vidi „Kako testirati update“).

### Poznata ograničenja
•	Nema instalera (portable ZIP); aplikaciju pokretati iz raspakovanog foldera.
•	SmartScreen/AV može prijaviti nepoznat binarni fajl (nema code-signing potpisa u ovoj fazi).
•	Osnovno logovanje/alerting (MessageBox); bez automatskog slanja crash izveštaja.

### Sistemski zahtevi
•	Windows 10/11 (x64), bez administratorskih prava.
•	Preporučeno: 8 GB RAM.

### Instalacija (prvi put)
1.	Preuzmi ZIP: EM_Analyzer_{{TAG}}_win64.zip
2.	Raspakuj u npr. C:\Users\<ime>\Apps\EM_Analyzer\
3.	Pokreni EM Analyzer\EM Analyzer.exe

### Kako testirati update
1.	Pokreni aplikaciju (naslov treba da prikazuje {{TAG}}).
2.	Kada izađe sledeći release, pojaviće se dijalog „Update dostupan“.
3.	Potvrdi; aplikacija će se zatvoriti, EMUpdater.exe će primeniti ZIP, pa će se app ponovo startovati sa novom verzijom.

### Provera integriteta
•	ZIP SHA256: {{SHA256}}

### Troubleshooting
•	SmartScreen/AV: „More info” → „Run anyway“ ili dodaj izuzetak za folder.
•	„Ne može da zameni fajl“ pri update-u: uveri se da je app zatvoren; sačekaj 10–15 s (AV skeniranje) i pokreni ponovo.
•	Map.html se ne vidi: proveri da lokacija\map.html postoji u podfolderu pored exe-a.
•	Šifarnici se ne učitavaju: proveri da podesavanja\ postoji i sadrži očekivane CSV fajlove.

### Napomene za testere
•	Prilikom prijave buga obavezno navedi tačnu verziju ({{TAG}}) i priloži screenshot/korake.

### Asseti uz release
•	EM_Analyzer_{{TAG}}_win64.zip — aplikacija (portable)
•	manifest.json — meta za autoupdate (verzija, URL, SHA256)






