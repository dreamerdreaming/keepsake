# Keepsake 💌

A tiny web app for wrapping a message, a photo, or a song into something someone will actually want to open — a wax-sealed envelope, a scratch-to-reveal card, or a note that unlocks at a specific moment.

**Live site:** _add your GitHub Pages link here once it's deployed_
`https://YOUR-USERNAME.github.io/keepsake/`

## What it does

- Write a message, optionally attach a photo and a Spotify song/playlist
- Choose how it opens: break a wax seal, or scratch to reveal
- Optionally lock it until a specific date/time (a countdown shows until then)
- Get a shareable link (plus a QR code) to send to the person
- They open the link and the envelope unfolds, the message types itself out, the song fades in, and a little flourish of sparkles finishes it off

## How it works

Everything is a single static HTML file — no backend, no database, no accounts.
The entire message (including the photo, if you add one) is encoded and embedded directly in the link itself. Opening the link decodes it client-side. Nothing is stored on a server, which also means:

- The link **is** the message — anyone who has it can open it, so share it somewhere private (text, DM, etc.), not publicly
- There's no way to "unsend" or edit a keepsake once the link is sent
- Adding a photo makes the link noticeably longer (it's compressed automatically, but still)

## Hosting it yourself

This repo is set up for [GitHub Pages](https://pages.github.com/):

1. Fork or clone this repo
2. In the repo settings, go to **Settings → Pages**
3. Under "Source," select the `main` branch and `/ (root)` folder
4. Your site will be live at `https://YOUR-USERNAME.github.io/REPO-NAME/`

Since it's just one HTML file with no build step, you could also host it on Netlify, Vercel, Cloudflare Pages, or literally any static file host — just make sure the file is named `index.html` at the root.

## Tech

Plain HTML/CSS/JS. No frameworks, no dependencies to install. Uses:
- Canvas for the scratch-to-reveal effect
- [QRCode.js](https://davidshimjs.github.io/qrcodejs/) (loaded from a CDN) for the shareable QR code
- Google Fonts (Fraunces, Caveat, Inter) for the look

## License

Do whatever you want with it — make it yours, change the copy, swap the colors, add your own touch before sending it to someone.
