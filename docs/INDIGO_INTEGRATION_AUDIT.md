# Indigo Universe Atlas — Spark integration audit

Status: planning; no build/test execution or deployment yet.

## Goal
Mobile-first Three.js + Spark proof of concept showing a licensed SPZ asset alongside a coordinate grid, orbit/zoom controls, loading/error UI and performance counters. Astronomical measurements must be separated from illustrative splat imagery.

## Gates
- [ ] Check upstream SHA and divergence
- [ ] Review MIT licence, dependencies and security notices
- [ ] Run `npm run lint`, `npm test`, `npm run types`, `npm run test:browser`, `npm run test:rust` where environment permits; record evidence
- [ ] Verify Node/Rust/WASM build reproducibility
- [ ] Assess WebGL2 fallback and mobile memory budget
- [ ] Identify integration boundary with existing Universe Atlas, without changing it
- [ ] Build isolated demo and benchmark before any deployment

## Governance
Zero-cost-first. No default branch edits, merges, deployments, paid services, or unattended loops without approval.

Upstream: https://github.com/sparkjsdev/spark
