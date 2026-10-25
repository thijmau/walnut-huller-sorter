# Drum Exit Endcap Design

![Render of the part](../../../images/parts/abrasive-drum-exit-endcap.png)

## Problem

While the walnuts are being hulled, they are not allowed to fall out if they're
not yet free of their husk. A simple way to prevent this is by adding holes in
the endcap based on the median size of the walnut. For example, as described in
the [drum design document](../abrasive-drum.md):

> _"...Another study measures $26.99\text{-}38.03\text{ mm}$ as geometric mean
diameter[^gharibzahedi], which seems to align more with the walnuts from the
source tree this drum is designed for..."_

Based on the walnuts from the actual tree this machine is designed for, the
initial design diameter is fixed at $35\text{ mm}$, this is subject to change as
the sample size from the source tree increase and are more thoroughly studied.

## Constraints

| Subject    | Constraint                                                        |
|------------|-------------------------------------------------------------------| 
| Hole Count | Balance between strength and chances for the walnut to exit       |
| Guidance   | Walnuts should easily roll out if their size passes the threshold |

## Summary

Having the same shared properties of
the [endcaps summary](README.md#summary), while being modified with 8
circular holes of $\varnothing 35 \text{ mm}$. This gives the walnut 8 chances
per full rotation to exit the drum while being tumbled.

## Decisions

- **Hole Count:** 8 holes of $\varnothing35\text{ mm}$ in diameter to provide a
  nice balance between having almost no chance to exit in a full rotation
  (e.g. $\approx 4$) and thin wall spacing between the exits (e.g. $\approx12$).
- **Guidance:** A steeply angled chamfer in the inside of each hole to bring the
  path angle downwards, making it easier for the walnut to exit.

<!-- @formatter:off -->

[^gharibzahedi]: S.M.T. Gharibzahedi, S.M. Mousavi, M. Hamedi and F. Khodaiyan, "Engineering characterization of Persian walnut and its kernel (*Juglans regia* L.) for obtaining high quality produce," *Quality Assurance and Safety of Crops & Foods*, vol. 5, no. 2, pp. 145–156, 2013. doi:10.3920/QAS2011.0110. Table 1, p. 147.
