# Indigo Atlas Spark prototype

This is an isolated proof of concept, **not a deployed Universe Atlas integration**.

## Preview locally

Serve the repository root using any local static HTTP server and open `/examples/indigo-atlas/`. The prototype imports Three.js 0.180.0 from jsDelivr and Spark 2.4.0 from the upstream Spark CDN. Internet access is required.

The scene initially displays a coordinate grid and axes. To view splats, paste a **trusted, licensed, HTTPS URL ending in .spz** and select **Load splat**. The source server must permit browser cross-origin requests (CORS). The sample scene is illustrative only; coordinates are not celestial astrometry.

## Verification checklist

- [ ] Confirm page opens with no JavaScript errors on desktop
- [ ] Confirm orbit, pan and zoom behavior
- [ ] Confirm reset returns camera to initial position
- [ ] Confirm missing WebGL2 produces a useful error
- [ ] Confirm invalid URLs are rejected
- [ ] Confirm a permitted .spz asset loads and displays
- [ ] Confirm CORS/network errors are surfaced adequately (current implementation may only log them)
- [ ] Measure mobile FPS, memory use and loading time
- [ ] Verify accessibility and small-screen layout
- [ ] Run upstream tests: `npm run lint`, `npm test`, `npm run types`, `npm run test:browser`, `npm run test:rust`
- [ ] Audit dependencies and security before deployment

## Known limitations

No CI or browser tests have been executed for this prototype. No sample asset is bundled; this avoids copying material without licence verification. The prototype is not yet integrated with Uranometria. Loading an untrusted remote URL may expose the viewer's IP address to the asset host. It does not implement astronomical reference frames, FITS/WCS reprojection, precise coordinates, observation epochs or scientific uncertainty.

## Scope guard

No merges, deployments, purchases or edits to other projects without approval.
