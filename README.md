# Turbo Morphing + TomSelect

This repository shows example "bad behavior" when morphing occurs
while using a JavaScript library (e.g. TomSelect) that modifies the DOM.

## Reproducing the Issue

1. `git clone git@github.com:weaverryan/turbo-morph-tom-select-reproducer.git`
2. Get a web server running - as simple as `php -S localhost:8000` or anything else.
3. Open the page. TomSelect will transform the `select` into a rich element.
   Click the `Same page navigate` to trigger a morph.

The result is that the HTML added by TomSelect is lost. However, the Stimulus
controller wasn't removed, so it's not disconnected and reconnected. There are also
no values or targets that are lost that we could respond to.
