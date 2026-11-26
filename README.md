# The Golden Sip website

A static website (plain HTML, CSS and JavaScript, no build step).

## Files (put ALL of these in the same folder, next to index.html)
- `index.html`: page structure
- `styles.css`: all styling
- `app.js`: menu, cart, WhatsApp ordering, Instagram QR page, owner dashboard
- `images.js`: your logo, the three cafe photos and the Instagram QR, built into the code so they always show
- `menu-data.js`: built-in copy of the full menu
- `menu.json`: the live menu. If present, it overrides `menu-data.js` (this is the file you replace to publish menu changes)
- `assets/`: the original image files, for your reference only. The site does not need this folder

Important: every file above must sit in the same folder as `index.html` in your repository (the root). If you upload a folder, make sure `index.html` is not inside an extra subfolder.

## Deploy
GitHub Pages: Settings, Pages, Deploy from a branch, `main` and `/ (root)`.
Vercel or Netlify: import the repository, leave the build command empty, publish directory is the root.

## Where each photo is used
- Logo: header (top left), footer, Instagram page, browser tab icon
- Reception and arch sign photo: top of the home page, under the main heading
- Booth with palm mural: Story section
- "Good food good mood" wall: Visit section

## Changing the menu
1. Open your site, go to the Owner page (add `#owner` to the address) and sign in.
2. Change prices, availability, dishes, categories, the contact phone or the UPI ID. Edits are saved on that device first.
3. Tap Download menu.json.
4. In GitHub, replace `menu.json` with the downloaded file and commit. Guests see the change after the host redeploys, usually within a minute.

## Notes
- The Owner login is a screen inside the page. It keeps casual visitors out but is not strong security. Do not store secrets in this site.
- Orders are sent as a WhatsApp message to the phone number in the menu.
- Opening hours (10 AM to 4 AM) are written in `app.js` and `index.html`; search for "10 AM".
- To test locally run `python3 -m http.server` in this folder and open http://localhost:8000
