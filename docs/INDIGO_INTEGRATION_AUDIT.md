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

## Verification pass — 2026-11-15
- Verified package metadata from default branch: Spark 2.4.0; MIT; Three.js peer dependency >=0.180.0; Node/Vite/TypeScript with Rust/WASM build stage.
- Available commands confirmed: `npm run lint`, `npm test`, `npm run types`, `npm run test:browser`, `npm run test:rust`, `npm run build:wasm`.
- README example loads `butterfly.spz` from a remote demo asset. This is a rendering example, **not** a scientific dataset; attribution/redistribution permissions must be checked before reuse.
- Execution blocker: current build environment cannot resolve github.com, so repository checkout and tests have **not** run. No CI success is claimed.
- Browser requirements: WebGL2; performance and fallback remain unverified on target mobile hardware.
- Next gate: use an accessible CI runner or checkout to execute tests; capture logs and commit SHA before demo integration.
