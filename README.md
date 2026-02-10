# Hawthorne Court — Static Site

A simple static website for Hawthorne Court, Jackson Heights, Queens, NYC.

## Structure

```
hawthornecourt/
├── index.html        ← Homepage
├── about.html        ← Building history
├── events.html       ← Community events (edit directly)
├── gallery.html      ← Photo gallery with lightbox
├── contact.html      ← Contact form (uses Formspree)
├── css/
│   └── style.css     ← All styles
├── images/           ← Put your images here
│   ├── centerCircle.png
│   ├── garden-spring.jpg
│   ├── hawk.jpg
│   ├── aster.jpg
│   ├── halloween.jpg
│   ├── fall-colors.jpg
│   ├── growing-up.jpg
│   ├── centennial.jpg
│   └── building-exterior.jpg
└── README.md
```

## Setup

### 1. Download your images

You'll need to save the images from your current Squarespace site into the `images/` folder. The filenames referenced in the HTML are listed below alongside the original Squarespace URLs:

| Filename              | Original URL |
|-----------------------|-------------|
| `centerCircle.png`    | `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1599233935693-WDKT93B2USG8AISRXQCC/centerCircle.png` |
| `garden-spring.jpg`   | `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1682171327616-O2ZLAZXFWLLPEMAQZYCD/image-asset.jpeg` |
| `hawk.jpg`            | `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1673198142762-LEYDZUKMD2RT676CV32T/image-asset.jpeg` |
| `aster.jpg`           | `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1667187610761-YGVA19OTL33OKHG32RIV/image-asset.jpeg` |
| `halloween.jpg`       | `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1667187610761-60PXZH4LI0I5LX3NQ9XJ/image-asset.jpeg` |
| `fall-colors.jpg`     | `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1666456087963-V5WL397AIO70SRBT4D88/image-asset.jpeg` |
| `growing-up.jpg`      | `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1658451638182-XMSYPUXXEEMGSSHIMBSB/image-asset.jpeg` |
| `centennial.jpg`      | `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1656875102968-U7EL8CTH5IWM81I6K8EJ/image-asset.jpeg` |
| `building-exterior.jpg` | (from the About page — `https://images.squarespace-cdn.com/content/v1/5f525ea0c0ecee1e0855cab8/1604431345271-69FCP2O9GH5GO4V5FHXN/image-asset.jpeg`) |

Save each image with the filename shown in the left column.

### 2. Set up the contact form

The contact page uses [Formspree](https://formspree.io) for form handling (free, no backend required):

1. Create a free account at formspree.io
2. Create a new form
3. Copy the form ID (looks like `xyzabcde`)
4. In `contact.html`, replace `YOUR_FORM_ID` with your actual ID

### 3. Preview locally

Open `index.html` in a browser, or run a local server:

```bash
cd hawthornecourt
python3 -m http.server 8000
# then visit http://localhost:8000
```

### 4. Deploy to Cloudflare Pages

1. Create a GitHub repository and push this folder to it
2. Go to [Cloudflare Pages](https://pages.cloudflare.com)
3. Connect your GitHub account and select the repository
4. Build settings: leave everything blank (no build command needed — it's plain HTML)
5. Deploy
6. Point your `hawthornecourt.org` domain to Cloudflare Pages in your DNS settings

### 5. Updating content

- **Events**: Edit `events.html` directly — copy an `<article class="event-item">` block and change the date, title, and description.
- **Gallery**: Add new images to `images/`, then add a `<figure class="gallery-grid__item">` block in `gallery.html`.
- **Text**: Edit the HTML directly in any page. All the visible text is easy to find.

Push changes to GitHub and Cloudflare Pages will auto-deploy.
