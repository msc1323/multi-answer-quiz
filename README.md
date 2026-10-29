# Multi-answer Quiz

Önálló, kliensoldali webapp több helyes válasszal rendelkező kérdések szerkesztéséhez és kitöltéséhez.

## Használat

Nyisd meg az `index.html` fájlt egy modern böngészőben. Az adatok a böngésző `localStorage`-ában maradnak.

## Szerkesztő

- Kérdések és válaszlehetőségek hozzáadása/szerkesztése/törlése
- Több helyes válasz megjelölése
- JSON és CSV import
- JSON export
- Élő előnézet

## Játék mód

A **Játék indítása** gombbal a mentett, játszható kérdések véletlenszerű sorrendben jelennek meg.

- Egy kérdésnél több válasz is kijelölhető.
- A kérdés **1 pontot ér**, ha a játékos pontosan az összes helyes választ jelöli meg.
- Ellenőrzéskor a helyes, hibás és kihagyott opciók külön jelölést kapnak.
- A végén megjelenik az összpontszám, hibás/helyes kérdések száma és a százalékos eredmény.
- Az **Újra ugyanaz a kvíz** gomb újraindítja a teljes kérdéssort új sorrendben.

## Import

### JSON
```json
[
  {
    "question": "Melyik a helyes?",
    "answers": [
      {"text": "A válasz", "correct": true},
      {"text": "B válasz", "correct": false},
      {"text": "C válasz", "correct": true}
    ]
  }
]
```

### CSV
Fejléc:
```csv
question,answer,correct
```
Egy kérdés több sorban szerepelhet; a `correct` értéke lehet például `true`, `1`, `igen`, `x`.
