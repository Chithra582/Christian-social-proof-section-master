---
name: "accessibility-contrast-auditing"
description: "Audits text and rating stars against WCAG AA accessibility standards to ensure high legibility."
license: MIT
---

# Accessibility Contrast Auditing Skill

## Overview
Checks color combinations across cards, rating headers, and subtle muted text to ensure compliance with WCAG AA benchmarks.

## Operational Workflow
1. Extract foreground and background color tokens.
2. Calculate contrast ratio using `contrast-checker`.
3. Adjust opacity or lightness values automatically if contrast falls below 4.5:1.
