# MaintainX Industry Watch — Style Guide

This guide defines the research, curation, writing, and formatting standards for the **MaintainX Industry Watch** newsletter. Written for autonomous use: any future session should read this guide before producing a new issue.

---

## 1. Purpose & Audience

**What it is:** A weekly internal newsletter tracking competitor and industry product releases — "what others shipped, and what it means for MaintainX."

**Primary audience:** MaintainX product managers, designers, and leadership.

**Goal:** Surface competitive signals, UX patterns, and strategic implications — not a news feed. Every item must answer "so what for MaintainX?"

---

## 2. Research Process

### When to run
Weekly, covering roughly the past 1–2 weeks of releases. Check the most recent issue for the last date covered, and pick up from there.

### What to search for
Search for recent product updates, changelog entries, release notes, and funding announcements across three categories (see Section 4).

**Recommended search queries per company:**
- `[Company] changelog [month year]`
- `[Company] product update [month year]`
- `[Company] new feature [month year]`
- `[Company] release notes [month year]`

### Source priority
1. Official release notes / changelog pages (most reliable)
2. Company blog posts announcing features
3. Tech press (TechCrunch, The Verge, VentureBeat) for funding news
4. LinkedIn / Twitter announcements as secondary confirmation

### What qualifies for inclusion
- New features that have **shipped** (not announced, not "coming soon")
- Funding rounds ≥ $50M if strategically relevant to MaintainX's space
- Model releases (foundation models) if they affect tooling or the competitive landscape
- Partner integrations that meaningfully expand a competitor's reach

### What to skip
- Bug fixes and minor patches
- UI refreshes with no functional change
- News without a clear "so what for MaintainX" angle

---

## 3. Watchlist

### Section 1 — Leading AI Products
Broad AI productivity and developer tools that influence UX expectations and AI patterns across all software.

**Core watchlist:**
- Notion (AI, agents, databases)
- Linear (project management AI)
- Cursor (AI coding)
- ChatGPT / OpenAI
- Claude / Anthropic
- Glean (enterprise AI search)
- Intercom (AI support)
- n8n (workflow automation)
- Figma (design + AI)
- Airtable
- Slack / Teams (AI features)

### Section 2 — Interesting AI Startups
Emerging tools and model releases that represent directional signals for where the industry is heading.

**Core watchlist:**
- High-growth AI startups with relevant functionality (agents, voice, vision, document AI)
- New foundation model releases (GPT-5, Gemini, Claude, etc.)
- Funding rounds that signal where capital is flowing in AI infrastructure

**Selection criteria:** Relevance > fame. A niche startup solving a maintenance-adjacent problem beats a big launch with no MaintainX angle.

### Section 3 — CMMS + EAM + Field Service
Direct competitors and adjacent platforms in the maintenance and field operations space.

**Core watchlist:**
- UpKeep
- Limble CMMS
- Fiix (by Rockwell)
- ServiceMax
- IBM Maximo
- SAP PM
- Prometheus Group
- eMaint / Fluke
- ServiceTitan (field service)

---

## 4. Card Count & Layout

- **Total cards per issue:** 8–12
- **Section 1 (AI Products):** 4–6 cards
- **Section 2 (Startups):** 2–4 cards
- **Section 3 (CMMS):** 2–3 cards
- **Layout:** 3-column CSS Grid (`repeat(3, 1fr)`)
- **Featured card:** Optional. One card per issue may be designated "Feature of the Week" if there's a standout release with exceptionally high MaintainX relevance. Use sparingly — max 1 per issue.

---

## 5. Writing Standards

### Card title
Format: `Feature Name — Short descriptor`
- Feature name is what the product team calls it, verbatim where possible
- Descriptor is a punchy phrase, not a full sentence
- Examples:
  - `Custom Agents — Set a job, set a trigger, let it run 24/7`
  - `Required Fields + Locked Tasks — Work orders can't close until the job is done right`
  - `Deeplink to AI Tools — Full issue context, one click`

