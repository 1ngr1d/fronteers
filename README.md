# Planning and Building a Big Front-End

## Source order

1. `settings/` – Variables, feature switches and other project specific
   settings. These are defined first and will be picked up and used by the
  framework later on.
2. `tools/` – Mixins and functions to make tasks easier. These appear early
   on so that they can be utilised in the main body of the codebase.
3. `generic/` – Resets, global `box-sizing`. These styles are really far
   reaching; they underpin every element we place on the page.
4. `base/` – Base elements, unclassed `h1`, `ol`, etc. These are semantic
   HTML elements that require some base styling for when they exist outside of
   a component context (e.g. a regular, bulleted list in some body copy).
5. `gui/` – Designed components and modules. These build on top of semantic
   HTML elements and are referred to mainly through class selectors.
6. `trumps/` – Style trumps, helper classes and overrides. These need to
   override any other styles and thus come last. It is now uncommon for these
   styles to carry `!important`.
