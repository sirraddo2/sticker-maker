# Sticker Maker

An installable, offline-capable app for turning photos into stickers — background removal, manual touch-up, a die-cut outline effect, and correctly-sized export for every major chat platform.

## Features
- **Background removal** — one-tap cutout using a flood-fill algorithm that starts from the image edges (samples the corner color, then removes matching background connected to the border). Unlike a simple "remove any pixel of this color" approach, it won't eat similar-colored regions *inside* your subject (like a white shirt) as long as they're not touching the frame edge.
- **Touch-up brush** — Erase or Restore, with adjustable brush size, for cleaning up edges the automatic cutout missed.
- **Die-cut outline** — adjustable color and width, the classic white (or any color) border around a sticker.
- **Auto-crop & center** — automatically crops to your subject's actual content before fitting it into the export size, so you don't waste resolution on empty transparent space.
- **Platform export presets**, sized against each platform's current published specs:
  - **WhatsApp** — 512×512px, 16px safe margin, WebP (100KB target)
  - **Telegram** — 512×512px, PNG or WebP (512KB limit)
  - **Signal** — 512×512px, 16px safe margin
  - **iMessage** — 618×618px (Apple's "large" sticker size)
  - **Discord Sticker** — 320×320px (512KB limit)
  - **Discord Emoji** — 128×128px (256KB limit)
  - **Messenger** — 512×512px (no strict published spec; this is a safe general default)

## Honest limitations
- This creates correctly-sized sticker **image files** — it does not connect to WhatsApp/Telegram/etc., publish a sticker pack, or complete each platform's specific import process. Each platform still has its own steps for turning a set of images into an actual installable sticker pack (e.g. WhatsApp needs a companion sticker-pack-building app; Telegram uses its @Stickers bot).
- WhatsApp officially requires WebP for the final upload. Most modern Android/Chrome browsers can export WebP directly from this app; if yours can't, it automatically falls back to PNG and tells you so — you'll need to convert that PNG to WebP with any converter before uploading.
- Background removal works best when the subject doesn't touch the photo's edges. If it does (or if there's a shadow/gradient background), use the tolerance slider and the touch-up brush to refine it.

## Files
- `index.html` — the app (all editing happens on-device, nothing is uploaded anywhere)
- `manifest.json`, `sw.js` — PWA install + offline support
- `icon.svg`, `icon-192.png`, `icon-512.png` — app icons

## Deploy
Create a new GitHub repo, upload these 7 files, enable GitHub Pages (Settings → Pages → Deploy from branch → main → root).
