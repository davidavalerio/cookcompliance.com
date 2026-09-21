# cookcompliance.com

The Cook Compliance Solutions website: a one-page static site in the refined brand (white ground, black type, red as accent only). Alma's company; David runs the site. The design record is the Claude Design canvas whose artboards live in the Drive at `0-Cook Compliance/Branding/source/website/` (`Main.dc.html` desktop, `Phone.dc.html` phone); the brand rules and voice are in `Branding/README.md` there. Change the live site here, in the repo. The artboards stay as the record of what Alma approved; a redesign starts there, a copy or layout fix starts here.

## Stack

Static HTML with inline CSS, no JavaScript, no build step. Type is Alma's own two faces, supplied by the visitor's device: Avenir Heavy for headlines and numerals, Helvetica Neue (Regular for text — Light only on the large hero question, since Light in gray at small sizes reads too faint on screens — 500 nav, 700 buttons) for the rest. Where Avenir is missing (Windows, Android) the page fetches Nunito Sans Bold from Google Fonts as its stand-in and text falls to Arial; Apple devices download no font. One responsive layout: the desktop artboard above 1024px, a stacked middle layout to 720px, the phone artboard below. Two sections open to the full screen: the hero fills the first screen under the header and the black sign-off band fills a screen of its own, content centered (`100svh`, with the paddings as the floor so a short window never clips); services and Why Cook keep their natural height. The header's three links — Services, Why Cook?, Contact — are identical: one weight, no underline, red on hover only (Contact is the only one on phones and on the 404 page). Where the phone artboard says a service row shorter, the page carries both texts and shows one per width (`.d` desktop, `.p` phone) — the two never differ in substance.

## Files

- `index.html` — the whole site. Sections: header, hero, `#services` (seven rows), `#about` (Why Cook?), `#contact` (black band), footer.
- `404.html` — branded not-found page.
- `cook-compliance-lockup.svg`, `favicon.ico`, `favicon.svg` — copies from `Branding/`; regenerate there, then copy.
- `CNAME` — `cookcompliance.com`.

## Switched off

The "Don't take our word for it" client-quote block sits in `index.html` as an HTML comment inside `#about`, waiting for quotes from current clients. The old Wix site's one testimonial (Andy Wagoner, Wagoner Enterprises, a former client) is in the Drive at `Reference/Website Archive/text/home.md` if Alma wants it used.

## Deployment

GitHub Pages from `main`, repo `davidavalerio/cookcompliance.com`. `/deploy` ships changes. HTTPS is enforced in the Pages settings.

## Domain

Registered at GoDaddy in Alma's name; David manages the DNS there (GoDaddy's web UI, no API access). Records that make the site work: four A records on `@` (GitHub Pages' `185.199.108.153` through `185.199.111.153`) and `www` as a CNAME to `davidavalerio.github.io`, so `www.cookcompliance.com` redirects to the apex. The mailbox stays on cookcompliance.co (Wix DNS) until the mail move; `hello@cookcompliance.com` forwards to it through GoDaddy, so the .com's MX and TXT records are GoDaddy's and are left alone — changing them breaks the forward.

Contact details on the page: `hello@cookcompliance.com` (the forward) and `(713) 478-9395` — David's number, since he handles sales end to end (Alma's (608) line stays in her email signature, not on the site).
