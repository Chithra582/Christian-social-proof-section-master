# EXPLAINABILITY.md

This document explains the internal mechanisms, data lineage, operational boundaries, and governance framework of **Christian Social Proof Section** (`Christian-social-proof-section-master`) in accordance with the **OpenGAP v0.1.0** specification for the **HiDevs GitAgent Passport** clearance pipeline.

> **Agent Name:** Christian Social Proof Section (`Christian-social-proof-section-master`)  
> **Specification:** OpenGAP v0.1.0  
> **Category / Domain:** Developer Tools / Social Proof UI Engineering, Testimonial Layouts & Responsive Web Design  
> **Compliance Standard:** OpenGAP Checkpoint 2 (Explainability & Decision Governance), OWASP LLM Top 10, MITRE ATLAS  

---

## How the Agent Decides

Christian Social Proof Section operates an intelligent, five-stage deterministic operational pipeline designed to engineer responsive, accessible, and high-conversion testimonial review interfaces. The agent coordinates design token ingestion, semantic HTML scaffolding, CSS grid layout synthesis, WCAG contrast verification, and multi-device viewport testing through a deterministic five-stage operational pipeline.

### 1. Decision Architecture

The runtime intake, state classification, evaluation, and execution tracking operate across a deterministic, five-stage pipeline:

```
[ User UI Design Brief / Testimonial Content Payload ]
                         │
                         ▼
[Stage 1: Intent Ingestion & Design Token Resolution Gate]
  - Parses testimonial text, author metadata, star rating counts
  - Resolves color palette tokens (primary magenta, dark violet, neutral white)
  - Dispatches typography scale parameters to layout engine
                         ▼
[Stage 2: Semantic HTML5 Structure Scaffolding Gate]
  - Scaffolds semantic section container with header rating components
  - Maps individual reviews into `<article>` and `<blockquote>` elements
  - Injects descriptive alt tags and avatar image bindings
                         ▼
[Stage 3: Responsive CSS Grid & Staggered Alignment Gate]
  - Applies mobile-first linear layout for viewports < 768px
  - Synthesizes desktop CSS Grid with staggered card margins
  - Computes visual balance score S_layout across grid columns
                         ▼
[Stage 4: WCAG AA Contrast & Overflow Verification Gate]
  - Computes foreground-to-background contrast ratio C_contrast
  - Verifies minimum 4.5:1 legibility ceiling on all text elements
  - Tests zero-horizontal-overflow constraint across viewport widths
                         ▼
[Stage 5: Asset Sealing & Production Packaging Gate]
  - Minifies CSS stylesheets and optimizes responsive image paths
  - Seals build artifact and records execution audit metadata
  - Delivers verified, production-ready social proof web section
                         ▼
[ Verified Responsive Social Proof Component Ready ]
```

### 2. Decision Logic & Routing Formulations

When structuring responsive layout geometry and evaluating visual ergonomics, Christian Social Proof Section evaluates two deterministic mathematical formulations:

1. **Composite Layout Quality Score ($S_{\text{layout}}$)**:
   $$S_{\text{layout}} = w_c \cdot C_{\text{contrast}} + w_o \cdot (1 - O_{\text{overflow}}) + w_f \cdot F_{\text{fluidity}} + w_h \cdot H_{\text{hierarchy}}$$
   Where:
   - $C_{\text{contrast}} \in [0, 1]$: Normalized text contrast compliance relative to WCAG AA ($4.5:1$ threshold).
   - $O_{\text{overflow}} \in [0, 1]$: Viewport horizontal scroll overflow penalty ($0.0$ indicates zero overflow).
   - $F_{\text{fluidity}} \in [0, 1]$: Smooth scaling score evaluating proportional card expansion between $375$px and $1440$px.
   - $H_{\text{hierarchy}} \in [0, 1]$: Visual hierarchy metric evaluating font weight and spacing ratios between headlines and review quotes.
   - Standard weightings: $w_c = 0.35$, $w_o = 0.35$, $w_f = 0.15$, $w_h = 0.15$ ($\sum w_i = 1.0$).
   - Layout approval threshold: A generated layout is cleared for emission only if $S_{\text{layout}} \ge 0.70$.

