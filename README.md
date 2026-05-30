# codex-guidelines

Référentiel personnel de règles, méthodes et skills pour Codex.

Ce dépôt sert de base commune pour tous mes projets de développement. Il contient des instructions globales, des standards de qualité et des skills réutilisables pour guider Codex dans un contexte de développement robuste, orienté QA, architecture propre, Docker et exploitation auto-hébergée.

## Objectifs

* Centraliser mes règles de travail avec Codex.
* Éviter de répéter les mêmes consignes dans chaque projet.
* Améliorer la cohérence des réponses et modifications de code.
* Renforcer la qualité QA, la maintenabilité et la lisibilité.
* Préparer des workflows réutilisables pour mes projets personnels et professionnels.

## Structure

```text
codex-guidelines/
├── README.md
├── AGENTS.md
└── skills/
    ├── qa-review/
    │   └── SKILL.md
    ├── docker-unraid/
    │   └── SKILL.md
    ├── coding-standards/
    │   └── SKILL.md
    └── architecture-rules/
        └── SKILL.md
```

## Rôle des fichiers

### README.md

Documentation destinée aux humains.

Il explique :

* le rôle du dépôt ;
* l'organisation des fichiers ;
* la stratégie d'utilisation des skills ;
* les principes généraux appliqués à tous les projets.

### AGENTS.md

Instructions globales destinées à Codex.

Ce fichier contient les règles permanentes à respecter :

* approche QA ;
* limitation des risques de régression ;
* qualité et maintenabilité du code ;
* stratégie de test ;
* gestion de la complexité ;
* respect de l'architecture ;
* documentation des impacts.

### skills/

Contient les skills spécialisés.

Chaque skill représente un domaine d'expertise ou un workflow spécifique :

| Skill              | Usage                                                    |
| ------------------ | -------------------------------------------------------- |
| qa-review          | Analyse QA, risques, stratégie de tests                  |
| docker-unraid      | Développement et déploiement Docker auto-hébergé         |
| coding-standards   | Standards de code et bonnes pratiques                    |
| architecture-rules | Architecture logicielle et découpage des responsabilités |

## Installation locale recommandée

### 1. Cloner le dépôt

```bash
git clone <repository-url> ~/codex-guidelines
```

### 2. Créer le répertoire global Codex

```bash
mkdir -p ~/.codex/skills
```

### 3. Copier les skills

```bash
cp -R ~/codex-guidelines/skills/* ~/.codex/skills/
```

### 4. Copier les instructions globales

```bash
cp ~/codex-guidelines/AGENTS.md ~/.codex/AGENTS.md
```

## Variante avec liens symboliques

Pour éviter les copies manuelles, il est possible de créer des liens symboliques vers les skills du dépôt.

### Linux / macOS

```bash
ln -s \
~/codex-guidelines/skills/qa-review \
~/.codex/skills/qa-review
```

### Windows (PowerShell)

```powershell
New-Item `
  -ItemType SymbolicLink `
  -Path "$HOME\.codex\skills\qa-review" `
  -Target "$HOME\codex-guidelines\skills\qa-review"
```

Cette approche permet de maintenir une seule version des skills.

## Utilisation recommandée

### Instructions globales

Les règles présentes dans `AGENTS.md` sont appliquées à tous les projets.

Elles couvrent notamment :

* qualité logicielle ;
* architecture ;
* stratégie de tests ;
* maintenabilité ;
* documentation ;
* bonnes pratiques Git.

### Skills spécialisés

Les skills sont utilisés lorsque le contexte l'exige.

Exemples :

#### Revue QA

```text
Utilise le skill qa-review.
```

#### Projet Docker

```text
Utilise le skill docker-unraid.
```

#### Revue d'architecture

```text
Utilise le skill architecture-rules.
```

## Organisation recommandée des futurs skills

```text
skills/
├── qa-review/
├── coding-standards/
├── architecture-rules/
├── docker-unraid/
├── python-project/
├── kotlin-project/
├── github-actions/
├── database-review/
├── api-design/
└── documentation/
```

## Bonnes pratiques

### À mettre dans AGENTS.md

Règles toujours vraies :

* philosophie QA ;
* exigences de qualité ;
* stratégie de test ;
* exigences de maintenabilité ;
* principes d'architecture ;
* conventions Git.

### À mettre dans un skill

Règles spécifiques :

* Docker ;
* Kotlin ;
* Python ;
* GitHub Actions ;
* PostgreSQL ;
* Unraid ;
* API REST ;
* projets de lecture numérique ;
* workflows de métadonnées.

## Gestion des informations sensibles

Ce dépôt ne doit contenir :

* aucun mot de passe ;
* aucune clé API ;
* aucun token ;
* aucune URL privée ;
* aucun chemin spécifique à une machine ;
* aucune configuration personnelle sensible.

Utiliser des valeurs génériques :

```text
<repository-url>
<project-root>
<data-directory>
<application-url>
<container-name>
```

ou :

```text
$HOME
~/.codex
~/projects
```

Les informations locales doivent être stockées dans des fichiers exclus du versionnement.

Exemple :

```text
.local/
private/
```

et déclarées dans `.gitignore`.

## Philosophie

Codex doit être utilisé comme un assistant de développement prudent :

* comprendre avant de modifier ;
* limiter le périmètre des changements ;
* préserver l'existant ;
* signaler les risques ;
* proposer les validations nécessaires ;
* produire un code maintenable ;
* respecter l'architecture du projet ;
* favoriser les évolutions incrémentales plutôt que les refactorings massifs.

L'objectif est d'obtenir des résultats cohérents, reproductibles et de qualité sur l'ensemble des projets.
