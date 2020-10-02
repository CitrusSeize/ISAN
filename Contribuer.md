# Comment contribuer

Le Collectif a rendu SINA complètement open-source. Cela signifie que vous verrez le développement du projet dans son entièreté, et non pas juste les belles parutions finales. Nous accueillons toutes les idées et l'aide venues de l'extérieur !

SINA a deux parties principales: Le Coeur et les Addons. "Le Coeur" fait référence à toutes les parties du système qui est directement lié à la résolution des coordonnées de n'importe quel ensemble de récepteurs. "Un Coeur" est l'entièreté du système necessaire à la résolution de la position d'un ensemble particulier de récepteurs. Les Addons sont des modules additionnels qui utilisent ces données de positionnement pour implémenter de nouvelles fonctionnalités.
Quelques exemples de SINAv2:

- Quelques parties du coeur
    - Processeur d'axes: Évalue une équation d'axes pour résoudre l'une ou plusieurs des coordonnées X, Y, Z
    - Moteur d'inversion: Effectue une matrice inverse pour pouvoir calculer lles constantes pour le Processeur d'axes
    - Scanner: Sélectionne les émetteurs à utiliser en temps que points de références et configure les récepteurs et les variables globales

- Quelques Addons prévus
    - Vélocité: Utilise plusieurs échantillons de la position du vaisseau pour déterminer sa vélocité moyenne
    - Pilote automatique: Pilote le vaisseau en utilisant les saisies d'un ou plusieurs coeurs SINA

Vous pouvez contribuer à ces deux parties, cependant les méthodes diffèrent un peu:
 - [Contribuer un nouvel Addon ou une idée d'Addon](#Contribuer-un-nouvel-Addon-ou-une-idée-d'Addon)
 - [Contribuer à l'implémentation d'une idée existante (avec une publication)](#Contribuer-à-l'implémentation-d'une-idée-existante-(avec-une-publication))
 - [Il y a déjà une repo en cours, mais je veux faire ma propre version](#Il-y-a-déjà-une-repo-en-cours,-mais-je-veux-faire-ma-propre-version)
 - [Contribuer au coeur](#Contribuer-au-coeur)
 - [Contribuer en français](#Contribuer-en-français)
 - [Signaler un bug](#Signaler-un-bug)

## Contribuer un nouvel Addon ou une idée d'Addon

**CHERCHEZ D'ABORD SI UNE PUBLICATION N'A PAS ÉTÉ OUVERTE**

Ouvrez une publication s'appelant "Nouvel Addon:" suivi d'un nom descriptif pour votre Addon. La description doit contenir une explication bref du but de l'Addon. Cela permet d'indiquer à d'autres personnes que l'idée a déjà été suggérée et est potentiellement en développement.

Si vous souhaitez implémenter l'idée en plus de la suggérer: Fork la repo et créer une nouvelle branche s'appelant `dev-addon-<nom de votre addon>` depuis la branche dev. Postez un commentaire sur la publication que vous avez créé contenant "WIP" (Work In Progress, travail en cours) et un lien vers **la branche** que vous venez de créer dans votre fork. A partir de là, vous pouvez créer d'autres branches si necessaire, en les nommant de cette façon: `dev-addon-<nom de votre addon>-<nom de sous-branche>`. Tout le travail effectué sur votre Addon doit être fait dans un nouveau dossier: `Development/Addon Modules/<nom de votre addon>`. Ce dossier doit suivre la structure décrite dans [Development/ALIRE.md](Development/ALIRE.md).

Travaillez à votre rythme, et quand vous être satisfait du fonctionnement de votre Addon, envoyez une requête de fusion de votre branche dans la branche `dev`.

## Contribuer à l'implémentation d'une idée existante (avec une publication)

Si il a un commentaire qui contient le terme "WIP" et un lien vers une fork, le travail a déjà été commencé. 

Si il n'y a pas de commentaire "WIP", suivez les instructions pour créer vous même une nouvelle publication et commencez le travail dans votre propre fork.

Dans le cas où il existe déjà une branche, contactez les personnes travaillant dessus. Par convention, il devrait un avoir un README.md contenant les informations de contacte des contributeurs principaux dans `Development/Addon Modules/<nom de votre addon>`, qui se trouve sur le `dev-addon-<nom de votre addon>`.

## Il y a déjà une repo en cours, mais je veux faire ma propre version

**N'OUVREZ PAS UNE NOUVELLE PUBLICATION POUR UN ADDON DÉJÀ EXISTANT SOUS UN AUTRE NOM**

Merci d'essayer de travailler avec l'équipe déjà existante. Cependant, en cas de conflit par rapport à l'évolution du projet, merci de contacter l'une des personnes suivante pour résoudre le conflit (**attention, ces personnes sont anglophones**, pour un contact français, merci de se référer à la section [Contribuer en français](#Contribuer-en-français)):
 - Solon (Solon#4472 sur discord)
 - Azurethi (Azurethi#0789 sur discord)

## Contribuer au coeur

Si vous avez des idées pour améliorer le coeur, merci de créer une publication titrée "Amélioration coeur" suivi d'un titre descriptif, et expliquez votre amélioration plus en détail dans les commentaires de la publication.

Si vous pensez que vos idées pourraient contribuer grandement à l'amélioration du coeur (quelque chose qui améliorera beaucoup la vitesse d'exécution, réduira le nombre de puces, ou qui améliorera la précision), ou si vous voulez contribuer à l'implémentation et au développement du coeur, merci de contacter Solon (Solon#4472 sur discord, anglophone), qui peut être contacté facilement sur le serveur DIscord du Collectif.

## Contribuer en français

L'équipe en charge du développement de SINA est entièrement anglophone. A ce titre, il est important que pour qu'une communiquation puisse exister entre elle et d'éventuels participants français, des efforts soient faits des deux côtés.

**Merci de veiller à ce que votre travail reste clair et compréhensible par tous**, en utilisant un niveau de français correct, clair, succint et facile à traduire, pour un logiciel (Google Traduction, Linguee, DeepL,...) ou un débutant dans l'apprantissage du français.
Contactez [CitrusSeize](https://github.com/1Solon "LemonGrab#3728 sur Discord") pour la traduction en anglais de votre projet si necessaire. Merci encore une fois de rester résonnable sur la longueur de vos textes. Restez égalemment à disposition au cas où des précisions seraient necessaire pour assurer la meilleure qualité de traduction possible.

## Signaler un bug

Ouvrez une publication titrée "BUG:" suivi d'un titre descriptif. Merci d'inclure un maximum d'informations sur la nature du bug ainsi que les manières de le reproduire.

Les choses qui ne sont pas (toujours) des bugs:
 - Perte de signal: sauf si vous êtes bien dans la zone d'émission de SINA
 - Problème du système après un déassemblage rapide non plannifié
