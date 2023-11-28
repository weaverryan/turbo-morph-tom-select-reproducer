# TomSelect "reinitializing"

This repository shows an example of a page reloading via Ajax and
TomSelect "losing" its selected value.

## Reproducing the Issue

1. `git clone git@github.com:weaverryan/turbo-morph-tom-select-reproducer.git`
2. Get a web server running - as simple as `php -S localhost:8000` or anything else.
3. Open the page. TomSelect will transform the `select` into a rich element. Yay!
   If you click "Destroy & Recreate", that will successfully destroy and reinitialize TomSelect.
4. However, if you change the value (e.g. select "Ice Cream") and then click "Destroy & Recreate",
   TomSelect is destroyed and recreated, but the value is lost.
