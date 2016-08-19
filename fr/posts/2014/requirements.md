---
category: Miscellaneous
description: Les quiz Kidoju sont comme des présentations PowerPoint&reg; avec la capacité d'enregistrer des réponses et de calculer un score.
icon: singer
keywords: Memba, Kidoju, logiciel, éducation, enseigner, apprendre, ètudier, connaissance, test, quiz, correction, question, réponse, score, version, workflow, powerpoint.
language: fr
title: Besoins fonctionnels et concepts
creation_date: 2014-08-17T13:16:33Z
uuid: 90bd371b-977e-490d-8268-0cf4c731fd98
author: jlchereau
author_url: https://github.com/jlchereau
avatar_url: https://avatars.githubusercontent.com/u/2556751?v=3
edit_url: https://github.com/kidoju/support.kidoju.com/blob/master/fr/posts/2014/requirements.md
site_url: https://www.kidoju.com/support/fr/posts/2016/04/requirements
---
> Après avoir décrit une [vision](https://www.kidoju.com/support/fr/posts/2015/05/vision) pour un système qui permettrait à tout enseignant
de concevoir et d'allouer le travail que tout étudiant pourrait exécuter sur un appareil mobile avec des corrections automatisées instantanées,
nous définissons ici les principales caractéristiques d'un tel système.

### Composants

Kidoju comprend:

- un système de gestion de contenus (CMS) avec utilisateurs, contenus indexés pour leur recherche, gestion de versions et suivi des activités,
- un éditeur de contenu, 
- un lecteur de contenu,

dans lequel:
 
- le contenu est essentiellement constitué de tests de connaissance ou quiz.
- les activités comprennent les vues, les commentaires, les notations par étoiles, et les scores.

[YouTube](https://www.youtube.com/) et [SlideShare](http://www.slideshare.net/) ont des systèmes de gestion de contenus similaires où le contenu est constitué respectivement de vidéos et de présentations de diapositives.
Remplacez ces vidéos et ces présentations de diapositives par des quiz, et vous devriez avoir une assez bonne idée de ce à quoi ce système de gestion de contenus devrait ressembler.
                                                                                
### Editeur/Lecteur


La plupart des systèmes de quiz existants sont conçus comme des listes de questions, des images optionnelles et des ensembles de réponses alternatives.
Lorsqu'un utilisateur exécute un quiz, chaque question est affichée avec une image et un ensemble de boutons représentant toutes les réponses possibles.

![Questions à Choix Multiples](https://raw.githubusercontent.com/kidoju/support.kidoju.com/master/fr/posts/2014/requirements.jpg)

**Notre objectif est de numériser la plupart des exercices qui peuvent être trouvés dans les livres d'étudiants et de fournir des corrections automatiques.**

Si les systèmes de quiz mentionnés ci-dessus ont le mérite de la simplicité, ils sont incapables d'atteindre cet objectif.
À cette fin, Kidoju nécessite une boîte à outils extensible, notamment:

- des contrôles standards, y compris les étiquettes, les images, les textboxes et les boutons,
- des widgets spécialisés pour gérer les interactions complexes y compris le glisser-déposer, les connexions, le dessin des fonctions mathématiques et des formules chimiques.

Microsoft PowerPoint® offre une interface utilisateur familière pour ordonner les pages et disposer des contrôles et des widgets.

Le paradigme PowerPoint® et une boîte à outils extensible de widgets spécialisés forment une combinaison idéale pour un éditeur riche
de conception de tests de connaissance ou quiz hautement interactifs et auto-corrigés.

![Microsoft PowerPoint®](https://raw.githubusercontent.com/kidoju/support.kidoju.com/master/fr/posts/2014/requirements.png)