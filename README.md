# cleanX — Illini Move & Clean experimental fork

This is a complete source-code fork of [howyoungx/illini-move-clean](https://github.com/howyoungx/illini-move-clean), created as the foundation for cleanX experimentation and adaptation.

## Credit and acknowledgment

The original website, visual design, animations, pricing-panel experience, AI chat interface, quote and booking flow, images, icons, and backend implementation are credited to **howyoungx and the original Illini Move & Clean contributors**. Their original commit history and authorship are preserved in this fork.

- Original repository: https://github.com/howyoungx/illini-move-clean
- Original website: https://howyoungx.github.io/illini-move-clean/
- Imported source revision: e52a40c7dcf1c673698730d6d7b3c006a3566011

The cleanX project owner has confirmed that the original author allowed this reuse for experimentation. This acknowledgment does not claim authorship of the original work, imply endorsement, or grant additional rights to third parties.

## What was copied

The full original main-branch source and its 20-commit history were forked, including index.html, the assets directory, the worker directory, .gitignore, and .nojekyll. The imported application files are unchanged at this stage; this README adds attribution and project context only.

## Experimental setup

This repository is separate from haxsupport/cleanX, preserving the existing cleanX site as a fallback. The intended adaptation retains the original design and interactions while substituting cleanX branding, Chicago service-area coverage, the approved residential prices, monthly commercial rates, and dani@hax.support for quote requests.

A repository fork copies code and assets, but not deployed Worker services, AI-provider credentials, private environment variables, email activation, or payment accounts. The imported code still references the original service endpoints. Before publishing an independent cleanX deployment or testing real customer submissions, replace those connections with cleanX-owned services. Do not use the original business’s AI quota, booking inbox, or payment account without separate authorization.
