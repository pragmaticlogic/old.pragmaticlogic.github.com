---
layout: post
title: Angular Progress Circle Directive
---

The [Angular UI](http://angular-ui.github.io/) team gave us a really nice [progressbar](http://angular-ui.github.io/bootstrap/#/progressbar).  But I want something like a progress circle and there is nothing like that built by the Angular UI team.  Fortunately, I found this great [Angular round progress directive](https://github.com/angular-directives/angular-round-progress-directive).  But since my requirement is to have the progress circle in a modal, I start with the following which seems to be the logical and correct way of including the progress circle in a modal:

<script src="https://gist.github.com/pragmaticlogic/8541747.js"></script>

and the script.js

<script src="https://gist.github.com/pragmaticlogic/8541858.js"></script>

but since the [Angular round progress directive](https://github.com/angular-directives/angular-round-progress-directive) doesn't quite work, i.e. the element does not get attached to the DOM, I began my journey to make it work.

The result that I achieve is [https://github.com/pragmaticlogic/angular-bootstrap-progress-circle](https://github.com/pragmaticlogic/angular-bootstrap-progress-circle).  As you can see in the [README](https://github.com/pragmaticlogic/angular-bootstrap-progress-circle/blob/master/README.md) file and from the codes, the part of the code that draws the circle in the canvas is from [Stéphane Bégaudeau](https://github.com/sbegaudeau).  I only had to change Angular directive part to make it work (in a modal).

Here are the examples.  This first example shows the progress circle in a modal, which was my original goal.  

<iframe style="border: 1px solid #999;width: 100%; height: 500px" src="http://embed.plnkr.co/h8zgE5PnL3zVCInU5YsC/preview" frameborder="0">&#160;</iframe>

This example shows that it stills works in any page.

<iframe style="border: 1px solid #999;width: 100%; height: 400px" src="http://embed.plnkr.co/jr8e4AfY6rR2KTW3R4v2/preview" frameborder="0">&#160;</iframe>

If you want to customize (to a certain degree), there are various configurations that you can use.  Let me know if you need any help.
