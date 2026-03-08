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
3. Tech press (TechCrunch, The Verge, VentureBeat, SAP Insider) for funding news or major launches
4. LinkedIn / Twitter announcements as secondary confirmation

### What qualifies for a dedicated card
- New features that have **shipped** (not announced, not "coming soon")
- Funding rounds ≥ $50M if strategically relevant to MaintainX's space
- Model releases (foundation models) if they affect tooling or the competitive landscape
- Partner integrations that meaningfully expand a competitor's reach

### What goes in the "Also Shipped" overflow card
Every watchlist company that released something during the issue window — even if minor or less directly relevant to MaintainX — gets a bullet in the "Also Shipped" card rather than being silently omitted. See Section 10.

### What to skip entirely
- Bug fixes and minor patches with no user-facing change
- UI refreshes with no functional change

---

## 3. Watchlist

### Section 1 — Leading AI Products
Broad AI productivity and developer tools that influence UX expectations and AI patterns across all software.

**Core watchlist:**
- Notion (AI, agents, databases)
- Cursor (AI coding)
- ChatGPT / OpenAI
- Claude / Anthropic
- Linear (project management AI)
- Glean (enterprise AI search)
- Intercom (AI support)
- n8n (workflow automation)

### Section 2 — Interesting AI Startups
Emerging tools and model releases that represent directional signals for where the industry is heading.

**Core watchlist:**
- High-growth AI startups with relevant functionality (agents, voice, vision, document AI)
- New foundation model releases (GPT-5.x, Gemini, Claude, etc.)
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

- **Total cards per issue:** 8–12 dedicated cards, plus one "Also Shipped" overflow card per section if needed
- **Section 1 (AI Products):** 4–6 dedicated cards
- **Section 2 (Startups):** 2–4 cards
- **Section 3 (CMMS):** 2–3 cards
- **Layout:** 3-column CSS Grid (`repeat(3, 1fr)`)
- **Featured card:** Optional. One card per issue may be designated "Feature of the Week" if there's a standout release with exceptionally high MaintainX relevance. Use sparingly — max 1 per issue.
- **Same company, multiple cards:** Allowed when a company shipped multiple distinct features worth separate callouts.

---

## 5. Writing Standards

### Card title
Write a clean, descriptive name that immediately conveys the solution and use case. No em-dash or "—" separator required.

- Use the product team's name for the feature where possible
- If the official name is vague, make the title self-explanatory
- Good: `MCP Server for Product Management`
- Good: `Required Fields + Locked Tasks`
- Good: `Deeplink to AI Tools`
- Avoid: `Feature Name — Short descriptor` (the dash format is no longer preferred)

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

### Card link
**Required on every dedicated card.** No exceptions — every card must have a source link. Prefer release notes over press. Never omit the link even if it points to a general changelog or product page.

Use the most specific label available:
- `Release notes ↗` — preferred for product releases
- `Changelog ↗` — for changelog pages
- `Product page ↗` — when no specific release link exists
- `TechCrunch ↗` / `SAP Insider ↗` / `Blog post ↗` — for press / announcements
- Always include `target="_blank"`

The "Also Shipped" overflow card uses inline text links (not `.card-link` buttons) — see Section 10.

### Dates on cards
- `Mon DD` — standard (e.g., `Feb 24`, `Mar 5`)
- `Mon YYYY` — when only the month is known (e.g., `Feb 2026`)
- `Mon DD – DD, YYYY` — when both dates are in the same month (e.g., `Feb 10 – 21, 2026` — note: drop the month on the second date)
- `Mon DD · $NNM` — for funding news (e.g., `Feb 10 · $315M`)
- `Mon DD · vX.XX` — for versioned releases (e.g., `Feb 23 · v5.17`)
- Seasonal labels are allowed when no exact date is known: `Winter 2026`, `Jan 2026 Drop`, `2026 Roadmap`

### Badge variants
```html
<span class="badge badge-ai">AI Product</span>      <!-- Section 1: AI products -->
<span class="badge badge-start">Startup</span>       <!-- Section 2: startups -->
<span class="badge badge-start">Model Launch</span>  <!-- Section 2: foundation model releases -->
<span class="badge badge-start">Platform</span>      <!-- Section 2: frontier/infrastructure platforms not yet fully productized -->
<span class="badge badge-cmms">CMMS</span>           <!-- Section 3: CMMS competitors -->
<span class="badge badge-cmms">EAM</span>            <!-- Section 3: EAM platforms (SAP, IBM Maximo) -->
```

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

