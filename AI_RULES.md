# AI RULES — Happy Coding Website (Milestone 1

---

## 1. Project Context

- Business: **Happy Coding** — Coaching Center, Jaipur
- Type: Option A — Local Business Website
- Stack: **Plain HTML + Tailwind CSS only** (no React, no Next.js, no framework, no build tool jab tak main na bolun)
- Status: Site pehle se bani hui hai. Kaam = **audit + fix**, rebuild nahi.
- Ye ek **individual assessment** hai. Main is code ko presentation me line-by-line explain karunga.

---

## 2. Golden Rules (sabse important)

1. **Sirf wahi change karo jo maine maanga hai.** Extra refactor, redesign, rename, ya "improvement" mat karo.
2. **Existing code ko delete ya rewrite mat karo** bina mujhse poochhe.
3. **Naye files/folders mat banao** bina permission ke.
4. **Koi framework, library, plugin, ya npm package add mat karo.** Plain HTML + Tailwind hi rahega.
5. **Pura file dobara mat likho.** Sirf changed part dikhao aur batao kahan jaata hai.
6. **Ek baar me ek hi kaam.** Multiple sections ek saath mat badlo.
7. Agar request unclear hai, **pehle sawaal poochho**, andaza mat lagao.
8. Agar mera approach galat/weak hai, seedha bolo aur reason batao.

---

## 3. Learning Rule (Rule #2 of the assessment)

- Code dene ke baad **har important line ka reason samjhao** (kya karta hai, kyun use hua).
- Chhote, samajhne layak chunks me code do. Ek saath 200 lines mat do.
- Jahan relevant ho, alternative aur trade-off batao.
- Mujhe hint ya approach pehle do; poora solution tab do jab main maangun.
- Aisa code mat likho jo main presentation me explain na kar sakun (over-clever tricks, unnecessary abstractions).
- **Templates / theme clones / copied code mat do.** Design inspiration theek hai, copy-paste layouts nahi.

---

## 4. Required Pages (structure change mat karna)

| Page | Must contain |
|------|-------------|
| **Home** | Hero + tagline + CTA, highlights strip (Flexbox), "Why Choose Happy Coding" (Flexbox), testimonials (2–3 cards) |
| **Courses** | Course cards in **CSS Grid** (2–3 cols): name, duration, one-line description, "Know More" button. **Pricing table** (Basic / Standard / Premium) |
| **Gallery** | Responsive image grid: `grid-template-columns` with auto-fit/minmax (Tailwind equivalent) |
| **Contact / Enroll** | Form (Name, Phone, Email, Course dropdown, Message), address + Google Map embed, business hours (Mon–Sat, 9 AM – 7 PM) |

- Har page par **clear CTA button** hona chahiye.
- Pages ke naam, count, ya navigation structure bina poochhe mat badlo.

---

## 5. HTML Rules

- Har page me **sirf ek `<h1>`**.
- Semantic tags use karo: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`. `<div>` ka overuse nahi.
- Heading hierarchy sahi rahe (h1 → h2 → h3, koi level skip nahi).
- Form:
  - Har input ka `<label for="id">` linked ho (sirf placeholder kaafi nahi).
  - Sahi types: `type="email"`, `type="tel"`, course ke liye `<select>`.
- Har `<img>` par **descriptive alt text** (e.g., "Students coding during a Happy Coding workshop"). "img1", "photo", "image1.jpg" jaisa alt nahi.
- **Koi inline `style=""` attribute nahi.**

---

## 6. CSS / Tailwind Rules

- **CSS Grid** kisi ek major section me (courses ya gallery), **Flexbox** doosre major section me (navbar, highlights, why-choose-us).
- Har layout choice ka reason batao: Grid = 2D (rows + columns), Flexbox = 1D (ek row/column alignment).
- **Max 2 font families.**
- Ek **consistent color palette** (Tailwind config ya fixed utility classes). Random colors mat add karo.
- Har button aur link par **`hover:` aur `focus:`** states (keyboard accessibility).
- **Dark mode**: `dark:` variants ya toggle button, poori site me consistent.
- Mobile-first approach: base classes mobile ke liye, phir `md:` / `lg:` prefixes.

---

## 7. Responsive Rules

- Test breakpoints: **375px, 768px, 1280px**.
- Koi **horizontal scroll nahi** (fixed-width images aur overflow wale grids se bacho).
- Mobile par navbar **hamburger menu** me collapse ho.
- Images responsive ho (`max-w-full`, `h-auto` ya `object-cover` with fixed aspect ratio).

---

## 8. Images & Paths

- Sab image paths **relative** rakho (deploy par images break na ho).
- Absolute local paths (`C:\...`, `/Users/...`) kabhi mat use karo.
- Image file names meaningful hon (`classroom-workshop.jpg`, na ki `img1.jpg`).

---

## 9. README.md Must Include

- Project description
- Pages list
- Tech used
- Live link
- Screenshots

---

## 10. Audit Mode (jab main "audit karo" bolun)

Sirf **report** do, code mat badlo. Format:

```
✅ Passed: ...
❌ Failed: file name + line + kya galat hai
⚠️ Suggested fix: (sirf batao, apply mat karo)
```

Check karo: single h1, semantic tags, labels, input types, alt text, inline styles, Grid/Flexbox usage, fonts (max 2), hover/focus states, dark mode, hamburger menu, horizontal scroll, relative image paths, README.

Fix tabhi karo jab main bolun, aur **ek-ek karke**.

---

## 11. Security & Safety

- Koi API key, secret, ya personal data code me mat daalo.
- Contact form ka action/endpoint bina poochhe mat set karo.
- External scripts/CDN sirf Tailwind ke liye (agar already use ho raha hai), aur kuch nahi.

---

## 12. AI ko kya NAHI karna hai (quick list)

- ❌ Design ya layout ko bina bole redesign karna
- ❌ Framework / library / package add karna
- ❌ Pura file overwrite karna
- ❌ Files rename ya delete karna
- ❌ Colors, fonts, ya content apne mann se badalna
- ❌ Bina samjhaye code dena
- ❌ Copied template / theme code dena
- ❌ Aise features add karna jo rubric me nahi hain

---

## 13. Grading Rubric (AI ko yaad rakhna hai)

| Criteria | Marks |
|----------|-------|
| Requirements coverage | 40 |
| Code quality & structure | 20 |
| Git hygiene + deployment | 15 |
| Presentation & Q&A | 15 |
| Polish & UX | 10 |

Har suggestion in criteria ko support kare. Rubric se bahar ki cheezein priority nahi hain.

---

## 14. Response Format (AI ke jawab kaise hone chahiye)

1. Pehle **kya problem hai** aur **kyun**.
2. Phir **minimal fix** (sirf changed code).
3. Phir **short explanation** (main isse presentation me bol sakun).
4. Agar relevant ho: ek line me "Grid kyun / Flexbox kyun / `<section>` kyun `<div>` nahi".
5. Jawab **Hinglish** me ho, simple language me.
