# Lesson 2 — HTML + CSS: Drawing Your First Page (The Skeleton + The Clothes)

## The story (for a 10-year-old)
Every webpage is like a **skyscraper**:
- **HTML** = the skeleton (walls, floors, rooms). It says WHAT is on the page.
- **CSS** = the clothes (paint, wallpaper, colors). It says HOW it LOOKS.

We'll build a **landing page** for our demo app (a "PetSitter" real-time app — a site where pet owners find sitters).

---

## What is HTML?

HTML = **H**yper **T**ext **M**arkup **L**anguage.
It's just **tags** that wrap your content:
- `<h1>` = big title
- `<p>` = paragraph (paragraphs = groups of sentences)
- `<a>` = a link
- `<button>` = a clickable button
- `<div>` = a box that holds other stuff
- `<img>` = an image

## What is CSS?

CSS = **C**ascading **S**tyle **S**heets.
It paints the HTML:
- `color` = text color
- `background` = box color
- `font-size` = text size
- `border-radius` = rounded corners
- `display: flex` = arrange boxes nicely (like arranging toys in a row)
- `padding` = space inside the box
- `margin` = space outside the box
- `@media` = rules for small screens (mobile)

---

## The landing page code

### File: `src/index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PetSitter — Find a sitter for your pet</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header class="navbar">
    <div class="logo">🐾 PetSitter</div>
    <nav>
      <a href="#features">Features</a>
      <a href="#how">How it works</a>
      <a href="#signup">Sign up</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Your pet's best friend is one click away</h1>
    <p>Find trusted sitters near you — real-time updates, so you always know how your pet is doing.</p>
    <button onclick="alert('Signed up! 🎉')">Get Started — It's Free</button>
  </section>

  <section id="features" class="features">
    <h2>Why choose PetSitter?</h2>
    <div class="card-grid">
      <div class="card">
        <h3>📡 Live Updates</h3>
        <p>See photos and messages from your sitter in real time.</p>
      </div>
      <div class="card">
        <h3>✅ Trusted Sitters</h3>
        <p>Every sitter is checked and rated by real pet owners.</p>
      </div>
      <div class="card">
        <h3>💳 Pay Simple</h3>
        <p>One plan, no hidden fees. Cancel anytime.</p>
      </div>
    </div>
  </section>

  <section id="how" class="how">
    <h2>How it works</h2>
    <ol>
      <li>Tell us your pet's name and needs.</li>
      <li>We match you with a nearby sitter.</li>
      <li>Sit! And watch the live updates pour in.</li>
    </ol>
  </section>

  <section id="signup" class="signup">
    <h2>Ready to try it?</h2>
    <button>Sign up free</button>
  </section>

  <footer>
    <p>© 2026 PetSitter</p>
  </footer>
</body>
</html>
```

### File: `src/style.css`

```css
/* --- Basic reset (makes every browser look the same) --- */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  line-height: 1.6;
  color: #1f2937;
  background: #f8fafc;
}

/* --- Navigation bar --- */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background: #1e293b;
  color: white;
}
.navbar .logo { font-size: 1.4rem; font-weight: bold; }
.navbar nav a {
  color: #cbd5e1;
  text-decoration: none;
  margin-left: 1.5rem;
}
.navbar nav a:hover { color: white; }

/* --- Hero section --- */
.hero {
  text-align: center;
  padding: 5rem 2rem;
  background: linear-gradient(135deg, #0ea5e9, #6366f1);
  color: white;
}
.hero h1 { font-size: 2.5rem; margin-bottom: 1rem; }
.hero p { font-size: 1.2rem; margin-bottom: 2rem; max-width: 600px; margin-inline: auto; }
.hero button {
  padding: 0.8rem 2rem;
  font-size: 1.1rem;
  border: none;
  border-radius: 8px;
  background: white;
  color: #6366f1;
  cursor: pointer;
}

/* --- Features grid --- */
.features { padding: 3rem 2rem; max-width: 1100px; margin: auto; }
.features h2 { text-align: center; margin-bottom: 2rem; }
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}
.card {
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}

/* --- How it works --- */
.how { padding: 3rem 2rem; background: white; }
.how h2 { text-align: center; margin-bottom: 1rem; }
.how ol { max-width: 600px; margin: auto; padding-left: 1.5rem; }
.how li { margin-bottom: 0.5rem; }

/* --- Signup --- */
.signup { text-align: center; padding: 3rem 2rem; background: #f1f5f9; }
.signup button { padding: 0.8rem 2rem; border: none; border-radius: 8px; background: #6366f1; color: white; cursor: pointer; }

/* --- Footer --- */
footer { text-align: center; padding: 1rem; background: #1e293b; color: #cbd5e1; }

/* --- Mobile responsive --- */
@media (max-width: 600px) {
  .hero h1 { font-size: 1.6rem; }
  .navbar { flex-direction: column; gap: 0.5rem; }
}
```

## How to open it
1. Save both files in a folder called `src/`.
2. In VS Code, open the project folder.
3. Press `` Ctrl + ` `` to open the terminal.
4. Type:
```
npx serve src
```
(First time? Run `npm install -g serve` then `npx serve src`.)
5. A browser tab opens — that's your landing page!
6. Resize the browser window — the page adapts to mobile width (that's **responsive design**).

## Key ideas to remember
| Concept | What it does |
|---|---|
| `<!DOCTYPE html>` | Tells the browser "this is HTML5" |
| `<meta name="viewport" ...>` | Makes the page shrink properly on phones |
| `class="..."` | A label we use in CSS to style a box |
| `display: flex` / `grid` | Arranges boxes in rows/columns |
| `@media (max-width: 600px)` | Only applies when screen is smaller than 600px |

## Homework (15 min)
1. Open `index.html` in your browser (just double-click it).
2. Change the **title**, **hero text**, and **card content** to your own idea (e.g., a tutoring app, a pizza shop).
3. Change the colors in `style.css` (try `background: #f97316` for orange).
4. Take a screenshot of both desktop and mobile-width views (make your browser window narrow).

> Next lesson: Git + GitHub — how to save versions of your work and show it online.

---

## 🧭 Checkpoint — Where we left off
- **Saved:** `state.json` at `2026-10-05T13:19:00Z` — "Wrote lessons/02-html-css-landing.md, src/index.html, src/style.css. Lesson files and source code saved on disk."
- **Current:** Lesson 2 code is written. **Homework:** open `src/index.html` in a browser, customize the text/colors, screenshot desktop + mobile views.
- **Current files:** `src/index.html` (page), `src/style.css` (styling).
- **Next lesson:** Git + GitHub workflow.
- **To resume:** tell me "continue" or edit `state.json` → `currentLesson`.