There are only three valid tag types. Do not create new tag classes.

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
- Date range in header-meta: `Mon DD – Mon DD, YYYY` when months differ (e.g., `Feb 22 – Mar 7, 2026`); `Mon DD – DD, YYYY` when same month (e.g., `Feb 10 – 21, 2026`)
- Read time: approximate based on card count (`~5 min read` for 8–10 cards, `~6 min read` for 11–13)
- Update count: accurate count of all updates covered (dedicated cards + overflow bullets)

### header-note (optional)
A brief callout pill shown in the header when the week had an especially notable through-line. Use when there's a clear theme worth surfacing before the TLDR.

- Format: `⭐ [Short framing sentence]`
- Keep under 10 words
- Example: `⭐ Big week — autonomous agents went from demo to product`
- **Omit if there's no strong theme** — don't force it

### Logo text
Logo text is: `MaintainX · Industry Watch` rendered as `Maintain<span>X</span> · Industry Watch`.

Do **not** include a logo-mark square element. The logo is text-only.

---

## 8. Sections

Three fixed sections, always in this order:

| # | Title | Icon | Badge class |
|---|-------|------|-------------|
| 1 | Leading AI Products | ✦ | `badge-ai` (blue) |
| 2 | Interesting AI Startups | 🚀 | `badge-start` (green) |
| 3 | CMMS + EAM + Field Service | 🔧 | `badge-cmms` (orange) |

### Section header company list and update count
The `.section-count` element always lists **all watchlist companies** for that section — even if some had no releases that week — followed by the total update count.

Format: `Company · Company · · · N updates`

Example: `Notion · Cursor · ChatGPT · Claude · Linear · Glean · Intercom · n8n · 8 updates`

The update count includes both dedicated cards and overflow bullets in the "Also Shipped" card.

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

## 10. "Also Shipped" Overflow Card

One overflow card per section, placed at the end of the section's card grid. It covers all watchlist companies that released something during the issue window but didn't earn a dedicated card.

**When to include:** Any time a watchlist company released something — even minor — but didn't get a dedicated card. Do not silently omit them.

**Format:** One bullet per company:
- **Company name** (bold, uppercase)
- One short sentence on the user problem
- One short sentence on the solution
- Inline `Release notes ↗` link in plain text

**CSS classes needed** (add to the `<style>` block):
```css
.card.also-shipped { border-top-color: #64748b; }
.also-shipped-banner {
  background: #f1f5f9;
  padding: 5px 16px;
  font-size: 10px; font-weight: 800;
  letter-spacing: 0.08em; text-transform: uppercase; color: #64748b;
  border-bottom: 1px solid #e2e8f0;
}
.also-list { list-style: none; display: flex; flex-direction: column; gap: 14px; padding: 0; }
.also-item { display: flex; flex-direction: column; gap: 3px; }
.also-co { font-size: 11px; font-weight: 800; color: #0D1F3C; text-transform: uppercase; letter-spacing: 0.05em; margin-bottom: 1px; }
.also-desc { font-size: 12px; color: #334155; line-height: 1.5; }
.also-link { font-size: 11px; font-weight: 600; color: #2563EB; text-decoration: none; }
.also-link:hover { text-decoration: underline; }
```

**Card HTML template:**
```html
<div class="card also-shipped">
  <div class="also-shipped-banner">Also Shipped</div>
  <div class="card-date-row">
    <div class="card-tags">
      <span class="product-name">[Co · Co · Co]</span>
    </div>
    <span class="card-date">[date range]</span>
  </div>
  <div class="card-body">
    <ul class="also-list">
      <li class="also-item">
        <span class="also-co">Company Name</span>
        <span class="also-desc">One sentence on user problem. One sentence on solution. <a class="also-link" href="[URL]" target="_blank">Release notes ↗</a></span>
      </li>
      <!-- repeat per company -->
    </ul>
  </div>
</div>
```

---

## 11. Brand & Visual Standards

### Colors
| Use | Hex |
|-----|-----|
| Primary blue (header, card borders, links) | `#2563EB` |
| Navy (body text, section headers, footer) | `#0D1F3C` |
| Featured orange | `#F5A623` |
| Background gray | `#F2F4F7` |
| TLDR background | `#0a1628` |
| Also Shipped banner background | `#f1f5f9` |
| Also Shipped border-top | `#64748b` |

### Typography
- Font stack: `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`
- Body text: 13px, `#334155`
- Card titles: 15px, 700 weight, `#0D1F3C`

### Do not modify
- 3-column CSS Grid layout
- TLDR dark background styling
- MX callout blue box (`.mx-box`) left-border pattern
- Section header bar + dark inner panel pattern
- Logo text: `MaintainX · Industry Watch` (text-only, no logo-mark square)
- H1 text: `What Others Shipped This Week`

