---
layout: post
title: Angular Progress Circle Directive
---

The [Angular UI](http://angular-ui.github.io/) team gave us a really nice [progressbar](http://angular-ui.github.io/bootstrap/#/progressbar).  But I want something like a progress circle and there is nothing like that built by the Angular UI team.  Fortunately, I found this great [Angular round progress directive](https://github.com/angular-directives/angular-round-progress-directive).  But since my requirement is to have the progress circle in a modal, and the [Angular round progress directive](https://github.com/angular-directives/angular-round-progress-directive) doesn't quite work, I began my journey to make it work.

The result that I achieve is [https://github.com/pragmaticlogic/angular-bootstrap-progress-circle](https://github.com/pragmaticlogic/angular-bootstrap-progress-circle).  As you can see in the [README](https://github.com/pragmaticlogic/angular-bootstrap-progress-circle/blob/master/README.md) file and from the codes, the part of the code that draws the circle in the canvas is from [Stéphane Bégaudeau](https://github.com/sbegaudeau).  I only had to change Angular directive part to make it work (in a modal).

Here are the examples, one works in a page and the other works in an Agular bootstrap modal:

http://embed.plnkr.co/jr8e4AfY6rR2KTW3R4v2/preview

http://embed.plnkr.co/h8zgE5PnL3zVCInU5YsC/preview