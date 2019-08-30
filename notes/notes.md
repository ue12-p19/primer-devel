# notebooks

Pour suivre ce cours, deux options :

* installation Jupyter locale
* utilisation à distance sur nbhosting

Dans l'esprit de la prise d'autonomie, c'est la première option qui est recommandée à terme.

Toutefois la plateforme nbhosting est disponible en guise de secours, notamment au début du cours, pour permettre de suivre les cours sans installation locale préalable.

# installation locale

Par rapport à une installation Python standard, plusieurs niveaux de dépendances doivent être envisagés

## dépendances dures

A minima, pour exécuter les notebooks de ce cours vous devez installer quelques bibliothèques; pour cela la méthode la plus simple consiste à faire 

```bash
pip install -r requirements.txt
```

## confort

Dans les slides on utilise fréquemment une extension jupyter qui s'appelle `splitcell`; elle permet d'avoir des cellules qui prennent une demie largeur, pour mieux utliser l'espace sur les slides, pour l'activer :

```bash
jupyter nbextension enable splitcell/splitcell
```

Noter que si vous avez un système de virtualenv ou d'environnement conda, il peut être utile d'ajouter cette option, afin de n'activer cette extension **que** dans votre virtualenv.

```bash
jupyter nbextension enable splitcell/splitcell --sys-prefix
```

Enfin la visionneuse peut être upgradée à la version 5.6, actuellement en  développement mais plus confortable:

```bash
pip install -U --pre rise
```

# nbhosting

Les images docker préparées pour exécuter le cours sous nbhosting contiennent tout ce qui est nécessaire.

Par contre il faut s'attendre à un délai assez long la première fois qu'on se connecte sur un cours, ou après une période d'inactivité, le temps de recréer un container.

Il existe aussi quelques fonctionnalités spécifiques à nbhosting :

* pour passer en mode plein écran, utiliser les petites icônes en forme de `<` et de `^` dans les coins supérieurs gauche et droit respectivement de l'iframe jupyter; avec n'importe quel modifier comme `Shift` ou `Control` ces icônes changent une seule direction. 

* dans le menu Jupyter `File` il y a deux ajouts qui sont
  * *Reset to Original* : permet de revenir à la version 'prof' du notebook courant
  * *Share Static Version* : pour exposer en read-only un notebook via une URL, par exemple pour une discussion dans un forum

* **git** : pour chaque étudiant qui ouvre un cours pour la première fois, on va cloner au sens git le repo du prof; si par exemple lors d'une 2ème ou 3ème session, du contenu a été ajouté depuis le début du cours, il est donc nécessaire pour l'étudiant de **tirer** dans ce repo git.

  Pour cela actuellement il est nécessaire de passer par jupyterlab (en bas à gauche dans la vue nbhosting, sortie du mode plein écran). Deux options :

  * jupyterlab est buildé avec l'extension 'jupyterlab-git` qui permet de tirer, voir les changements, les abandonner si nécessaire..
  
    ![](nbhosting-git-pull.png)

  * en ligne de commande, pour cela créer un terminal sous jupyter et aller dans `work`

    ![](git-terminal.png)]

  