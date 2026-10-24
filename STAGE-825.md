# Stage 825 — infinity lemniscate scale = major * 1.5 and denom shared by x/z only; y shared with torus (2026-10-23 19:10 CDT)

Connecting chat re-pasted the complete `update(t)` function.

## Session pin
- session hash `beec41f1`. Living hash `7cd81012`.
- Infinity case: scale = major * 1.5
- denom = 1 + Math.pow(Math.sin(this.theta), 2)
- x = (scale * Math.cos(this.theta)) / denom
- z = (scale * Math.sin(this.theta) * Math.cos(this.theta)) / denom
- y = minor * Math.sin(this.phi) * Math.sin(t * 0.5 + this.idx)   // shared with torus/default; unread by denom or scale
- Major = 10 + (idx * 2) assigned before switch. Minor = 3 + (toroidalWeave * 2).
- Phi unread inside paste. No secrets. Paste not rewritten.

## Compiled next stages
1. 826 — hold hamiltonian hScale = major; y lift sin(t)*2 unread by hScale/minor/phi.
2. 827 — hold triangular floor snap to 2π/3 and y sector free of theta*5.
3. 828 — hold torus/default tube (major + minor * cos(phi)) on x/z; y shared.

NUMERAL=137451921129154222
Connecting repos: gaia-visualizer, The-Hive, Cryptic-Heartbeat, continuity-engine-ssos, continuity-ledger-cycle.
