# 🔭 SolarFlare – Low-tech Sun Tracking Concepts  

SolarFlare can work **without any tracking**: it can simply be re-oriented by hand from time to time.

This document gathers several **low-tech sun-tracking ideas** to keep SolarFlare “roughly aligned” with the sun over the day, with a focus on:

- **low-tech**, repairable mechanisms,  
- compatibility with **SolarLift** (gravity storage) and **SolarWell** (solar distillation),  
- no heavy electronics or high-precision control.

It is a **concept toolbox**, not a fixed blueprint.

---

## Sun tracking concepts

### 🎯 Goal of tracking

Tracking is optional, but it can:

- reduce how often someone needs to adjust SolarFlare,
- keep the **focus zone** within an acceptable range (for SolarLift, SolarWell, or a focal spot),
- stay within a **low-tech, resilient** approach.

We are aiming for **“good enough” tracking**, not telescope-grade accuracy.

---

### ⚙️ Basic constraints

- Must tolerate:
  - dust, heat, thermal expansion,
  - approximate hand-made tolerances.
- Works on **slow time scales** (minutes / hours), not milliseconds.
- Should fail **gracefully**: if tracking is not perfect, SolarFlare still works.

> Note: **manual adjustment** (every 30–60 minutes) remains the zero-tech baseline and should always be possible, even if tracking modules fail.

---

## 1️⃣ Thermal tracking with bimetallic strips

### 🧠 Idea

Use **bimetallic strips** as both **sensor and actuator** for orientation, inside a small box heated by a **dedicated lens**.

- A bimetal strip bends when heated.
- The better the lens alignment with the sun, the **stronger the heating** → the more the strip bends.
- By geometry + positioning of the lens, one can design a system that “prefers” a certain orientation.

### 🔍 Example principle

- A small **thermal box** is attached to or near SolarFlare.
- On top: a **mini lens** that concentrates light on one or more bimetallic strips.
- The setup is tuned so that at **solar noon**, when SolarFlare is properly oriented:
  - the lens gives **maximum heating** to the strip → maximum bending.
- Before/after noon, the sun angle changes:
  - concentration decreases,
  - strip temperature & curvature decrease.

The bimetal deformation can:

- push a **lever**,
- or act on a **ratchet system**,

to rotate SolarFlare by small steps.

### ✅ Pros

- No electronics.
- Few moving parts if designed well.
- Self-limiting: when temperature drops, the strip returns.

### ⚠️ Limits

- Requires **experimental tuning**:
  - material choice, thickness, lens size/position, etc.
- Strong dependency on weather (clouds, ambient temperature).
- Likely better suited for **small corrections** rather than full daily tracking.

---

## 2️⃣ Gravity-driven tracking (clock / “watch button”)

### 🧠 General idea

Inspired by **weight-driven clocks**:

- A weight slowly descends,
- gear trains convert this into **very slow rotation**.

Here, the goal is to obtain:

- either a **roof-clock style** ultra-slow rotation → SolarFlare tracks the sun,
- or a **“watch with a push button”** wound by SolarLift / SolarWell.

---

### 2.1 Slow clock-like tracking

- A **weight** (concrete, metal…) is attached to a drum.
- A **gear reduction** slows the motion drastically.
- The drum drives a **rotation axis** carrying SolarFlare.
- The weight drop yields a **nearly continuous rotation**, e.g.:
  - ≈ 180° over 6–8 h of sunlight.

Motion is stabilized by:

- a **clock-style escapement**,  
- or ratchets + springs that smooth the movement.

The weight can be reset:

- manually (crank, winch), or  
- someday by **SolarLift** (SolarLift lifts a weight that then drives tracking).

---

### 2.2 “Watch with push button” – recharged by SolarLift / SolarWell

Treat the tracking module like a **mechanical watch**:

- A **main spring** stores energy.
- A small “clockwork” (gears, escapement) provides a **slow rotation** of SolarFlare.
- Instead of winding the watch manually, it can be:

  - recharged by a **SolarLift** module (lifting a small internal weight or compressing a spring),  
  - or driven by **SolarWell** (pressure changes acting on a push mechanism).

Examples:

- **With SolarLift**:  
  the main SolarLift mass (or a fraction of its motion) is used to wind a smaller spring or to lift an internal tracking weight.

- **With SolarWell**:  
  the **pressure variation** in a distillation chamber drives a small **membrane** or piston, which periodically presses a **“ratchet button”** → one click at a time, winding the spring or advancing a gear tooth.

Key idea:  
> SolarLift / SolarWell act as **mechanical chargers** for the tracking system.

---

## 3️⃣ Hybrid tracking (micro-powered)

