# Assignment 7.5 — Solution: Flexbox Mini-Project (Responsive Landing Page)

## Project Structure
```
landing-page/
├── index.html
├── style.css
└── images/
    ├── hero.svg
    ├── icon-speed.svg
    ├── icon-chart.svg
    └── icon-shield.svg
```
The complete code is in the attached files.

## Required Sections
| Section | HTML | Flexbox usage |
|---------|------|---------------|
| **Navigation bar** | `header.site-header` (sticky) with logo, `nav` links and a button | `display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap` |
| **Hero** | `section.hero`: eyebrow tag, `h1`, paragraph, two buttons, note, illustration | `.hero__inner` is a flex row: text left, image right, `align-items: center`, `flex-wrap: wrap`, so the image goes below the text on small screens |
| **3 feature cards** | `section.features`: Fast setup, Simple analytics, Secure hosting | `.features__cards { display: flex; justify-content: center; align-items: stretch; flex-wrap: wrap; gap: 32px; }` and `.feature-card { flex: 1 1 280px; max-width: 360px; }` |
| **Call to action** | `section.cta`: heading, text and a button on a gradient panel | Flex row with `justify-content: space-between; align-items: center; flex-wrap: wrap`; stacks in a column on phones |
| **Footer** | `footer.site-footer`: brand, links, copyright | Flex row with `justify-content: space-between; align-items: center; flex-wrap: wrap` |

There is also a small **"How it works"** section (a flex row of three numbered steps) between the features and the CTA.

## Rules Checklist
| Rule | How it is met |
|------|---------------|
| 1. Flexbox in navbar and hero | See table above |
| 2. Feature cards in a responsive row | `flex: 1 1 280px` + `flex-wrap: wrap`: 3 per row, then 2, then 1 |
| 3. `gap`, `justify-content`, `align-items`, `flex-wrap` | All four are used in the navbar, hero, features, steps, CTA and footer |
| 4. Consistent colors, typography, spacing | CSS variables in `:root` (`--color-*`, `--space-sm/md/lg/xl`, `--radius`); one font stack; one reusable `.button` component with modifiers (`--small`, `--outline`, `--light`) |
| 5. No overflow on small screens | `img { max-width: 100%; height: auto }`, `box-sizing: border-box`, fluid headings with `clamp()`, wrapping flex rows, and a media query at 720px |

## Tested at Different Widths
| Width | Feature cards per row | Horizontal overflow |
|-------|-----------------------|---------------------|
| 1280px | 3 | none |
| 800px | 2 | none |
| 600px | 1 | none |
| 375px | 1 | none |

All images load, and every internal `#anchor` link has a matching section `id`.

## Publish to GitHub
```bash
git init
git add .
git commit -m "Add responsive Flexbox landing page"
git branch -M main
git remote add origin https://github.com/<your-username>/landing-page.git
git push -u origin main
```

## Submission
- ✅ Complete landing page: `index.html`, `style.css` and the `images` folder (attached)
- 🔗 GitHub link: `https://github.com/<your-username>/landing-page`
- 📸 Optional screenshots (attached `screenshot-1280px.png` and `screenshot-375px.png` are references rendered by me)