---

## 12. File Naming & Hosting

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

## 13. Footer Format

The footer appears at the bottom of every issue. Two lines:

**Line 1:** `MaintainX Industry Watch · Issue #[N] · [Date range]`
- Date range format: same-month shortening (e.g., `Feb 10–21, 2026` — no spaces around the dash); cross-month uses spaces (e.g., `Feb 22 – Mar 7, 2026`)

**Line 2:** Full watchlist summary, split by category
- Format: `Leading AI: [list]  ·  CMMS/EAM: [list]`
- Example: `Leading AI: Notion · Cursor · ChatGPT · Claude · Linear · Glean · Intercom · n8n  ·  CMMS/EAM: UpKeep · Limble · Fiix · ServiceMax · SAP`

```html
<div class="footer">
  <p><strong>MaintainX Industry Watch</strong> · Issue #[N] · [Date Range]</p>
  <p style="margin-top:5px;">Leading AI: [list] &nbsp;·&nbsp; CMMS/EAM: [list]</p>
</div>
```

---

## 14. Card HTML Template

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
    <div class="card-title">[Descriptive Feature Name]</div>
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

### Featured card
```html
<div class="card featured">
  <div class="featured-banner">⭐ Feature of the Week</div>
  <!-- identical card structure below, starting with .card-date-row -->
</div>
```

---

## 15. Full Issue Structure (Skeleton)

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
    <!-- 3 tldr-item divs, using tag-shift / tag-pattern / tag-problem only -->
  </div>
</div>

<!-- CONTENT -->
<div class="content">

  <!-- SECTION 1 -->
  <div class="section-header">
    <div class="section-header-bar"></div>
    <div class="section-header-inner">
      <span class="section-title">✦ Leading AI Products</span>
      <span class="section-count">Notion · Cursor · ChatGPT · Claude · Linear · Glean · Intercom · n8n · [N] updates</span>
    </div>
  </div>
  <div class="card-grid">
    <!-- 4–6 dedicated cards -->
    <!-- 1 "Also Shipped" card if any watchlist companies had minor releases -->
  </div>

  <!-- SECTION 2 -->
  <div class="section-header">
    <div class="section-header-bar"></div>
    <div class="section-header-inner">
      <span class="section-title">🚀 Interesting AI Startups</span>
      <span class="section-count">[Co · Co · N updates]</span>
    </div>
  </div>
  <div class="card-grid"><!-- 2–4 cards --></div>

  <!-- SECTION 3 -->
  <div class="section-header">
    <div class="section-header-bar"></div>
    <div class="section-header-inner">
      <span class="section-title">🔧 CMMS + EAM + Field Service</span>
      <span class="section-count">UpKeep · Limble · Fiix · ServiceMax · SAP · [N] updates</span>
    </div>
  </div>
  <div class="card-grid">
    <!-- 2–3 dedicated cards -->
    <!-- 1 "Also Shipped" card if applicable -->
  </div>

</div>

<!-- FOOTER -->
<div class="footer">
  <p><strong>MaintainX Industry Watch</strong> · Issue #[N] · [Date Range]</p>
  <p style="margin-top:5px;">Leading AI: Notion · Cursor · ChatGPT · Claude · Linear · Glean · Intercom · n8n &nbsp;·&nbsp; CMMS/EAM: UpKeep · Limble · Fiix · ServiceMax · SAP</p>
</div>
```

---

## 16. Quality Checklist

Before publishing each issue:

- [ ] All dedicated cards have Problem, Solution, and MaintainX callouts
- [ ] All dedicated cards have a source link — no exceptions
- [ ] Every MaintainX callout names a specific workflow, persona, or feature — not a vague suggestion
- [ ] TLDR has exactly 3 items using only `tag-shift`, `tag-pattern`, or `tag-problem`
- [ ] Section 1 `.section-count` shows all 8 watchlist companies + update count
- [ ] "Also Shipped" card added for any watchlist companies with minor releases
- [ ] Issue number, date range, and update count in header are accurate
- [ ] All links verified working and open in new tab (`target="_blank"`)
- [ ] Featured card used at most once — and it earns it
- [ ] header-note included only if there's a genuine theme
- [ ] No logo-mark element in the header — logo is text-only
- [ ] Card titles are descriptive names — no em-dash separator required
- [ ] File named correctly: `issue-[N]-[dates].html`
- [ ] README updated with new live link (newest issue at top of table)

---

*Last updated: March 2026. Before producing a new issue, read the most recent issue from GitHub to pick up any format evolution since this guide was written.*
