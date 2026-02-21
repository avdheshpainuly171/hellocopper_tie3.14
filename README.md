# 🎂 Birthday Wish Webpage

A personalised Happy Birthday webpage that reads the recipient's name from the
code or a URL query parameter — perfect for sending as a link via email.

## How it works

Open `birthday.html` in a text editor, fill in the `CONFIG` block near the top
of the `<script>` section, then host it anywhere and share the link.

## Quick-start: edit the CONFIG

Near the bottom of `birthday.html` you will find a clearly marked `CONFIG`
section:

```js
var CONFIG = {
  // Name shown on the card (overridden by ?name= in the URL if provided)
  name: 'Alice',

  // Background image URL or relative path.  Leave empty ('') for the default gradient.
  bgImage: 'https://example.com/party.jpg',

  // Song URL or relative path to an audio file.  Leave empty ('') to disable music.
  songUrl: 'https://example.com/happy-birthday.mp3'
};
```

Change `name`, `bgImage`, and `songUrl` to the values you want, save the file,
and you're done.

## Usage

### 1. Host the file

Upload `birthday.html` (and any local image/audio files you reference) to any
static web host (GitHub Pages, Netlify, Vercel, your own server, etc.).

### 2. (Optional) Generate a personalised link via URL

The `?name=` query parameter still works and takes priority over `CONFIG.name`:

```
https://your-domain.com/birthday.html?name=Alice
https://your-domain.com/birthday.html?name=John%20Doe
```

### 3. Send the link via email

Paste the URL into your email. The recipient clicks it and sees a
personalised Happy Birthday page with background photo and music — no server,
no database required.

## Example

```
https://your-domain.com/birthday.html?name=Sarah
```

Opens a full-screen animated birthday card addressed to **Sarah**.

## Features

- 🎉 Animated confetti (canvas-based, pure JS — no dependencies)
- 🎂 Bouncing cake emoji
- ✨ Shimmering gradient text
- 🖼️ Background image — set `CONFIG.bgImage` to any image URL or file path
- 🎵 Background music — set `CONFIG.songUrl` to any audio URL or file path;
  a floating ▶/⏸ button lets the visitor control playback
- 📝 Name configurable directly in the code via `CONFIG.name` (no URL needed)
- 📱 Responsive — works on desktop and mobile
- 🔒 Name is sanitized client-side (only letters, spaces, hyphens and apostrophes allowed; max 60 characters); name is injected via `textContent` so HTML injection is impossible
- 🚫 Zero external dependencies — a single self-contained HTML file
