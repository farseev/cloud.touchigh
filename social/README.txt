Touchigh Social prototype (self-hostable copy)

Open index.html in Chrome, Edge or Safari, or upload this folder to any static host.
Keep ws/ next to index.html: the page loads each workspace and its insight engine from there when you switch.

Included for hosting
- Favicons: favicon.ico, favicon.svg, apple-touch-icon.png, icon-192.png, icon-512.png, site.webmanifest
- Social preview: og-image.png (1200 x 630) with Open Graph and X card tags
- robots.txt plus a noindex robots meta tag. Search engines and AI crawlers stay out;
  link-preview bots can still fetch the page and image so shared links show a card.
  The prototype holds client workspace data, which is why indexing is off.

Before you share a hosted link
1. og:image and twitter:image are relative paths. Facebook, LinkedIn and X need a full URL.
   Ask for a rebuild with your address, or replace "og-image.png" in those two tags with the full URL.
2. robots.txt only works at the root of a domain. If the prototype sits in a subfolder,
   merge its rules into that domain's robots.txt.
3. For stronger protection, send the header "X-Robots-Tag: noindex, nofollow, noarchive"
   or put the folder behind a password.
