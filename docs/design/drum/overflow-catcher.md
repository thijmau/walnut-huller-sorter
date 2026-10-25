# Overflow Catcher Design Document

![Render of the part](../../images/parts/abrasive-drum-exit-overflow-catcher.png)

## Problem

Because of the slight angle, once the drum gets fuller, the nuts start to stack
towards the exit cap. The problem is that if nuts get through at the top, then
they fall down the machine. They are supposed to land on the guiding rail, which
in turn guides them to the sorting tube. In order to fix this, a cap must be
placed that catches nuts falling at the top and guides them to the exit.

## Constraints

| Subject  | Constraint                                                                            |
|----------|---------------------------------------------------------------------------------------|
| Size     | The inner diameter should at least be the outer diameter of the exit holes outer path |
| Mounting | The cap should be easy to mount and adjust                                            |
| Bolts    | The outer diameter should not touch the bolts or nuts from the stopper roller wheels  |

## Summary

A circular cap, fixed in position to the frame with a small distance to the drum
to allow for wobble. It is connected to a custom bracket using the 3 holes on
the back wall. It is large enough to encapsulate the outer rotation of the exit
holes, so all nuts falling in roll down towards the main guide rail.

## Decisions

- **Size:** The inner diameter is based on the inner diameter of the abrasive
  drum, this makes it impossible for it to block.
- **Mounting:** 3 holes in the backplate to allow for mounting the catching drum
  to a custom bracket on the frame.
- **Bolts:** A wall thickness of $3\text{ mm}$ on the entire perimeter provides
  enough strength to absorb deflection and the falling nuts, as well as enough
  room for the endstop roller wheel bolts. 