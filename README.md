# 🎂 Birthday Wish Webpage

A personalised Happy Birthday webpage that reads the recipient's name from a
URL query parameter — perfect for sending as a link via email.

## How it works

The page (`birthday.html`) reads a `name` query parameter from the URL and
displays a personalised greeting with animated confetti, a bouncing cake emoji,
and shimmering text.

## Usage

### 1. Host the file

Upload `birthday.html` to any static web host (GitHub Pages, Netlify, Vercel,
your own server, etc.).

### 2. Generate a personalised link

Append `?name=<recipient name>` to the URL:

```
https://your-domain.com/birthday.html?name=Alice
https://your-domain.com/birthday.html?name=John%20Doe
```

### 3. Send the link via email

Paste the link into your email. The recipient clicks it and sees a
personalised Happy Birthday page — no server, no database required.

## Example

```
https://your-domain.com/birthday.html?name=Sarah
```

Opens a full-screen animated birthday card addressed to **Sarah**.

## Features

- 🎉 Animated confetti (canvas-based, pure JS — no dependencies)
- 🎂 Bouncing cake emoji
- ✨ Shimmering gradient text
- 📱 Responsive — works on desktop and mobile
- 🔒 Name is sanitized client-side (only letters, spaces, hyphens and apostrophes allowed; max 60 characters); name is injected via `textContent` so HTML injection is impossible
- 🚫 Zero external dependencies — a single self-contained HTML file