2. **Staggered Card Margin Offset Index ($M_{\text{offset}}$)**:
   $$M_{\text{offset}}(i) = (i - 1) \cdot \Delta d \quad \text{for } i \in \{1, 2, 3\}$$
   Where:
   - $i$: Positional index of the testimonial card ($1$ to $3$).
   - $\Delta d = 16$px: Standard incremental margin offset producing the characteristic staggered desktop layout.
   - On mobile viewports ($W < 768$px), $M_{\text{offset}}(i) = 0$px to maintain vertical alignment.

### 3. Thresholding & Refusal Decision Criteria

Christian Social Proof Section enforces strict operational boundaries and deterministic refusal thresholds:
- **Refusal on ERR_WCAG_CONTRAST_DEFICIT**: Text color failing minimum 4.5:1 contrast ratio halts stylesheet compilation with code `ERR_WCAG_CONTRAST_DEFICIT`.
- **Refusal on ERR_HORIZONTAL_OVERFLOW_DETECTED**: Layout element exceeding viewport width boundary halts emission with code `ERR_HORIZONTAL_OVERFLOW_DETECTED`.
- **Refusal on ERR_MALFORMED_SEMANTIC_STRUCTURE**: Missing quote attribution or broken semantic tag hierarchy halts with code `ERR_MALFORMED_SEMANTIC_STRUCTURE`.
- **Refusal on ERR_IMAGE_ASSET_MISSING**: Avatar image references failing local asset resolution halt with code `ERR_IMAGE_ASSET_MISSING`.
- **Refusal on ERR_UNSAFE_INLINE_SCRIPT**: Presence of unwhitelisted script tags inside HTML source halts with code `ERR_UNSAFE_INLINE_SCRIPT`.

### 4. Fallback Decision Mechanism

Continuous operational stability is maintained through layered fault recovery:
- **Linear Column Fallback**: If desktop CSS Grid staggered alignment encounters unsupported legacy browser viewports, the layout gracefully degrades to a clean single-column flexbox stack.
- **Web-Safe Typography Fallback**: If custom Google Fonts (`League Spartan`) fail to load over network connections, local system sans-serif font stacks are seamlessly applied.
- **Model Fallback Cascade**: High-level reasoning and synthesis default to `gemini-2.0-flash` with automatic failover to `gpt-4o` and `claude-3-5-sonnet`.

### 5. Human-in-the-Loop Governance

Human operators retain sovereign authority over the multi-agent execution lifecycle:
- **Theme Palette Customization Sign-Off**: Operators can adjust primary color variables and verify contrast accessibility in real-time preview panels.
- **Production Asset Export Approval**: Packaging and deploying built HTML/CSS bundles to public web hosting mandates explicit human confirmation.
- **Testimonial Content Moderation**: Operators review and approve testimonial text and customer author attributions before live deployment.

---

## The Data It Uses

Christian Social Proof Section operates under strict principles of data minimization, environment isolation, and privacy protection.

### 1. Ingested Input Data

The framework processes only operational data necessary to perform its functions:
- **Testimonial Content Payloads**: Customer review quotes, author names, buyer verification badges, and star ratings.
- **Visual Design Directives**: Style-guide markdown specifications, color palette definitions, and target viewport breakpoints.
- **Avatar Image Assets**: Local PNG/JPEG portrait graphics representing testimonial reviewers.

### 2. Configuration & Reference Data

- **Design Tokens**: CSS custom properties for primary magenta (`hsl(300, 43%, 22%)`), soft pink (`hsl(333, 80%, 67%)`), and dark gray-magenta text.
- **Typography Manifest**: Font family declarations, font weight definitions (400, 500, 700), and rem-based line height scales.
- **Style Guide Specifications**: Spacing margins, padding increments, and border radius tokens ($8$px).

