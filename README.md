**Language:** [English](#-solar-flare-v1--open-hardware-prototype) | [Français](#-solar-flare-v1--prototype-open-hardware)

# 🔆 Solar Flare V1 – Open Hardware Prototype

![Solar Flare V1 – schema](images/schema_solar_flare.png)  
![Solar Flare V1 – fermé](images/mesure_fermé_2.png)

Solar Flare is an experimental prototype of a **foldable solar concentrator**, designed to demonstrate the possibility of turning a small, portable surface into a powerful solar focal point.  
This project is released as **open hardware** (under a dual license, see below) to share the idea, gather feedback, and explore wider applications.

---

## ⚙️ How it works

The system uses a **folded optical path**:  
- Foldable **lower parabolic reflectors** form the main deployed solar aperture.  
- They redirect the collected light toward an **upper parabolic / concave reflector**.  
- The upper reflector sends the flux back downward through the central **Fresnel lens**.  
- The Fresnel lens performs the final concentration into a **primary focal zone** below the device.

The Fresnel lens is therefore not simply a directly illuminated collector surrounded by auxiliary mirrors: it is the final concentrating stage of a larger folded reflective aperture.

👉 Special feature:  
An **optional secondary deflector mirror** can be added at the bottom of the device.  
- Without the mirror: the focal point is vertical, directly under the lens (maximum efficiency).  
- With the mirror: the beam is redirected horizontally, which effectively deviated the final focal. This makes it easier to light a cigarette or ignite material while holding the device sideways, **without risking damage to the lens or burning the structure** due to the short focal length (~3 cm).  
This mirror acts as an **ergonomic module**, optional but practical for portable use.

---

## 📐 Current dimensions (V1)

- **Open**: ~282 mm × 282 mm × 184 mm (mirrors deployed).  
- **Closed**: ~170 mm × 170 mm × 150 mm (mirrors folded).  
- **V1 historical collecting-area estimate**: about 321 cm². The associated ~18 W figure is a **calculated V1 estimate, not a measured result**. The enlarged POC uses different geometry and must be evaluated separately from its CAD and physical tests.

---

## 🛠️ Improvement goals

- **Portability**: optimize folding to reduce packed size.  
- **Automation**: design a synchronization system for simultaneous mirror opening/closing.  
- **Locking**: add solid blocking systems to prevent unwanted movement.  
- **Performance**:  
  - optimize geometry to reduce optical losses,  
  - explore a **miniature version** (portable fire starter),  
  - and a **large-scale version** (solar heating, cooking, industrial applications).  

---

## 💡 Potential applications

- 🔥 **Portable fire starter** (campfire, barbecue, cigarette).  
- 🌞 **Educational demonstration module** for solar energy.  
- 🔋 **Possible extensions**:  
  - detachable photovoltaic cell for USB charging,  
  - small Stirling engine to produce motion or ventilation,  
  - large-scale version for home heating, camper vans, or light industry.  
[futur](docs/futur.md)

---

## 🔗 Used in other open-hardware projects

Solar Flare is also used as a **core solar heat module** in other open-hardware concepts:

- **[SolarLift](https://github.com/f-buisson/SolarLift)** – thermal-lift-based **gravity energy storage** (heat → mechanical lift → potential energy).  
- **[SolarWell](https://github.com/f-buisson/SolarWell)** – **low-tech solar distillation** unit to turn seawater or polluted water into drinkable water using only the sun.

These projects reuse Solar Flare as a **shared concentrator**, and explore how the same solar hardware can:
- lift weights slowly (SolarLift),
- produce small amounts of clean water (SolarWell).

---

## 🌞 Sun-tracking concepts (doc)

Solar Flare can be used with or without tracking.  
Several **low-tech ideas** to keep the concentrator roughly aligned with the sun (thermal tracking with bimetal strips, gravity-driven “clock” systems, hybrid micro-powered tracking, and integration with SolarLift / SolarWell) are described in:

- **[Sun tracking concepts](docs/Sun_Tracking_concepts.md)**

---

## 📂 Provided resources

- 3D SolidWorks plans (screenshots and flat drawings).
  [Solar open](images/Solar_Open.PNG)
  [Solar divers](images/vue_divers.PNG)
 
- PDF files showing the **open** and **closed** versions.
  [Assemblage V1 – fermé](images/Assemblage_V1_fermé.PNG)
  [Assemblage V1 – ouvert](images/Assemblage_V1_ouvert.PNG)
  
---

## 🧪 Prototyping approach (planned)

To avoid jumping directly into miniaturization, the next physical build will be a **scale ×2,5 Proof of Concept** (relative to the current V1 CAD).
The goal is to obtain a **more robust, less portable but more performant** first unit and to validate the global geometry and mechanical behavior more easily.

This ×2,5 scale also helps reduce early issues linked to a **very short focal distance** in the ×1 format, making alignment and testing safer and more repeatable.

Planned steps:
- **POC ×2,5**: validate optics, folding logic, mechanical reliability, and thermal constraints.
- **DFM pass**: simplify parts and improve tolerances for easier assembly.
- **Portable scale ×1**: re-miniaturize with validated geometry.
- **Micro-series (~10 units)**: optimize cost and assembly for limited production.

The current final-POC engineering package uses an **Edmund Optics #43-013 Fresnel lens (139.7 × 139.7 mm, EFL 254 mm)**. A larger 170.18 mm / 304.8 mm lens was evaluated earlier but is not the current final-POC baseline.

Engineering gates and measurement plan: **[docs/ROADMAP.md](docs/ROADMAP.md)**.

---

## 🔐 License & Usage

This project is **open-hardware**: you are free to learn from it, modify it, repair it, and reproduce it.

- **Personal / educational / non-commercial use** → OK ✅  
  (CERN-OHL-S 2.0 + CC BY-NC-SA 4.0)

- **Commercial use of the hardware design** → permitted under CERN-OHL-S 2.0, provided every derivative is published under the same licence.

- **Commercial use of the documentation and media** → outside the scope of CC BY-NC-SA 4.0. There is nothing to purchase: describe the intended use by e-mail and the request is answered case by case. See [DUAL_LICENSE.md](governance/DUAL_LICENSE.md).

---

## Project evolution

  * [Version 1.1](docs/SolarFlare_V1.1.md) – Added a functional solar sight + first cable system (to be optimized).
  * [Version 1.2](docs/SolarFlare_V1.2.md) – Added a synchronized mirror actuation system using cable routing + alignment rails.
    * All mirrors open/close together
    * Improved global alignment
    * Trade-off: slightly larger mechanism + requires precise cable tensioning
  * [Version 1.3](docs/SolarFlare_V1.3.md) – Added a rotating aiming module under the device**
    * New bottom block that can rotate 360° around the main axis.
    * Flat mirror mounted on a hinge, tilting from 0° to ~90°.
    * Allows aiming the concentrated spot **anywhere below the device** (from slightly downward to near-horizontal).
    * If the mirror is tilted out of the beam, the spot simply appears vertically under Solar Flare.
    * V1.3 does not change the optical design; it only adds an ergonomic “steering” layer.

![Solar Flare V1.3 – rotating aiming module](images/schematic_solarflare_v1.3.png)

---

## 📣 Contribution & feedback

This project is still at the **experimental prototype stage**.  
Any constructive criticism, suggestions for mechanical or optical improvements are welcome.  
You can open an **issue** or submit a **pull request**.

---

### 🫶 Support this work

These projects are released as open hardware so anyone can study, adapt and rebuild them.
If you want to support the work, GitHub Sponsors is open:
👉 https://github.com/sponsors/f-buisson

Sponsoring is entirely optional. It grants **no** commercial rights, **no** licence and **no** private access — it simply helps fund materials and prototypes.

---

## ⚠️ Disclaimer

This prototype is an **experimental project**.  
It is **not designed for direct commercial use**, nor guaranteed in terms of safety.  
⚠️ Warning: the solar focal point can reach dangerous temperatures. Use only outdoors, with caution.

---

# 🔆 Solar Flare V1 – Prototype Open Hardware

![Solar Flare V1 – schema](images/schema_solar_flare.png)  
![Solar Flare V1 – fermé](images/mesure_fermé_2.1.png)


Solar Flare est un prototype expérimental de **concentrateur solaire pliable**, conçu pour démontrer la possibilité de transformer une petite surface transportable en un foyer solaire puissant.  
Ce projet est publié en **open hardware** (sous licence mixte, voir plus bas) afin de partager l’idée, recueillir des retours, et explorer des usages plus larges.

---

## ⚙️ Fonctionnement

Le système utilise un **trajet optique replié** :  
- Des **réflecteurs paraboliques inférieurs** déployables constituent l’ouverture solaire principale.  
- Ils renvoient la lumière collectée vers un **réflecteur parabolique / concave supérieur**.  
- Ce réflecteur supérieur renvoie ensuite le flux vers le bas, à travers la **lentille de Fresnel** centrale.  
- La Fresnel assure la concentration finale vers une **zone focale principale** sous l’appareil.

La lentille de Fresnel n’est donc pas simplement un collecteur directement éclairé entouré de miroirs auxiliaires : elle constitue le dernier étage de concentration d’une ouverture réfléchissante repliée plus grande.

👉 Particularité :  
Un **miroir déflecteur secondaire optionnel** peut être ajouté en bas du dispositif.  
- Sans miroir : le foyer est vertical, directement sous la lentille (rendement maximal).  
- Avec miroir : le rayon est dévié horizontalement, ce qui permet de dévier la focale finale et par exemple d’allumer une cigarette ou un combustible en tenant l’objet sur le côté, **sans risquer d’endommager la lentille ni de brûler la structure** à cause de la courte distance focale (~3 cm).  
Ce miroir agit comme un **module ergonomique**, facultatif mais pratique pour un usage portatif.

---

## 📐 Dimensions actuelles (V1)

- **Ouvert** : ~282 mm x 282 x 184 mm  (miroirs déployés).  
- **Fermé** : ~170 mm x 170 x 150 mm (miroirs repliés).  
- **Estimation historique de zone collectrice V1** : environ 321 cm². La valeur associée d’environ 18 W est une **estimation calculée de la V1, pas une mesure**. Le POC agrandi possède une géométrie différente et doit être évalué séparément à partir de sa CAO puis d’essais physiques.

---

## 🛠️ Objectifs d’amélioration

- **Portabilité** : optimiser le pliage pour réduire l’encombrement.  
- **Automatisation** : concevoir un système de synchro pour ouverture/fermeture simultanée des miroirs.  
- **Verrouillage** : ajouter des systèmes de blocage solides pour éviter les mouvements parasites.  
- **Performance** :  
  - optimiser la géométrie pour réduire les pertes optiques,  
  - envisager une version **miniature** (allume-feu portable),  
  - et une version **grande échelle** (chauffage solaire, cuisine, applications industrielles).  

---

## 💡 Applications envisagées

- 🔥 **Allume-feu portable** (feu de camp, barbecue, cigarette).  
- 🌞 **Module de démonstration pédagogique** sur l’énergie solaire.  
- 🔋 **Extensions possibles** :  
  - cellule photovoltaïque amovible pour recharge USB,  
  - micro-moteur Stirling pour produire du mouvement ou ventiler,  
  - version géante pour chauffage domestique, camping-car, ou petite industrie.  
[futur](docs/futur.md)

---

## 🔗 Utilisé dans d’autres projets open-hardware

Solar Flare est également utilisé comme **module de chaleur solaire central** dans d’autres concepts open-hardware :

- **[SolarLift](https://github.com/f-buisson/SolarLift)** – système de **stockage d’énergie gravitaire** par élévation lente de poids via la chaleur solaire.  
- **[SolarWell](https://github.com/f-buisson/SolarWell)** – unité de **distillation solaire low-tech** pour transformer de l’eau de mer ou légèrement polluée en eau potable uniquement grâce au soleil.

Ces projets réutilisent Solar Flare comme **concentrateur commun**, et explorent comment le même hardware solaire peut :
- stocker un peu d’énergie (SolarLift),  
- produire un peu d’eau potable (SolarWell).

---

## 🌞 Concepts de suivi solaire (doc)

Solar Flare peut être utilisé avec ou sans système de suivi.  
Quelques pistes **low-tech** pour garder le concentrateur à peu près aligné sur le soleil (suivi thermique par lames bimétalliques, systèmes gravitaires type horloge, suivi hybride micro-alimenté, intégration avec SolarLift / SolarWell) sont décrites ici :

- **[Concepts de suivi solaire](docs/Sun_Tracking_concepts.md)**

---

## 📂 Ressources fournies

- Plans 3D SolidWorks (captures et mises à plat).
  [Solar open](images/Solar_Open.PNG)
  [Solar divers](images/vue_divers.PNG)
  
- Fichiers PDF illustrant la version **ouverte** et **fermée**.  
  [Assemblage V1 – fermé](images/Assemblage_V1_fermé.PNG)
  [Assemblage V1 – ouvert](images/Assemblage_V1_ouvert.PNG)

  ---

## 🧪 Approche de prototypage (prévue)

Pour éviter de commencer directement par la miniaturisation, la prochaine réalisation physique sera un **Proof of Concept à l’échelle ×2,5** (par rapport à la CAO actuelle V1).
L’objectif est d’obtenir un premier prototype **plus robuste, moins portable mais plus performant**, afin de valider la géométrie globale et le comportement mécanique avec un confort de test supérieur.

Cette échelle ×2,5 permet aussi de limiter les difficultés initiales liées à une **distance focale très faible** au format ×1, rendant l’alignement et les essais plus sûrs et plus reproductibles.

Étapes envisagées :
- **POC ×2,5** : validation optique, logique de pliage, fiabilité mécanique et contraintes thermiques.
- **Passe DFM** : simplification des pièces et optimisation des tolérances.
- **Version portable ×1** : re-miniaturisation avec géométrie validée.
- **Micro-série (~10 unités)** : optimisation coût/assemblage pour production limitée.

---

## 🔐 Licence & Conditions d’usage

Ce projet est publié en **open-hardware** : vous êtes libre de l’**étudier**, le **modifier**, le **réparer** et le **reproduire**.

- **Usage personnel / éducatif / non-commercial** → Autorisé ✅  
  (CERN-OHL-S 2.0 + CC BY-NC-SA 4.0)

- **Usage commercial de la conception matérielle** → autorisé par CERN-OHL-S 2.0, à condition de publier chaque dérivé sous la même licence.

- **Usage commercial de la documentation et des médias** → hors du périmètre de CC BY-NC-SA 4.0. Rien n’est à acheter : décrivez l’usage envisagé par e-mail, la demande est traitée au cas par cas. Voir [DUAL_LICENSE.md](governance/DUAL_LICENSE.md).


---

## Évolution du projet

  * [Version 1.1](docs/SolarFlare_V1.1.md) – Ajout d’un viseur solaire fonctionnel + premier système de câbles (à optimiser).
  * [Version 1.2](docs/SolarFlare_V1.2.md) – Ajout d’un système de synchronisation des miroirs via câbles + rails de guidage.
    * Ouverture / fermeture simultanée des panneaux
    * Alignement global amélioré
    * Compromis : légère augmentation de l’encombrement + nécessité d’un réglage précis des câbles
  * [Version 1.3](docs/SolarFlare_V1.3.md) – Ajout d’un module de visée rotatif sous l’appareil**
    * Nouveau bloc inférieur rotatif à 360° autour de l’axe principal.
    * Miroir plan monté sur charnière, inclinable de 0° à ~90°.
    * Permet de viser le point chaud **vers n’importe quelle direction située sous l’appareil** (du légèrement vers le bas jusqu’au quasi horizontal).
    * Quand le miroir est sorti du faisceau, le point focal apparaît simplement à la verticale, sous Solar Flare.
    * La V1.3 ne modifie pas le design optique ; elle ajoute uniquement une couche de pilotage plus ergonomique.

![Solar Flare V1.3 – rotating aiming module](images/schematic_solarflare_v1.3.png)

---

## 📣 Contribution & retours

Ce projet est encore **au stade de prototype expérimental**.  
Toute critique constructive, suggestion d’optimisation mécanique ou optique est la bienvenue.  
Vous pouvez ouvrir une **issue** ou proposer une **pull request**.

---

### 🫶 Soutenir ce travail

Ces projets sont publiés en open hardware pour que chacun puisse les étudier, les adapter et les reconstruire.
Si vous souhaitez soutenir ce travail, GitHub Sponsors est ouvert :
👉 https://github.com/sponsors/f-buisson

Le sponsoring est entièrement facultatif. Il n’ouvre **aucun** droit commercial, **aucune** licence et **aucun** accès privé — il aide simplement à financer le matériel et les prototypes.

---

## ⚠️ Disclaimer

Ce prototype est un projet **expérimental**.  
Il n’est **pas conçu pour un usage commercial direct**, ni garanti en termes de sécurité.  
⚠️ Attention : le foyer solaire peut atteindre des températures dangereuses. Utiliser uniquement en extérieur, avec précaution.

---
