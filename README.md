Armour mod

This mod provides the ability to give clothing objects the ability to block attacks.
This is done by adding a transition with the weapon as actor and armour as target.
The newActor and new Target should be the same as the actor and target, unless it
is desirable to have one of them change.

The server check for what the weapon turns into after using it is still performed,
e.g. the bow and arrow will still turn into a bloody bow after shooting it at
someone, even if their armour blocks it. Transitions should be updated accordingly.

The backpack slot is repurposed as the arms slot for the purposes of armour. In this
way, a shield can be set up as a backpack clothing item, and this will block the arms.

An example of how this can be used is to create a piece of armour with several uses
and a percentage useChance, and various sprites at the usage levels to show damage.
Next create a generic transition for the object, with the newActor as itself (this
handles the reduction of uses). Next add a generic last use transition where the
object either disappears or turns into a ruined version of itself.

When this armour blocks an attack, there will be a chance for it to take damage,
which will appear on the object, then the object will eventually be destroyed and
no longer protect the wearer.

To slow down attacks, a weapon could be made to turn into an undeadly version of itself
which decays back into its useable version after a number of seconds. This can be used
to make some weapons quicker than others, although it is limited to whole numbers
of seconds.