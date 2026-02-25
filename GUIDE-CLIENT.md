# 🏆 The 5 Cup — Guide d'administration v2.1

---

## 🗂️ Structure du projet

```
the-5-cup/
├── public/
│   └── assets/
│       ├── logos-sans-fond/
│       │   └── logo_sans_titre.png         ← LOGO PRINCIPAL
│       ├── poules/
│       │   ├── poule_terre.png             ← Logo poule Terre
│       │   ├── poule_air.png              ← Logo poule Air
│       │   └── poule_eau.png              ← Logo poule Eau
│       └── teams/
│           ├── poule_terre_equipe1.png    ← Équipes poule Terre (1-5)
│           ├── poule_terre_equipe2.png
│           ├── poule_terre_equipe3.png
│           ├── poule_terre_equipe4.png
│           ├── poule_terre_equipe5.png
│           ├── poule_air_equipe1.png      ← Équipes poule Air (1-5)
│           ├── poule_air_equipe2.png
│           ├── poule_air_equipe3.png
│           ├── poule_air_equipe4.png
│           ├── poule_air_equipe5.png
│           ├── poule_eau_equipe1.png      ← Équipes poule Eau (1-5)
│           ├── poule_eau_equipe2.png
│           ├── poule_eau_equipe3.png
│           ├── poule_eau_equipe4.png
│           └── poule_eau_equipe5.png
├── src/
│   ├── layouts/
│   │   └── Layout.astro
│   ├── components/
│   │   ├── Header.astro
│   │   ├── HeroSection.astro
│   │   ├── MarqueeBanner.astro
│   │   ├── CountdownTimer.astro
│   │   ├── PoulesSection.astro
│   │   ├── CTASection.astro
│   │   └── Footer.astro
│   └── pages/
│       ├── index.astro                    ← Page d'accueil
│       ├── competition.astro              ← Page compétition
│       ├── social.astro                   ← Page Instagram
│       ├── about.astro                    ← À propos
│       ├── rules.astro                    ← Règlement
│       ├── teams.astro                    ← Équipes
│       ├── faq.astro                      ← FAQ
│       ├── privacy.astro                  ← Politique de confidentialité
│       ├── terms.astro                    ← Conditions d'utilisation
│       └── legal.astro                    ← Mentions légales
├── tailwind.config.mjs
└── package.json
```

---

## 🚀 Démarrage rapide

```bash
npm install
npm run dev
# → http://localhost:4321
```

Pour publier :
```bash
npm run build
```

---

## 🖼️ Convention de nommage des fichiers images

### Logo principal
- Fichier : `public/assets/logos-sans-fond/logo_sans_titre.png`
- Format : PNG fond transparent

### Logos des poules
- Répertoire : `public/assets/poules/`
- Convention : `poule_{element}.png` (tout en minuscules)
- Exemples : `poule_terre.png`, `poule_air.png`, `poule_eau.png`

### Logos des équipes
- Répertoire : `public/assets/teams/`
- Convention : `poule_{element}_equipe{numero}.png` (tout en minuscules)
- Exemples : `poule_terre_equipe1.png`, `poule_air_equipe3.png`, `poule_eau_equipe5.png`

**Important** : Les numéros vont de 1 à 5 pour chaque poule. Si vous ajoutez une équipe, incrémentez le numéro.

---

## ✏️ Modifications courantes

### Changer le lien billetterie

Dans **TOUS les fichiers** suivants, remplacez la valeur de `TICKET_LINK` :

- `src/components/Header.astro`
- `src/components/HeroSection.astro`
- `src/components/CTASection.astro`
- `src/pages/competition.astro`

### Changer la date

Fichier : `src/components/CountdownTimer.astro`

```js
const targetDate = new Date('2026-04-29T09:00:00');
//                           ANNÉE-MOIS-JOUR à HEURE
```

Pensez aussi à mettre à jour le texte de date dans :
- `HeroSection.astro` (hero-side-label + meta)
- `CountdownTimer.astro` (countdown-date)
- `competition.astro` (hero-info-grid)
- `MarqueeBanner.astro` (items par défaut)

### Changer le lien Instagram

Modifiez la constante `INSTAGRAM_LINK` dans :
- `src/components/Header.astro`
- `src/components/Footer.astro`
- `src/pages/social.astro`

### Modifier les noms des équipes

Fichiers à modifier :
- `src/components/PoulesSection.astro` (pour la page d'accueil)
- `src/pages/competition.astro` (pour la page compétition)
- `src/pages/teams.astro` (pour la page équipes dédiée)

---

## 📱 Pages disponibles

| Route | Page | Description |
|---|---|---|
| `/` | Accueil | Hero + countdown + poules + CTA |
| `/competition` | Compétition | Équipes, règlement, inscription |
| `/social` | Instagram | Lien vers le profil Instagram |
| `/about` | À propos | Présentation de l'événement |
| `/rules` | Règlement | Règles détaillées |
| `/teams` | Équipes | Galerie des équipes avec logos |
| `/faq` | FAQ | Questions fréquentes |
| `/privacy` | Confidentialité | Politique de données |
| `/terms` | Conditions | Conditions d'utilisation |
| `/legal` | Mentions légales | Informations juridiques |

---

## 📞 Contact & infos à mettre à jour

Fichier : `src/components/Footer.astro`

- Email : `thefivecup5@gmail.com`
- Téléphone : `06 34 82 92 83`
- Adresse : `UrbanSoccer Toulouse Sept Deniers, 2 Rue de l'Égalité, 31200 Toulouse`
- Instagram : `https://www.instagram.com/the_five_cup` (compte : `@the_five_cup`)
