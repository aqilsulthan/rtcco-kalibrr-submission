# 03: Execution - Aqil Sulthan

## Prinsip

```
SETIAP STEP:
1. Kirim prompt ke AI
2. Review output AI
3. Fix jika perlu
4. Lanjut step berikutnya
```

---

## RTCC-O Checklist (Per Prompt)

```
[x] R - Role dispesifikasi?
[x] T - Task konkret?
[x] C - Context cukup?
[x] C - Constraints jelas?
[x] O - Output format ditentukan?
```

---

## Step 1: HTML Semantic Structure

### Prompt

```
R: Senior front-end developer spesialis HTML semantik.
T: Buat struktur HTML5 untuk portfolio single page Cloud Engineer.
C: HTML5 murni, mobile-first, Bahasa Indonesia, audience recruiter.
C: Zero <div>/<span> untuk layout, wajib <header>/<nav>/<main>/<section>/<article>/<footer>, wajib <figure>/<blockquote>/<time> jika relevan, wajib Open Graph tags, wajib skip link, wajib aria-label.
O: Hanya kode HTML dalam 1 file index.html.
```

### RTCC-O Check
- R: ✅
- T: ✅
- C: ✅
- C: ✅
- O: ✅

### AI Response

HTML semantic lengkap dengan 6 section: hero, tentang, skills, proyek, kontak, footer. Zero `<div>`. Navigasi dengan hamburger checkbox hack. Form kontak dengan label eksplisit. Skip link sebagai elemen pertama. Open Graph + meta tags.

### Review
- [✅] Sesuai constraints? - Zero div, semua semantic HTML5
- [✅] Format sesuai? - 1 file index.html
- [✅] Bisa dipahami? - Struktur jelas, comments bersih
- Changes: Tambah checkbox hack untuk menu, tambah filter radio inputs

---

## Step 2: CSS Global + Hero + Navigation

### Prompt 2a - CSS Global Styles

```
R: CSS architect spesialis design system.
T: Buat CSS base: custom properties, reset, typography, utility classes.
C: CSS3 murni, mobile-first, no preprocessor.
C: Wajib CSS variables di :root, wajib clamp() fluid typography, wajib utility classes (.container, .section-title, .btn), wajib Google Fonts @import, no media queries.
O: 1 file style.css.
```

### AI Response

CSS variables lengkap (warna indigo+cyan, neutral slate, font scale, spacing, shadow, radius). Reset box-sizing. Typography Inter + Poppins. Utility: .section-title (dengan underline gradient), .btn-primary/secondary, .skip-link.

### Review
- [✅] Sesuai constraints? - Zero media queries, full variables
- [✅] Format sesuai? - 1 file
- [✅] Bisa dipahami? - Terorganisir per section

### Prompt 2b - Navigation & Hero

```
R: Front-end developer CSS layout.
T: Style nav sticky + hero section, mobile-first.
C: CSS3 murni, pakai custom properties yang sudah ada.
C: Nav sticky dengan glassmorphism, hamburger CSS-only (checkbox), hero 100svh dengan gradient text, zero JS, zero <div>.
O: Tambahan CSS untuk style.css.
```

### AI Response

Sticky header dengan backdrop-filter blur. Hamburger animasi (X rotation via checkbox). Drawer slide-in mobile, horizontal desktop. Hero 100svh, gradient text pada nama, radial gradient background, CTA buttons dengan hover effect.

### Review
- [✅] Sesuai constraints? - CSS-only, zero JS
- [✅] Format sesuai? - Append ke style.css
- [✅] Bisa dipahami? - Navigasi responsive

---

## Step 3: Skills + Projects + Contact + Footer + Desktop

### Prompt 3a - About & Skills

```
R: CSS layout specialist.
T: Style tentang + skills section.
C: CSS3 murni, mobile-first.
C: About: foto circular, stacked mobile, grid desktop (foto + teks). Skills: CSS grid 3 card, fadeInUp animation cascade, progress tag styling. Zero <div>.
O: Append ke style.css.
```

### AI Response

About: foto circular clamp(150px, 30vw, 220px) dengan border + shadow, blockquote dengan border-left accent. Skills: card dengan fadeInUp cascade (delay 0.1s per card), tech tags pill styling, hover translateY. Desktop (>=768px): CSS Grid 2 kolom, (>=1024px): 3 kolom.

