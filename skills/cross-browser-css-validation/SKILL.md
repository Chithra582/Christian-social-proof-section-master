---
name: "cross-browser-css-validation"
description: "Simulates multiple viewport aspect ratios and verifies zero horizontal scroll overflow."
license: MIT
---

# Cross-Browser CSS Validation Skill

## Overview
Simulates rendering across standardized device viewports (375px, 768px, 1440px) to verify layout integrity and zero overflow.

## Operational Workflow
1. Initialize viewport simulation via `viewport-tester`.
2. Inspect bounding box dimensions for container overflows.
3. Emit automated layout verification report.
