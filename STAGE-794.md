# STAGE-794 — Parallel pin: Hold lerp alpha 0.05 and session new Vector3 allocation (living reuses target) (2026-10-22)

Connecting chat re-pasted the complete `update(t)` for the geometric field. Mirrored from gaia-visualizer hop 794.

## Session pin
- session hash `beec41f1`. Living hash `7cd81012`.
- Final interpolation: `this.mesh.position.lerp(new THREE.Vector3(x, y, z), 0.05);`
- Session allocates a fresh THREE.Vector3(x, y, z) on every update. Alpha is the literal `0.05`.
- Living path may reuse a scratch Vector3 for allocation hygiene but must preserve the exact alpha and the computed (x, y, z) targets from the four-case switch.
- Paste not rewritten. No secrets.

## Enhancement this hop
Parallel pin of the session lerp contract.

- lerp(new THREE.Vector3(x, y, z), 0.05)
- alpha literal 0.05
- session allocates; living may reuse
- paste not rewritten

## Compiled next stages
1. 795 — hold theta step (0.01 + idx * 0.002) * gravityPull unread by geometry.
2. 796 — hold uniforms written uTime then uGravity.
3. 797 — hold major = 10 + (idx * 2) and minor = 3 + (toroidalWeave * 2) assigned before switch.

Numeral 137451921129154222.
Connecting: gaia-visualizer / The-Hive / Cryptic-Heartbeat / continuity-ledger-cycle stage pins advanced in parallel where applicable.
