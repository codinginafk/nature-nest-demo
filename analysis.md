# Nature Nest — Skill & Tool Analysis

## Research Sources

| Source | Status | Key Findings |
|--------|--------|-------------|
| Instagram @naturenest0001 | ⚠️ Blocked (login wall) | Couldn't scrape feed for visual inspiration — recommend you share screenshots |
| Reddit r/DigitalMarketing | ⚠️ Blocked (403) | Network policy — couldn't access the discussion thread |
| Ahrefs Blog /claude-skills/ | ⚠️ Partial (CSS only) | Article content blocked by rendering requirements |
| GitHub: awesome-design-skills | ✅ Full README | 67 design system skills for AI tools |
| GitHub: Agentic-SEO-Skill | ✅ Full README | 16 sub-skills, 10 agents, 89 scripts |
| GitHub: agent-analytics-skill | ✅ Full README | AI bot traffic + agent analytics |

---

## 1. Design Skills (awesome-design-skills)

**What it is:** A curated registry of 67 design system skill files (SKILL.md + DESIGN.md) for AI-powered coding agents like Claude Code, Cursor, and Codex. Pull any design style with `npx typeui.sh pull <skill>`.

### Recommended for Nature Nest

| Skill | Why | Priority |
|-------|-----|----------|
| **Cafe** | Warm, cozy, inviting — matches a handcrafted candle brand perfectly. Earthy tones, soft textures, artisan feel. | 🔴 Top Pick |
| **Artistic** | Creative, expressive layouts. Works well for a brand that sells art objects (wax flowers, sculpted candles). | 🔴 Top Pick |
| **Clean** | Ensures the site doesn't feel cluttered. Clean typography and whitespace to let product imagery breathe. | 🟡 Secondary |
| **Claymorphism** | Soft, tactile 3D feel — mimics the handcrafted, molded nature of wax products. Subtle but effective. | 🟡 Secondary |
| **Colorful** | For product category pages and seasonal collections — adds warmth and variety. | 🟢 Nice-to-have |
| **Bento** | Modern grid layouts for product showcases and collection pages. | 🟢 Nice-to-have |

**Skills to skip for this brand:** Brutalism, Corporate, Enterprise, Dramatic, Dithering, Cosmic — these aesthetics clash with the natural, warm brand identity.

### How to Use
```bash
npx typeui.sh pull cafe
npx typeui.sh pull artistic
npx typeui.sh pull clean
```
Each pull places a SKILL.md in your project that gives your AI coding assistant design rules.

---

## 2. SEO Skills (Agentic-SEO-Skill)

**What it is:** An LLM-first SEO analysis skill with 16 specialized sub-skills, 10 specialist agents, and 89 utility scripts. Has an **E-commerce industry template** built in.

### Integration Priority for Nature Nest

| Sub-Skill | Why It Matters for an Ecommerce Candle Site | Priority |
|-----------|-------------------------------------------|----------|
| **SEO Audit** | Baseline full-site health check. First thing to run. | 🔴 Critical |
| **SEO Technical** | Crawlability, Core Web Vitals, mobile-first indexing. Ecommerce sites are heavy — performance is make-or-break. | 🔴 Critical |
| **SEO Content** | E-E-A-T scoring for product descriptions. Candle descriptions need to be unique, detailed, and trustworthy. | 🔴 Critical |
| **SEO Schema** | Product schema (price, availability, reviews), Organization schema, BreadcrumbList. Essential for rich results in Google. | 🔴 Critical |
| **SEO Images** | Product images need alt text, responsive srcset, lazy loading, proper compression. Ecommerce lives and dies by images. | 🔴 Critical |
| **SEO Sitemap** | XML sitemaps for product pages, categories, blog. Auto-generation as inventory changes. | 🟡 High |
| **SEO GEO** | Optimize for AI overviews — "best handmade candles UAE" type queries. Growing channel. | 🟡 High |
| **SEO AEO** | Featured snippets for how-to content (candle care guides, DIY tutorials). | 🟡 High |
| **SEO Competitors** | Analyze competing candle brands' SEO strategies. Know what you're up against. | 🟢 Medium |
| **SEO Plan** | Strategic plan with the built-in E-commerce template. Topical clusters around candles, wax art, home fragrance. | 🟢 Medium |
| **SEO Links** | Internal linking structure for product categories + backlink strategy. | 🟢 Medium |
| **SEO Hreflang** | If expanding to multiple UAE languages (Arabic + English). | 🟢 Later |
| **SEO Programmatic** | If auto-generating product variant pages at scale. | 🟢 Later |
| **SEO GitHub** | For the site's code repository SEO (if open source). | ⚪ Skip |

