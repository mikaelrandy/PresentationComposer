# PHPTour Nantes 2012

## Présentation

TODO

Parler de TEA

## Plan

### Gestion des dépendances

* Problématiques
* Dépendances de dépendances qui dépendent de dépendances
* Seules les dépendances primaires nous intéressent
* Et s'il y a des conflits entre les dépendances ?

### Solutions existantes

* Installation manuelle
	* (Tout à la main)
	* (Phar)
* Git submodule


### Qu'est-ce que composer

* Présentation générale

IDEA : utiliser l'image weNeedANewIdea

### Comment l'installer ?

* Une simple commande pour installer

```
curl -s https://getcomposer.org/installer | php
```

* Locallement, globalement, à volontée
* Auto-mise à jour

### Un fichier central : composer.json

#### name

* Différence entre un projet et une librairie

#### require

* Ce que j'ai besoin d'installer
* package : version
	* package : vendor/project
	* version
		* Version exacte
		* Rnage
		* Wildcard
		* Next Significat Release

#### require-dev

* Version de dev

#### conflict

* Gérer les problèmes d'installations concurrentes de package

#### replace

* permet d'indiquer que le package courant satisfait l'installation d'un autre

#### suggest

* Propositions de librairies associées/complémentaires

#### package/librairies

* Possibilité de vérifier l'installation de php/extensions/librairies sur la machine

### L'état du projet : composer.lock

### Et les gestionnaires de versions

* Il faut commiter les fichers composer.json ET composer.lock

### Installer le projet dans le même état

* --dry-run : tester l'installation sans la faire
* --dev : dépendances de développement
* --optimize-autoloader : utiliser classmap plutôt que PSR-0


### Mettre à jour le projet

* composer update
* possible de ne mettre à jour que partie des dépendances

### ?

* Autoloading
	* Il suffit d'inclure autoload.php
	* Possibilité d'ajouter ses propres règles
		* PSR-0
		* classmap
		* file
* Repository
	* Packagist
* Scripts (hooks)
* create-project

## Autres

* Tester Satis
* Stone
* Proxyfier Composer (http://moquet.net/blog/proxify-composer-php/)