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
- `tools/`: pomocne PowerShell skripte za build, update i test pokretanje

## Lokalni razvoj

Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install --upgrade pip
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

Pokretanje aplikacije:

```powershell
.\.venv\Scripts\python.exe .\main.py
```

Pokretanje testova:

```powershell
.\.venv\Scripts\python.exe -m pytest
```

Ako u Codex sandbox okruzenju standardni `pytest` cleanup pravi problem, koristi:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File .\tools\run_pytest_codex.ps1
```

## Dependency fajlovi

- `requirements.txt`: jedini dependency fajl za lokalni development, CI i Codex okruzenje
- fajl je pinovan na konkretne verzije da bi setup bio sto reproduktivniji na oba racunara

## Napomene

- Veliki i binarni backup fajlovi ne treba da budu u ovom source repou.
- Lokalni sekretni fajlovi kao `client_secret.json`, `token.json` i slicno treba da ostanu van verzionisanog koda ili pod `.gitignore`.
- `pyproject.toml` trenutno centralizuje pytest i Ruff konfiguraciju.
