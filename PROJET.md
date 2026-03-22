# Projet Jean-Mi — Domotique Home Assistant

> Résumé complet du projet : matériel, configuration, préférences d'achat, comparatifs et déploiement GitHub.

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
| **Coordinateur Zigbee** | SONOFF ZigBee 3.0 USB Dongle Plus (EFR32MG21) |
| **Plateforme domotique** | Home Assistant + Zigbee2MQTT |

---

## Préférences d'achat

| Priorité | Plateforme | Critères |
|----------|------------|----------|
| 1 | **eBay** | Occasion de préférence, vendeurs UE uniquement |
| 2 | **Le Bon Coin** | Particuliers France, remise en main propre |
| 3 | **Google Products** | Revendeurs spécialisés UE (Domadoo, OpenELAB…) |
| 4 | **Rakuten FR** | Marketplace FR, vendeurs pro, occasion certifiée, retours 30j |
| 5 | **Domotique-Store** | Spécialiste FR — hors ligne depuis mars 2026 |
| 6 | **IKEA** | Magasin physique FR, retrait immédiat, gamme DIRIGERA/TRÅDFRI — pertinent uniquement pour les prises Zigbee |

> **Règles absolues**
> - Provenance **Zone Économique Européenne (ZEE) uniquement**
> - Livraison **en France uniquement**
> - Occasion de préférence, neuf si introuvable

---

## Matériel à acheter

### 1. Micro USB pieuvre — ReSpeaker XVF-3800

> **Le ReSpeaker XVF-3000 est EOL** (End of Life). Son prix actuel est ~96,95 € chez OpenELAB, ce qui le rend moins compétitif que son successeur. Le **XVF-3800** (~75,95 €) est la référence recommandée.

| Produit | Plateforme | État | Origine | Prix | Port | Total |
|---------|------------|------|---------|------|------|-------|
| ⭐ ReSpeaker XVF-3800 | Google Products (OpenELAB 🇩🇪) | Neuf | 🇩🇪 Munich | ~75,95 € | 0 € (≥50€) | **~76 €** |
| ReSpeaker XVF-3000 *(EOL)* | Google Products (OpenELAB 🇩🇪) | Neuf | 🇩🇪 Munich | ~96,95 € | 0 € (≥50€) | ~97 € |
| ReSpeaker XVF-3000 *(EOL)* | Le Bon Coin | Occasion | 🇫🇷 | ~25–35 € | 0 € | **~25–35 €** *(si disponible)* |
| ReSpeaker XVF-3000 *(EOL)* | Rakuten FR | Neuf | 🇫🇷/🇵🇱 | ~50–60 € | Variable | ~55–65 € |
| ReSpeaker XVF-3000 *(EOL)* | Google Products (Botland 🇵🇱) | Neuf | 🇵🇱 | ~47 € | ~6–8 € | ~53–55 € |

**Caractéristiques XVF-3800 :** 4 mics · AEC · AGC · NS · DOA · champ lointain 5m · plug & play Linux · LED RGB
**Lien recommandé :** https://openelab.io/fr/products/respeaker-usb-mic-array-v2

---

### 2. Prise Zigbee secteur — contrôle lampe branchée

| Produit | Plateforme | État | Origine | Prix | Port | Total |
|---------|------------|------|---------|------|------|-------|
| ⭐ NOUS A1Z | eBay.fr | Neuf | 🇵🇱 | ~11–14 € | 0 € | **~11–14 €** |
| NOUS A1Z | Le Bon Coin | Occasion | 🇫🇷 | ~6–10 € | 0 € | **~6–10 €** |
| NOUS A1Z | Rakuten FR | Neuf | 🇪🇺 | ~13–16 € | Variable | ~15–18 € |
| SONOFF S60ZBTPF | Google Products (Domadoo 🇫🇷) | Neuf | 🇫🇷 | ~13 € | 6,90 € | ~20 € |
| Innr SP 240 | eBay.fr | Neuf | 🇳🇱 | ~19–22 € | ~3–4 € | ~22–26 € |
| IKEA INSPELNING E2201 | IKEA (magasin FR) | Neuf | 🇸🇪/🇫🇷 | 9,99 € | 0 € | **~9,99 €** *(⚠️ précision conso aléatoire)* |
| IKEA TRETAKT E22x4 | IKEA (magasin FR) | Neuf | 🇸🇪/🇫🇷 | 7,99 € | 0 € | **~7,99 €** *(sans mesure conso)* |

**Caractéristiques NOUS A1Z :** 16A · mesure conso (W/V/A/kWh) · routeur Zigbee · compatible Zigbee2MQTT + ZHA + HA · marque UE (Pologne)
**Lien recommandé :** https://www.ebay.fr/sch/i.html?_nkw=NOUS+A1Z+Zigbee

---

### 3. Module plafonnier — interrupteur sans neutre

| Produit | Plateforme | État | Origine | Prix | Port | Total |
|---------|------------|------|---------|------|------|-------|
| ⭐ SONOFF ZBMINIL2 | eBay.fr | Neuf | 🇩🇪 | ~10–14 € | 0 € | **~10–14 €** |
| SONOFF ZBMINIL2 B-WARE | eBay.fr (MatimEU) | Expo | 🇵🇱 | 16,87 € | ~4–5 € | ~21–22 € |
| SONOFF ZBMINIL2 | Le Bon Coin | Occasion | 🇫🇷 | ~8–12 € | 0 € | **~8–12 €** |
| SONOFF ZBMINIL2 | Rakuten FR | Neuf | 🇫🇷/🇩🇪 | ~13–16 € | Variable | ~15–18 € |
| SONOFF ZBMINIL2 | Google Products (Domadoo 🇫🇷) | Neuf | 🇫🇷 | 14,90 € | 6,90 € | ~21,80 € |

**Caractéristiques :** Sans neutre · 6A/1440W · Zigbee 3.0 · ultra-compact · compatible Zigbee2MQTT + ZHA + HA
**⚠️ Note :** End-device (pas routeur Zigbee) — vérifier câblage avant achat
**Lien recommandé :** https://www.ebay.fr/itm/314632303696

---

### Budget total optimal

| Article | Source | Total |
|---------|--------|-------|
| ReSpeaker XVF-3800 | OpenELAB 🇩🇪 | ~76 € |
| NOUS A1Z | eBay.fr 🇵🇱 | ~12 € |
| SONOFF ZBMINIL2 | eBay.fr 🇩🇪 | ~12 € |
| **TOTAL** | | **~100–102 €** |

> Frais de port inclus · Provenance UE garantie · Livraison France

---

## Structure du projet GitHub

```
jean-mi/
├── jean-mi.html   # Comparatif interactif (source de vérité)
├── README.md      # Présentation du projet
├── PROJET.md      # Ce fichier — résumé complet
└── CLAUDE.md      # Guide de contexte pour Claude Code
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

*Projet : jean-mi · GitHub : [@bczy](https://github.com/bczy) · Généré avec Claude*
