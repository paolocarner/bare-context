# BARE Consulting — Tool-Building Preferences
> Use this file whenever building any tool, app, artifact, calculator, or interactive output for BARE.

---

## General Principles

- **Build for Paolo first, clients second.** Most tools are internal or used in client-facing delivery — optimise for clarity and professional appearance.
- **Evidence-based defaults.** Where tools surface numbers, methodology should be visible (FAIR, ENISA data, Gordon-Loeb, etc.).
- **Advisory framing.** Tools assist decision-making — they don't make decisions. Outputs should always contextualise, never just output a number.
- **European context.** Default currency: EUR. Default regulatory framing: EU (NIS2, GDPR, DORA). Default jurisdiction: Netherlands unless specified.

---

## Visual Design Defaults

When building any HTML, React, or web-based tool, apply BARE brand unless told otherwise:

```css
/* BARE Brand CSS Variables */
--color-primary:    #4E1686;  /* Deep Violet */
--color-secondary:  #C09FE1;  /* Lavender */
--color-tertiary:   #F3E7FF;  /* Lilac */
--color-bg-light:   #EDF1FD;  /* Light Silver */
--color-accent-red: #FF9596;  /* Coral */
--color-accent-grn: #167B50;  /* Lush Green */
--color-accent-yel: #FFF06C;  /* Sunshine Yellow */
--color-white:      #FFFFFF;
--color-black:      #000000;

--font-primary:     'Alata', sans-serif;       /* Display/headings */
--font-office:      'SEN', sans-serif;         /* Office-compatible */
--font-body:        system-ui, sans-serif;     /* Web fallback */

--radius-sm: 6px;
--radius-md: 12px;
--radius-lg: 20px;
```

**Layout preferences:**
- Clean, spacious layouts — generous padding, not cramped
- Deep Violet headers/navbars with white text
- Light Silver or white content areas
- Lavender for secondary UI elements, selected states, borders
- Lush Green for positive/success indicators; Coral for warnings/alerts
- Sunshine Yellow used very sparingly, for single highlight elements only

**Typography in tools:**
- Headings: Alata or SEN, Deep Violet or White
- Body: system sans-serif, dark on light backgrounds
- Section labels: spaced caps in Deep Violet (matching brand style)
- Avoid: Inter, Roboto, Arial as primary fonts

---

## Output Format Preferences

| Output type | Preferred format | Notes |
|---|---|---|
| Reports / documents | `.docx` or `.md` | BARE letterhead style where applicable |
| Presentations | `.pptx` | Use BARE slide templates (white+fingerprint or violet) |
| Spreadsheets / models | `.xlsx` | Deep Violet header rows, clean data tables |
| Web tools / calculators | Single-file HTML or React artifact | Self-contained, no external dependencies where possible |
| PDFs | Generated from HTML or docx | Branded header/footer |
| Data exports | `.csv` or `.json` | Clean, labelled columns |

---

## Technical Preferences

**Languages / frameworks:**
- Python for backend scripts, data processing, automation
- HTML/CSS/JS for simple interactive tools (single-file preferred)
- React (with Tailwind) for more complex UI components
- No heavy frameworks for simple tools — keep dependencies minimal

**Charting / visualisation:**
- Recharts (React) or Chart.js for web tools
- Matplotlib / Plotly for Python outputs
- Prefer simple, clean chart styles over decorative ones
- Brand colours applied to chart elements

**Data handling:**
- Prefer local/in-memory processing — avoid requiring cloud APIs for tools Paolo runs himself
- Where external data is needed, document the source and methodology
- FAIR methodology preferred for risk quantification outputs (Monte Carlo simulation approach)

**Code style:**
- Clear variable names, commented methodology sections
- Functions over long scripts
- Include a brief usage note at the top of any standalone script

---

## Methodology Defaults

When building risk or financial tools, default to:

| Topic | Default methodology |
|---|---|
| Cyber risk quantification | FAIR (Factor Analysis of Information Risk) — Monte Carlo simulation |
| Security investment ROI | Gordon-Loeb model |
| Incident cost reference | ENISA threat landscape reports, IBM Cost of a Data Breach |
| Risk scoring | Financial impact ranges, not qualitative High/Medium/Low alone |
| Compliance cost modelling | Phase-based (gap assessment → implementation → certification → maintenance) |

---

## Tone in Tool UI / Copy

Tool interface copy should match BARE brand voice:
- Clear and direct — no filler text
- Action-oriented labels ("Calculate exposure" not "Submit")
- Results framed as insights, not verdicts ("This suggests..." not "Your risk is X")
- Where methodology is complex, offer a brief explanation or tooltip
- No fear-based framing in results copy

---

## Domains & Identities

| Domain | Purpose |
|---|---|
| bare-consult.nl | Primary NL domain |
| bare-consult.com | International |
| bare-alliance.eu | BARE Alliance network |

**Email:** paolo@bare-consult.nl (primary, ProtonMail)  
**Communications:** Matrix/Element for BARE Alliance internal; standard email for clients

---

## Reusable Tool Patterns

These patterns have been built before — reuse or adapt rather than rebuilding from scratch:

- **ISO 27001 / SOC 2 cost calculator** — Phase-based cost + duration model with client size input (v4 is the current version)
- **FAIR Monte Carlo simulator** — Risk quantification with loss magnitude and frequency distributions
- **Balanced Scorecard for Cyber Resilience (BSCR)** — Adapted from MIT CAMS; four-quadrant scorecard
- **DMARC report analyser** — Email authentication reporting tool
- **NIS2 compliance toolkit** — Gap assessment template
- **Business Impact Analysis template** — Standard BIA structure
- **Cybersecurity ROI calculator** — Gordon-Loeb + ENISA data integration
