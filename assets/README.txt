assets/
=======

Drop your personalisation files into this folder and reference them in the
CONFIG block inside birthday.html.

Background image
----------------
  Recommended filename : bg.jpg  (or bg.png, bg.webp, etc.)
  Supported formats    : JPEG, PNG, WebP, GIF
  Recommended size     : 1920 × 1080 px (or larger)

  After copying your image here, open birthday.html in a text editor and
  set the bgImage value in CONFIG:

      bgImage: 'assets/bg.jpg',


Background music
----------------
  Recommended filename : song.mp3  (or song.ogg, song.wav, etc.)
  Supported formats    : MP3, OGG, WAV, AAC

  After copying your audio file here, set the songUrl value in CONFIG:

      songUrl: 'assets/song.mp3',


Notes
-----
  • Make sure to upload the assets/ folder alongside birthday.html when
    hosting the page (GitHub Pages, Netlify, Vercel, etc.).
  • Large audio files may cause slow page loads on mobile. A 2–3 minute
    MP3 encoded at 128 kbps is typically under 3 MB and loads quickly.
