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

## Previewing Locally

Open `index.html` in a browser, or run a local server:

```bash
cd hawthornecourt
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Updating content

- **Events**: Edit `events.html` directly — copy an `<article class="event-item">` block and change the date, title, and description.
- **Gallery**: Add new images to `images/`, then add a `<figure class="gallery-grid__item">` block in `gallery.html`.
- **Text**: Edit the HTML directly in any page. All the visible text is easy to find.
