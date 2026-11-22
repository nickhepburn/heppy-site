# Nick Hepburn – personal site

A static site: no build step, no dependencies.

- `index.html` – the whole site (text, styles, code)
- `photos/`, `videos/` – media used by the Adventures pages

## Editing text
Open `index.html` and search for `var PAGES = [`. Each page's text is a list of quoted lines
(About Me, Projects, Blog, Contact, and each Adventures page). Edit the words inside the quotes,
save, commit, push. Keep each line inside `"..."` followed by a comma, except the last line.

## Adding photos / videos
Put the file in `photos/` or `videos/`, then add a line to that trip's list in `index.html`
(search for `IRELAND_PHOTOS`, `ROWING_PHOTOS`, `GRAD_TRIP_MEDIA`, `ROCKIES_WINTER_MEDIA`, `TUCKERMAN_MEDIA`).
Photos: JPG, longest side about 1400px. Videos: H.264/AAC `.mp4` (convert iPhone `.mov` files first).

## Contact form
The form posts to Web3Forms using `WEB3FORMS_KEY` near the top of the script. Messages are emailed to the address set up in your Web3Forms account.

## Publishing (GitHub Pages)
Repo Settings > Pages > Deploy from branch `main`, folder `/ (root)`.
Custom domain: add it under Pages > Custom domain, and set DNS at your registrar:
- apex domain (example.com): four A records -> 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
- www: CNAME -> <your-github-username>.github.io
Then tick "Enforce HTTPS".
