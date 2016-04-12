---
category: Developer
description: Kidoju has a micro-services architecture based on the MEAN stack.
icon: server_client
keywords: architecture, web, mobile, Phonegap, MEAN, MongoDB, node, nodeJS, express, expressJS, angular, angularJS, jQuery, Telerik, Kendo, Kendo UI, docker, Amazon, REST, API
language: en
title: Technical architecture
creation_date: 2016-01-15T10:32:22Z
uuid: 27bf89e0-faef-11e5-af20-a53f004f8aa7
author: jlchereau
author_url: https://github.com/jlchereau
avatar_url: https://avatars.githubusercontent.com/u/2556751?v=3
edit_url: https://github.com/kidoju/support.kidoju.com/blob/master/en/posts/2015/architecture.md
site_url: https://www.kidoju.com/support/en/posts/2016/01/architecture
---
## Technical requirements

Our technical requirements were the following:

1. web and mobile applications (common code);
2. rich user interface (drag and drop);
3. cloud deployment and scalability (Amazon AWS, Microsoft Azure or Google App Engine);
4. one-click deployment, ideally with continuous integration.

and more specifically:

1. database support for full-text indexing;
2. storage of multimedia files;
3. RESTful API feeding both the web and mobile applications;
4. oAuth logins integrated with Facebook, Google and Twitter among others;
5. a rich library of HTML controls;
6. code-factoring between web and mobile for potability across devices and operating systems.

## Prototypes

We did two server prototypes inplementing oAuth logins and a RESTful API for CRUD operations:

1. A [Microsoft ASP.NET MVC](http://www.asp.net/mvc) application with a [SQL Server](https://www.microsoft.com/en-us/server-cloud/products/sql-server/) backend,
2. A MEAN ([MongoDB](https://www.mongodb.org/), [expressJS](http://expressjs.com/), [angularJS](https://angularjs.org/), [nodeJS](https://nodejs.org/)) application with a NoSQL backend.  

We did three client prototypes implementing drawing, dragging, dropping, translating, scaling, rotating all kinds of components including text, images, videos:

1. an SVG-based prototype using [RaphaelJS](http://raphaeljs.com/);
2. a Canvas-based prototype using [CreateJS](http://www.createjs.com/);
3. an HTML-based prototype using [jQuery](https://jquery.com/);

and we ran them in various browsers and in a [Phonegap](http://phonegap.com/) environement.

The client prototypes also used HTML control libraries including [jQuery UI](https://jqueryui.com/), [Telerik Kendo UI](http://www.telerik.com/kendo-ui),
[GrapeCity Wijmo](http://wijmo.com/) and [Infragistics Ignite UI](http://www.igniteui.com/) 

## Weighing our options

// --------------------------------------------------------------------------------> TODO: Add MEAN Logo Here

Although we enjoyed C# compilation and the ability of [ASP.NET Web API](http://www.asp.net/web-api) and [Entity Framework](http://www.asp.net/entity-framework)
to automatically present a uniform interface for [content negotiation](https://msdn.microsoft.com/en-gb/magazine/dn574797.aspx),
the MEAN stack proved much more scalable, versatile and easily debuggable (end-to-end JavaScript).

Using the MEAN stack, we naturally turned to [Amazon AWS](https://aws.amazon.com/) and [dockerized containers](https://www.docker.com/) for deployment.

Telerik Kendo UI was definitely the richest HTML control framework at the time and we did not retain angularJS in our MEAN stack
because Kendo UI includes data-binding and routing and because AngularJS 2 was planned to break compatibility with AngularJS 1.

Considering an SVG interface to design quizzes was inspired by the likes of [SVG-Edit](http://svg-edit.googlecode.com/svn/trunk/editor/svg-editor.html).
Although RaphaelJS made vector drawing, dragging and dropping very easy, a simple textbox proved to be a challenge especially to trigger the keyboard on mobile devices.
Considering most browsers do not support the ```<foreignObject>``` tag to embed HTML within SVG, some widgets like form controls and videos would have required an HTML layer on top of SVG.

Considering a canvas interface to design quizzes was inspired by Adobe Edge Animate CC among [other editors](https://www.picozu.com/editor/) and the idea of gamification in education. 
CreateJS is like RaphaelJS but targets the HTML ```<canvas>``` with a focus on complex animations.
CreateJS offers the benefit to manage an [HTML layer on top of the canvas](http://www.createjs.com/docs/easeljs/classes/DOMElement.html).
Like RaphaelJS, CreateJS would make drawing, dragging and dropping very easy, and the ability to include HTML components, although still experimental in version 0.82, would have filled the gap
to display form controls and video. Note that canvas is for rasterized images, but CreateJS offers the ability to keep a display list of text, shapes, bitmaps and DOM elements.

Although jQuery offers a uniform API across browsers, HTML elements are much more difficult to style, position, size and rotate properly due to margins, padding, and else.
Also drawing lines and shapes on an HTML stage is not possible without involving a canvas or an svg surface so we were going in circles.
We needed both HTML and a drawing surface (SVG or canvas). The question was which should be our primary target?
We took a step back to figure out what type of bricks could be considered to make our highly interactive quizzes in addition to the obvious text, audio and video widgets:

- we definitely needed all types of form controls including textboxes, checkboxes, option groups and drop-down lists, and there was no point redeveloping them for a canvas or SVG surface;
- we could also consider tapping into all sorts of Javascript controls, including [mathematic formulas](https://www.mathjax.org/), [charts](http://demos.telerik.com/kendo-ui/bar-charts/index),
[spreadsheets](http://demos.telerik.com/kendo-ui/spreadsheet/index) or else.

Drawing lines and shapes was definitely a secondary objective and HTML was our first target.
In other words, from a technical perspective, our highly interactive quizzes are a collection of HTML components.
Drawing surfaces are only one type of quiz components whether they are drawn with RaphaelJS, CreateJS, D3, MathJax or any other JavaScript library that best fits requirements.