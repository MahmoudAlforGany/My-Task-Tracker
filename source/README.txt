Mahmoud AlforGany Task Tracker — Images Folder
================================================

Drop your personal photo and the company logo into this folder.
The app will pick them up automatically when you refresh.

Required filenames (DO NOT prefix with "images" — that's the folder, not the name):

  photo.jpg / photo.jpeg / photo.png / photo.webp
      — your personal photo (right side of the header)

  logo.png / logo.jpg / logo.jpeg / logo.svg / logo.webp
      — company / DF logo (left side of the header)

The first matching file in each list above is loaded automatically.
Just put your image in this folder, name it correctly, and refresh the page.

Tips:
- Square images (e.g. 256x256 or 512x512) look best — the header crops them into a rounded square.
- Keep file sizes under ~1 MB for fast loading.
- If both files are missing the app falls back to the built-in placeholder
  icons, OR to whatever you previously uploaded via the in-app uploader
  (those are saved in browser LocalStorage).

Folder priority (first match wins):
  1) images/photo.jpg     2) images/photo.png     3) LocalStorage upload     4) Placeholder
  1) images/logo.png      2) images/logo.jpg      3) LocalStorage upload     4) Placeholder
