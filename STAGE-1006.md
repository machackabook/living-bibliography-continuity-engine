# STAGE-1006 — Parallel pin: hold theta step (0.01 + this.idx * 0.002) * state.gravityPull unread by geometry switch (2026-11-02)

Connecting chat re-pasted the complete `update(t)` geometric field kernel. Mirrored from gaia-visualizer hop 1006.

## Session pin (paste not rewritten)
- this.theta += (0.01 + this.idx * 0.002) * state.gravityPull;
- Occurs before switch(targetState.geometry); unread by any case body.
- Full kernel otherwise as prior reaffirmation (four-case sole dispatcher).
- prior holds: 987 hamiltonian x/z free of minor; y lift free of hScale/minor.

## Enhancement this hop
Pins the theta step formula and its position outside the switch. Living path matches. Session paste remains untouched. Paste not rewritten. No secrets. No device rooted.

## Next stages compiled
1. 1007 — hold session lerp new Vector3 allocation with literal alpha 0.05.
2. 1008 — hold phi as external binding (referenced, never assigned inside update(t)).
3. 1009 — hold major/minor declarations before switch.

Numeral 137451921129154222. Paste not rewritten. No secrets. No device rooted.
Connecting: continuity-engine-ssos next in waterfall.
