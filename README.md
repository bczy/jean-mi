# 🏠 Projet Jean-Mi — Domotique Home Assistant

Comparatif matériel pour un projet domotique **Home Assistant** avec commande vocale locale, piloté par IA.  
Conçu pour un salon de ~20m², entièrement local (pas de cloud), basé sur le protocole **Zigbee**.

---

## 📋 Description

Ce projet recense et compare le matériel nécessaire pour :

- **Commander la maison à la voix** (Spotify, YouTube, lumières)
- **Contrôler les lumières** du salon via Zigbee
- **Faire tourner une IA locale** sur Linux sans dépendance cloud

Le fichier `index.html` contient les tableaux comparatifs interactifs, avec prix, frais de port, avantages/inconvénients et liens directs vers les vendeurs.

---

## 🖥️ Stack technique

| Composant | Détail |
|-----------|--------|
| **PC** | NiPoGi E3B Mini PC — AMD Ryzen 7 7735HS (8C/16T, 4.75 GHz) |
| **RAM** | 16 Go LPDDR5 5500 MT/s |
| **Stockage** | 512 Go M.2 NVMe PCIe 3.0 |
| **OS** | Ubuntu 24.04 + GNOME |
| **Domotique** | Home Assistant + Zigbee2MQTT |
| **Coordinateur Zigbee** | SONOFF ZigBee 3.0 USB Dongle Plus |

---

## 🛒 Matériel à acheter

### 🎤 Micro USB pieuvre
**ReSpeaker USB Mic Array** — 4 mics XMOS XVF-3000, champ lointain 5m, AEC/AGC/NS, plug & play Linux

| Source recommandée | Prix | Port | Total |
|--------------------|------|------|-------|
| OpenELAB 🇩🇪 (Google Products) | ~45 € | Gratuit ≥ 50 € | **~45 €** |

### 🔌 Prise Zigbee secteur
**NOUS A1Z** — 16A, mesure de consommation, routeur Zigbee, compatible Zigbee2MQTT + HA

| Source recommandée | Prix | Port | Total |
|--------------------|------|------|-------|
| eBay.fr 🇵🇱 (vendeur UE) | ~11–14 € | Gratuit | **~11–14 €** |

### 💡 Module plafonnier (sans neutre)
**SONOFF ZBMINIL2** — Zigbee 3.0, 6A/1440W, ultra-compact, sans fil neutre requis

| Source recommandée | Prix | Port | Total |
|--------------------|------|------|-------|
| eBay.fr 🇩🇪 (vendeur UE) | ~10–14 € | Gratuit | **~10–14 €** |

### 💰 Budget total estimé : ~69 €

---

## 🗂️ Structure du projet

```
jean-mi/
├── index.html     # Comparatif interactif (Tailwind CSS CDN)
└── README.md      # Ce fichier
```

---

## 🚀 Utilisation

Ouvrir `index.html` directement dans un navigateur — aucune dépendance à installer.

Le fichier utilise :
- [Tailwind CSS](https://cdn.tailwindcss.com) via CDN
- [Google Fonts](https://fonts.google.com) via CDN (Syne + DM Mono)

---

## ⚙️ Préférences d'achat

| Priorité | Plateforme | Critères |
|----------|------------|----------|
| 1 | **eBay** | Occasion de préférence, vendeurs UE uniquement |
| 2 | **Le Bon Coin** | Particuliers France, remise en main propre |
| 3 | **Google Products** | Revendeurs spécialisés UE (Domadoo, OpenELAB…) |

> ⚠️ **Règles absolues** : provenance Zone Économique Européenne uniquement · Livraison en France uniquement

---

## 🔗 Liens utiles

- [Home Assistant](https://www.home-assistant.io/)
- [Zigbee2MQTT](https://www.zigbee2mqtt.io/)
- [Compatibilité appareils Zigbee](https://home-assistant-devices.com/fr)
- [OpenELAB — ReSpeaker](https://openelab.io/fr/products/respeaker-usb-mic-array)
- [Domadoo — SONOFF](https://www.domadoo.fr/fr/336_sonoff)

---

## 🌐 GitHub Pages

Ce projet est conçu pour être hébergé sur GitHub Pages.  
Une fois le repo créé, activer dans **Settings → Pages → Branch: main**.

Accessible sur : `https://TON_USER.github.io/jean-mi/`

---

*Généré avec Claude · Données indicatives, vérifier les prix avant achat*
