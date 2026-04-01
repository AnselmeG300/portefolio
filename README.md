# Portfolio — CI/CD GitHub Pages

Ce repository contient le pipeline de déploiement automatique du portfolio personnel vers **GitHub Pages**.

## Fonctionnement

Le code source du portfolio est hébergé dans un repository séparé : [`AnselmeG300/projectsportofolio`](https://github.com/AnselmeG300/projectsportofolio).

Ce repository a pour unique rôle de **déclencher et orchestrer le déploiement** via GitHub Actions.

## Workflow CI/CD (`.github/workflows/pages.yml`)

Le workflow se déclenche :
- À chaque **push sur la branche `main`**
- Manuellement via l'interface GitHub (**`workflow_dispatch`**)

### Étapes du pipeline

1. **Clone du repository source** — récupère le contenu du portfolio depuis `AnselmeG300/projectsportofolio`
2. **Configuration de GitHub Pages** — prépare l'environnement de publication
3. **Upload de l'artifact** — package le contenu statique du portfolio
4. **Déploiement** — publie le site sur GitHub Pages

## URL du portfolio

Le portfolio est accessible à l'adresse générée par GitHub Pages lors du déploiement.