### Review
- [✅] Sesuai constraints?
- [✅] Format sesuai?
- [✅] Bisa dipahami?

### Prompt 3b - Projects (CSS Filter) + Contact + Footer

```
R: Front-end developer CSS Grid & component design.
T: Style proyek dengan filter CSS-only (radio button) + kontak form + footer.
C: CSS3 murni.
C: Filter proyek: radio button hack, card grid di desktop. Kontak: validasi :valid/:invalid, form grid 2 kolom di tablet. Footer dark. Zero JS, zero <div>.
O: Append ke style.css.
```

### AI Response

Filter tabs dengan 4 kategori (Semua, Frontend, Backend, Fullstack). Radio button hidden, label sebagai tab. Card: hover scale(1.02), image zoom 1.08 melalui overflow. Tech tags warna berbeda (biru, pink, hijau). Kontak: input border berubah hijau/merah berdasarkan validasi. Footer dark dengan flex layout.

### Review
- [✅] Sesuai constraints?
- [✅] Format sesuai?
- [✅] Bisa dipahami?

### Prompt 3c - Desktop Enhancement

```
R: CSS responsive design specialist.
T: Review & polish semua media queries.
C: CSS3 murni, file style.css sudah ada.
C: Semua breakpoint (768px & 1024px) harus optimal. No horizontal scroll. Projects grid 3 kolom desktop. Contact form 2 kolom di tablet. Footer horizontal di tablet.
O: Append ke style.css.
```

### AI Response

Semua media queries dirapikan. Projects: 3 kolom grid di desktop. Skills: 2 kolom tablet, 3 kolom desktop. Contact: 2 kolom grid untuk nama+email. Footer: flex row di tablet. Font size scaling dengan clamp().

### Review
- [✅] Sesuai constraints?
- [✅] Format sesuai?
- [✅] Bisa dipahami?

---

## Step 4: Animations + Accessibility + Content + Final

### Prompt 4a - Animations

```
R: Front-end developer CSS animation.
T: Tambah micro-interactions + stagger animation.
C: CSS3 murni, prefers-reduced-motion support.
C: Hero stagger (h1 → p1 → p2 → CTA1 → CTA2). Skill cards cascade. Project cards hover. Reduced motion support. Zero JS.
O: Append ke style.css.
```

### AI Response

Hero: fadeInUp stagger dengan delay (0s, 0.15s, 0.3s, 0.45s, 0.55s). @keyframes: fadeInUp, fadeIn, slideInLeft, pulse. Reduced motion: semua durasi 0.01ms. Utility classes: .animate-fade-in-up, .animate-fade-in.

### Review
- [✅] Sesuai constraints?
- [✅] Format sesuai?
- [✅] Bisa dipahami?

### Prompt 4b - Accessibility Audit

```
R: Accessibility specialist.
T: Audit & fix aksesibilitas portfolio.
C: WCAG 2.1 AA, HTML5 + CSS3.
C: Skip link, alt text, aria-label, color contrast, focus visible, heading hierarchy, landmark roles, keyboard navigable, prefers-reduced-motion.
O: Checklist + kode fix.
```

### AI Response

Audit selesai. Fix yang diterapkan: nav menu visibility hidden saat closed (removes from a11y tree), filter inputs opacity bukan display:none (tetap accessible), figcaption sr-only bukan display:none, role="list" di navigation ul.

### Review
- [✅] Sesuai constraints?
- [✅] Format sesuai?
- [✅] Bisa dipahami?

### Prompt 4c - Content Personalization

Personalize seluruh konten: nama Aqil Sulthan, title Cloud Engineer, skills cloud infrastructure (AWS, Docker, Terraform, dll), 3 proyek (Cloud Health Monitor, AutoDeploy Pipeline, Health Dashboard), social links GitHub/LinkedIn/Email.

### Review
- [✅] Sesuai constraints?
- [✅] Format sesuai?
- [✅] Bisa dipahami?

---

## Common Mistakes

| Mistake | How to Avoid |
|---------|--------------|
| Prompt terlalu panjang | Pecah jadi step kecil ✅ |
| Skip review | Baca setiap baris output ✅ |
| Copy-paste tanpa paham | Tanya ke AI jika bingung ✅ |
| Lanjut tanpa fix | Fix sebelum next step ✅ |
