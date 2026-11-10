# cookcompliance.com

The Cook Compliance Solutions website: one screen in the refined brand (white ground, black type, red as accent only). David and Alma's business; David runs the site. The design record is the Claude Design canvas "Cook Website Options" (https://claude.ai/artifact/HYufQeJNFpSjM2u7sNBk9Q), whose Option A is the live page; the earlier multi-section design is the artboards in the Drive at `Administrative/David/Branding/source/website/` (`Main.dc.html` desktop, `Phone.dc.html` phone). The brand rules and voice are in the Cook Design System and `Branding/README.md`. Change the live site here, in the repo; a redesign starts on the canvas, a copy or layout fix starts here.

## Stack

Static HTML with inline CSS, no build step and no script. Type is Alma's own two faces, supplied by the visitor's device: Avenir Heavy for headlines and numerals, Helvetica Neue (Regular for text, Light only on the large hero question, 700 for the button and phone number) for the rest. Where Avenir is missing (Windows, Android) the page fetches Nunito Sans Bold from Google Fonts as its stand-in and text falls to Arial; Apple devices download no font. One responsive layout. Above 1024px the page is one screen on a large display (about 1000px of window height and up) and scrolls a little on a laptop, the services set large and open by David's direction, their row spacing growing with the window's height: the header (logo alone), then the hook, its question, the email button and the phone number on the left, the six services on the right, and the copyright line at the foot; the body fills the window (`100svh`) and grows when the content needs more. To 720px the two halves stack, and below that is the phone layout. There are no in-page links and no navigation: the email button and the phone number are the only ways out.

## Files

- `index.html` — the whole site: header, `.hero`, `.services` (six rows), footer.
- `404.html` — branded not-found page; its Contact link opens an email to hello@cookcompliance.com.
- `logo-horizontal.png` (header), `logo.png` (the full stacked logo, used on the 404 page), `favicon.ico`, `favicon.png`, `apple-touch-icon.png` — copies of Alma's logo files in `Branding/logo/`; replace them there, then copy.
- `CNAME` — `cookcompliance.com`.

## Left off the page

David's cuts from the earlier design: Why Cook?, the black sign-off band, the audience line under the services heading, the header links, the footer logo and the promise under it. The earlier page, with all of them, the longer wording of each service and the switched-off client-quote block, is in the git history before the one-screen rebuild. The old Wix site's one testimonial (Andy Wagoner, Wagoner Enterprises, a former client) is in the Drive at `Reference/Website Archive/text/home.md`.

## Deployment

GitHub Pages from `main`, repo `davidavalerio/cookcompliance.com`. `/deploy` ships changes. HTTPS is enforced in the Pages settings.

## Domain

Registered at GoDaddy in Alma's name; David manages the DNS there (GoDaddy's web UI, no API access). Records that make the site work: four A records on `@` (GitHub Pages' `185.199.108.153` through `185.199.111.153`) and `www` as a CNAME to `davidavalerio.github.io`, so `www.cookcompliance.com` redirects to the apex. The mailbox is on cookcompliance.co (Google Workspace mail, DNS at GoDaddy); `hello@cookcompliance.com` forwards to it through GoDaddy, so the .com's MX and TXT records are GoDaddy's and are left alone — changing them breaks the forward.

Contact details on the page: `hello@cookcompliance.com` (the forward) and `(713) 478-9395` — David's number, since he handles sales end to end (Alma's (608) line stays in her email signature, not on the site).
