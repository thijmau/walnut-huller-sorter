# Rollers Design Document

![Render of the part](../../images/parts/abrasive-drum-rollers.png)

## Problem

Because the drum cannot have a center axis, it should rotate on its outside
faces, which are provided by the [endcaps](endcaps/README.md). Furthermore, the
drum should be slightly angled to allow gravity to guide the nuts towards the
exit. This introduces another problem, where the drum wants to slide off the
same rollers guiding it, so stopper rollers at the end should prevent it from
doing so, while not limiting its rolling abilities.

## Constraints

| Subject        | Constraint                                                                                  |
|----------------|---------------------------------------------------------------------------------------------|
| Contact Points | The drum should not be imbalanced or roll/slide off                                         |
| Servicability  | Do not lock the drum in its place, it should be free rolling                                |
| Friction       | Do not provide significant restriction to the rolling abilities                             |
| Angle          | Provide enough angle over the length to allow gravity to guide the walnuts towards the exit |
| Mountability   | Allow for removable and accessible mounting                                                 |
| Wear           | Take into account that water or debris could enter the wheel axis                           |

## Summary

Four symmetric pillars, angled at $\angle30^\circ$ from the vertical axes, based
on the outer diameter of the flange of $\approx \varnothing 250 \text{ mm}$.
While having two endstop rollers (one on each side of the lower pillar) to
prevent the drum from sliding off while its rolling. The wheels
are $\varnothing40\text{ mm}\times14\text{ mm}$, with a max load of $30\text{kg}$
per wheel, which provides more than enough margin.

## Decisions

- **Contact points:** Because of two endcaps, the drum allows for two locations
  where rollers could be connected. Two wheels on each side of the
  flange—totaling four—is the most obvious choice here. For example, if you do
  another middle roller tangentially lower in the middle, a manufacturing or
  alignment error could cause the drum to wobble. While one on each side causes
  the drum to align itself perfectly.
- **Serviceability:** The rollers are easily replaced by removing the bolt and
  nut, and the drum is simply placed on top of the rollers and rolls freely.
- **Friction:** With a PE/PU tire surface, it allows for slight
  deforming when a load is applied, thus increasing contact patch. While this in
  theory does increase the friction, its considered negligible because of the
  bearing rolling resistance as well as the max load of 30kg per wheel, of which
  the drum is only a very small portion. PVC wheels for example could cause
  slipping due to their rigidity.
- **Angle:** As described in the [drum design document](./abrasive-drum.md), the
  drum should be slightly angled. The starting angle is $\angle 5^\circ$ from
  the horizontal axis. If this proves to be too little to overcome the guiding
  hump on the [exit endcap](./endcaps/exit-endcap.md), then this angle can be
  increased accordingly.
- **Mountability:** Two deeply recessed holes in each pillar, which allows the
  pillar to be mounted to its target surface using a nut. This allows for water
  to be trapped there, but drainage holes are also an option.
- **Wear:** The wheels are supported by 2RS[^bds-bearing-guide] graded bearings,
  which minimizes outdoor damage to the rolling abilities.

<!-- @formatter:off -->

[^bds-bearing-guide]: [“Bearing Seals Explained: Types, Functions, and Selection Guide”](https://www.bdsbearing.com/blog/guide-to-bearings-seals-types-functions-and-applications), BDS.
