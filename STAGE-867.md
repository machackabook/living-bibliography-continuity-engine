# STAGE-867 — hold theta step (0.01 + this.idx * 0.002) * state.gravityPull unread by the geometry switch (2026-10-26)

Connecting chat re-pasted the complete `update(t)` kernel for the geometric field (Three.js).

## Session pin
- `this.theta += (0.01 + this.idx * 0.002) * state.gravityPull;`
- step form is the sole gravityPull consumer; unread by the geometry switch cases
- uniforms: uTime then uGravity
- major/minor pre-switch
- sole four-case: infinity | hamiltonian | triangular | torus/default
- lerp alpha literal 0.05; session allocates new Vector3
- phi external

## Compiled next stages
1. 868 — hold major = 10 + (this.idx * 2) and minor = 3 + (state.toroidalWeave * 2) assigned before the switch
2. 869 — hold phi referenced but never assigned inside the session paste (external binding)
3. 870 — hold session paste allocates new THREE.Vector3 inside lerp; living path may reuse target

NUMERAL=137451921129154222
Connecting repos: The-Hive, gaia-visualizer, hamiltonian-incursion.
Paste not rewritten. No secrets. No device rooted.