### Problem field
- **One sentence only**
- Lead with the specific friction, not a generalization
- Present tense ("Users can't..." not "Users couldn't...")
- No hedging ("often," "sometimes") — state the problem directly

**Good:** `Every AI task starts with manual copy-paste — context degrades in the transfer every time.`
**Bad:** `Users sometimes find it difficult to transfer context when starting AI tasks.`

### Solution field
- **One sentence only**
- Lead with what shipped, not how it works
- Include concrete specifics: numbers, scope, integration names
- Present tense

**Good:** `One click opens Cursor or Claude pre-filled with full issue context — description, comments, attachments, all of it.`
**Bad:** `Linear has added a new feature that allows users to deeplink to AI tools with context.`

### MaintainX callout (💡 MaintainX)
This is the most important field. Every callout must do one of three things:
1. **Competitive signal:** What this tells us about what a competitor is prioritizing
2. **UX pattern to adopt:** A specific interaction pattern applicable to MaintainX's context
3. **Strategic opportunity:** A gap or whitespace this release reveals for MaintainX

Rules:
- **One sentence only**
- Be specific — name the MaintainX workflow, screen, or persona affected
- Do not just restate the solution — extrapolate to MaintainX's context
- Use MaintainX vocabulary: work orders (WOs), PMs (preventive maintenance), assets, technicians, SOPs

**Good:** `Tapping a work order should open MaintainX AI pre-loaded with asset history, last failure, and the SOP — zero copy-paste.`
**Bad:** `This is a pattern MaintainX could consider for its AI features.`

### Card link text
Use the most specific label available:
- `Release notes ↗` — preferred for product releases
- `Changelog ↗` — for changelog pages
- `Product page ↗` — when no specific release link exists
- `TechCrunch ↗` / `Blog post ↗` — for press / announcements
- Always include `target="_blank"`

### Dates
- Use `Mon DD` format (e.g., `Feb 24`, `Mar 5`)
- If only the month is known, use `Mon YYYY` (e.g., `Feb 2026`)
- For funding news, append the amount: `Feb 10 · $315M`
- For versioned releases, append the version: `Feb 23 · v5.17`

---

## 6. TLDR Section

The TLDR appears immediately below the header, before the cards. It synthesizes patterns across the full issue — not individual items.

### Format
- Exactly **3 TLDR items** per issue
- Each item: one tag pill + one sentence with a **bolded claim** followed by an em-dash implication
- Structure: `**Bold claim** — one sentence implication.`

### Tag types and when to use them

| Tag | CSS class | Color | Use when... |
|-----|-----------|-------|-------------|
| Category Shift | `tag-shift` | Red | The industry is moving in a new direction |
| UX Pattern | `tag-pattern` | Purple | A specific interaction model is emerging across products |
| User Problem | `tag-problem` | Green | A clear pain point is being validated across products |
| Competitive Signal | `tag-compete` | Amber | A direct competitor made a notable strategic move |

### Writing the TLDR
- Write TLDR **last**, after all cards are written
- Identify the 3 biggest patterns across the full issue
- The bolded claim should be specific and falsifiable — not vague
- The implication should name a concrete MaintainX action or angle

**Good:** `**Linear's deeplink opens AI pre-filled with full context in one click** — tapping a MaintainX WO should load asset history + SOP the same way.`
**Bad:** `**AI features are becoming more common** — MaintainX should consider how to respond.`

---

## 7. Header Elements

### Issue number and date range
- Issue number: sequential (`Issue #1`, `Issue #2`, etc.)
- Date range: `Mon DD – Mon DD, YYYY` (e.g., `Feb 22 – Mar 7, 2026`)
- Read time: approximate based on card count (`~5 min read` for 8–10 cards)
- Update count: accurate count in header-meta

### header-note (optional)
A brief callout pill shown in the header when the week had an especially notable through-line. Use when there's a clear theme worth surfacing before the TLDR.