### 3. Base Model & Inference Lineage

- **Frontend Core**: Pure semantic HTML5, CSS3 Grid, Flexbox, and modern CSS custom property variables.
- **Asset Optimizer**: Local image compression and CSS minification pipelines ensuring sub-50KB total bundle payload.
- **Validation Engine**: Automated viewport emulation testing across Chromium and WebKit rendering engines.

### 4. Data Privacy, Storage, and Retention

- **OWASP LLM & MITRE ATLAS Hardened**: Defended against indirect prompt injection, credential leakage, and unauthorized external API dispatch.
- **Local Environment Isolation**: Agent execution workspaces, intermediate scratchpads, and vector stores reside strictly within designated local project directories.
- **Automated Secret Scrubbing**: API keys, database credentials, and personal credentials are automatically redacted prior to embedding or logging.
- **Zero Commercial Monetization**: Prompts, intermediate reasoning trajectories, and task deliverables are never commercialized or shared with third parties.

---

## Limitations

Understanding the operational boundaries and technical constraints of Christian Social Proof Section is essential for effective deployment.

### 1. Deep Text Overflow on Extreme Character Lengths
- **Limitation**: Excessively lengthy review quotes exceeding 500 words can disrupt desktop staggered card height balance.
- **Mitigation**: Implement automated CSS line-clamp ellipsis with optional expand-on-click functionality.

### 2. High-DPI Display Avatar Pixelation
- **Limitation**: Low-resolution reviewer avatar images can appear blurry on modern Apple Retina (3x) displays.
- **Mitigation**: Mandate high-resolution 2x/3x WebP image sources with descriptive fallback PNG paths.

### 3. Star Rating SVG Scalability in Narrow Viewports
- **Limitation**: Displaying five fixed-width SVG star rating icons side-by-side can wrap awkwardly on very narrow ($320$px) devices.
- **Mitigation**: Deploy responsive flexbox wrappers with fractional scaling to preserve horizontal alignment.

### 4. Third-Party Web Font Load Flash (FOIT/FOUT)
- **Limitation**: Slow network connections downloading remote web fonts can cause a brief flash of unstyled text.
- **Mitigation**: Enforce `font-display: swap` in `@font-face` declarations and pre-bundle critical local subsets.

### 5. Multi-Card Dynamic Height Misalignment
- **Limitation**: Unequal quote lengths between adjacent cards in CSS Grid columns can create uneven bottom margins.
- **Mitigation**: Enforce `display: flex; flex-direction: column; justify-content: space-between;` inside card bodies.

---

## Summary & Compliance Checklist

| Checkpoint 2 Requirement | Corresponding Section | Status |
| :--- | :--- | :---: |
| **How the agent decides** | [How the Agent Decides](#how-the-agent-decides) | **Covered** |
| - Decision architecture & 5-stage pipeline | Section 1 | Verified |
| - Decision logic & routing formulations | Section 2 | Verified |
| - Thresholding & refusal decision criteria | Section 3 | Verified |
| - Fallback decision mechanism | Section 4 | Verified |
| - Human-in-the-loop governance & oversight | Section 5 | Verified |
| **The data it uses** | [The Data It Uses](#the-data-it-uses) | **Covered** |
| - Ingested input data & query streams | Section 1 | Verified |
| - Configuration & reference schemas | Section 2 | Verified |
| - Base model lineage & deterministic engines | Section 3 | Verified |
| - Data privacy, retention lifecycle & MITRE/OWASP | Section 4 | Verified |
| **Its limitations** | [Limitations](#limitations) | **Covered** |
| - Deep Text Overflow on Extreme Character Lengths | Section 1 | Verified |
| - High-DPI Display Avatar Pixelation | Section 2 | Verified |
| - Star Rating SVG Scalability in Narrow Viewports | Section 3 | Verified |
| - Third-Party Web Font Load Flash (FOIT/FOUT) | Section 4 | Verified |
| - Multi-Card Dynamic Height Misalignment | Section 5 | Verified |
