# 🪙 Crypto Génie — Dashboard Personnel

> Tableau de bord pour suivre vos cryptos en temps réel, créé pour les ateliers **Crypto Génie** de [Génie Montauban](https://genie-montauban.fr).

---

## ✨ Fonctionnalités

- 📊 **Prix en temps réel** via l'API publique Binance (sans clé API requise)
- 💼 **Suivi de portefeuille** : prix d'achat, quantité, valeur actuelle, plus/moins-value
- 📅 **Tableau de routines** avec cases à cocher (quotidien / hebdo / mensuel)
- 🔔 **Alertes de prix** personnalisables
- 📱 **100% responsive** — fonctionne sur smartphone
- 🔒 **Tout en local** — vos données ne quittent jamais votre navigateur (localStorage)
- 🔄 Rafraîchissement automatique toutes les 30 secondes

---

## 🚀 Installation en 3 étapes

### Option A — En ligne (la plus simple)

1. Allez sur [GitHub Pages](https://pages.github.com/) après avoir forké ce repo
2. Activez GitHub Pages sur la branche `main`, dossier `/` (root)
3. Votre dashboard est accessible à `https://VOTRE-PSEUDO.github.io/crypto-genie-dashboard`

### Option B — En local sur votre ordinateur

```bash
# 1. Cloner le repo
git clone https://github.com/VOTRE-PSEUDO/crypto-genie-dashboard.git

# 2. Ouvrir le dossier
cd crypto-genie-dashboard

# 3. Ouvrir index.html dans votre navigateur
# Sur Mac :
open index.html
# Sur Windows :
start index.html
# Sur Linux :
xdg-open index.html
```

> ⚠️ **Aucun serveur, aucune installation de Node.js requise.** Le fichier `index.html` fonctionne directement dans n'importe quel navigateur moderne.

---

## 📁 Structure du projet

```
crypto-genie-dashboard/
├── index.html          ← Application complète (tout-en-un)
├── README.md           ← Ce fichier
└── .gitignore
```

L'application entière tient dans un seul fichier `index.html` pour une installation maximale.

---

## 🔧 Comment personnaliser

### Ajouter une crypto à la liste

Dans `index.html`, cherchez `DEFAULT_CRYPTOS` et ajoutez votre paire Binance :
```javascript
const DEFAULT_CRYPTOS = ["BTCUSDT", "ETHUSDT", "SOLUSDT", "VOTRE_PAIRE"];
```

### Modifier l'intervalle de rafraîchissement

Cherchez `REFRESH_INTERVAL` et changez la valeur (en millisecondes) :
```javascript
const REFRESH_INTERVAL = 30000; // 30 secondes
```

---

## 🔗 API utilisée

Ce dashboard utilise l'**API publique Binance** (pas de clé API requise) :
- Prix en temps réel : `https://api.binance.com/api/v3/ticker/price`
- Variation 24h : `https://api.binance.com/api/v3/ticker/24hr`

> ℹ️ L'API Binance est gratuite et publique pour les données de marché. Elle est soumise à une limite de débit (1200 requêtes/minute), largement suffisante pour un usage personnel.

---

## ⚠️ Avertissement légal

Ce tableau de bord est un **outil pédagogique**. Il ne constitue pas un conseil en investissement. Les données affichées proviennent de Binance et sont fournies à titre informatif uniquement.

> Les performances passées ne préjugent pas des performances futures. N'investissez jamais plus que ce que vous pouvez vous permettre de perdre.

---

## 🤝 Contribuer

Ce projet est open-source pour les participants des ateliers Crypto Génie.

1. Fork le repo
2. Créez votre branche : `git checkout -b ma-fonctionnalite`
3. Committez : `git commit -m 'Ajout de ma fonctionnalité'`
4. Push : `git push origin ma-fonctionnalite`
5. Ouvrez une Pull Request

---

## 📄 Licence

MIT — Libre d'utilisation, de modification et de partage.

---

*Créé avec ❤️ pour les ateliers **Crypto Génie** — Génie Montauban*