### Recommended Workflow
1. Run `audit_runner.py` → get full-site audit JSON + HTML dashboard
2. Run `pagespeed.py` → Core Web Vitals evidence
3. Run `crawl_audit.py` → multi-page crawl for metadata, status, dupes
4. Run `validate_schema.py` → check product schema
5. Generate report with `generate_report.py`
6. Apply findings → re-audit in 30 days

**Critical rules enforced by this skill:**
- INP not FID (Google replaced FID Sep 2024)
- FAQ schema restricted (only government/healthcare)
- HowTo schema deprecated (Sep 2023)
- JSON-LD only, never Microdata or RDFa
- E-E-A-T applies to ALL competitive queries (since Dec 2025)
- 100% mobile-first indexing (since Jul 2024)

---

## 3. Agent Analytics (siteline-ai/agent-analytics-skill)

**What it is:** Server-log analysis tool that classifies 30+ AI bots and tracks AI-referred human traffic. Tells you what ChatGPT, Claude, Gemini etc. are asking about your site.

### Recommendation: Post-Launch Tool

This skill is **not needed during the design/build phase**. It becomes valuable after the site is live to:
- See which AI platforms cite your content
- Find technical issues blocking AI crawlers
- Identify content gaps that AI users are searching for
- Track AI → human conversion (ChatGPT users clicking through to your site)

**Setup when ready:** Connect Cloudflare MCP server (free plan works) and run the SKILL.md with Claude.

---

## 4. Reddit & Ahrefs (Blocked)

Both sources were unreachable due to network restrictions:
- **Reddit:** 403 Forbidden
- **Ahrefs:** Article content rendered via JavaScript, raw HTML only returned CSS

If they're important, you can:
- Share screenshots of the relevant Reddit thread
- Share the Ahrefs article as a saved HTML or text file

---

## 5. Design Decisions for the Demo

### Brand Translation (Instagram → Web)

Based on the brand name "Nature Nest" and product line (handmade wax, candles, wax flowers):

| Element | Choice | Rationale |
|---------|--------|-----------|
| **Primary Color** | Deep sage green (#2d5a3f) | Nature, calm, premium |
| **Accent** | Warm terracotta (#c17f59) | Warmth, handmade, earthy |
| **Background** | Cream (#faf7f2) | Clean, natural, airy |
| **Typography** | Playfair Display + Inter | Elegant but readable |
| **Layout** | Organic, flowing sections | Feels handcrafted, not templated |
| **Imagery** | Botanical, warm-toned | Matches wax/nature theme |
| **Tone** | Warm, personal, artisan | "Made by hand" story |

### What's Built in the Demo

- ✅ Full responsive single-page preview
- ✅ Sticky navigation with scroll effect
- ✅ Hero section with brand tagline + CTA
- ✅ 4 product cards with SVG illustrations
- ✅ 3 category banners (Candles / Wax Flowers / DIY Kits)
- ✅ About section with brand story + value props
- ✅ Customer testimonials
- ✅ Instagram feed teaser (6 placeholder slots)
- ✅ Newsletter signup
- ✅ Full footer with shop/help/company links
- ✅ Scroll animations (fade-in)
- ✅ Toast notifications (cart simulation)
- ✅ Mobile responsive

### What's NOT Built (intentionally — this is a preview)

- ❌ Real cart/Shopping cart page
- ❌ Product detail pages
- ❌ Checkout flow
- ❌ Search functionality
- ❌ Account/login system
- ❌ Real product data
- ❌ Payment integration
