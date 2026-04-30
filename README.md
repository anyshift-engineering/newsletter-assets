# Anyshift Newsletter

The public archive of the [Anyshift](https://anyshift.io) product newsletter. Each edition is published here as a self-contained HTML page plus the images it references, so anyone can read past editions without an inbox or a sign-up.

> [Anyshift](https://anyshift.io) is the AI-SRE platform built on a versioned resource graph. Annie, our agent, traces incidents to deployments and commits across AWS, GCP, Azure, Kubernetes, your codebase, your logs and your dashboards.

## Read the newsletter

Browse any past edition by opening `<last_day>/newsletter.html`. Editions are dated by the last day of the date window they cover.

| Edition | Window | URL |
|---|---|---|
| #2 | Apr 21–27, 2026 | <https://newsletter.getanyshift.com/2026-04-27/newsletter.html> |

## Subscribe

[anyshift.io](https://anyshift.io) → footer signup. Or wait for the next edition to land in your inbox; the archive here gets the same content, in the same window.

## How it's served

Files are served via GitHub Pages under the custom domain **`newsletter.getanyshift.com`** (CNAME pinned at the repo root). Pages source: branch `main`, root directory; HTTPS auto-provisioned via Let's Encrypt.

DNS: `newsletter.getanyshift.com  CNAME  anyshift-engineering.github.io.`

We use Pages rather than `raw.githubusercontent.com` so the asset host matches the newsletter sender domain (`getanyshift.com`), which gives Gmail's image proxy on iOS a smoother time. Cache invalidations flow through Fastly's tighter TTLs; same-name file replacements still hit CDN cache, so we rename when swapping.

## Repository layout

One folder per edition, named after the edition's last day:

```
2026-04-27/
  newsletter.html           ← the published edition (open this)
  images/
    devopscon-photo.jpg
    report-templates.gif
    terminal.png
    ...
2026-MM-DD/
  newsletter.html
  images/
    ...
```

URLs:

```
https://newsletter.getanyshift.com/<last_day>/newsletter.html
https://newsletter.getanyshift.com/<last_day>/images/<filename>
```

## License

Anyshift brand assets, all rights reserved. Newsletter copy is licensed for personal reading; redistribution or republication requires permission.
