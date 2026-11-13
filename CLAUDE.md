# cookcompliance.com

The Cook Compliance Solutions website: one screen in the refined brand (white ground, black type, red as accent only). David and Alma's business; David runs the site. The design record is the Claude Design canvas "Cook Website Options" (https://claude.ai/artifact/HYufQeJNFpSjM2u7sNBk9Q), whose Option A is the live page; the earlier multi-section design is the artboards in the Drive at `Administrative/David/Branding/source/website/` (`Main.dc.html` desktop, `Phone.dc.html` phone). The brand rules and voice are in the Cook Design System and `Branding/README.md`. Change the live site here, in the repo; a redesign starts on the canvas, a copy or layout fix starts here.

## Stack

Static HTML with inline CSS, no build step and no script. Two faces: Metropolis Bold for headlines and numerals, the face nearest the logo's lettering, served from this repo (`metropolis-bold.woff2`, public domain) so every device shows it, and Helvetica Neue (Regular for text, Medium on the large hero question, 700 for the button and phone number) for the rest, supplied by the visitor's device, text falling to Arial where it is missing. Nothing is fetched from Google Fonts. One responsive layout. Above 1024px the page is one screen from about 800px of window height up, the copyright line sitting at the bottom of the window (David's direction), and scrolls a little on anything shorter, the services set large and open by David's direction, their row spacing growing with the window's height: the header (logo alone), then the hook, its question, the email button and the phone number on the left, the six services on the right, and the copyright line at the foot; the body fills the window (`100svh`) and grows when the content needs more. To 720px the two halves stack, and below that is the phone layout. There are no in-page links and no navigation: the email button and the phone number are the only ways out.

## Files

- `index.html` — the whole site: header, `.hero`, `.services` (six rows), footer.
- `404.html` — branded not-found page; its Contact link opens an email to hello@cookcompliance.com.
- `logo-horizontal.svg` (header), `logo.svg` (the full stacked logo, used on the 404 page), `favicon.ico`, `favicon.png`, `apple-touch-icon.png` — copies of the logo set in `Branding/logo/` (the vector masters in `print/`, the icons in `icons/`); replace them there, then copy.
- `metropolis-bold.woff2` — the heading face, a copy of `Branding/source/fonts/Metropolis-Bold.woff2`.
- `CNAME` — `cookcompliance.com`.

## Left off the page

David's cuts from the earlier design: Why Cook?, the black sign-off band, the audience line under the services heading, the header links, the gray rule under the header (here and on the not-found page), the footer logo and the promise under it. The earlier page, with all of them, the longer wording of each service and the switched-off client-quote block, is in the git history before the one-screen rebuild. The old Wix site's one testimonial (Andy Wagoner, Wagoner Enterprises, a former client) is in the Drive at `Reference/Website Archive/text/home.md`.

## Deployment

GitHub Pages from `main`, repo `davidavalerio/cookcompliance.com`. `/deploy` ships changes. HTTPS is enforced in the Pages settings.

## Domain

Registered at GoDaddy in Alma's name; David manages the DNS there (GoDaddy's web UI, no API access). Records that make the site work: four A records on `@` (GitHub Pages' `185.199.108.153` through `185.199.111.153`) and `www` as a CNAME to `davidavalerio.github.io`, so `www.cookcompliance.com` redirects to the apex. The mailbox is on cookcompliance.co (Google Workspace mail, DNS at GoDaddy); `hello@cookcompliance.com` forwards to it through GoDaddy, so the .com's MX and TXT records are GoDaddy's and are left alone — changing them breaks the forward.

Contact details on the page: `hello@cookcompliance.com` (the forward) and `(713) 478-9395` — David's number, since he handles sales end to end (Alma's (608) line stays in her email signature, not on the site).
