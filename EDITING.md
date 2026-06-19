# Editing the site — cheat sheet

The site is plain static HTML/CSS. No build step. To preview any change, just
double-click the `.html` file and open it in a browser — what you see is what ships.

Two ways to edit:
- **Quick text tweak:** open the file on github.com → pencil icon ✏️ → edit → "Commit changes". Live in ~30s.
- **Bigger change:** clone the repo, edit in any text editor (VS Code), `git push`.

When changing words, type over the text *between* the tags — leave the `<tags>` alone.

---

## Two gotchas

1. **After editing `assets/css/site.css`**, bump the version number in the stylesheet
   link near the top of EVERY html page so browsers load the new styles:
   `…/site.css?v=30"` → `…/site.css?v=31"`
2. **Keep paths relative** (`assets/...`, `research/...`). Don't add a leading `/`.

---

## Add a publication

In `index.html`, find the `<ol class="a-pub-list">` block. Copy one entry, paste it
in the right spot (newest at top), and edit the fields:

```html
<li class="a-pub">
  <div class="mono a-pub__year">2026</div>
  <div class="a-pub__body">
    <h4><a class="a-pub__link" href="https://doi.org/XXXX" target="_blank" rel="noopener">Paper title here</a></h4>
    <p class="a-pub__auth"><strong>Johnson C</strong>, Coauthor A, Coauthor B.</p>
    <p class="a-pub__ven mono">Journal Name · 2026 · 10.xxxx/xxxxx</p>
  </div>
</li>
```
- Bold your name with `<strong>…</strong>`.
- To highlight a flagship paper, add the class: `<li class="a-pub a-pub--hl">`.

---

## Add an invited talk

In `index.html`, find `<ul class="a-talks-list">`. Copy one entry:

```html
<li class="a-talk">
  <div class="a-talk__yr mono">2026</div>
  <div class="a-talk__body">
    <h4>Conference or seminar name</h4>
    <p class="a-talk__meta mono">Invited speaker · host / society</p>
  </div>
</li>
```

---

## Add a "Beyond the Bench" entry

1. Put a **square** image (e.g. 600×600) in `assets/img/beyond/`, named like `newentry.jpg`.
2. In `index.html`, find `<ul class="a-beyond__list">`. Copy one entry:

```html
<li class="a-beyond__item">
  <a href="https://link-to-the-piece" target="_blank" rel="noopener">
    <div class="a-beyond__kind mono">Essay · Outlet name</div>
    <h3>Title of the piece</h3>
    <p>One or two sentences describing it.</p>
    <span class="a-beyond__go mono">Read ↗</span>
  </a>
  <img class="a-beyond__thumb" src="assets/img/beyond/newentry.jpg" alt="Short description" loading="lazy">
</li>
```
- Change "Read ↗" to "Listen ↗", "Watch ↗", etc. as fits.

---

## Add a research project

1. Create a new page by copying an existing one in `research/` (e.g. duplicate
   `3d-fastr.html` → `new-project.html`) and edit its content.
2. In `index.html`, find `<section class="a-projects"`. Copy one `<article class="a-project">`
   block, point its link at `research/new-project.html`, and set a preview image.
   (Alternating left/right layout: add `a-project--flip` to every other article.)

---

## Edit the CV

Open `cv.html`, edit the text (same tag rules). Each row is a copy-paste block —
look for `class="entry"`, `class="pub"`, `class="talk"`, `class="side__item"`.
To regenerate the PDF: open `cv.html` in a browser and click **Save as PDF**.

---

## Update the "last updated" date

In `index.html`, search for `Last updated` in the footer and edit the month/year.

---

## Lowest-friction option

You don't have to touch any of this yourself — bring the repo (or the zip) back to
the assistant that built it and just say what you want changed. It'll edit the HTML
and hand back the updated files.
