# Design

This folder contains all the different design decisions made throughout this
project. These include (but are not limited to) material choices, engineering
calculations, manufacturing methods, and design considerations.

All plastic parts are based on injection-molded ABS plastic, this has two
advantages:

1. This gives more margin if parts end up lighter, thus giving less strain to rotating parts such as rollers, coasters or motors. 
2. Fusion directly exports mass based on this property, so you won't have to put each part into the slicer and account for an optimal infill.

The files are categorized based on their main function within the machine. See the following layout:

```
design/ (this directory)
├── drum/                 # All design relevant to the rotational drum
│   ├── abrasive-drum.md  # Specifications of the drum itself
│   └── ...               # Other relevant files such as endcaps or rollers
│
├── waste/                # All design relevant to waste management
│   ├── flap.md           # Specifications of the dump flap 
│   └── ...               # Other relevant files such as weights or gaskets
│ 
└── sorting/              # All design relevant to the air-sorting mechanism
    ├── airspeed.md       # Calculations and physics e.g. regarding target airspeed
    └── ...               # Other relevant files such as duct size or bellmouth
```