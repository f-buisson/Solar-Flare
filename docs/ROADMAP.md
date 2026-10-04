# Solar Flare — Engineering Roadmap

This roadmap turns the existing V1.3 design into a measured, reproducible POC before further feature work.

## Current engineering baseline

- Public design documentation: V1.1 → V1.2 → V1.3.
- A complete offline POC package exists with SolidWorks assemblies/parts, STEP export, STL exports, BOM and fabrication notes.
- Current POC lens baseline: **Edmund Optics #43-013**, 139.7 × 139.7 mm (5.5 × 5.5 in), EFL 254 mm (10 in), acrylic, uncoated, 85% typical transmission, 80 °C maximum operating temperature.
- The offline final-POC BOM dated 2026-01-27 identifies the lens by dimensions and focal length (5.5 × 5.5 in, 10 in focal length), which is consistent with #43-013. The BOM still needs an explicit manufacturer part number before P0 can close.
- The same BOM specifies a nominal Ø12 retaining ring with **+0.2 to +0.3 mm recommended internal clearance (12.2–12.3 mm)**. This documents the intended clearance, but does not yet prove that the final printable geometry implements it.
- An older candidate lens (#32-686, 170.18 × 170.18 mm, EFL 304.8 mm) exists in the engineering archive but is **not** the current final-POC baseline.
- The current final POC STL package spans roughly **709 × 466 × 709 mm** in its export coordinate frame. This is an engineering-envelope check, not a certified product dimension.

The public ~18 W figure remains an **estimate** until calorimetric or equivalent measurements are published.

## P0 — Freeze one buildable POC baseline

Before adding new features:

- [ ] Confirm the final assembly, STEP and STL exports all correspond to the same configuration.
- [ ] Confirm #43-013 is the lens used by the BOM, CAD support and test plan. **Partial evidence:** the offline final BOM matches #43-013 dimensions/EFL, but names no manufacturer part number; CAD support and test-plan checks remain open.
- [ ] Resolve all historical ×3 / larger-lens references so they cannot be confused with the current POC.
- [ ] Check the 0.2 mm-clearance printable variant against the final assembly. **Partial evidence:** the offline BOM explicitly recommends 12.2–12.3 mm ID for the nominal Ø12 retaining ring; exported/final CAD geometry still needs verification.
- [ ] Produce a single definitive BOM revision with materials, quantities, mirror substrate/film and adhesives.
- [ ] Record the intended hinge-axis materials and flexible-cap solution.

**Exit proof:** one archived build package with a revision ID, matching CAD/export/BOM/lens reference.

## P1 — Mechanical and safety validation

Priority is safe control of concentrated sunlight, not aesthetics.

- [ ] Verify all four reflector hinges move through their full range without interference.
- [ ] Validate the synchronized opening/closing mechanism under realistic cable tension.
- [ ] Add/verify positive open and closed stops.
- [ ] Ensure a fast, reliable way to remove the focused beam from the target.
- [ ] Verify the lower aiming mirror cannot redirect the focus onto the structure in normal use.
- [ ] Replace load-bearing hinge pins with metal where required.
- [ ] Keep flexible caps/bushings in TPU/TPE or use commercial retaining hardware rather than stressed PLA.
- [ ] Define a safe exclusion zone around the focal path.

**Exit proof:** repeated open/close cycles without jam, loss of alignment, unsafe beam path or structural damage.

## P2 — Optical and thermal test campaign

Do not infer output power from collection area alone.

Measure at minimum:

1. ambient conditions and solar irradiance;
2. aperture/configuration used;
3. focal-spot size and position;
4. useful thermal power with a controlled absorber or calorimetric target;
5. temperature at the absorber, lens mount and nearby polymer parts;
6. sensitivity to angular misalignment;
7. performance with and without the lower deflector mirror;
8. shutdown/defocus time.

The acrylic Fresnel lens is specified for **80 °C maximum operating temperature**. The test setup must verify that the lens and mount remain below their safe operating limits.

**Exit proof:** a repeatable test sheet with raw measurements, uncertainty and at least three comparable runs.

## P3 — Reconcile claims with measurements

After P2:

- [ ] Replace estimated power claims with measured ranges.
- [ ] Publish the exact tested configuration.
- [ ] Separate incident solar power, optical throughput and useful delivered thermal power.
- [ ] Document losses from reflector alignment, lens transmission, beam clipping and the deflector mirror.
- [ ] Remove or qualify any use-case claim that exceeds the measured envelope.

## P4 — Public build package

Only after the POC baseline is stable:

- [ ] Publish validated STEP/STL exports and a clean BOM.
- [ ] Decide whether to publish native SolidWorks sources with the same validated revision.
- [ ] Add assembly instructions and printable-part orientation/tolerance notes.
- [ ] Add a reproducible test protocol and measured results.

## P5 — Downstream projects

SolarLift and SolarWell must consume a **measured Solar Flare thermal envelope**, not a nominal or theoretical figure.

A downstream design should state:

- tested input configuration;
- useful thermal-power range;
- duty cycle / tracking assumptions;
- allowable target geometry;
- thermal and alignment limits.

No downstream performance claim should exceed that measured envelope without an explicitly larger collector or additional energy source.

---

## French summary

Priorité : figer un seul POC cohérent, le construire, vérifier la mécanique et la sécurité, puis mesurer réellement la puissance utile. Les améliorations et intégrations SolarLift/SolarWell viennent ensuite. La lentille POC actuellement retenue est la **#43-013 (139,7 mm, focale 254 mm)** ; l'ancienne piste 170,18 mm / 304,8 mm reste historique tant qu'elle n'est pas réadoptée explicitement.
