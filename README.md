# China Tiger sample website

## Files
- `index.html`: homepage with a Contact Us link at the top right.
- `contact.html`: contact page with the original two phone numbers and address.
- `styles.css`: shared appearance for both pages.
- `chinatigerlogo.png`: restaurant logo.

## How it works

1. Create another HTML file for the new page. Here it is `contact.html`, in the same folder as `index.html`.
2. Move the contact section into the new page's `<main>` element. The original phone numbers and address are preserved. `<h1>` identifies the main heading on that page; `<address>` marks up the contact address.
3. Link to it from the homepage with `<a class="nav-button" href="contact.html">Contact Us</a>`. `href` is the destination. Because both files are in the same folder, only the filename is needed. A normal link is appropriate for navigation; CSS makes it look like a button. No JavaScript is needed.
4. Put shared CSS in `styles.css` and include `<link rel="stylesheet" href="styles.css">` in each page's `<head>`. This replaces the original inline `<style>` block so changes to the header apply to both pages.
5. The header preserves the original full-width gradient box, `padding: 20px 0`, bottom border, and Flexbox centering. `position: relative` makes the header the reference box for the navigation.
6. The navigation uses `position: absolute; top: 20px; right: 20px;`. This places the button in the top-right corner without moving the centered logo. On narrow screens, the logo can shrink to leave room for the button while staying centered.
7. The contact page links back using `href="index.html"`. Clicking the logo also returns home. The phone links use `tel:` so supported devices can open the dialer.

## Try it
Extract the ZIP, then open `index.html` in a browser. Click Contact Us, verify the phone numbers and address, and click Home to return. For GitHub Pages, upload both HTML files, the CSS, and the logo to the same folder. Keep the filenames and their capitalization consistent.
