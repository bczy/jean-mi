# CLAUDE.md — Projet Jean-Mi

Guide de contexte pour Claude Code. À lire avant toute modification du projet.

---

## Vue d'ensemble

**Jean-Mi** est un guide d'achat comparatif pour construire un système domotique **Home Assistant** local (sans cloud) pour un salon de ~20m², avec commandes vocales en français (Spotify, YouTube, lumières).

---

## Stack technique

| Composant | Détail |
|-----------|--------|
| PC | NiPoGi E3B Mini PC |
| CPU | AMD Ryzen 7 7735HS — 8C/16T — 4,75 GHz |
| RAM | 16 Go LPDDR5 5500 MT/s |
| Stockage | 512 Go M.2 NVMe PCIe 3.0 |
| OS | Ubuntu 24.04 LTS + GNOME |
| Coordinateur Zigbee | SONOFF ZigBee 3.0 USB Dongle Plus (EFR32MG21) |
| Plateforme | Home Assistant + Zigbee2MQTT |

---

## Règles absolues (ne jamais déroger)

- **Provenance : Zone Économique Européenne (ZEE) uniquement**
- **Livraison : France uniquement**
- Occasion de préférence, neuf si introuvable

---

## Préférences d'achat

| Priorité | Plateforme | Critères |
|----------|------------|----------|
| 1 | eBay | Occasion de préférence, vendeurs UE uniquement |
| 2 | Le Bon Coin | Particuliers France, remise en main propre |
| 3 | Rakuten FR | Vendeurs pro UE |
| 4 | Domadoo / OpenELAB / spécialistes UE | Revendeurs spécialisés domotique, neuf uniquement |

> Domotique-Store.fr : hors ligne depuis mars 2026 — ne pas utiliser.

---

## Produits cibles et budget de référence (mars 2026)

| Produit | Référence | Prix indicatif | Source recommandée |
|---------|-----------|---------------|--------------------|
| Micro USB | **ReSpeaker XVF-3800** (successeur XVF-3000 EOL) | ~75,95 € | OpenELAB 🇩🇪 |
| Prise Zigbee | **NOUS A1Z** — 16A, mesure conso, routeur | ~11–14 € | eBay.fr 🇵🇱 |
| Module plafonnier | **SONOFF ZBMINIL2** — sans neutre, 6A/1440W | ~10–14 € | eBay.fr 🇩🇪 |
| **TOTAL** | | **~102 €** | |

> Le ReSpeaker XVF-3000 est **EOL** (End of Life) — son prix actuel a grimpé à ~96,95 €. Le successeur XVF-3800 (~75,95 €) est la référence recommandée.

---

## Carte des fichiers

| Fichier | Rôle | À modifier en priorité |
|---------|------|------------------------|
| `jean-mi.html` | **Source de vérité** — comparatif interactif complet | Oui, en premier |
| `README.md` | Intro rapide, stack, budget résumé, déploiement | Après jean-mi.html |
| `PROJET.md` | Spec complète, tableaux détaillés, checklist, SSH/GitHub | Après jean-mi.html |
| `CLAUDE.md` | Ce fichier — contexte pour Claude Code | Mettre à jour si changement majeur |
| `.claude/settings.local.json` | Permissions WebFetch par domaine | Si nouveau vendeur à autoriser |

**Règle de cohérence** : toujours mettre `jean-mi.html` à jour en premier, puis propager les changements de prix/produits dans `README.md` et `PROJET.md`.

---

## Points d'attention

- Le tableau HTML a une colonne **Conso élec.** (consommation propre du module, pas de la charge)
- Les prises Zigbee affichent leur conso en **veille** (~0,5 W) — la charge (lampe) s'ajoute
- SONOFF ZBMINIL2 est un **end-device** (pas routeur Zigbee) — à noter dans les inconvénients
- Le port est **gratuit** chez OpenELAB pour commandes ≥ 50 € — à vérifier si commande < 50 €
- GitHub Pages : `https://bczy.github.io/jean-mi/` — fichier principal : `jean-mi.html`
