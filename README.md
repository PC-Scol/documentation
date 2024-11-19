# Guide de contribution github/PC-Scol

## Description

Le github PC-Scol est un lieu d'échange entre établissements de l'enseignement supérieur qui souhaitent partager les outils et les librairies qu'ils pensent être utiles pour d'autres établissements. L'équipe PC-Scol peut également y déposer des outils ou des librairies. Le contenu de ce github est accessible à tous.

## Accessibilité

### Lecteur

Tous les repository sont accessibles au public en lecture. Il n'est pas nécessaire de faire partie de l'organisation github/PC-Scol pour y accéder.

### Contributeur

Le contributeur a la capacité de créer un repository, créer des branches et commiter. 

**ATTENTION**, il y a plusieurs prérequis pour contribuer :
* effectuer une demande d'adhésion à l'organisation github/PC-Scol en indiquant la motivation de la demande et le compte github à rajouter,
* le compte utilisé doit disposer à minima d'un [Personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) avec le scope "public_repo".

### Mainteneur

Le mainteneur d'un repository est un contributeur désigné comme tel. Il valide les Pull Request.

## Gestion des comptes

Il est recommandé de pouvoir identifier qui contribue et à quel établissement il appartient.

## Organisation du dépôt github/PC-Scol

### Utilisation de topics

Il n'y a pas d'arborescence pour répartir ou organiser les repositories. Il est proposé d'utiliser des "topics" pour identifier les dépôts selon leur(s) sujet(s). Exemple du topic 'rdd' sur le repo 'mise_en_qualite_RDD' :

![image](https://github.com/user-attachments/assets/90c6b821-0a7a-4712-b676-f7502a17474c)

Exemple de recherche de repositories sur le topic "dre" pour l'organisation Github PC-Scol :

![image](https://github.com/user-attachments/assets/785d05b1-e63b-44c2-8ebf-d3cb44125fa1)

Topics proposés :
* api
* dre
* rdd
* moodle
* technique

Nous souhaitons limiter le nombre de topics utilisés, aussi leur création est centralisée, au besoin vous pouvez contacter le projet PC-Scol pour en ajouter.

## Choix de la licence

Les licences recommandées par défaut sur PC-Scol sont :

* « GNU Affero General Public License v3.0 or later » (SPDX : AGPL-3.0-or-later) : Pour tous les composants métiers et la plupart des composants techniques, la licence du code et des composants associés. Cette licence est consultable à l’adresse : [https://spdx.org/licenses/AGPL-3.0-or-later.html#licenseText](https://spdx.org/licenses/AGPL-3.0-or-later.html#licenseText). Il s’agit d’une licence dite « à réciprocité » ce qui signifie que toutes les contributions faites par des tiers devront être redistribuées sous cette même licence afin de garantir les mêmes droits et libertés. Cela permet notamment au projet, si cela est jugé pertinent, d’intégrer des développements faits par des tiers ou des établissements de l’Enseignement Supérieur et de la Recherche.
* « Apache 2.0 » (SPDX : Apache-2.0) : Pour les composants techniques génériques sans valeur métier. La licence est consultable à l’adresse : https://www.apache.org/licenses/LICENSE-2.0.html. Cette licence dite « permissive » permet une diffusion plus large des modifications apportées aux composants et donc une augmentation du nombre des potentiels contributeurs.

## Gestion des versions

Il est recommandé mais pas obligatoire de gérer la version des sources dans un repository au travers de tags github. Le choix est laissé à la discrétion des contributeurs. Si une contribution change régulièrement il est fortement préconisé de versionner.

Étant donné un numéro de version MAJEUR.MINEUR.CORRECTIF, avec les incrémentations suivantes :

1. le numéro de version MAJEUR quand il y a des changements non rétrocompatibles,
2. le numéro de version MINEUR quand il y a des ajouts de fonctionnalités rétrocompatibles,
3. le numéro de version de CORRECTIF quand il y a des corrections d’anomalies rétrocompatibles.

Des libellés supplémentaires peuvent être ajoutés pour les versions de pré-livraison et pour des méta-données de construction sous forme d’extension du format MAJEURE.MINEURE.CORRECTIF.

## Fichiers présents dans le dépôt

Avoir au minimum les fichiers :

* LICENSE : licence de publication du logiciel (il est créé automatiquement lors du choix de la licence au moment de la création du repository).
* README : description du projet. Peut décrire l’objectif et l’administration à l’origine de la publication.

Ces fichiers doivent être en texte simple ou avec du marquage minimum (ie Markdown). Il n’est pas recommandé d’utiliser des formats binaires (ie PDF).

## Entête des fichiers sources
Conformément aux préconisations détaillées dans https://reuse.software il est recommandé que chaque fichier de code source dispose de son auteur, de son identifiant de licence SPDX, ainsi que d’une copie de la licence dans le dépôt local.

Exemple :
```
/*
 * Auteur : juliette.renard@pc-scol.fr
 *
 * SPDX-License-Identifier: AGPL-3.0-or-later
 * License-Filename: LICENSE
 */
```

## Bonnes pratiques de contribution

**ATTENTION**, Ne pas communiquer de mots de passe, secrets ou informations sensibles dans les contributions .

### Signaler un problème

* En cas de problème de sécurité, NE PAS effectuer une public issue. Contacter le contributeur principal du repository
* Cliquer sur les menus "Issues" puis "New Issue". Indiquer le cas échéant sur quelle version le problème a été détecté puis être le plus exhaustif possible : cas de reproduction, logs fichiers, logs écran

### Processus nominal

En cas de développement de nouvelle fonctionnalité ou de hotfix, cloner le repository en local puis effectuer les changements dans une nouvelle branche (il est très fortement déconseillé de travailler directement sur main; les propriétaires/créateurs de repository peuvent même protéger la branche par défaut) :

* Si c'est une branche corrective (fix branch), l'appeler **fix-XXXX-description** where XXXX est le numéro de l'issue dans le repository github
* Si c'est une branche de nouvelle fonctionnalité (feature branch), créer une issue d'amélioration (enhancement issue) pour expliquer l'objectif de la nouvelle fonctionnalité et la nommer **feature-XXXX-description** où XXXX est le numéro de l'issue.

Après le push de la branche, il est demandé au contributeur de créer une Pull Request (PR) dans la foulée afin qu'elle puisse être examinée par un mainteneur. L'URL pour créer la PR est indiquée dans le terminal après le premier push de la branche.

### Commit
Les messages de commit commencent par référencer l'issue à laquelle ils se rapportent, il décrivent une synthèse de l'objectif et du contexte

### Pull request
Les PR sont approuvées par le/les mainteneurs du repository dans lequel la PR a été effectuée. Le mainteneur est par défaut l'initiateur du repository.

## Support
PC-Scol n'est pas responsable des scripts et outils partagés et ne garantit pas leur contenu. Il est de la responsabilité de chaque établissement de s'assurer de l'effet des scripts exécutés.

PC-Scol ne fait pas de support sur le code partagé. De même, les contributeurs ne s'engagent pas à fournir du support.
