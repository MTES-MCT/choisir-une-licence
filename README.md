# TL;DR

 - il est légalement obligatoire à partir du 7 octobre 2018 que le code des projets de la fabrique soit open source
 - la politique de contribution DINSIC est [dispo](https://disic.github.io/politique-de-contribution-open-source/). 
 - votre projet doit à minima:
  - choisir une license. En prendre une parmi celles dispo sur [data.gouv.fr/fr/licences](https://www.data.gouv.fr/fr/licences)
  - ouvrir son code
  - préciser qui est mainteneur (pour fournir un point de contact)
 - ne pas hésiter à demander des coups de main à la DSI pour tout ce qui est conformité

# Contexte

A partir du 7 octobre 2018 : tout projet public (porté par les ministères, ou les collectivités de plus de 3500 hab) doit être open source. 3 exceptions:
 - secret (industriel, prop)
 - sécurité (des personnes physiques et du SI)
 - protection de la fraude

La sécurité ne concerne pas la sécurité de votre applicatif. Si le code est une passoire, avec des failles de sécurité partout, ca ne veut pas dire qu'elle ne doit pas être publiée, l'argument n'est pas recevable: les failles doivent être corrigées et le code publié.

# la politique de contribution DINSIC

 - publication officielle de la [politique de contribution DINSIC cette semaine](https://disic.github.io/politique-de-contribution-open-source/). C'est une mise au propre de bonnes pratiques déjà bien connus (issues, pour certaines, de la Linux Foundation). Pour info, il y a quelqu'un du MTES dans les contributeurs.

Le but pour eux c'est maintenant de la faire infuser dans la culture des ministères. Dans les grandes lignes:

  - pas d'obligations: le but, c'est d'expliciter au contraire les autorisations, définir une cible raisonnable, atteignable ("voici les bonnes pratiques : si vous les respectez, vous vous éviterez des écueils par la suite")
  - si un ministère a des règles particulières, il doit le faire savoir de manière publique
  - s'adresse aux développeurs, cherche à valoriser les compétences techniques et montrer de la reconnaissance auprès de ceux déjà impliqués dans des communautés.
  - un projet doit a minima:
   - choisir une license
   - ouvrir son code (obligation légale à partir du 7 octobre 2018)
   - dire qui est mainteneur (pour avoir un point de contact)

# Choisir une license

2 problèmes: 
 - Quelles licenses peut-on utiliser ?
 - Parmi les licenses autorisées, comment choisir ?

## Quelles sont les licences autorisées

 - Projet déjà existant, ou projet sur lequel on contribue: on prend des licenses reconnues. L'état délègue à 2 organisations (FSF, OSI) le travail de décider si une license est open source ou non. Si un des 2 organisme dit qu'une license est open-source, on peut l'utiliser. Se référer à spdx.org/licenses (du coup, si une brique logicielle n'a pas une license autorisée, vous ne pouvez pas l'utiliser)
 - Nouveau projet: pas le droit de prendre n'importe laquelle. Prendre celles sur data.gouv.fr/licences (le but, c'est d'éviter une prolifération de licenses. Si on en veut une autre, on peut en discuter pour la rajouter)
 - ne pas avoir de licence est pire qu'avoir une licence peu permissive. Fournissez une licence avec votre projet, et évitez à tout prix les composants qui n'ont pas de licence.

## Comment choisir parmi celles dispo ?

 1) Lire [cet article](https://www.gnu.org/licenses/license-recommendations.fr.html) qui dégrossit le travail 
 2) Utiliser un site de résumé:
  - [choosealicense.com/licenses](https://choosealicense.com/licenses/) (utilisé dans github)
  - [tldrlegal.com](tldrlegal.com)

Il y a également les [ressources libres pour l'éducation](https://www.slideshare.net/bzg/ressources-libres-pour-lducation-lesquelles-et-pourquoi-15552125) à partir des slides 34-35

Quelques remarques:

 - derrière un choix de license, il y a un choix juridique, mais aussi un choix de philosophie. On embarque pas les même gens quand on propose de la GPL et pas du MIT.
 - il faut choisir des licenses adaptées au logiciel. Le CC n'est pas adapté au logiciel
 - il y a une license dinsic, mais il ne faut pas l'utiliser (préco dinsic ! pour le logiciel, elle est moins bien que d'autres licenses plus adaptées)
 - dans la logique DINSIC, quand on choisit une license, on n'en change plus
 - préco: mettre l'identifiant de license spdx en commentaire dans chaque fichier (en entête, peut se faire via l'IDE) 

# Des réticenses à l'ouverture ?

Concernant la sécurité:

 - ne pas hésiter à se rapprocher de la DSI 
 - demander le cahier de cohérence technique
 - voir éventuellement pour un audit

Globalement, si vous avez peur qu'on voit du code pourri, dites vous qu'écrire du code open source va vous forcer à écrire du code de meilleure qualité ;). Pensez au PACS, à mettre en oeuvre à chaque étape du projet :

 - Performance
 - Accessiblité
 - Conformité (respectez les licenses)
 - Sécurité
