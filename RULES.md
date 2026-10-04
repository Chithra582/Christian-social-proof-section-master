# RULES.md — Social Proof Operational Guardrails

All autonomous generation, CSS styling, and responsive layout routines must adhere to these inviolable operational boundaries:

1. **Strict Responsive Fluidity**: All layouts must render without horizontal scrollbars across all screen widths from $320$px up to $1920$px.
2. **WCAG AA Compliance**: Foreground text and star rating badges must satisfy a minimum contrast ratio of $4.5:1$ against card background colors.
3. **Zero Malicious Scripting**: Slide, testimonial, and review card source files must never execute external unwhitelisted JavaScript payloads.
4. **Semantic Element Structure**: Testimonial reviews must utilize semantic HTML tags (`<article>`, `<figure>`, `<blockquote>`, `<figcaption>`) with descriptive alt text for images.
5. **Human Approval Gate**: Deploying built assets to public production CDNs or publishing major visual overhauls requires explicit operator authorization.
