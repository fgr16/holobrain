# HOLO-brain

*Second cerveau collectif de l'équipe HOLO Sapiens.*

---

## Structure

```
HOLO-brain/
├── JARDIN/
│   ├── florian/
│   ├── thomas/
│   ├── gregoire/
│   ├── nicolas/
│   ├── faustine/
│   └── jf/
└── INBOX/
```

- **JARDIN/[prénom]/** — notes-concepts matures que chaque membre choisit de partager
- **INBOX/** — dépôts temporaires, notes en cours de curation, questions collectives

---

## Conventions

### Quoi partager dans JARDIN ?

Seulement des notes **matures et autonomes** :
- Une note = une idée (atomique)
- **Titre = affirmation** (ex : `La monnaie est un langage des flux.md`, pas `Monnaie.md`)
- La note doit se comprendre sans contexte extérieur
- Pas de brouillons, pas de notes personnelles

### Format des notes

```yaml
---
member_tag : [member_name]
date: today_date (format YYYY-MM-DD)
MOC:
  - "[[MOC_name]]"
  - "[[MOC_2_name_if_needed]]"
source: source_link
author: "[[author_name]]"
---

Note content...
```

### INBOX

Zone libre : dépôts rapides, questions au groupe, documents de travail communs.
Nommer les fichiers : `YYYY-MM-DD [sujet].md`

### Règle de base

- Chacun écrit **uniquement dans son sous-dossier JARDIN**
- On ne modifie pas la note de quelqu'un d'autre — on crée un lien ou on ouvre une discussion

---

## Workflow

1. Tu rédiges dans ton vault personnel
2. La note est mature → tu la copies dans `JARDIN/[ton-prénom]/`
3. Git : commit + push
4. L'équipe pull et découvre ta contribution

---

## Setup (nouveaux membres)

### Prérequis

- Avoir [Obsidian](https://obsidian.md) installé
- Avoir [Git](https://git-scm.com/downloads) installé
- Avoir un compte [GitHub](https://github.com) et avoir demandé à Florian d'être ajouté comme collaborateur

---

### Étape 1 — Cloner le vault sur ton ordinateur

Le "clonage" consiste à télécharger le vault partagé sur ton ordinateur via le terminal.

**Ouvre le Terminal** (Mac : `Cmd+Espace` → tape "Terminal" → Entrée)

Choisis où tu veux placer le vault. Par exemple, dans ton dossier Obsidian existant :

```bash
cd ~/Documents
```

> `cd` signifie "aller dans ce dossier". Remplace `~/Documents` par le chemin de ton choix.

Puis clone le repo :

```bash
git clone https://github.com/fgr16/HOLO-brain.git
```

Un dossier `HOLO-brain/` est maintenant créé à cet endroit.

---

### Étape 2 — Ouvrir le vault dans Obsidian

1. Ouvre Obsidian
2. Sur l'écran d'accueil → **Ouvrir un dossier comme vault**
3. Navigue jusqu'au dossier `HOLO-brain/` que tu viens de créer → **Ouvrir**

Tu vois maintenant le vault HOLO-brain dans Obsidian.

---

### Étape 3 — Installer le plugin Git

Ce plugin permet de synchroniser le vault avec GitHub directement depuis Obsidian, sans utiliser le terminal.

1. Dans Obsidian → **Paramètres** (icône engrenage en bas à gauche)
2. **Extensions tierces** → désactiver le mode restreint si demandé
3. **Parcourir** → cherche `Git` → **Installer** → **Activer**

---

### Étape 4 — Configurer Git

1. Retourne dans **Paramètres** → **Git**
2. Active `Pull updates on startup` ✓ — récupère automatiquement les nouveautés au démarrage
3. Dans `Author name` : entre ton prénom
4. Dans `Author email` : entre ton email GitHub

---

### Étape 5 — Authentification GitHub

La première fois que tu fais un push, Git te demandera tes identifiants GitHub.

Le plus simple : installe GitHub CLI.

**Mac :**
```bash
brew install gh
gh auth login
```

> Si `brew` n'est pas installé : va sur [brew.sh](https://brew.sh) et suis les instructions (1 commande à coller dans le terminal).

Suis les instructions : `GitHub.com` → `HTTPS` → `Login with a web browser` → autorise dans le navigateur.

---

### Étape 6 — Tester la synchronisation

Dans Obsidian : `Cmd+P` → tape `commit` → **Git: Commit-and-sync**

Si aucune erreur n'apparaît, tu es connecté et synchronisé. ✓

---

### Au quotidien

- **Recevoir les notes des autres** : se fait automatiquement au démarrage d'Obsidian
- **Partager une note** : copie-la dans `JARDIN/[ton-prénom]/`, puis `Cmd+P` → Commit-and-sync
