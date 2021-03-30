# adresses-ftth

Extraction des adresses contenues dans les [fichiers de déploiement FTTH](https://www.data.gouv.fr/datasets/547d8d7ac751df405d090fcb).

## Pré-requis

* [Node.js](https://nodejs.org) version 12 ou supérieure
* yarn ou npm
* 8 Go de mémoire vive

## Utilisation

### Installation des dépendances

```bash
yarn
```

### Téléchargement des dernières données de déploiement

Les données peuvent être récupérées sur [cette page](https://www.data.gouv.fr/datasets/547d8d7ac751df405d090fcb).
L’archive éventuelle doit être extraite au préalable car le script ne supporte que les données brutes ou gzippées.

Par exemple : `unar 2020t1-immeuble.7z`

### Pré-chargement des données

```bash
yarn preload /chemin/vers/mv_immeubles_xxxxx.csv
```

Cette opération, qui dure plusieurs minutes (5 minutes sur un ordinateur portable de 2015), récupère les données et les range par code commune actuelle.

### Production des fichiers

```bash
yarn build
```

Cette opération dure plusieurs dizaines de minutes et va produire les fichiers finaux, après plusieurs étapes de traitement.
Les fichiers résultants sont disponibles dans le dossier `dist`.

## Licence

Licence du code : MIT

Licence des données : Licence Ouverte
