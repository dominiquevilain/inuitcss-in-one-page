Inuit en une page avec des liens vers les divers modules
========================================================

SETTINGS
--------

- The [settings.defaults](https://github.com/inuitcss/settings.defaults/blob/master/_settings.defaults.scss) module contains a few variables and settings that are **required** for using any of the rest of the framework.
- The [settings.responsive](https://github.com/inuitcss/settings.responsive/blob/master/_settings.responsive.scss) module defines our initial breakpoint aliases and conditions.

TOOLS
-----

- The [tools.functions](https://github.com/inuitcss/tools.functions/blob/master/_tools.functions.scss) module—like mixins—contains a few framework functions that are **required** for using any of the rest of inuitcss. 
- The [tools.mixins](https://github.com/inuitcss/tools.mixins/blob/master/_tools.mixins.scss) module contains a few framework mixins that are **required** for using any of the rest of inuitcss.
- The [tools.responsive](https://github.com/inuitcss/tools.responsive/blob/master/_tools.responsive.scss) module just sets up our media query mixin.

GENERIC
-------
- The [generic.normalize](https://github.com/inuitcss/generic.normalize/blob/master/_generic.normalize.scss) module contains @necolas’ normalize.css. 
- The [generic.reset](https://github.com/inuitcss/generic.reset/blob/master/_generic.reset.scss) module is a considered approach to resetting elements. It selectively removes margins and paddings from certain elements, and provides some sensible defaults for some others.
- The [generic.box-sizing](https://github.com/inuitcss/generic.box-sizing/blob/master/_generic.box-sizing.scss) module causes all elements to use the more useful border-box box model.
- The [generic.shared](https://github.com/inuitcss/generic.shared/blob/master/_generic.shared.scss) module contains several high-level rulesets which apply a consistent, shared declaration (typically margins) across a number of elements.

BASE
----
- The [base.page](https://github.com/inuitcss/base.page/blob/master/_base.page.scss) module is a very high-level module which styles very basic, global, page-level aspects such at the project’s base font-size and line-height.
- The [base.headings](https://github.com/inuitcss/base.headings/blob/master/_base.headings.scss) module defines font sizes for base-level heading elements from h1 through to h6.
- The [base.paragraphs](https://github.com/inuitcss/base.paragraphs/blob/master/_base.paragraphs.scss) module provides a very small amount of additional styles for paragraphs.
- The [base.lists](https://github.com/inuitcss/base.lists/blob/master/_base.lists.scss) module provides very basic styling for regular ordered and unordered lists.
- The [base.images](https://github.com/inuitcss/base.images/blob/master/_base.images.scss) module provides very basic styling for images (img).

OBJECTS
-------
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

The framework does not provide any component module. It's the place where you define the styles specific to your site’s components.

TRUMPS
------
- The [trumps.clearfix](https://github.com/inuitcss/trumps.clearfix/blob/master/_trumps.clearfix.scss) module is a minimal clearfix helper class.
- The [trumps.widths](https://github.com/inuitcss/trumps.widths/blob/master/_trumps.widths.scss) module is a simple file of helper classes to drop widths onto elements such as grid systems.
- [trumps.widths-responsive](https://github.com/inuitcss/trumps.widths-responsive/blob/master/_trumps.widths-responsive.scss)
- [trumps.spacing](https://github.com/inuitcss/trumps.spacing/blob/master/_trumps.spacing.scss)
- [trumps.spacing-responsive](https://github.com/inuitcss/trumps.spacing-responsive/blob/master/_trumps.spacing-responsive.scss)
- [trumps.print](https://github.com/inuitcss/trumps.print/blob/master/_trumps.print.scss)
