# InstaBlock

Outil open source pour bloquer en masse des comptes Instagram à partir d'une liste `.txt`.  
Fonctionne directement dans votre navigateur — sans serveur, sans compte tiers, sans transmission de données.

---

## ⚠️ Avant de commencer

- L'extension introduit des délais aléatoires entre chaque blocage pour rester discrète. **Le processus peut être très long.**
- Instagram peut détecter l'automatisation et limiter temporairement votre compte
- Si Instagram modifie son interface, l'extension peut cesser de fonctionner sans préavis
- Desktop uniquement — ne fonctionne pas sur mobile
- Fourni tel quel, sans garantie ni support. Utilisez-le à vos risques et sous votre responsabilité.

---

## Ce que ça fait

| ✅ | ❌ |
|---|---|
| Importe une liste de comptes (fichier `.txt` ou URL) | Collecte vos données |
| Bloque automatiquement chaque compte | Utilise un serveur ou proxy externe |
| Utilise votre session Instagram ouverte | Demande vos identifiants |
| Ne stocke rien hors de votre navigateur | Nécessite la création d'un compte |

---

## Installation

**Firefox**
1. Ouvrez `about:debugging` → **Ce Firefox** → **Charger un module complémentaire temporaire**
2. Sélectionnez `extension/manifest.json`

> Publication sur les stores prévue une fois le projet stabilisé.

---

## Utilisation

1. Connectez-vous à Instagram normalement dans votre navigateur
2. Cliquez sur l'icône de l'extension
3. Importez une liste (fichier local ou URL)
4. Lancez — ne fermez pas l'onglet

---

## Format des listes

Fichier `.txt`, un username par ligne, sans `@`.  
Les lignes commençant par `#` sont des commentaires (ignorées).

```txt
# name: Ma liste personnelle
# author: monpseudo
# updated: 2025-01-15

compte_exemple_1
compte_exemple_2
```

**Partager une liste :** hébergez votre .txt sur GitHub (raw), Pastebin, ou toute URL publique.

> Vous êtes libre de bloquer qui vous voulez. Les raisons vous appartiennent.

---

## Structure du projet

```txt
instablock/
├── README.md
├── extension/
│   ├── manifest.json       # Manifest V3
│   ├── background.js       # Service worker
│   ├── content.js          # Script injecté sur Instagram
│   ├── popup/
│   │   ├── popup.html
│   │   ├── popup.js
│   │   └── popup.css
│   └── icons/
├── listes/
│   └── exemple.txt
└── docs/
    └── trouver-un-username.md
```

---

## Contribuer

Issues et PRs bienvenues. Pas de roadmap, pas de promesses.
Pour un bug : navigateur + version, ce que vous avez fait, ce qui s'est passé.

---

## Licence : GPL-3.0
Vous pouvez utiliser, modifier et redistribuer ce code, y compris dans vos propres projets open source, à condition de conserver la même licence.
