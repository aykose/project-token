# project-token
# 🎮 EliteArena — Compete. Win. Dominate.

> Plateforme de tournois esport multi-jeux avec système de tokens, live matches et leaderboard mondial.

![EliteArena Preview](https://img.shields.io/badge/Status-Live-brightgreen?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-2.0.0-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## 📋 Table des matières

- [Aperçu](#-aperçu)
- [Fonctionnalités](#-fonctionnalités)
- [Structure du projet](#-structure-du-projet)
- [Pages & Navigation](#-pages--navigation)
- [Stack technique](#-stack-technique)
- [Installation locale](#-installation-locale)
- [Déploiement GitHub Pages](#-déploiement-github-pages)
- [Personnalisation](#-personnalisation)
- [Roadmap](#-roadmap)
- [Contribuer](#-contribuer)
- [Licence](#-licence)

---

## 🌟 Aperçu

**EliteArena** est une refonte complète d'une plateforme de tournois esport, construite en **HTML/CSS/JS pur** — aucune dépendance, aucun framework, aucun build tool requis. Le fichier `index.html` s'ouvre directement dans un navigateur ou se déploie instantanément sur GitHub Pages.

### Design

Le design adopte une direction artistique **esport colorée** :
- Palette néon **cyan / rose / jaune** sur fond sombre profond
- Typographie impactante : **Bebas Neue** (titres) + **Rajdhani** (UI) + **JetBrains Mono** (chiffres)
- Animations CSS fluides : grille animée, orbes lumineux, effets de glow
- Scores Live mis à jour dynamiquement via JavaScript

---

## ✨ Fonctionnalités

### 🏆 Tournois
- Grille de tournois avec cartes par jeu (Fortnite, Warzone, Valorant, Rocket League)
- Badges LIVE / SOON animés
- Barres de progression des inscriptions
- Filtres par jeu, format, statut et type (Gratuit / Premium)
- Tabs de navigation par jeu

### ⚡ Live Matches
- Affichage des matchs en cours avec score en temps réel
- Simulation de mise à jour des scores (toutes les 3,5 secondes)
- Filtres par jeu

### 📊 Leaderboard
- Classement Top 10 mondial
- Colonnes : Rang, Joueur, Victoires, K/D, Gains en tokens
- Médailles or / argent / bronze pour le podium
- Tabs : Global, par jeu, Mensuel

### 💰 Token Shop
- 5 packs de tokens (Starter → Legend)
- Badge "Best Value" sur le pack optimal
- Section Battle Pass mensuel avec avantages premium
- Affichage du solde joueur

### 🎯 Autres
- **Ticker live** en haut de page avec les tournois actifs
- **Compteur animé** du nombre de joueurs au chargement
- **Navigation SPA** (Single Page Application) sans rechargement
- Design **responsive** (mobile, tablette, desktop)
- **Scrollbar custom**, cursor et noise overlay

---

## 📁 Structure du projet

```
elitearena/
│
├── index.html          # Fichier principal — contient tout (HTML + CSS + JS)
├── README.md           # Ce fichier
├── GITHUB_GUIDE.md     # Guide de déploiement GitHub Pages
└── LICENSE             # Licence MIT
```

> **Note :** Le projet est intentionnellement mono-fichier pour une portabilité maximale et un déploiement en une commande.

---

## 🗺 Pages & Navigation

Le site utilise une navigation SPA — toutes les pages sont dans `index.html` et s'affichent/masquent via JavaScript.

| Page | ID interne | Description |
|------|-----------|-------------|
| 🏠 Home | `page-home` | Hero, stats, features, tournois en vedette |
| 🏆 Tournaments | `page-tournaments` | Grille complète + filtres + tabs |
| ⚡ Live Matches | `page-matches` | Matchs en cours avec scores live |
| 📊 Leaderboard | `page-leaderboard` | Classement mondial top 10+ |
| 💰 Shop | `page-shop` | Packs tokens + Battle Pass |

---

## 🛠 Stack technique

| Technologie | Usage |
|------------|-------|
| **HTML5** | Structure sémantique |
| **CSS3** | Animations, variables CSS, Grid, Flexbox |
| **Vanilla JS** | Navigation SPA, compteurs, simulation live |
| **Google Fonts** | Bebas Neue, Rajdhani, JetBrains Mono |
| **CSS Custom Properties** | Système de tokens de design (couleurs, shadows, radius) |

Aucune dépendance npm. Aucun build requis. Taille totale : **< 80 KB**.

---

## 💻 Installation locale

### Option 1 — Ouvrir directement

```bash
# Clone le repo
git clone https://github.com/TON_USERNAME/elitearena.git

# Ouvre dans le navigateur
open index.html
# ou double-clic sur index.html
```

### Option 2 — Serveur local (recommandé pour éviter les CORS)

**Avec Python :**
```bash
# Python 3
python -m http.server 8080

# Puis ouvre : http://localhost:8080
```

**Avec Node.js :**
```bash
npx serve .
# Puis ouvre l'URL affichée dans le terminal
```

**Avec VS Code :**
Installe l'extension **Live Server** → clic droit sur `index.html` → *Open with Live Server*

---

## 🚀 Déploiement GitHub Pages

> Consulte le fichier **[GITHUB_GUIDE.md](./GITHUB_GUIDE.md)** pour le guide complet étape par étape avec captures d'écran descriptives.

**En résumé :**

```bash
# 1. Init git et push
git init
git add .
git commit -m "feat: initial EliteArena site"
git remote add origin https://github.com/TON_USERNAME/elitearena.git
git push -u origin main

# 2. Active GitHub Pages dans Settings > Pages > Source: main / root

# 3. Ton site est en ligne sur :
# https://TON_USERNAME.github.io/elitearena/
```

---

## 🎨 Personnalisation

### Changer les couleurs

Toutes les couleurs sont dans les variables CSS au début de `index.html` :

```css
:root {
  --c-neon1:    #00f5ff;   /* Cyan principal */
  --c-neon2:    #ff2d78;   /* Rose accent */
  --c-neon3:    #ffe234;   /* Jaune tokens/or */
  --c-neon4:    #7c3aed;   /* Violet secondaire */
  --c-bg:       #080b12;   /* Fond principal */
}
```

### Changer le nom du site

Recherche `EliteArena` dans `index.html` et remplace par ton nom.

### Ajouter un tournoi

Duplique un bloc `.t-card` dans la section `page-tournaments` et modifie les valeurs.

### Changer les polices

Les polices sont chargées via Google Fonts. Remplace le lien `<link>` en haut du `<head>` et mets à jour les variables `--font-title`, `--font-ui`, `--font-mono`.

---

## 🗓 Roadmap

- [ ] 🔐 Système d'authentification (Firebase Auth)
- [ ] 🗃 Base de données tournois en temps réel (Firebase Firestore)
- [ ] 💳 Intégration paiement tokens (Stripe)
- [ ] 📱 App mobile (PWA)
- [ ] 🌐 Internationalisation (FR / EN / ES)
- [ ] 🤖 Bot Discord pour annonces automatiques
- [ ] 📈 Dashboard analytics joueur
- [ ] 🔔 Système de notifications push

---

## 🤝 Contribuer

Les contributions sont les bienvenues !

```bash
# Fork le repo, puis :
git checkout -b feature/ma-feature
git commit -m "feat: ajout de ma feature"
git push origin feature/ma-feature
# Ouvre une Pull Request
```

---

## 📄 Licence

Ce projet est sous licence **MIT** — libre d'utilisation, modification et distribution.

---

<div align="center">

**Fait avec ❤️ pour les gamers**

[🌐 Demo Live](https://TON_USERNAME.github.io/elitearena/) · [🐛 Report Bug](https://github.com/TON_USERNAME/elitearena/issues) · [✨ Request Feature](https://github.com/TON_USERNAME/elitearena/issues)

</div>
