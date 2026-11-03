# STAGE-1013 — pin from gaia-visualizer: hold torus/default tube (major + minor * cos(phi)) on x/z only; y shared with infinity (2026-11-02 18:11 CDT)

Connecting chat re-pasted the complete `update(t)` geometric field kernel to gaia-visualizer.

## Session pin (paste not rewritten)
- case 'torus' / default:
  - x = (major + minor * Math.cos(this.phi)) * Math.cos(this.theta);
  - z = (major + minor * Math.cos(this.phi)) * Math.sin(this.theta);
  - y = minor * Math.sin(this.phi) * Math.sin(t * 0.5 + this.idx);
- Tube radius applied only to x/z; y shared with infinity case.
- gaia-visualizer advanced to stage 1013.

## Enhancement this hop
Mirrors the kernel hold. Paste not rewritten. No secrets. No device rooted.

Numeral 137451921129154222. Next: lerp new Vector3 allocation with literal alpha 0.05.