- Format: `⭐ [Short framing sentence]`
- Keep under 10 words
- Example: `⭐ Big week — autonomous agents went from demo to product`
- **Omit if there's no strong theme** — don't force it

---

## 8. Sections

Three fixed sections, always in this order:

| # | Title | Icon | Badge class |
|---|-------|------|-------------|
| 1 | Leading AI Products | ✦ | `badge-ai` (blue) |
| 2 | Interesting AI Startups | 🚀 | `badge-start` (green) |
| 3 | CMMS + EAM + Field Service | 🔧 | `badge-cmms` (orange) |

### Section header company list
The `.section-count` element lists the companies covered in that section, separated by ` · `. Update this to match the actual cards in that section each issue.

---

## 9. Featured Card

Use at most once per issue, for the single most important release.

**When to feature:**
- The release is a category-defining move (not just a good feature)
- It has direct, high-confidence implications for MaintainX strategy
- It's the clear standout if you had to pick one thing from the entire issue

**How to feature:**
- Add class `featured` to the `.card` div: `<div class="card featured">`
- Add `<div class="featured-banner">⭐ Feature of the Week</div>` as the **first child** of the card (before `.card-date-row`)
- The card automatically gets an orange top border (`#F5A623`) via the `featured` CSS class

---

## 10. Brand & Visual Standards

### Colors
| Use | Hex |
|-----|-----|
| Primary blue (header, card borders, links) | `#2563EB` |
| Navy (body text, section headers, footer) | `#0D1F3C` |
| Featured orange | `#F5A623` |
| Background gray | `#F2F4F7` |
| TLDR background | `#0a1628` |

### Typography
- Font stack: `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`
- Body text: 13px, `#334155`
- Card titles: 15px, 700 weight, `#0D1F3C`

### Do not modify
- 3-column CSS Grid layout
- TLDR dark background styling
- MX callout blue box (`.mx-box`) left-border pattern
- Section header bar + dark inner panel pattern
- Logo text: `MaintainX · Industry Watch` (with `<span>X</span>` for the gray X)
- H1 text: `What Others Shipped This Week`

---

## 11. File Naming & Hosting

### File name format
`issue-[N]-[startmonDD]-[endmonDD].html`

Examples:
- `issue-1-feb10-feb21.html`
- `issue-2-feb22-mar7.html`
- `issue-3-mar8-mar14.html`

### GitHub repository
- Repo: `github.com/joyliu-maintainx/product-digest`
- Pages base URL: `https://joyliu-maintainx.github.io/product-digest/`
- Live URL pattern: `https://joyliu-maintainx.github.io/product-digest/issue-[N]-[dates].html`

### After creating a new issue
1. Upload the HTML file to the GitHub repo (Add file → Create new file)
2. Update `README.md` — add new row at top of the issues table
3. The README table is newest-first (most recent issue at the top)

---

## 12. Card HTML Template

### Standard card
```html
<div class="card">
  <div class="card-date-row">
    <div class="card-tags">
      <span class="product-name">[Company]</span>
      <span class="badge badge-ai">AI Product</span>
    </div>
    <span class="card-date">[Mon DD]</span>
  </div>
  <div class="card-body">
    <div class="card-title">[Feature Name] — [Short descriptor]</div>
    <div class="detail">
      <div class="detail-label">Problem</div>
      <div class="detail-text">[One punchy sentence leading with specific friction.]</div>
    </div>
    <div class="detail">
      <div class="detail-label">Solution</div>
      <div class="detail-text">[One punchy sentence on what shipped and why it matters.]</div>
    </div>
    <div class="mx-box">
      <div class="detail-label">💡 MaintainX</div>
      <div class="detail-text">[One sentence — competitive signal, UX pattern, or opportunity.]</div>
    </div>
    <a class="card-link" href="[URL]" target="_blank">Release notes ↗</a>
  </div>
</div>
```

