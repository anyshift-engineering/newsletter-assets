# Anyshift Newsletter Assets

Public image hosting for the [Anyshift](https://anyshift.io) newsletter.

The newsletter ships as HTML email; its illustrations (PNG, GIF, JPEG) live here so any inbox can fetch them over HTTPS without authentication.

## Serving

Files are served via GitHub Pages under the custom domain **`assets.getanyshift.com`** (CNAME pinned at the repo root). Pages source: branch `main`, root directory; HTTPS auto-provisioned via Let's Encrypt.

DNS: `assets.getanyshift.com  CNAME  anyshift-engineering.github.io.`

We use Pages rather than `raw.githubusercontent.com` so the asset host matches the newsletter sender domain (better Gmail-image-proxy behavior on iOS) and so cache invalidations flow through Fastly's tighter TTLs. Same-name file replacements still hit CDN cache; rename when swapping.

## Layout

One folder per edition, named after the edition's closing date:

```
2026-04-27/
  devopscon-photo.jpg
  terminal.png
  ...
2026-MM-DD/
  ...
```

Each file is reachable at:

```
https://assets.getanyshift.com/<last_day>/<filename>
```

## Subscribe

[anyshift.io](https://anyshift.io) → footer signup, or wait for the next edition to land in your inbox.

## License

Anyshift brand assets, all rights reserved.
