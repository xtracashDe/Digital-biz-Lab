# Digital Biz Lab Website

Official website for Digital Biz Lab (digitalbizlab.net).

**Learn Digital. Build Better.**

## What this is

A static site. No build step, no dependencies. The home page is a single `index.html` with its CSS and JS inline. The legal pages share one stylesheet. Fonts and images are self hosted under `assets/`.

## Structure

```
index.html              Home page (HTML, CSS and JS inline)
privacy/index.html      Privacy Policy      (served at /privacy/)
terms/index.html        Terms of Service    (served at /terms/)
refund-policy/index.html  Refund Policy      (served at /refund-policy/)
assets/legal.css        Shared styles for the legal pages
assets/fonts/           Sora and Plus Jakarta Sans (self hosted woff2)
assets/img/             Founder photo
og-image.png            Social share image (1200 x 630)
favicon.*, icon-*       Icons and web manifest
robots.txt, sitemap.xml Crawler files
_headers                Security and cache headers (Netlify format)
_redirects              www to apex redirect, legal page aliases, fallback (Netlify format)
```

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy on Netlify

1. Push this repo to GitHub.
2. In Netlify, choose Add new site, then Import an existing project, and pick this repo.
3. Leave the build command empty and set the publish directory to `/`.
4. Add the custom domain `digitalbizlab.net`.

The corporate enquiry form uses Netlify Forms (`data-netlify="true"`). Submissions appear under Forms in the Netlify dashboard once the site is deployed. Turn on email notifications there so enquiries reach you.

## Cookie consent and the TikTok Pixel

The TikTok Pixel loads only after a visitor clicks Accept on the cookie banner. The choice is stored in the browser under `dbl_cookie_consent`. Visitors can change it from Cookie Settings in the footer. The consent script sits at the bottom of `index.html`. If you add any other analytics or advertising tag, load it inside the same `loadPixel` style function so it also waits for consent, and list it in the Privacy Policy.

## Things to update each cohort

Search `index.html` for these and change them when a new season opens:

* Cohort dates (`Tue 6, Wed 7 and Thu 8 Oct 2026`, and the hero badge)
* Early bird price, deadline and regular price
* Seat cap
* The Selar link (`https://selar.co/digitalbizlab`)

If the cohort format changes (number of sessions, WhatsApp support period, recordings, certificate), also check the Refund Policy and Terms so they still match what you sell.

## Legal pages

The Privacy Policy, Terms and Refund Policy were drafted on 19 September 2026 for a Nigerian audience, with reference to the Nigeria Data Protection Act 2023 and the Federal Competition and Consumer Protection Act 2018. They should be reviewed by a Nigerian lawyer before you rely on them. Update the "Last updated" date on a page whenever you change it.

Business choices written into the pages that you should confirm or change:

* Refund window: full refund if requested at least 48 hours before the first live session.
* Refund replies within 3 business days, and payouts within 7 to 14 business days.
* Retention: enquiries up to 24 months, session recordings up to 12 months.
* Data requests answered within one month.
* Complaints handled within 30 days before mediation or court.
