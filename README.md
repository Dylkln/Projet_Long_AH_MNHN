# Programme de détection des recombinaisons

Ce programme a pour but de donner les frÃ©quences de bipartitions calculÃ©es par maximum de vraisemblance Ã  partir d'un alignement de sÃ©quence.

## Prérequis

L'utilisation d'un OS Linux ainsi que [Miniconda3](https://docs.conda.io/en/latest/miniconda.html) est fortement recommandÃ©e.
Il est impÃ©ratif d'avoir [RAxML](https://cme.h-its.org/exelixis/web/software/raxml/) installÃ© sur votre machine. Vous pouvez le faire *via* conda par la commande suivante : 
```
conda install -c bioconda raxml
```

## Télécharger le programme

1. Clonage du rÃ©pertoire github

> Lien HTTPS

```
git clone https://github.com/Dylkln/Projet_Long_AH_MNHN.git
```

> Lien SSH

```
git clone git@github.com:Dylkln/Projet_Long_AH_MNHN.git
```

2. Initialiser l'environnement conda Ã  partir du fichier *environment.yml*

```
conda env create --file environment.yml
```

3. Activer l'environnement conda

```
conda activate phylo
```

## Utilisation du programme

Pour utiliser le programme, vous devez Ãªtre dans le rÃ©pertoire "program" et lancer la commande suivante :

```
python phylo.py -f <FASTA_FILE> -n <NREP> -ws <WINDOW_SIZE> -s <STEP> -t <THREADS>
```

Avec les arguments suivants:

**OBLIGATOIRES**
- *FASTA_FILE* : Le fichier au format fasta contenant les alignements de sÃ©quences.

**OPTIONNELS**
- *NREP* : Nombre de matrice de rÃ©plication de bootstrap qui seront gÃ©nÃ©rÃ©es (par dÃ©faut 100). 
- *WINDOW_SIZE* : La taille de fenÃªtre dÃ©sirÃ©e (par dÃ©faut 1000). 
- *STEP* :  Le pas de la fenÃªtre dÃ©sirÃ©e (par dÃ©faut 100).
- *THREADS* : Le nombre de Coeurs que le programme peut utiliser (par dÃ©faut 1).

##### Exemple d'utilisation

```
python phylo.py -f ../data/exemple.fasta -n 10 -ws 1000 -s 100 -t 1
```
