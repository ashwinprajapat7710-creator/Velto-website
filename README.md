# Velto — Creator Management

Website for **Velto**, a modern creator management agency that represents creators, develops their personal brands, and connects them with the right brands and opportunities.

Contact: [velto.creators@gmail.com](mailto:velto.creators@gmail.com)

## About this site

A single-file static website. No build step, no dependencies to install.

- **Stack:** HTML, CSS and vanilla JavaScript in one `index.html`
- **Font:** Inter Tight (loaded from Google Fonts)
- **Logo:** embedded in the file, so there are no image files to manage
- **Sections:** Navigation, Hero, Creator Network, What We Do, For Brands, Why Velto, Culture Statement, Final CTA, Contact, Footer

## Run locally

Open `index.html` in any modern browser. That's it.

## Deploy with GitHub Pages

1. Push `index.html` to the `main` branch.
2. Go to **Settings → Pages**.
3. Set **Source** to *Deploy from a branch*, choose **main** and **/ (root)**, then save.
4. The site goes live at `https://YOUR-USERNAME.github.io/REPO-NAME/` within a couple of minutes.

To use a custom domain, add it under **Settings → Pages → Custom domain** and point your domain's DNS to GitHub.

## Updating content

Everything below lives in `index.html`.

### Creators

Edit the `CREATORS` array in the `<script>` at the bottom of the file:

```js
{
  name: "Creator Name",
  cat: "Fashion / Lifestyle",
  platform: "Instagram",
  handle: "@handle",
  desc: "Short description of the creator goes here.",
  image: "images/creator1.jpg", // leave "" to show the placeholder
  c: ["#2a2a31", "#0e0e11"]      // placeholder gradient colors
}
```

Add photos to an `images/` folder in the repo and point `image` at them. Add or remove objects to change the number of cards.

### Contact form

The form validates name, email, role and message. By default, with no backend, it opens the visitor's email app with the inquiry pre-filled.

To receive inquiries directly, set `FORM_ENDPOINT` in the script to your form service URL (for example a Formspree endpoint). The form then sends the inquiry as JSON:

```json
{ "name": "", "email": "", "role": "Creator | Brand", "message": "" }
```

### Social links

The footer links for Instagram, YouTube and LinkedIn are placeholders (`href="#"`). Replace them with real profile URLs once the accounts exist.

### Social sharing preview

To show an image when the link is shared, add an `og-image.png` (about 1200×630) and this tag inside `<head>`:

```html
<meta property="og:image" content="https://YOUR-DOMAIN/og-image.png">
```

## Brand

| Role | Color |
| --- | --- |
| Obsidian Black | `#0B0B0D` |
| Warm Ivory | `#F5F2EC` |
| Electric Lime | `#C7FF3D` |
| Graphite | `#1A1A1F` |
| Muted Grey | `#9B9BA3` |
| Logo Cyan (accent) | `#4FD6FF` |

The logo must not be redrawn, recolored or distorted.

## Content rules

The brand is new. Do not add client logos, follower counts, campaign results, testimonials, awards or partnerships until they are real.

## Accessibility and performance

- Semantic HTML with a clear heading hierarchy
- Keyboard-focusable navigation, cards and form, with visible focus states
- Respects `prefers-reduced-motion`
- Responsive from mobile to desktop, with a dedicated mobile menu and creator carousel

© 2026 Velto. All rights reserved.
