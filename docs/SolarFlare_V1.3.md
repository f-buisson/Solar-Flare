# Solar Flare V1.3 — Rotating Aiming Module

> V1.3 is a **mechanical / ergonomic** evolution of Solar Flare.  
> The optical system is unchanged compared to V1.2 (see `SolarFlare_V1.2.md` for detailed optics).  
> This version adds a **rotating and tiltable aiming module under the device**, to control *where* the concentrated spot is sent.

---

## 1. Concept (EN)

The idea behind V1.3 is simple:

- keep the **same concentration system** as V1.2,
- add a **“steering block”** under the device,
- so the user can aim **anywhere below Solar Flare** without moving the main body.

The module combines:

- a **360° rotating block** around the main axis,
- a **flat mirror** mounted on a hinge, tilting from **0° to ~90°**.

![Solar Flare V1.3 – rotating aiming module](./images/SolarFlare_V1.3_schema.png)

---

## 2. Mechanical design (EN)

Main elements:

- **Circular ring** fixed under the central base.
- **Rotating block** sitting on this ring:
  - continuous **360° rotation** (or limited by mechanical stops if needed),
  - axis of rotation aligned with the optical axis.
- **Flat mirror** mounted on a **hinge** at the edge of the block:
  - tilt range: **0–90°** relative to the incoming beam,
  - the mirror is sized to intercept the full spot in the typical working range.

This design gives a **full “lower hemisphere” aiming capability**:

- with rotation (azimuth) + tilt (elevation),
- the user can practically target **any point below the device**:
  - slightly downward,
  - horizontal,
  - steeper angles towards the ground.

---

## 3. Typical use cases (EN)

- **Hand-held lighter mode**
  - Moderate tilt (e.g. ~40–60°) for a beam going downwards but still accessible in front of the user.
  - 360° rotation to position the hot spot exactly where the cigarette / tinder is.

- **Horizontal / near-horizontal aiming**
  - Tilt angle chosen so the beam is almost horizontal.
  - Useful to reach a target at similar height without putting the device in an awkward posture.

- **Vertical spot under the device**
  - Mirror tilted enough so that it **no longer intercepts the beam**.
  - The spot forms directly below Solar Flare, convenient if the device is on a stand or tripod.

---

## 4. Integration with V1.1 / V1.2 (EN)

- V1.1 introduced the **solar sight** and the first cable system.
- V1.2 added the **synchronized mirror closing mechanism**.
- V1.3:
  - does **not** modify the optical geometry,
  - only adds an **optional bottom module**,
  - can be:
    - removed,
    - replaced by a simpler fixed mirror,
    - or kept for ergonomic, “point-where-you-want” usage.

For detailed optical explanations (mirrors, Fresnel lens, focal distance), refer to:

- `SolarFlare_V1.1.md`
- `SolarFlare_V1.2.md`

---

## 5. Current status & next steps (EN)

Status:

- Concept **fully defined in CAD**.
- First schematic image available:  
  `docs/images/...` (V1.3 schema).

Next steps:

- 3D printing / machining of the rotating block.
- Check:
  - alignment between **beam axis** and **hinge axis**,
  - **mirror size vs. spot size** for all useful tilt angles,
  - friction / locking system for rotation and tilt.
- Real-sun tests to:
  - validate comfort and aiming precision,
  - confirm that the mirror survives local heating.

---

# Solar Flare V1.3 — Module de visée rotatif

> La V1.3 est une évolution **mécanique / ergonomique** de Solar Flare.  
> Le système optique reste inchangé par rapport à la V1.2  
> (voir `SolarFlare_V1.2.md` pour les détails optiques).  
> Cette version ajoute un **module de visée rotatif et inclinable sous l’appareil**, pour contrôler *où* le point chaud est envoyé.

---

## 1. Concept (FR)

L’idée de la V1.3 :

- conserver le **même système de concentration** que la V1.2,
- ajouter un **“bloc de pilotage”** sous l’appareil,
- permettre à l’utilisateur de viser **n’importe où vers le bas** sans bouger le corps principal.

Le module combine :

- un **bloc rotatif à 360°** autour de l’axe principal,
- un **miroir plan** monté sur une charnière, inclinable de **0° à ~90°**.

![Solar Flare V1.3 – rotating aiming module](./images/SolarFlare_V1.3_schema.png)

---

## 2. Conception mécanique (FR)

Éléments principaux :

- **Couronne circulaire** fixée sous la base centrale.
- **Bloc rotatif** monté sur cette couronne :
  - rotation continue à **360°** (ou limitée par des butées),
  - axe de rotation aligné sur l’axe optique.
- **Miroir plan** monté sur une **charnière** en bout de bloc :
  - plage d’inclinaison : **0–90°** par rapport au faisceau descendant,
  - dimensionné pour couvrir tout le spot dans la zone de fonctionnement.

Ce design offre une **capacité de visée sur toute la “demi-sphère” inférieure** :

- rotation = azimut,
- inclinaison = élévation,
- au final, on peut viser pratiquement **n’importe quel point situé sous l’appareil** :
  - légèrement vers le bas,
  - presque horizontal,
  - ou fortement incliné vers le sol.

---

## 3. Exemples d’utilisation (FR)

- **Mode “allume-feu en main”**
  - Inclinaison modérée (≈40–60°) pour un faisceau dirigé vers le bas tout en restant accessible devant l’utilisateur.
  - Rotation à 360° pour placer le point chaud exactement là où se trouve la cigarette / l’amadou.

- **Visée horizontale ou quasi horizontale**
  - Angle choisi pour que le faisceau soit presque horizontal.
  - Pratique pour atteindre une cible à hauteur comparable, sans mettre l’appareil dans une position inconfortable.

- **Point focal vertical sous l’appareil**
  - Miroir suffisamment relevé pour **ne plus intercepter le faisceau**.
  - Le point chaud apparaît directement sous Solar Flare, utile si l’appareil est posé sur un support.

---

## 4. Intégration avec V1.1 / V1.2 (FR)

- La V1.1 a introduit le **viseur solaire** et un premier système de câbles.
- La V1.2 a ajouté le **mécanisme de fermeture synchronisée** des miroirs.
- La V1.3 :
  - ne touche pas à la **géométrie optique**,
  - ajoute uniquement un **module inférieur optionnel**,
  - peut être :
    - démonté,
    - remplacé par un miroir fixe simple,
    - ou conservé pour une utilisation plus ergonomique “je vise où je veux”.

Pour les explications détaillées sur l’optique, se référer à :

- `SolarFlare_V1.1.md`
- `SolarFlare_V1.2.md`

---

## 5. État actuel & prochaines étapes (FR)

État :

- Concept **entièrement défini en CAO**.
- Un schéma de la V1.3 est disponible dans `docs/images/...`.

Prochaines étapes :

- Impression / usinage du bloc rotatif.
- Vérifier :
  - l’alignement **axe du faisceau / axe de charnière**,
  - la **taille du miroir par rapport au spot** pour les angles utiles,
  - le système de friction / verrouillage de la rotation et de l’inclinaison.
- Tests en plein soleil pour :
  - valider le confort de visée,
  - confirmer la tenue thermique du miroir et du bloc.
