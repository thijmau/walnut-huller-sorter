# Hopper Design Document

![Render of the part](../../images/parts/hopper.png)

## Problem

When people want to deposit walnuts into the drum, it would be unintuitive to
just throw them into it, due to the water sprayer and the entry cap being in the
way. A hopper allows for a larger area, this make it easier to guide walnuts
into the drum. Another advantage is that it provides some extra room as a buffer
in case the drum starts to get fuller, and it could also restrict flow.

## Constraints

| Subject       | Constraint                                                                      |
|---------------|---------------------------------------------------------------------------------|
| Size          | The husks should not be blocked by the water pipe in the center                 |
| Buffer        | Allow for a few dozen of husks to be deposited at once                          |
| Mounting      | The hopper should be mounted to a bracket to allow adjustment or replacement    |
| Manufacturing | It should minimize support usage while printing                                 |
| Plumbing      | The center of the hopper should provide room for the center water spraying tube | 

## Summary

A two-part assembly based on a large trapezoidal hopper, which goes to a
shallower joint to constrict the flow. It then goes into the output tube, which
provides enough room for the husks to go around the center water spraying tube.
The two parts are mounted together using bolts, and printed separately. It is
mounted to the frame using a custom bracket by connecting it to the 4 holes at
the back.

## Decisions

- **Size:** Given a water sprayer diameter of $\varnothing16\text{ mm}$, this
  should allow husks to not get blocked all sides. Using a maximum diameter
  of $60\text{ mm}$ for the fruits[^treesandshrubs], this results in an inner
  diameter of:
  $$
  D_\text{outer} \geq 2\left (60\text{ mm} + \frac{16\text{ mm}}{2}\right)
  = 136\text{ mm}
  $$
- **Buffer:** The buffer should provide additional room for the husks to stay
  while the hopper is unloading. This is done by basing the tangential
  connection on about half the output diameter, and a trapezoidal expansion
  upwards to allow a smooth transition to the larger input area.
- **Mounting:** 4 holes at the back of the output to allow for a custom bracket
  to mount to the hopper assembly.
- **Manufacturing:** Split the hopper assembly into two parts, a trapezoidal
  buffer which can be mounted using 4 countersunk bolts to the hopper output.
  This allows for easier printing, because the shape would be too complex to
  print in one go.
- **Plumbing:** A $\varnothing20\text{ mm}$ hole in the center of the output to
  provide margin for the tube to pass through.

<!-- @formatter:off -->

[^treesandshrubs]: [“Juglans regia”](https://www.treesandshrubsonline.org/articles/juglans/juglans-regia/), *Trees and Shrubs Online*.
