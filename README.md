# My Portfolio

Personal portfolio site built with vanilla HTML/CSS/JS, hosted on GitHub Pages.

---

## Setup

1. Clone this repo locally
2. Fill in your details in the `content/` JSON files (see below)
3. Push to GitHub — the site updates automatically

---

## File structure

```
/
├── index.html              ← Site shell — design and layout only
├── cv.pdf                  ← Drop your CV PDF here
├── images/
│   ├── photo.jpg           ← Your portrait (replaces placeholder)
│   └── sketches/           ← Doodle images go here
└── content/
    ├── profile.json        ← Name, bio, skills, interests, social links
    ├── cv.json             ← Experience and education timeline
    ├── updates.json        ← Blog posts
    └── sketches.json       ← Doodle gallery entries
```

---

## How to update content

### Your profile (`content/profile.json`)
Fill in your `name`, `tagline`, `bio`, social links and `contact_email`.
The `skills` and `interests` arrays are already populated — edit freely.

### Adding a blog post (`content/updates.json`)
Copy an existing entry and add it to the top of the array:
```json
{
  "id":      "post-2",
  "title":   "My new post",
  "date":    "01 Jul 2026",
  "tag":     "Engineering",
  "excerpt": "A short summary shown in the list.",
  "body":    "The full post text goes here.\n\nUse \\n\\n for new paragraphs.",
  "emoji":   "🚀",
  "bg":      "#E0EFFC"
}
```

### Adding a sketch (`content/sketches.json`)
1. Drop your image into `images/sketches/` (e.g. `my-drawing.jpg`)
2. Add an entry to `sketches.json`:
```json
{
  "id":    "sketch-2",
  "title": "My drawing",
  "date":  "01 Jul 2026",
  "desc":  "What I wrote about this doodle.",
  "image": "images/sketches/my-drawing.jpg",
  "bg":    "#DDF4EE",
  "size":  "med"
}
```
`size` can be `"short"`, `"med"`, or `"tall"` — mix these up to make the masonry grid interesting.

### Adding your photo
Drop a photo named `photo.jpg` into the `images/` folder.
It will automatically appear in the homepage hero and the About page avatar.

### Adding your CV PDF
Drop your CV as `cv.pdf` into the root folder.

---

## Pushing updates
```bash
git add .
git commit -m "describe what you changed"
git push
```
GitHub Pages will rebuild within ~30 seconds.
