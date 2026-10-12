# TP 2 — Simulation multi-agents avec Mesa 3

Ce TP étudie la formation de l’opinion publique à l’aide d’un modèle multi-agents en Python. Chaque agent représente un citoyen dont l’opinion évolue selon les opinions des agents voisins.

## Objectifs

- Décrire le modèle avec le protocole ODD : objectifs, entités, variables d’état et processus.
- Implémenter un agent `CitizenAgent` et un modèle `OpinionModel` avec Mesa 3.
- Observer l’évolution des opinions grâce aux données globales et individuelles.
- Comparer l’influence sociale pour plusieurs valeurs du paramètre `alpha`.

## Fonctionnement du modèle

Les agents sont placés sur une grille torique de 10 × 10. Chaque opinion est comprise entre 0 et 1. À chaque étape, un agent calcule la moyenne des opinions de ses voisins, puis rapproche sa propre opinion de cette moyenne selon `alpha`.

Le notebook compare trois réglages : `alpha = 0`, `alpha = 0,5` et `alpha = 1`. Il affiche l’opinion moyenne et la variance de la population, ainsi que les trajectoires d’un échantillon de 20 agents. Le `DataCollector` de Mesa recueille ces données pendant 50 étapes.

## Fichiers

- Notebook du TP : `src/python_uv_workspace/TP2Mesa_Simulation_MA.ipynb`
- Rapport : `rapport_abderrahim_chokri.ipynb`

Le rapport contient les graphiques issus des exécutions et les réponses aux cinq premières questions de la dernière cellule de questions du TP.

## Ouvrir le notebook

Depuis la racine du projet, lancez JupyterLab avec l’environnement `uv` :

```bash
uv run jupyter lab
```

Puis ouvrez le notebook du TP ou le rapport dans JupyterLab, Jupyter Notebook ou Visual Studio Code.
