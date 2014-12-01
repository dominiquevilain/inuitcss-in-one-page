Inuit in one page with links to the various modules
===================================================

SETTINGS
--------

The *settings* layer is essentially usefull when using a preprocessor (which is, of course, recommended). Compared to a regular dev. framework (like rails, or symfony, or laravel, etc.), it plays the same role as the conventions defined in the framework, the config variables and constants and the various namespaces used. In InuitCSS, serveral values are defined, but of course, it’s easy to [override those you want to](https://github.com/inuitcss/getting-started#modifying-inuitcss). Always keep in mind the rule *don’t hack the core*. If you want to change something, don’t touch Inuit, extend/override it.

Whatever you write in this layer, it shouldn’t ouput any CSS after compilation.

- The [settings.defaults](https://github.com/inuitcss/settings.defaults/blob/master/_settings.defaults.scss) module contains a few variables and settings that are **required** for using any of the rest of the framework.
- The [settings.responsive](https://github.com/inuitcss/settings.responsive/blob/master/_settings.responsive.scss) module defines our initial breakpoint aliases and conditions.

TOOLS
-----

The *tools* layer is also fondamentaly usefull when using a preprocessor. It’s the place to define all your functions, mixins, helpers.

This code written in this layer shouldn’t output any CSS either.

- The [tools.functions](https://github.com/inuitcss/tools.functions/blob/master/_tools.functions.scss) module—like mixins—contains a few framework functions that are **required** for using any of the rest of inuitcss. 
- The [tools.mixins](https://github.com/inuitcss/tools.mixins/blob/master/_tools.mixins.scss) module contains a few framework mixins that are **required** for using any of the rest of inuitcss.
- The [tools.responsive](https://github.com/inuitcss/tools.responsive/blob/master/_tools.responsive.scss) module just sets up our media query mixin.

GENERIC
-------

At the *generic* level you begin to define rules that will ouput only basic definitions for generic elements (ie. tags). In the [Inverted Triangle model](https://www.youtube.com/watch?v=1OKZOV-iLj4) that layer is still a broad one and the rules in it should target a great amount of elements in you page (all paragraphs, all lists, etc.), so the rules should be associated with extremely low specifictiy selectors (tag selectors or the universal selector. Eventually, some attribute selectors like `input[type=submit]`). It’s the place to include your *reset* and/or *normalize* rules. The rules defined here are not necessarily linked to your particular project, but rather rules you might use in every project you make.

- The [generic.normalize](https://github.com/inuitcss/generic.normalize/blob/master/_generic.normalize.scss) module contains @necolas’ normalize.css. 
- The [generic.reset](https://github.com/inuitcss/generic.reset/blob/master/_generic.reset.scss) module is a considered approach to resetting elements. It selectively removes margins and paddings from certain elements, and provides some sensible defaults for some others.
- The [generic.box-sizing](https://github.com/inuitcss/generic.box-sizing/blob/master/_generic.box-sizing.scss) module causes all elements to use the more useful border-box box model.
- The [generic.shared](https://github.com/inuitcss/generic.shared/blob/master/_generic.shared.scss) module contains several high-level rulesets which apply a consistent, shared declaration (typically margins) across a number of elements.

BASE
----

At the *base* level, it is time to speak about your particular project. That layer contains low-specificity rules (tag rules essentially), like the previous layer. In this layer, you will probably override or extend rules defined in the previous layer. 

- The [base.page](https://github.com/inuitcss/base.page/blob/master/_base.page.scss) module is a very high-level module which styles very basic, global, page-level aspects such at the project’s base font-size and line-height.
- The [base.headings](https://github.com/inuitcss/base.headings/blob/master/_base.headings.scss) module defines font sizes for base-level heading elements from h1 through to h6.
- The [base.paragraphs](https://github.com/inuitcss/base.paragraphs/blob/master/_base.paragraphs.scss) module provides a very small amount of additional styles for paragraphs.
- The [base.lists](https://github.com/inuitcss/base.lists/blob/master/_base.lists.scss) module provides very basic styling for regular ordered and unordered lists.
- The [base.images](https://github.com/inuitcss/base.images/blob/master/_base.images.scss) module provides very basic styling for images (img).

OBJECTS
-------

Once you have thought about the basic stuffs, it is time to watch your page/layout and to try to find the recuring pattens in it. Here, the designer must acquire some developper skills. The idea behind that layer is to find the smallest common multiple between the components of your pages. It is very likely that several parts of your pages will share common properties. Try to find those common properties, and more specifically, try to find the structural ones. What it means is that you have to look at your layout in a schematic way. Remove all colors and borders, all the chrome of your interface and try to expose its skeletton. There you are, you see the structure, and there you can start to find the common rules that the components of your page share. When you are there, you can extract your CSS rules in order to avoid repetition. The main objective of this layer is to write a few rules that you can use in as many locations as possible in your DOM tree. It’s the [DRY principle](http://en.wikipedia.org/wiki/Don't_repeat_yourself) that leads you at this step.

If that step is difficult, you can get help using good tools and methodologies in your design process. Let’s face it, becoming aware of that rational methodology of implementing CSS might change (and should change), the way you design interfaces or the way give feedbacks to designers when they make graphical propositions for an interface.  Using a wireframing tool like Balsamiq Mockup for instance helps you to stay at the structural level. And when you launch a graphical package like Sketch or Photoshop you know that you begin to think about the chrome/skin level.

- The [objects.layout](https://github.com/inuitcss/objects.layout/blob/master/_objects.layout.scss) system is a powerful, flexible, highly advanced evolution of the traditional grid system. It is based on [csswizardry-grids](http://csswizardry.com/csswizardry-grids/).
- The [objects.box](https://github.com/inuitcss/objects.box/blob/master/_objects.box.scss) module simply boxes off content.
- The [objects.media](https://github.com/inuitcss/objects.media/blob/master/_objects.media.scss) module is inuitcss’ implementation of [Nicole Sullivan](https://twitter.com/stubbornella)’s media object—the poster child of OOCSS. To find out where it all started, read [Nicole’s blog post](http://www.stubbornella.org/content/2010/06/25/the-media-object-saves-hundreds-of-lines-of-code/).
- The [objects.list-inline](https://github.com/inuitcss/objects.list-inline/blob/master/_objects.list-inline.scss) module simply displays a list as one horizontal row.
- The [objects.block](https://github.com/inuitcss/objects.block/blob/master/_objects.block.scss) module simply stacks an image on top of some text content. This incredibly frequently occurring design pattern is now wrapped up in a simple, reusable, configurable abstraction.
- The [objects.pack](https://github.com/inuitcss/objects.pack/blob/master/_objects.pack.scss) module simply causes any number of elements pack up horizontally to automatically fill an equal, fluid width of their parent.
- The [objects.list-ui](https://github.com/inuitcss/objects.list-ui/blob/master/_objects.list-ui.scss) module creates blocky, keyline-delimited list items.
- The [objects.list-block](https://github.com/inuitcss/objects.list-block/blob/master/_objects.list-block.scss) module simply creates blocky lists from uls or ols.
- The [objects.flag](https://github.com/inuitcss/objects.flag/blob/master/_objects.flag.scss) module is an object similar in appearance to the media object, but which provides slightly more advanced functionality.
- The [objects.tabs](https://github.com/inuitcss/objects.tabs/blob/master/_objects.tabs.scss) module is a simple abstraction for force a series of elements (usually a list) into an equal-width, tab-like format.
- The [objects.tables](https://github.com/inuitcss/objects.tables/blob/master/_objects.tables.scss) module provides some useful helpers for common table patterns.
- The [objects.buttons](https://github.com/inuitcss/objects.buttons/blob/master/_objects.buttons.scss) module is a simple, robust, extensible baseline for building entire suites of buttons onto.
- The [objects.list-bare](https://github.com/inuitcss/objects.list-bare/blob/master/_objects.list-bare.scss) module simply removes bullets and indents from lists.

COMPONENTS
----------

The framework does not provide any component module. It's the place where you define the styles specific to your site’s components. Of course, in this layer, you will probably increase a bit specificity (but not too much, use classes instead of other kind of selectors and use the [BEM](http://bem.info/method/definitions/) syntax which allows you to express in one word necessary dependencies (specificity stays at 10) that you would otherwise express using descendant or child selectors (specificity reaches 20 or more)). 

Remember, that layer is the *photoshop* layer, the one where you decorate your abstract entities defined in the *objects* layer. Like Harry Roberts says, it’s where your ui-list becomes your products-list. So it’s normal that you won’t find anything provided by the framework at this level. And that’s what makes the difference between a methodology/framework like inuit and a UI-package like Bootstrap. Bootstrap is an opinated way to style components. Bootstrap imposes a way to style components to the designer. At the contrary, Inuit lets you decide whatever style you want. It is just a proposition to help you organise your base code.  

TRUMPS
------

And finally there can be rules you want to win in every situation. When it’s the case, you define those rules in the *trumps* layer. Of course, here, the specificity has to be high. It’s the layer where you define exceptions or extremely particular cases, like for instance, the fact that you want to hide an element visually. If you want to hide an element visually, no matter what rules you’ve defined previously that might reach it, the hiding rule has to win, it is `!important`.

- The [trumps.clearfix](https://github.com/inuitcss/trumps.clearfix/blob/master/_trumps.clearfix.scss) module is a minimal clearfix helper class.
- The [trumps.widths](https://github.com/inuitcss/trumps.widths/blob/master/_trumps.widths.scss) module is a simple file of helper classes to drop widths onto elements such as grid systems.
- The [trumps.widths-responsive](https://github.com/inuitcss/trumps.widths-responsive/blob/master/_trumps.widths-responsive.scss) module is an extension of the default widths module. 
- The [trumps.spacing](https://github.com/inuitcss/trumps.spacing/blob/master/_trumps.spacing.scss) module is a small collection of helper classes for spacings like margin and padding.
- The [trumps.spacing-responsive](https://github.com/inuitcss/trumps.spacing-responsive/blob/master/_trumps.spacing-responsive.scss) module provides breakpoint-based classes for nudging margins and paddings around responsively, e.g. .lap-mb0, .desk-mb++.
- The [trumps.print](https://github.com/inuitcss/trumps.print/blob/master/_trumps.print.scss) module is a very crude, very basic reset-like module for print styles. It borrows basic rules from HTML5 Boilerplate.
