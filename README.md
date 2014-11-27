inuitcss at a glance
====================

Settings - defaults
-------------------

```sass
// High-level base settings.
$inuit-base-font-size: 16px !default;
$inuit-base-line-height: 24px !default;
$inuit-base-text-color: #333 !default;
$inuit-base-background-color: #fff !default;

// Namespace.
//
// Would you like inuitcss’ classes to be prepended with a namespace? If so,
// define it here.
$inuit-namespace: null !default;


// These variables are framework variables, sourced from variables defined
// above. Feel free to use these variables throughout your project, but do not
// modify or reassign them.
$inuit-base-spacing-unit: $inuit-base-line-height;
$inuit-base-spacing-unit--small: round($inuit-base-spacing-unit / 2);
$inuit-base-spacing-unit--large: round($inuit-base-spacing-unit * 2);
```

Settings - responsive
---------------------
```sass
// Hold our breakpoint aliases and conditions in a list.
//
// These can be invoked later on via the `media-query()` mixin found in
// `_tools.responsive`.
$breakpoints: (
  "palm" "screen and (max-width: 719px)",
  "lap" "screen and (min-width: 720px) and (max-width: 1023px)",
  "lap-and-up" "screen and (min-width: 720px)",
  "portable" "screen and (max-width: 1023px)",
  "desk" "screen and (min-width: 1024px)",
  "retina" "(-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi)"
) !default;

// If we have included this file, set a variable to tell the rest of the
// framework that we have some responsive settings.
$inuit-responsive-settings: true;
```
