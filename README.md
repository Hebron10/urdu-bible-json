# Urdu Bible JSON API

Structured JSON dataset generated from the uploaded WordProject Urdu Bible HTML package.

## Structure

- `books.json` — book metadata and chapter lists
- `<BOOK_CODE>/<chapter>.json` — chapter data with one object per verse

Example:

`PYD/1.json`

Each chapter has:

```json
{
  "translation": "WordProject Urdu Bible",
  "language": "ur",
  "direction": "rtl",
  "book_code": "PYD",
  "book": "Pyaidaish",
  "chapter": 1,
  "verses": [
    {"verse": 1, "text": "..."}
  ]
}
```

## GitHub Pages

This repository can be served as static JSON through GitHub Pages. A client can request:

`https://hebron10.github.io/urdu-bible-json/PYD/1.json`

after GitHub Pages is enabled for this repository.

## Data note

Verse text is preserved from the supplied HTML. Blank verse entries in the source are left blank rather than fabricated or substituted.
