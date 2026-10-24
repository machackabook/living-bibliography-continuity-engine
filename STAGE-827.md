# Stage 827 — triangular floor snap to 2π/3 and y sector free of theta*5 (2026-10-23 19:10 CDT)

Connecting chat re-pasted the complete `update(t)` function.

## Session pin
- session hash `beec41f1`. Living hash `7cd81012`.
- Triangular case: tAngle = Math.floor(this.theta / (Math.PI * 2 / 3)) * (Math.PI * 2 / 3);
- x = major * Math.cos(tAngle) + minor * Math.cos(this.theta * 5);
- z = major * Math.sin(tAngle) + minor * Math.sin(this.theta * 5);
- y = (this.idx % 3 - 1) * major * 0.5 + Math.sin(t) * minor;
- Floor snap to 2π/3 for lattice vertex. Raw theta*5 on minor ripple (x/z only). Y sector free of theta*5.
- No secrets. Paste not rewritten.

## Compiled next stages
1. 828 — hold torus/default tube (major + minor * cos(phi)) shared by x/z; y shared with infinity.
2. 829 — hold uniforms order uTime then uGravity.
3. 830 — hold lerp alpha literal 0.05; session allocates new Vector3 (living may reuse).

NUMERAL=137451921129154222
