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
5. The header uses CSS Grid with `grid-template-columns: 1fr auto 1fr`: equal left and right spaces around the centered logo. The logo is in column 2 and the navigation in column 3. `justify-self: end` places navigation on the right.
6. The `@media (max-width: 600px)` rule switches to two columns on smaller screens: a logo that can shrink and a button on the right. The viewport meta tag makes mobile browsers use the device's width.
7. The contact page links back using `href="index.html"`. Clicking the logo also returns home. The phone links use `tel:` so supported devices can open the dialer.

## Try it
Extract the ZIP, then open `index.html` in a browser. Click Contact Us, verify the phone numbers and address, and click Home to return. For GitHub Pages, upload both HTML files, the CSS, and the logo to the same folder. Keep the filenames and their capitalization consistent.
