---
category: Miscellaneous
description: Kidoju quizzes are like PowerPoint&reg; presentations with the ability to record answers and calculate a score.
icon: singer
keywords: Memba, Kidoju, software, education, teach, learn, study, knowledge, test, quiz, correction, tablets, SAT, Quizlet, Khan Academy
language: en
title: Functional requirements and concepts
creation_date: 2014-08-17T13:16:33Z
uuid: 27948240-faef-11e5-af20-a53f004f8aa7
author: jlchereau
author_url: https://github.com/jlchereau
avatar_url: https://avatars.githubusercontent.com/u/2556751?v=3
edit_url: https://github.com/kidoju/support.kidoju.com/blob/master/en/posts/2014/requirements.md
site_url: https://www.kidoju.com/support/en/posts/2016/04/requirements
---
> After having described a [vision](https://www.kidoju.com/support/en/posts/2015/05/vision) for a system that would allow any teacher
to design and assign work that any student could complete on a mobile device with instant automated corrections, we define here the key requirements for such a system. 

### Components

Kidoju comprises:

- a Content Management System (CMS) with users, searchable content, versioning and activity tracking,
- a content editor, 
- a content player,

where:
 
- content essentially consists of knowledge tests or quizzes;
- activities include views, comments, ratings and scores.

[YouTube](https://www.youtube.com/) and [SlideShare](http://www.slideshare.net/) have similar Content Management Systems where content respectively consists in videos and slide presentations.
Replace those videos and slide presentations by quizzes, and you should have a pretty good idea what such a Content Management System should look like.

### Editor/Player

Most existing quiz systems are designed as lists of questions, optional images and sets of alternative answers.
When a user executes a quiz, each question is displayed with an image and a set of buttons representing all possible answers.

![Multiple Choice Questions](https://raw.githubusercontent.com/kidoju/support.kidoju.com/master/en/posts/2014/requirements.jpg)

**Our objective is to digitize most exercises that can be found in student books and provide automated corrections.**
If the aforementioned quiz systems have the merit of simplicity, they fall short of reaching this objective.

To this end, Kidoju requires an extensible toolbox of:

- standard controls including labels, images, textboxes and buttons,
- specialized widgets to handle complex interactions including dragging and dropping, connecting, drawing math functions and chemical formulas. 

Microsoft PowerPoint® makes a familiar user interface to order pages and layout controls and widgets.

The PowerPoint® paradigm and an extensible toolbox of specialized widgets make the ideal combination for a rich editor
to design highly-interactive self-corrected knowledge tests or quizzes.

![Microsoft PowerPoint®](https://raw.githubusercontent.com/kidoju/support.kidoju.com/master/en/posts/2014/requirements.png)