### Featured card (add before `.card-date-row`)
```html
<div class="card featured">
  <div class="featured-banner">⭐ Feature of the Week</div>
  <!-- rest of card identical to standard -->
</div>
```

### Badge variants
```html
<span class="badge badge-ai">AI Product</span>      <!-- Section 1 -->
<span class="badge badge-start">Startup</span>       <!-- Section 2 -->
<span class="badge badge-start">Model Launch</span>  <!-- Section 2, model releases -->
<span class="badge badge-cmms">CMMS</span>           <!-- Section 3 -->
```

### TLDR item
```html
<div class="tldr-item">
  <span class="tldr-tag tag-shift">Category Shift</span>
  <p><strong>[Bold claim]</strong> — [Implication for MaintainX].</p>
</div>
```

---

## 13. Full Issue Structure (Skeleton)

```html
<!-- HEADER -->
<div class="header">
  <div class="header-top">
    <div class="logo">
      <div class="logo-text">Maintain<span>X</span> · Industry Watch</div>
    </div>
    <div class="issue-tag">Issue #[N]</div>
  </div>
  <h1>What Others Shipped This Week</h1>
  <div class="header-meta">
    <strong>[Mon DD – Mon DD, YYYY]</strong> &nbsp;·&nbsp; [N] updates · ~[N] min read
  </div>
  <!-- OPTIONAL header-note: -->
  <!-- <div class="header-note">⭐ [Theme sentence]</div> -->
</div>

<!-- TLDR -->
<div class="tldr">
  <div class="tldr-label">TLDR — Trends &amp; Patterns</div>
  <div class="tldr-list">
    <!-- 3 tldr-item divs -->
  </div>
</div>

<!-- CONTENT -->
<div class="content">

  <!-- SECTION 1 -->
  <div class="section-header">
    <div class="section-header-bar"></div>
    <div class="section-header-inner">
      <span class="section-title">✦ Leading AI Products</span>
      <span class="section-count">[Co · Co · Co]</span>
    </div>
  </div>
  <div class="card-grid"><!-- 4–6 cards --></div>

  <!-- SECTION 2 -->
  <div class="section-header">
    <div class="section-header-bar"></div>
    <div class="section-header-inner">
      <span class="section-title">🚀 Interesting AI Startups</span>
      <span class="section-count">[Co · Co]</span>
    </div>
  </div>
  <div class="card-grid"><!-- 2–4 cards --></div>

  <!-- SECTION 3 -->
  <div class="section-header">
    <div class="section-header-bar"></div>
    <div class="section-header-inner">
      <span class="section-title">🔧 CMMS + EAM + Field Service</span>
      <span class="section-count">[Co · Co]</span>
    </div>
  </div>
  <div class="card-grid"><!-- 2–3 cards --></div>

</div>

<!-- FOOTER -->
<div class="footer">
  <p><strong>MaintainX Industry Watch</strong> · Issue #[N] · [Date Range]</p>
  <p style="margin-top:5px;">Leading AI: [list] &nbsp;·&nbsp; CMMS/EAM: [list]</p>
</div>
```

---

## 14. Quality Checklist

Before publishing each issue:

- [ ] All cards have Problem, Solution, and MaintainX callouts
- [ ] Every MaintainX callout names a specific workflow, persona, or feature — not a vague suggestion
- [ ] TLDR has exactly 3 items, each with a bolded claim + em-dash implication
- [ ] Section company list in `.section-count` matches the actual cards in that section
- [ ] Issue number, date range, and update count in header are accurate
- [ ] All links verified working and open in new tab (`target="_blank"`)
- [ ] Featured card used at most once — and it earns it
- [ ] header-note included only if there's a genuine theme (omit if nothing stands out)
- [ ] File named correctly: `issue-[N]-[dates].html`
- [ ] README updated with new live link (newest issue at top of table)

---

*Last updated: March 2026. Before producing a new issue, read the most recent issue from GitHub to pick up any format evolution since this guide was written.*
