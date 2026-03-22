# Projet Jean-Mi — Domotique Home Assistant

Comparatif matériel pour un projet domotique **Home Assistant** avec commande vocale locale.
Conçu pour un salon de ~20m², entièrement local (sans cloud), basé sur le protocole **Zigbee**.

---

## Stack technique

| Composant | Détail |
|-----------|--------|
| **PC** | NiPoGi E3B Mini PC — AMD Ryzen 7 7735HS (8C/16T, 4.75 GHz) |
| **RAM** | 16 Go LPDDR5 5500 MT/s |
| **Stockage** | 512 Go M.2 NVMe PCIe 3.0 |
| **OS** | Ubuntu 24.04 LTS + GNOME |
| **Domotique** | Home Assistant Container (Docker) + Zigbee2MQTT |
| **Coordinateur Zigbee** | SONOFF ZBDongle-E (EFR32MG21, `1a86:55d4`, `ttyACM0`) |
| **Freebox Player** | Décodeur TV contrôlable via HA (HACS · freebox_player) |

---

## Matériel

Consulter [jean-mi.html](jean-mi.html) pour le comparatif complet.

---

## Structure du projet

```
jean-mi/
├── index.html        # Page d'accueil — navigation vers les autres pages
├── jean-mi.html      # Comparatif interactif (source de vérité)
├── avancement.html   # Suivi des achats et de la progression
├── installation.html # Guide d'installation software (SSH · Docker · HA · Z2M · Voix)
├── achats.json       # État des achats
├── README.md         # Ce fichier
├── PROJET.md         # Spec complète, SSH, déploiement, checklist
└── CLAUDE.md         # Guide de contexte pour Claude Code
```

---

## Liens utiles

- [Home Assistant](https://www.home-assistant.io/)
- [Zigbee2MQTT](https://www.zigbee2mqtt.io/)
- [Compatibilité appareils Zigbee](https://home-assistant-devices.com/fr)
- [OpenELAB — ReSpeaker XVF-3800](https://openelab.io/fr/products/respeaker-usb-mic-array-v2)
- [Domadoo — SONOFF](https://www.domadoo.fr/fr/336_sonoff)

---

## GitHub Pages

Accessible sur : `https://bczy.github.io/jean-mi/`

Activer dans **Settings → Pages → Branch: main**.

---

*Dernière mise à jour : mars 2026*
