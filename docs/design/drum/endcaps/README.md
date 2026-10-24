# Drum Endcaps Design Document

This document contains information about the shared properties of the endcaps.
As described earlier in the [drum design document](../abrasive-drum.md), the
endcaps are mounted to the drum on its flanges using 6 bolts, washers and nuts
for each endcap.

Two variants exist for the endcaps, as described below:

1. An [entry endcap](./entry-endcap.md) through which the drum is driven and the
   hopper is mounted so that the nuts can enter the drum. It consists of two
   parts, one with a large hole for the hopper and a pulley for the belt. Which
   can be mounted together and allows for easy swapping of pulley size if
   applicable.
2. An [exit endcap](./exit-endcap.md) through which the hulled walnuts exit
   the drum if they have shrunk enough to pass through the allowed size. It
   keeps walnuts inside that have not yet passed that threshold.

The endcaps function as a large rolling surface for the drum. They both have an
extruded wall based on the width of the wheels from
the [rollers](../rollers.md), this makes it easy for the drum to roll, compared
to for example having a special steel surface fabricated for it.

## Problem

The walnuts should not fall out of either ends of the drum when they are being
processed, but it should still allow entry and exit based on specific
parameters.

## Constraints

| Subject       | Constraint                                                                                          |
|---------------|-----------------------------------------------------------------------------------------------------|
| Mounting      | Mounting pattern of 6 holes needs to match the drum flange PCD[^wiki-bolt-circle] of $225\text{mm}$ |
| Material      | Resistant to UV, rain, rust and corrosion                                                           |
| Tolerance     | Account for sheet metal warping or printing inaccuracies                                            |

## Summary

A circular endcap being $\varnothing250 \text{mm}$ in diameter,
with $0.4\text{mm}$ of expansion tolerance for the sheet metal flange. Bolted to
the drum flange using 6 countersunk holes to provide a seamless look and allow
for easy maintenance.

## Decisions

- **Mounting:** 6 clearance holes for countersunk bolts to provide seamless
  clearance (_e.g. compared to socket or button heads_).
- **Tolerance:** 0.4mm of tolerance to start with, which could be reduced if
  necessary.

<!-- @formatter:off -->

[^wiki-bolt-circle]: [“Bolt circle”](https://en.wikipedia.org/wiki/Bolt_circle), Wikipedia.
