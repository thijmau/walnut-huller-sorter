# Abrasive Drum Design

## Problem

The walnuts fall from the tree in their green, pulpy and protective husks,
these—of course—are not meant for direct consumption. Before the actual walnut
inside can be collected, the husk has to be removed. This is a repetitive and
tedious process if done by hand.

In order to solve this problem efficiently, commercial walnut-hulling machines
solve this problem by tumbling the nuts. This is done primarily using either
rotating or rolling drums[^nutmec]. However, these machines are large and costly
for low-volume usage.

## Constraints

When developing this part, there are some constraints that could limit or impact
development decisions. See the table below:

| Subject           | Constraint                                                                               |
|-------------------|------------------------------------------------------------------------------------------|
| **Mounting**      | An easy way to connect and remove the drum to caps for maintenance                       |
| **Material**      | Resistance to water, rain, rust and corrosion                                            |
| **Manufacturing** | Relatively simple to manufacture (e.g. without requiring 5-axis CNC machines)            |
| **Rotation**      | Allow rotation, while allowing a water spray pipe through the center                     |
| **Flow**          | Walnuts should move towards the exit on their own while tumbling                         |
| **Volume**        | Require enough space for walnuts to tumble, but too much and they don't abrade eachother |
| **Abrasion** | Holes assisting the abrasion cannot catch walnuts, but too small and they don't abrade |


## Summary

The walnuts will abrade in a perforated stainless steel tube
of $\varnothing 200\,\text{mm} \times 350\,\text{mm}$. Using a wall size
of $1.5\text{mm}$, this gives it an inner volume of 10.7 liters.

$$
\begin{aligned}
d_\text{o} &= 200\,\text{mm} \\
d_\text{i} &= d_\text{o} - 2 \times 1.5\,\text{mm} = 197\,\text{mm} \\
V_\text{inner} &= \frac{\pi}{4} d_\text{i}^2 \times 350\,\text{mm} \approx 10.67\,\text{L}
\end{aligned}
$$

The diameter is sized so
that a single cross-section of the tube holds $\approx 3\text{–}4$ walnuts with
room to tumble. Based on them having a geometric mean diameter
between $60\text{-}80\text{mm}$[^vdberk].

Dehulled in-shell walnuts measure $35.7\text{-}45.9\text{mm}$ in geometric mean
diameter across ten cultivators[^ercisli]. Another study
measures $26.99\text{-}38.03\text{mm}$ as geometric mean
diameter[^gharibzahedi], which seems to align more with the walnuts from the
source tree this drum is designed for. This allows for enough tumbling room
for $\approx 6\text{-}7$ walnuts in the same cross-section when they are
gradually hulled.

Although, the sample of nuts from the source tree seem to
have a smaller overall geometric mean diameter, but the sample size is currently
too small to conclude and might require a manual study.
<!-- TODO: Provide actual measurements of nut samples from source tree -->

## Decisions

- **Mounting:** Six bolts and nuts in the flange on either ends, connecting
  endcaps to the drum.
  <!-- TODO: link to endcaps -->

- **Material:** Due to the hygienic, corrosion-resistant, food-grade and smooth
  properties of stainless steel[^ulbrich], it is the obvious choice for
  this project.
- **Manufacturing:** Made from sheet metal, since this easily allows a pattern
  to be cut into the metal. It is then rolled into a cylindrical shape and
  welded along the seam to form a tube.
- **Rotation:** The drum should rotate on rollers, since doing it via an
  internal axis is impossible due to that location being reserved for the hopper
  and water sprayer. It rolls on the tangential faces of the endcaps.
  <!-- TODO: link to endcaps and rollers -->
- **Flow:** Angle the drum slightly, e.g. 5-7 degrees, to find a good balance
  between abrasion and travel speed. Too high and it clogs, too low, and they
  don't move towards the exit.
- **Abrasion:** 8mm perforation holes spaced diagonally across the entire tube, this is subject to change based on experiments. 

<sub>An alternative is to just print the tube directly upright, but due to
Z-layer seams/weaknesses and porous properties of FDM this is definitely not the
best option and highly discouraged.</sub>

[^ercisli]: Ercisli, S., Sayinci, B., Kara, M., Yildiz, C., & Ozturk, I. (2012). Determination of size and shape features of walnut (*Juglans regia* L.) cultivars using image processing. *Scientia Horticulturae*, *133*, 47–55. [https://doi.org/10.1016/j.scienta.2011.10.014](https://doi.org/10.1016/j.scienta.2011.10.014)

[^gharibzahedi]: S.M.T. Gharibzahedi, S.M. Mousavi, M. Hamedi and F. Khodaiyan, "Engineering characterization of Persian walnut and its kernel (*Juglans regia* L.) for obtaining high quality produce," *Quality Assurance and Safety of Crops & Foods*, vol. 5, no. 2, pp. 145–156, 2013. doi:10.3920/QAS2011.0110. Table 1, p. 147.

[^nutmec]: Nutmec, [Walnut Huller Machines](https://nutmec.com/product-category/processing-machines/for-nuts/hulling/walnut-huller-machines/). Product catalog illustrating commercially available walnut-hulling machinery.

[^ulbrich]: Ulbrich, [Why Stainless? Its Benefits and Unique Characteristics](https://www.ulbrich.com/blog/why-stainless-its-benefits-and-unique-characteristics/). Overview of the properties and benefits of stainless steel.

[^vdberk]: Van den Berk Nurseries, [Juglans regia – Common walnut](https://www.vdberk.com/trees/juglans-regia/) Product description and Specifications table ("Fruits").
