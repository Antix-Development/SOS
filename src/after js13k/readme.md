# SOS - Extended code
<div align="justify">

After the js13k competition ended, I messed about with the code some more.

**13/9/2021**

- Basic debug out can be toggled with the "o" key. When debugging is enabled onscreen enemies have circles drawn to show their collision radius (`actor.cR`), targeting range (`actor.range`), and a line pointing to whichever other actor they might be targeting (``actor.T`).

- Tried minifying even more using RoadRoller, and JSCrush but both caused issues when running the game.

- Actor now has a dedicated target attribute (`actor.T`). This makes it easier to manage which other actor any particular actor might be targeting.

- `home()` was renamed to `seek()` which is a more appropriate name. `seek()` now takes jut one parameter `actor` to correspond with the actor now having a dedicated target attribute.

- Discovered a bug when the player dies.
 When entering game over mode, `enteringName` is not defined so 'keyUp()' throws a console error. Set `enteringName` to `false` when initiating a new game which resolved it.

</div>