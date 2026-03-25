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
member_tag : [add_member_name]
date: add_today_date (format YYYY-MM-DD)
MOC:
  - "[[add_MOC_name]]"
  - "[[add_MOC_2_name_if_needed]]"
source: add_source_link
author: "[[add_author_name]]"
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
3. Obsidian Git : commit + push
4. L'équipe pull et découvre ta contribution

---

## Setup (nouveaux membres)

1. Cloner le repo : `git clone https://github.com/fgr16/HOLO-brain.git`
2. Ouvrir le dossier `HOLO-brain` comme vault dans Obsidian
3. Installer le plugin **Obsidian Git** (Community plugins)
4. Configurer Obsidian Git : pull au démarrage, push manuel ou auto
