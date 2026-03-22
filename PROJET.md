# Projet Jean-Mi — Domotique Home Assistant

> Résumé complet du projet : configuration, préférences d'achat, déploiement GitHub.

---

## Objectif

Créer un système domotique **Home Assistant** avec commande vocale locale (sans cloud) pour un salon de ~20m².

**Exemples de commandes vocales :**
- "Joue tel titre de tel artiste sur Spotify"
- "Joue ma playlist X"
- "Allume la lumière du salon"
- "Je voudrais regarder ça sur YouTube"

---

## Configuration matérielle

| Composant | Détail |
|-----------|--------|
| **PC** | NiPoGi E3B Mini PC |
| **Processeur** | AMD Ryzen 7 7735HS — 8C/16T — jusqu'à 4,75 GHz |
| **RAM** | 16 Go LPDDR5 5500 MT/s |
| **Stockage** | 512 Go M.2 NVMe PCIe 3.0 |
| **OS** | Ubuntu 24.04 LTS + GNOME |
| **Coordinateur Zigbee** | SONOFF ZBDongle-E (EFR32MG21, `1a86:55d4`, `ttyACM0`) |
| **Plateforme domotique** | Home Assistant Container (Docker) + Zigbee2MQTT |

---

## Règles absolues

> - Provenance **Zone Économique Européenne (ZEE) uniquement**
> - Livraison **en France uniquement**
> - Occasion de préférence, neuf si introuvable

---

## Préférences d'achat

| Priorité | Plateforme | Critères |
|----------|------------|----------|
| 1 | **eBay** | Occasion de préférence, vendeurs UE uniquement |
| 2 | **Le Bon Coin** | Particuliers France, remise en main propre |
| 3 | **Google Products** | Revendeurs spécialisés UE (Domadoo, OpenELAB…) |
| 4 | **Rakuten FR** | Marketplace FR, vendeurs pro, occasion certifiée, retours 30j |
| 5 | **Domotique-Store** | Spécialiste FR — hors ligne depuis fin 2024 |
| 6 | **IKEA** | Magasin physique FR, retrait immédiat, gamme DIRIGERA/TRÅDFRI — pertinent uniquement pour les prises Zigbee |

---

## Matériel à acheter

Voir [jean-mi.html](jean-mi.html) pour le comparatif complet et les prix à jour.

Budget estimé : ~102 € — voir `jean-mi.html` pour le détail.

---

## Structure du projet GitHub

```
jean-mi/
├── index.html          # Page d'accueil — navigation vers les autres pages
├── jean-mi.html        # Comparatif interactif matériel (source de vérité)
├── avancement.html     # Suivi des achats et de la progression
├── installation.html   # Guide d'installation software (SSH · Docker · HA · Z2M · Voix)
├── achats.json         # État des achats (micro, prise Zigbee, module plafonnier)
├── README.md           # Présentation du projet
├── PROJET.md           # Ce fichier — résumé complet
└── CLAUDE.md           # Guide de contexte pour Claude Code
```

---

## Configuration SSH GitHub (macOS / zsh)

### Générer la clé ED25519

```zsh
ssh-keygen -t ed25519 -C "ton.email@example.com" -f ~/.ssh/github_jean-mi
```

### Charger la clé dans l'agent

```zsh
eval "$(ssh-agent -s)"
ssh-add --apple-use-keychain ~/.ssh/github_jean-mi
```

### Copier la clé publique

```zsh
cat ~/.ssh/github_jean-mi.pub | pbcopy
```

Coller dans **GitHub → Settings → SSH and GPG keys → New SSH key**

### Config `~/.ssh/config`

```
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/github_jean-mi
  AddKeysToAgent yes
  UseKeychain yes
```

### Vérifier la connexion

```zsh
ssh -T git@github.com
# → Hi bczy! You've successfully authenticated
```

---

## Déploiement GitHub

### Initialiser et pousser le projet

```zsh
cd ~/jean-mi
git init
git add .
git commit -m "feat: init projet jean-mi domotique HA"
git remote add origin git@github.com:bczy/jean-mi.git
git push -u origin main
```

### Changer le remote (HTTPS → SSH)

```zsh
git remote set-url origin git@github.com:bczy/jean-mi.git
```

### GitHub Pages

Dans le repo GitHub → **Settings → Pages → Branch: main**
Accessible sur : https://bczy.github.io/jean-mi/

---

## Liens utiles

| Ressource | URL |
|-----------|-----|
| Repo GitHub | https://github.com/bczy/jean-mi |
| GitHub Pages | https://bczy.github.io/jean-mi/ |
| Home Assistant | https://www.home-assistant.io/ |
| Zigbee2MQTT | https://www.zigbee2mqtt.io/ |
| Appareils compatibles HA | https://home-assistant-devices.com/fr |
| OpenELAB (ReSpeaker XVF-3800) | https://openelab.io/fr/products/respeaker-usb-mic-array-v2 |
| Domadoo (SONOFF) | https://www.domadoo.fr/fr/336_sonoff |
| eBay.fr recherche NOUS A1Z | https://www.ebay.fr/sch/i.html?_nkw=NOUS+A1Z+Zigbee |
| eBay.fr ZBMINIL2 🇩🇪 | https://www.ebay.fr/itm/314632303696 |
| LBC Sonoff Zigbee | https://www.leboncoin.fr/ck/bricolage/sonoff-zigbee |

---

## Prochaines étapes

- [ ] Recevoir le matériel
- [ ] Installer Home Assistant sur Ubuntu 24.04
- [ ] Appairer le coordinateur SONOFF Zigbee Dongle Plus
- [ ] Configurer Zigbee2MQTT
- [ ] Appairer la prise NOUS A1Z
- [ ] Installer le ZBMINIL2 derrière l'interrupteur du plafonnier
- [ ] Brancher le ReSpeaker XVF-3800
- [ ] Configurer la reconnaissance vocale locale
- [ ] Intégrer Spotify et YouTube

---

*Dernière mise à jour : mars 2026*
