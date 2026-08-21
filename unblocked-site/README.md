# Games Site

Minimal, self-hosted games hub. Drop in open-source HTML games and they show up as boxes on the homepage.

## Adding a game

1. Make a new folder inside `games/`, named after the game (e.g. `games/2048/`).
2. Put the game's files in there. It needs an `index.html` at the root of that folder — if the game came as a zip with `index.html` + assets, just dump the whole thing in.
3. Open `games.js` and add one entry:

```js
{
  title: "2048",
  folder: "2048",
  thumb: "" // optional, path to an image, e.g. "games/2048/thumb.png"
}
```

That's it — refresh the homepage and the box appears automatically, with search working too.

## Notes

- If a game uses relative paths for its assets (css/js/images), it'll work fine as long as everything lives inside that game's own folder.
- If a game is a single HTML file with everything inlined, just name it `index.html` and drop it directly in its folder.
- No thumbnail? It'll fall back to a placeholder box automatically.
- To run locally: any static file server works, e.g. `python3 -m http.server` from this folder, then visit `localhost:8000`.
