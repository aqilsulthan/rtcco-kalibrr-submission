# 01: Brainstorm - Aqil Sulthan

## Langkah

### 1. Kirim Prompt ke AI

```
Role: UX/UI consultant untuk portfolio developer.
Task: Bantu brainstorm desain portfolio untuk Cloud Engineer.

Context:
- Nama: Aqil Sulthan
- Skills: Cloud infrastructure (AWS, Docker, Terraform), DevOps, Monitoring
- Target: Perusahaan teknologi / startup
- Role target: Cloud Engineer

Constraints:
- Mobile-first
- Simple tapi stand out
- Zero JavaScript (CSS-only interactions)
- Semantic HTML5 (zero <div>)
- Warna: profesional, techy

Output:
1. 3 color palette options
2. Typography recommendation
3. Section structure
4. 1 unique element
```

### 2. Lanjutkan Diskusi

- **"Kenapa pilih indigo + cyan?"** - Memberi kesan tech/modern tanpa terlihat seperti template Bootstrap. Indigo memberi otoritas, cyan memberi sentuhan segar.
- **"Inter vs Poppins?"** - Poppins untuk headings (bold, modern), Inter untuk body text (highly readable di layar).
- **"Single page vs multi-page?"** - Single page, recruiter bisa scroll semua dalam 1-2 menit.
- **"Bagaimana beda dari candidate lain?"** - CSS-only filter proyek + hamburger menu tanpa JavaScript, layout semantic murni tanpa satu pun `<div>`.

---

## Dokumentasi

### Prompt 1 - Brainstorm Desain

```
Role: UX/UI consultant untuk portfolio developer.
Task: Bantu brainstorm desain portfolio untuk Cloud Engineer.
Context: Nama Aqil Sulthan, skills cloud infrastructure, target perusahaan teknologi.
Constraints: Mobile-first, zero JS, semantic HTML, zero <div>.
Output: 3 palette, typography, section structure, 1 unique element.
```

### AI Response 1

```
Palette rekomendasi:
1. Indigo (#6366f1) + Cyan (#06b6d4) + Neutral slate - techy, profesional
2. Emerald (#10b981) + Navy (#1e293b) - growth, stabil
3. Rose (#f43f5e) + Warm gray - bold, kreatif

Typografi:
- Heading: Poppins (bold, modern, tegas)
- Body: Inter (clean, high legibility)
- Scale: clamp() untuk fluid typography

Section structure:
1. Hero - nama, title, tagline, 2 CTA
2. Tentang - foto profil + bio + quote
3. Skills - 3 kategori card (grid)
4. Proyek - card grid + filter kategori
5. Kontak - form + social links
6. Footer - copyright + links

Unique element: CSS-only filter untuk proyek (radio button hack)
```

**Keputusan:** Pilih palette Indigo + Cyan, Poppins + Inter, semantic HTML murni.

---

### Prompt 2 - Detail Warna & Aksesibilitas

```
Dari opsi yang diberikan, saya pilih palette indigo + cyan.
Bantu refine color palette dengan memperhatikan WCAG contrast ratio.
```

### AI Response 2

```
Primary: #6366f1 (indigo 400), #4f46e5 (indigo 500), #4338ca (indigo 600)
Secondary: #06b6d4 (cyan 400), #0891b2 (cyan 500)
Neutral: Dari #f8fafc sampai #0f172a (slate scale)
→ Contrast ratio >= 4.5:1 di semua kombinasi text-background
```

---

### Prompt 3 - Validasi Layout

```
Review section structure untuk single page portfolio Cloud Engineer.
Apakah ada section yang perlu ditambah/dikurangi?
```

### AI Response 3

```
Struktur sudah optimal. Saran tambahan:
- Hero: tambah gradient text untuk nama (indigo → cyan)
- Skills: card dengan tech stack tags
- Proyek: tambah filter dengan radio button hack
- Kontak: validasi form visual dengan :valid/:invalid
- Navigation: hamburger dengan checkbox hack (CSS-only)
```

---

## Key Decisions

| Decision | Value | Why |
|----------|-------|-----|
| Color | Indigo (#6366f1) + Cyan (#06b6d4) | Techy, profesional, contrast >= 4.5:1 |
| Typography | Poppins (heading) + Inter (body) | Modern, readable, pairing solid |
| Layout | Single page, 6 sections | Recruiter bisa scan cepat |
| Style | Glassmorphism nav, gradient hero, card grid | Modern tanpa framework |
| Unique Element | CSS-only filter proyek (radio hack) | Zero JS, impressive untuk technical role |
| HTML Approach | Zero `<div>` - semantic elements only | Membuktikan pemahaman HTML semantic |

---

## Minimum Requirements

- ✅ Minimal 3 prompts
- ✅ 3+ decisions documented
- ✅ Reasoning untuk setiap decision
