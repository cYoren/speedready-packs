# Speedready dictionaries

Word-by-word dictionaries for the [Speedready](https://github.com/cYoren/speedready) web, Android and iOS reader:
one file per language pair, `dict-<book language>-<your language>.json.gz`, for English, German, Spanish, French,
Italian, Portuguese, Dutch, Polish, Russian and Swedish in every combination. The app downloads only the pair a
reader needs, once, and keeps it offline.

Built by `tools/export_web.py` in the Speedready repository from the published gloss packs.
Data: Wiktionary (via kaikki.org) under CC BY-SA 4.0, FrequencyWords under MIT. See DATA-LICENSES.md in Speedready.

## Noun genders and the book catalog

`genders-<language>.json.gz` is the der/die/das colouring data for German, Spanish, French, Italian, Dutch,
Polish, Portuguese, Russian and Swedish, and `catalog.json.gz` is the public-domain book catalog the reader
searches when you open a downloadable book.

The browser extension does not bundle them: it fetches the one language it needs, and the catalog on first
search, from this repository and keeps them in IndexedDB. That keeps the store package small.
