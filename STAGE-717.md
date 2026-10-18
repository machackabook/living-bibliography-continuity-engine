# STAGE-717 — Hold triangular sector floor (2π/3) and y lane (idx % 3 - 1) * major * 0.5 (2026-10-18)

Connecting chat re-pasted the complete `update(t)` for the geometric field.

## Session pin
- session hash `beec41f1`. Living hash `7cd81012`.
- triangular case:
  const tAngle = (Math.floor(this.theta / (Math.PI * 2 / 3)) * (Math.PI * 2 / 3));
  x = major * Math.cos(tAngle) + minor * Math.cos(this.theta * 5);
  z = major * Math.sin(tAngle) + minor * Math.sin(this.theta * 5);
  y = (this.idx % 3 - 1) * major * 0.5 + Math.sin(t) * minor;
- Floor snap to 2π/3. Y sector free of theta*5.
- Paste not rewritten. No secrets.

## Compiled next stages
1. 718 — hold torus/default tube radius (major + minor * cos(phi)) on x/z only; y shared infinity formula.
2. 719 — hold lerp alpha 0.05 and session new Vector3 allocation (living reuses _kernelTarget).

Numeral 137451921129154222.
Connecting: gaia-visualizer, The-Hive, Cryptic-Heartbeat, continuity-engine-ssos, continuity-ledger-cycle.
