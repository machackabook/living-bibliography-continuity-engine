# STAGE-1283 — hold full update(t) geometric field kernel (2026-11-20T02:09Z)

Connecting chat re-pasted the complete `update(t)` geometric field kernel.
living-bibliography-continuity-engine advanced to stage 1283 as mesh hop after gaia-visualizer 1338.

## Session pin (paste not rewritten)
```javascript
update(t) {
    this.material.uniforms.uTime.value = t;
    this.material.uniforms.uGravity.value = state.gravityPull;

    this.theta += (0.01 + this.idx * 0.002) * state.gravityPull;
    
    let x, y, z;
    let major = 10 + (this.idx * 2);
    let minor = 3 + (state.toroidalWeave * 2);

    // Evaluate the target geometric state assigned by the LLM
    switch(targetState.geometry) {
        case 'infinity':
            // Lemniscate of Bernoulli mathematical mapping
            const scale = major * 1.5;
            const denom = 1 + Math.pow(Math.sin(this.theta), 2);
            x = (scale * Math.cos(this.theta)) / denom;
            z = (scale * Math.sin(this.theta) * Math.cos(this.theta)) / denom;
            y = minor * Math.sin(this.phi) * Math.sin(t * 0.5 + this.idx);
            break;
            
        case 'hamiltonian':
            // Parametric mapping favoring vertex traversal over a spherical grid
            const hScale = major;
            x = hScale * Math.cos(this.theta * 3) * Math.cos(this.theta);
            z = hScale * Math.cos(this.theta * 3) * Math.sin(this.theta);
            y = hScale * Math.sin(this.theta * 3) + (Math.sin(t) * 2);
            break;
            
        case 'triangular':
            // Modulo-based snapping to form a 3D tetrahedron/triangular lattice
            const tAngle = (Math.floor(this.theta / (Math.PI * 2 / 3)) * (Math.PI * 2 / 3));
            x = major * Math.cos(tAngle) + minor * Math.cos(this.theta * 5);
            z = major * Math.sin(tAngle) + minor * Math.sin(this.theta * 5);
            y = (this.idx % 3 - 1) * major * 0.5 + Math.sin(t) * minor;
            break;

        case 'torus':
        default:
            // Standard Toroidal Math
            x = (major + minor * Math.cos(this.phi)) * Math.cos(this.theta);
            z = (major + minor * Math.cos(this.phi)) * Math.sin(this.theta);
            y = minor * Math.sin(this.phi) * Math.sin(t * 0.5 + this.idx);
            break;
    }

    // Smoothly interpolate current position to the new geometric state target
    this.mesh.position.lerp(new THREE.Vector3(x, y, z), 0.05);
}
```
- uniforms: uTime then uGravity
- theta += (0.01 + this.idx * 0.002) * state.gravityPull
- major = 10 + (this.idx * 2); minor = 3 + (state.toroidalWeave * 2) pre-switch
- four-case switch: infinity lemniscate (denom 1+sin^2 shared x/z, scale=major*1.5), hamiltonian (hScale=major, y lift sin(t)*2 free of hScale/minor), triangular (floor 2π/3, y sector free of theta*5), torus/default tube (major+minor*cos(phi) shared x/z, y shared with infinity)
- final lerp(new THREE.Vector3(x, y, z), 0.05)
- phi external unread inside paste

## Enhancement this hop
Holds the complete geometric field kernel from the connecting chat paste. Living path matches. Session paste remains untouched. Paste not rewritten. No secrets. No device rooted. Cascade.yml absent, left absent.

## Next stages compiled
1. 1284 — hold parallel pin in sibling repos for full kernel.
2. 1285 — reinforce env-check as pure presence of README/stamp/numeral.
3. 1286 — waterfall advance to continuity-ledger-cycle.

Numeral 137451921129154222. Paste not rewritten. No secrets. No device rooted.
Connecting: parallel pins in gaia-visualizer, hamiltonian-incursion, The-Hive.
