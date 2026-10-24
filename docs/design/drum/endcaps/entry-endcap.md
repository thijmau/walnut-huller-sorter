# Drum Entry Endcap Design Document

![Render of the part](../../../images/parts/abrasive-drum-entry-drive-endcap.png)

## Problem

The walnuts when in their husk should be able to enter the drum, but should
still be prevented from exiting back to where they entered from. While the drum
is rotating, it is possible that it could scuff against the hopper entry, so
margin is required to prevent this. Furthermore, it should drive the drum using
a large pulley, which should be easily swappable.

## Constraints

| Subject         | Constraint                                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| 
| Entry Hole Size | Account for the [hopper](../hopper) outlet size of $\varnothing 140mm$, while preventing scuffing                                                        |
| Pulley Size     | The pulley should stay within the outside diameter described in [endcaps](./README) (_including belt_) to prevent rollers or dirt from damaging the belt |
| Changeability   | Allow for easy swapping of the pulley to the flange mount in case of damage or gearing changes                                                           | 
| Manufacturing   | Do not require supports when manufacturing                                                                                                               |

## Summary

Having the same shared properties of
the [endcaps summary](README.md#summary), while being modified with a large
concentric hole of $\varnothing 145\text{mm}$ in diameter. This allows for more
margin to prevent scuffing the hopper outlet. The endcap consists of two parts,
which are bolted together to allow for easy serviceability, and allow for
printing without supports.

## Decisions

- **Entry Hole Size:** Having a total margin of $5\text{mm}$ on the diameter,
  resulting in a hole size of $145\text{mm}$ in which the hopper output should
  be concentrically aligned.
- **Pulley Size:** The pulley size should be no more
  than $\varnothing240\text{mm}$ in diameter, giving $\approx 5\text{mm}$ margin
  on either side of the pulley for the belt. Given that the tooth count is
  variable, the pulley outer diameter should be
  between $\varnothing160\text{-}240\text{mm}$
- **Changeability:** The pulley is mounted to the flange mount using a different
  set of 6 holes, which are offset between the main mounting holes to the drum
  flange. This allows for easy swapping of the pulley in case of wear.
- **Manufacturing:** The entire endcap is printed in two parts, the "Flange
  Mount" and the "Pulley", which are mounted together as described previously.
  This allows both parts to lay flat and don't require support when printing.
