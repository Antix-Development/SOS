# SOS - Extended code
<div align="justify">

After the js13k competition ended, I messed about with the code some more.

**13/9/2021**

- Basic debug out can be toggled with the "o" key. When debugging is enabled onscreen enemies have circles drawn to show their collision radius (`actor.cR`), targeting range (`actor.range`), and a line pointing to whichever other actor they might be targeting (``actor.T`).

- Tried minifying even more using RoadRoller, and JSCrush but both caused issues when running the game.

- Actor now has a dedicated target attribute (`actor.T`). This makes it easier to manage which other actor any particular actor might be targeting.

- `home()` was renamed to `seek()` which is a more appropriate name. `seek()` now takes jut one parameter `actor` to correspond with the actor now having a dedicated target attribute.

- Discovered a bug when the player dies ( *Uncaught TypeError: Cannot read properties of undefined (reading 'n') at keyUp (sos.js:2274)*). The issue was caused by `enteringName` being set to true at the wrong place in the code so 'keyUp()' throws a console error. Set `enteringName` to `false` when initiating a new game which resolved it.

These fixes and additions take the zip file up to 13,227 bytes, not far from the maximum allowed for js13k. I'll try to manually mangle some object attributes and see if I can;t get that size down a l,ittle.

After minifying with Terser, I ran the code through RoadRoller. Whilst the game was fine in FireFox, The UI elements flickered a few times in Chrome before disappearing totally. That's a shame because when zipped the whole thing is only 11,886 bytes.

It might be worth investigating whay it fails so terribly in Chrome as I think I could do quite a lot with an extra 1426 bytes ;)

</div>