In some cases, **a tiny amount of electricity** can simplify the mechanics without abandoning the low-tech spirit.

### 🔌 Potential sources

- **Mini solar panel**:
  - powers a **micro motor** or gear motor,
  - runs sporadically (one small step every few minutes).
- **Water current**:
  - a **micro-turbine** in a river / tidal flow provides a few milliwatts,
  - enough for very slow rotation or an electromagnetic latch.
- **Mini wind turbine**:
  - small rotor + dynamo on a windy site.

### 🧠 Logic

Electronics should remain **ultra simple**:

- ideally just a few **limit switches** or a crude timer,
- no heavy microcontroller / complex firmware.

The motor only:

- **corrects orientation** occasionally, or  
- **returns to start position** at the end of travel.

This could also become a **BioSym node** in the future:  
a tiny control unit deciding **where to point SolarFlare** (toward SolarLift, SolarWell, etc., depending on needs).

---

## 4️⃣ Integration with SolarLift & SolarWell

Tracking is not an isolated function; it can be seen as a **sub-module** in a bigger chain:

- **SolarFlare** → concentrated heat.
- **SolarLift** → gravity-based energy storage.
- **SolarWell** → solar distillation for potable water.

A few integration scenarios:

- SolarLift lifts a small internal weight used to **drive tracking** (clock / watch system).
- SolarWell’s pressure cycles drive a **push-ratchet system**, feeding a tracking spring.
- In a BioSym context, a higher-level controller decides whether SolarFlare should:
  - prioritize **energy storage** (SolarLift), or  
  - prioritize **water production** (SolarWell).

---

## 5️⃣ Status & contributions

All ideas described here are:

- **conceptual**,
- meant to be explored with **rough prototypes**, tests, and failures,
- open to **criticism, improvements, or alternative approaches**.

If you build even a partial or rough version of any of these concepts, documentation is welcome.

🔧 Contributions (issues / PRs) on:

- bimetallic strip experiments,
- clockwork / watch-like mechanics,
- ultra-low-power tracking,

are appreciated.

---

## Concepts de suivi solaire

### 🎯 Objectif du suivi

Le suivi est **optionnel**, mais il permet de :

- réduire la fréquence de réorientation manuelle de SolarFlare,
- garder la **zone de focalisation** dans une plage acceptable (SolarLift, SolarWell, foyer, etc.),
- rester dans une logique **low-tech** et résiliente.

On vise un suivi **“suffisamment bon”**, pas une précision de télescope.

---

### ⚙️ Contraintes de base

- Doit supporter :
  - poussière, chaleur, dilatations,
  - tolérances de fabrication artisanales.
- Fonctionne sur des **temps longs** (minutes / heures).
- Doit **échouer en douceur** : même si le suivi est mauvais, SolarFlare reste utilisable.

> Remarque : le **réglage manuel** (toutes les 30–60 min) reste la base zéro-tech, et doit toujours rester possible, même si un module de suivi tombe en panne.

---

## 1️⃣ Suivi thermique par lames bimétalliques

### 🧠 Idée

Utiliser des **lames bimétalliques** comme **capteur + actionneur** d’orientation, dans une petite boîte chauffée par une **lentille dédiée**.

- Une lame bimétallique se **courbe** en chauffant.
- Plus la lentille est bien alignée avec le soleil, plus la lame **chauffe** → plus elle se déforme.
- En jouant sur la **géométrie** et la **position** de la lentille, on peut créer un système qui “préfère” une orientation donnée.

### 🔍 Principe d’exemple

- Une petite **boîte thermique** est fixée sur / près de SolarFlare.
- Sur le dessus : une **mini-lentille** qui concentre la lumière sur une ou plusieurs lames bimétalliques.
- Le montage est conçu pour qu’à **midi solaire**, si SolarFlare est bien orienté :
  - la lentille concentre **au maximum** sur la lame → courbure maximale.
- Avant / après midi, l’angle des rayons change :
  - la concentration diminue,
  - la lame chauffe moins → courbure plus faible.

La déformation peut :

- pousser un **levier**,  
- ou agir sur un **système à cliquets**,  

pour faire tourner SolarFlare par petits pas.

### ✅ Avantages

- Aucune électronique.
- Peu de pièces mobiles si bien conçu.
- Auto-limité : quand la température baisse, la lame revient en arrière.

### ⚠️ Limites

- Nécessite un **réglage expérimental** fin :
  - matériaux, épaisseur, position de la lentille…
- Très dépendant de la météo (nuages, température ambiante).
- Probablement mieux adapté à des **petites corrections** qu’à un suivi complet sur toute la journée.

---

## 2️⃣ Suivi gravitaire type horloge / “montre à bouton”

### 🧠 Idée générale

