# JumpAnime extensions

Source descriptions for JumpAnime. An extension is a small JSON file, not code. The app reads it and does the fetching.

## Manga extension

```json
{
  "apiVersion": 1,
  "type": "manga",
  "id": "en.example",
  "name": "Example",
  "version": "1.0.0",
  "baseUrl": "https://example.com",
  "engine": "madara",
  "options": {}
}
```

`engine` is `madara` or `mangathemesia`, the two WordPress themes the app understands. `options` can override any of these selectors:

| Option | Meaning |
|---|---|
| `searchUrl` | Search address. `{base}` and `{q}` are filled in. |
| `searchItem` | CSS selector for one search result. |
| `searchLink` | Selector for the link inside a result. |
| `chapterItem` | Selector for one chapter row. |
| `chapterLink` | Selector for the link inside a chapter row. |
| `chapterName` | Selector for the chapter name inside a row. |
| `chaptersAjax` | `true` if chapters load from `/ajax/chapters/`. |
| `pageItem` | Selector for the page images in a chapter. |

Bump `version` after a change so installed copies update.

## Adding a source in the app

Manga → open a title → Manage sources → Store, or paste a link to your JSON file.

Add new files under `manga/` and list them in `manga/index.json`.
