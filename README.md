# Sticker Bench

A free, single-file sticker maker that runs entirely in your browser — no server, no upload, no install.

Frame a photo, auto-remove the background, add a caption, and export a sticker sized and formatted correctly for **WhatsApp, Telegram, Signal, iMessage, Discord, or Facebook Messenger**.

## Use it

**Option 1 — GitHub Pages (recommended, gives you a shareable link):**
1. In this repo, go to **Settings → Pages**.
2. Under "Build and deployment", set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Save. GitHub will publish it at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

**Option 2 — Download and open locally:**
1. Click `index.html` in this repo, then the **Download raw file** button.
2. Open the downloaded file in any browser (double-click it — no server needed).

## Features

- **Auto background removal** — flood-fills in from the corners to cut out a plain/solid backdrop
- **Die-cut white outline** — traces the transparent edges like a real sticker
- **Caption text** — add a title with fill + outline colors
- **Platform presets** — correct size, format (WebP/PNG), and file-size target for each app
- **Sticker pack tray** — build multiple stickers and download them all as a `.zip`

## Limitations

- Background removal is color-based (corner flood-fill), not AI subject detection — works best against a plain backdrop, not busy scenes.
- Only makes **static** stickers. Animated sticker packs (Telegram/Discord) need a different tool.
- This produces sticker-ready image files — actually publishing a pack to iMessage or Discord still goes through that platform's own app/developer tools.

## License

MIT — do whatever you'd like with it.
