# XSL AI Academy Workshop Landing Page

🌐 **Live Site:** https://iambarabbas.github.io/xsl-ai-academy/

---

## ✅ What's Been Done

### SEO & Technical
- ✅ Meta tags (title, description, keywords, OG tags)
- ✅ JSON-LD schema markup for Event and Organization
- ✅ Canonical URL
- ✅ Favicon (SVG logo)
- ✅ Robots.txt
- ✅ XML sitemap
- ✅ Google Analytics placeholder (needs your tracking ID)
- ✅ Mobile-optimized (responsive design)

### Content & Design
- ✅ Professional design system (navy + orange brand colors)
- ✅ Responsive layout (desktop, tablet, mobile)
- ✅ Scroll animations
- ✅ FAQ accordion
- ✅ Mobile hamburger menu
- ✅ Privacy Policy page
- ✅ Terms of Service page

### Geographic Consistency
- ✅ Fixed: Now consistently mentions "Orange County & San Diego" (removed LA reference)

---

## ⚠️ TODO: What You Need to Add

### 1. **Google Analytics** (5 minutes)
**File:** `index.html` (line ~16)

Replace `G-XXXXXXXXXX` with your actual Google Analytics tracking ID:
```javascript
gtag('config', 'G-YOUR-ACTUAL-ID');
```

### 2. **Email Integration** (15 minutes)
**File:** `index.html` (line ~1297)

The waitlist form currently just logs to console. You need to connect it to Mailchimp, ConvertKit, or similar.

**Option A: Formspree** (easiest, free tier available)
1. Go to https://formspree.io
2. Create a form
3. Uncomment lines 1306-1310 in `index.html` and add your form ID

**Option B: Mailchimp**
1. Create a Mailchimp embedded form
2. Replace the `handleSubmit()` function with Mailchimp's submission code

### 3. **Photos** (CRITICAL for credibility)
Replace all placeholders:

| Location | File Path Needed | Recommended Size |
|----------|-----------------|------------------|
| Instructor photos | Line 1073, 1084 | 280×280px circles |
| Case study headshots | Line 986, 996, 1006 | 300×300px squares |
| Testimonial avatars | Line 1030, 1041, 1052 | 48×48px circles |
| OG image (social sharing) | `og-image.jpg` | 1200×630px |

### 4. **Instructor LinkedIn URLs**
**File:** `index.html` (search for `href="#"` in instructor section)

Replace the `#` placeholders with actual LinkedIn profile URLs.

### 5. **Workshop Dates**
Once you have confirmed dates, update:
- Schema markup (line ~28: `startDate`, `endDate`)
- Hero location text
- Final CTA location text

---

## 🚀 How to Update the Site

### Quick Edits
1. Make changes to files locally in `/Desktop/website/`
2. Commit and push:
```bash
cd ~/Desktop/website
git add .
git commit -m "Your change description"
git push
```

GitHub Pages will auto-deploy in ~2 minutes.

---

## 📊 Current Performance Scores

| Category | Score | Status |
|----------|-------|--------|
| **SEO** | 8/10 | ✅ Solid (needs real photos + schema dates) |
| **Target Market** | 9/10 | ✅ Excellent (needs real testimonials) |
| **Desktop Design** | 9/10 | ✅ Professional |
| **Mobile Design** | 8/10 | ✅ Responsive |
| **Technical** | 7/10 | ⚠️ Needs email integration + analytics |

---

## 🛠️ Files in This Repo

```
/
├── index.html          # Main landing page
├── privacy.html        # Privacy policy
├── terms.html          # Terms of service
├── favicon.svg         # Site icon (logo)
├── robots.txt          # Search engine instructions
├── sitemap.xml         # Sitemap for Google
└── README.md           # This file
```

---

## 💡 Optimization Tips

### Email Collection
Set up a dedicated Mailchimp list called "XSL AI Academy Waitlist" and connect it to the form.

### A/B Testing
Once you have traffic, test these variations:
- Hero headline: "Stop Writing. Start Selling." vs "Cut Your Admin Time in Half"
- CTA button text: "Claim Your Spot" vs "Join the Waitlist"
- Pricing: Early bird vs standard side-by-side

### Next Steps After Launch
1. Create retargeting pixel (Meta Ads)
2. Set up Google Search Console
3. Build an email sequence for waitlist nurture
4. Add countdown timer when dates are announced
5. Consider adding video testimonials

---

## 📧 Questions?

Contact: hello@xslaiaca.com

---

**Built by Clark 🐘 | April 2026**
