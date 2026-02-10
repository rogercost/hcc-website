# Hawthorne Court — Static Site

A simple static website for Hawthorne Court, Jackson Heights, Queens, NYC.

## Structure

```
hawthornecourt/
├── index.html        ← Homepage
├── about.html        ← Building history
├── events.html       ← Community events (edit directly)
├── gallery.html      ← Photo gallery with lightbox
├── css/
│   └── style.css     ← All styles
├── images/           ← Put your images here
│   ├── centerCircle.png
│   ├── garden-spring.jpg
│   ├── ...
└── README.md
```

## Setup

### 1. Preview locally

Open `index.html` in a browser, or run a local server:

```bash
cd hawthornecourt
python3 -m http.server 8000
# then visit http://localhost:8000
```

### 2. Deploy to Cloudflare Pages

1. Create a GitHub repository and push this folder to it
2. Go to [Cloudflare Pages](https://pages.cloudflare.com)
3. Connect your GitHub account and select the repository
4. Build settings: leave everything blank (no build command needed — it's plain HTML)
5. Deploy
6. Point your `hawthornecourt.org` domain to Cloudflare Pages in your DNS settings

### 3. Updating content

- **Events**: Edit `events.html` directly — copy an `<article class="event-item">` block and change the date, title, and description.
- **Gallery**: Add new images to `images/`, then add a `<figure class="gallery-grid__item">` block in `gallery.html`.
- **Text**: Edit the HTML directly in any page. All the visible text is easy to find.

Push changes to GitHub and Cloudflare Pages will auto-deploy.
