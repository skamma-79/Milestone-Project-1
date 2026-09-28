# Milestone 1 — Project Brief: Happy Coding

> Ye file project ka full context hai. Agent AI ko `AI_RULES.md` ke saath ye bhi do.

---

## 1. Project Snapshot

| Field | Value |
|-------|-------|
| Business type | Coaching Center |
| Name | Happy Coding |
| Location | Jaipur |
| Category | Option A — Local Business Website |
| Approach | Plain HTML + Tailwind CSS (no framework) |
| Status | Site already built → needs auditing/fixing against rubric |

---

## 2. Required Pages (Domain-Mapped for a Coaching Center)

Rubric ke 4 generic pages ko coaching-center context me is tarah map karo:

### a) Home

- **Hero section:** "Happy Coding" ka tagline (e.g., "Master Coding, Master Your Future") + CTA button ("Enroll Now" / "View Courses")
- **Highlights strip:** e.g., "500+ Students Trained", "10+ Years Experience", "95% Placement Rate" — ye Flexbox row me achha lagta hai
- **Testimonials:** 2-3 student reviews (card layout)

### b) Services / Courses page
*(ye "Menu" ka coaching-center equivalent hai)*

- **Course cards:** "Web Development Bootcamp", "DSA + Interview Prep", "Python for Beginners", "Full Stack Program" — CSS Grid me arrange karo (2-3 columns)
- Har card me: course name, duration, ek line description, "Know More" button
- **Pricing table** (domain must-have): batch fees compare karta hua table/cards — e.g., "Basic / Standard / Premium" batch

### c) Gallery

- Classroom photos, students working, workshop/event photos
- Responsive image grid (CSS Grid, `grid-template-columns` with `auto-fit`/`minmax` for responsiveness)

### d) Contact / Enroll

- Accessible form: Name, Phone, Email, Course dropdown (jo course interested hain), Message
- Address + Google Map embed
- Business hours ("Mon-Sat, 9 AM - 7 PM")

### Domain must-haves (mat bhoolna, rubric me directly check hoga)

- [ ] Pricing / batch table
- [ ] "Why Choose Happy Coding" section (Flexbox — icons + short text, e.g., "Expert Mentors", "Live Projects", "Placement Support")
- [ ] Business hours + clear CTA buttons on every page

---

## 3. Technical Audit Checklist (Apni Existing Site Pe Ye Check Karo)

### HTML

- [ ] Har page me sirf ek `<h1>` hai (aksar log gallery/contact page pe bhool jaate hain)
- [ ] `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` use hue hain — `<div>` ka overuse nahi
- [ ] Contact form: har input ka `<label for="id">` linked hai (sirf placeholder text kaafi nahi hai — accessibility fail hoga)
- [ ] Input types sahi hain: `type="email"`, `type="tel"`, dropdown ke liye `<select>`
- [ ] Har `<img>` ka meaningful alt text — "image1.jpg" jaisa generic alt nahi, balki "Students coding during a Happy Coding workshop" jaisa descriptive

### CSS / Tailwind

- [ ] **Grid** kisi ek major section me use hua hai (courses grid ya gallery)
- [ ] **Flexbox** kisi doosre major section me (highlights strip, "why choose us", navbar)
- [ ] Max 2 font families — mixed nahi honi chahiye
- [ ] Consistent color palette (Tailwind config ya utility classes se)
- [ ] Har button/link pe `hover:` aur `focus:` states hain (keyboard navigation ke liye focus important hai — log bhool jaate hain)
- [ ] Koi inline `style=""` attribute nahi kahin bhi
- [ ] Dark mode: `dark:` variant use kiya hai ya toggle button banaya hai

### Responsive Design

- [ ] Chrome DevTools me **375px, 768px, 1280px** — teeno pe test karo
- [ ] Koi horizontal scroll nahi (common bug: fixed-width images ya overflow wale grids)
- [ ] Mobile pe navbar hamburger menu me collapse hota hai (agar nahi, ye ek gap hai)

---

## 5. Suggested Action Plan (Since Site Already Ready Hai)

1. Pehle upar wali checklist se apni site **audit** karo — jo bhi ❌ mile use note kar lo
2. Missing items **fix** karo (ek-ek karke, commit karte jao)
3. **Git branches + PR** structure set karo (agar abhi tak sirf `main` pe kaam kiya hai)
4. **Deploy** karo aur mobile data pe test karo
5. Presentation ke liye ek line ready rakho: **"sabse mushkil kya tha aur kaise solve kiya"** (rubric me directly poochha jaata hai)

---

## 6. Presentation — Exact 7 Min Breakdown

| Time | Kya karna hai |
|------|---------------|
| 0:00–0:30 | "Maine Happy Coding coaching center ke liye website banayi hai — Option A (Local Business) choose kiya kyunki main real-world business logic samajhna chahta tha" |
| 0:30–3:30 | **Live demo** — Home → Courses → Gallery → Contact, desktop pe. Phir DevTools se resize karke mobile view live dikhao |
| 3:30–5:30 | **Code walkthrough** — ek section kholo (jaise Courses page) aur bolo: "Yahan maine CSS Grid use kiya kyunki courses ko 2D layout me arrange karna tha (rows + columns), aur navbar me Flexbox use kiya kyunki wo sirf ek row me align karna tha" |
| 5:30–6:30 | **GitHub** dikhao — commit history (10+ commits), branches (main + feature/contact-form), merged PR |
| 6:30–7:00 | "Sabse mushkil part X tha (e.g., form validation ya responsive navbar), maine ye solve kiya isse (e.g., media queries se / Tailwind ke `md:` prefix se)" |


## 7. Grading Rubric — 100 Marks

| Criteria | Marks | Iska matlab tumhare project ke liye |
|----------|:-----:|-------------------------------------|
| **Requirements coverage** | **40** | Checklist ka har item (Section 3) — sabse zyada weight yahi hai |
| Code quality & structure | 20 | Clean HTML, sahi class naming, files organized |
| Git hygiene + deployment | 15 | Commits, branches, PR, live link kaam kar raha ho |
| Presentation & Q&A | 15 | Confidence + samajh (memorized nahi, genuine understanding) |
| Polish & UX | 10 | Spacing, typography, dark mode consistency |

👉 Sabse zyada marks (40) requirements coverage me hain — isliye **Section 3 ki checklist sabse important hai**, usko skip mat karna.

---

## 8. Rules (Important — Especially Rule 2)

1. **Individual work** — ideas discuss kar sakte ho, code khud likhna hai
2. **AI allowed for learning/debugging**, lekin Q&A me har line explain karni hogi — agar explain nahi kar paye toh marks katenge. Isiliye jab bhi AI code de, use samajh ke hi aage badhna, copy-paste mat karna bina samjhe
3. **No templates / theme clones** — design inspiration lena fine hai, copied code nahi
4. **2-week window** ke andar submit karna hai — incomplete-but-deployed, complete-but-local se better hai