S’inspirer des **horloges à poids** :

- Un poids descend très lentement,
- des engrenages convertissent cette chute en **rotation très lente**.

Objectif : obtenir :

- soit une **“horloge de toit”** très lente → SolarFlare suit le soleil,
- soit une **“montre à bouton poussoir”** rechargée par SolarLift / SolarWell.

---

### 2.1 Horloge lente à poids

- Un **poids** (béton, métal…) est accroché à un tambour.
- Une **réduction d’engrenages** ralentit fortement le mouvement.
- Le tambour entraîne un **axe de rotation** portant SolarFlare.
- La descente du poids produit une **rotation quasi continue**, par exemple :
  - ≈ 180° sur 6–8 h de soleil.

Le mouvement est stabilisé par :

- un système d’**échappement** (type horloge),  
- ou des **cliquets** + ressorts qui lissent la progression.

Le poids peut être remonté :

- à la main (manivelle, treuil), ou  
- plus tard via **SolarLift** (SolarLift remonte un poids dédié au suivi).

---

### 2.2 Variante “montre à bouton poussoir” rechargée par SolarLift / SolarWell

Considérer le module de suivi comme une **montre mécanique** :

- Un **ressort principal** accumule l’énergie.
- Une petite cinématique (engrenages, échappement) fournit une **rotation lente** de SolarFlare.
- Au lieu de remonter la montre à la main, on peut :

  - la recharger via un **module SolarLift** (en relevant un petit poids interne ou en comprimant un ressort),  
  - ou via **SolarWell** (variations de pression agissant sur un mécanisme de poussée).

Exemples :

- **Avec SolarLift** :  
  le mouvement de montée du poids SolarLift sert à remonter un **petit poids interne** ou un ressort dédié au suivi.

- **Avec SolarWell** :  
  la **variation de pression** dans une chambre de distillation actionne une **membrane** ou un petit piston qui joue le rôle de **“bouton poussoir”**, donnant un cran de plus à un cliquet ou remontant légèrement un ressort.

Idée clé :  
> SolarLift / SolarWell se comportent comme des **chargeurs mécaniques** pour le système de suivi.

---

## 3️⃣ Suivi hybride micro-alimenté

Dans certains cas, **un tout petit peu d’électricité** peut simplifier la mécanique sans trahir l’esprit low-tech.

### 🔌 Sources possibles

- **Mini panneau solaire dédié** :
  - alimente un **micro-moteur** ou motoréducteur,
  - fonctionne par impulsions occasionnelles (un petit pas toutes les X minutes).
- **Courant d’eau** :
  - une **micro-turbine** dans un courant (rivière, marée) fournit quelques mW,
  - suffisant pour une rotation très lente ou un verrouillage électromagnétique.
- **Mini éolienne** :
  - petite hélice + dynamo sur un site venteux.

### 🧠 Logique

L’électronique doit rester **ultra simple** :

- quelques **fins de course** ou un timer rudimentaire,
- pas de gros contrôleur complexe.

Le moteur ne sert qu’à :

- **corriger l’orientation** de temps en temps, ou  
- **ramener SolarFlare en position de départ** en fin de course.

Ce type de suivi pourrait aussi devenir un **nœud BioSym** :  
un module qui décide **où pointer SolarFlare** (vers SolarLift, SolarWell, etc.) en fonction des besoins (énergie vs eau).

---

## 4️⃣ Intégration avec SolarLift & SolarWell

Le suivi n’est pas un module isolé ; il s’inscrit dans une **chaîne plus large** :

- **SolarFlare** → concentre la chaleur.
- **SolarLift** → stocke une partie de l’énergie en **gravité**.
- **SolarWell** → utilise la chaleur pour distiller de l’eau potable.

Quelques scénarios :

- SolarLift sert à **remonter** un petit poids interne, dédié au suivi (système horloge / montre).
- SolarWell fournit des cycles de **pression** qui alimentent un système à **cliquet poussé**.
- Dans un contexte BioSym, un module de plus haut niveau pourrait décider de **prioriser** :
  - SolarLift (stockage d’énergie), ou  
  - SolarWell (production d’eau),  

et ajuster l’orientation de SolarFlare en conséquence.

---

## 5️⃣ Statut & contributions

Toutes ces pistes sont :

- **conceptuelles**,  
- à explorer via **maquettes**, tests imparfaits et bricolages,  
- ouvertes à la **critique, correction, amélioration**.

Si un prototype, même très imparfait, est réalisé à partir de ces idées, sa documentation est la bienvenue.

🔧 Contributions (issues / PR) sur :

- essais de lames bimétalliques,
- mécanismes type horloge / montre,
- suivi ultra basse consommation,

sont appréciées.
