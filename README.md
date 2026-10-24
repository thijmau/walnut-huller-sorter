# Walnut Huller & Sorter Machine

> [!NOTE]
> This project is currently a work in progress and is not yet validated by a
> complete build.
> Many files are also not yet populated, so some references may be broken, this
> will be fixed in due time.

This machine is a small walnut huller and sorter, featuring a rotating abrasive
drum, an air sorter and a dump flap. It is portable due to the size and caster
wheels, making it easily stored in a shed.

![Render of the machine in its current state](docs/images/machine-render.png)

> [!WARNING]
> **Not certified!** This machine does not possess any CE, UKCA, FC or UL
assessment, nor is it planned as of now. Whoever builds this machine is its
manufacturer and is responsible for its safety and compliance, including a risk
assessment, guarding, an emergency stop and the electrical installation.
>
> See the [safety manual](./docs/manuals/safety-manual.md) for more information.

## Background

My family has a large walnut tree for decades. It drops a lot of walnuts
every year. Hulling and sorting them by hand works, but is quite a slow and
tedious process. While commercial machines exist, they are either expensive,
built for mass production rather than a single tree, and/or rarely do both jobs
at once.

So I am trying to design a small machine that is trying to do both, built on the
same principles used commercially or in science. The nuts are for our own use;
the machine is meant to save us the work, and building it is a way to sharpen my
engineering skills.

## How it works

1. **Automated hulling:** The walnuts continuously tumble in a perforated
   stainless steel drum and are sprayed with water. This combination causes the
   husk to abrade and thus allows the hulled walnut to pass through the holes to
   get to the sorting system.
2. **Air sorting:** After being hulled, the nuts drop into a vertical pipe
   through a sidepipe. This vertical pipe has air rising through it as a high
   speed, causing waste and fragments to get sucked out, while healthy nuts fall
   straight down into a collection sack or bin.
3. **Periodic/controlled dumping:** At a configured interval or when the button
   is pressed, the machine stops and the dump flap opens to let the waste fall
   into a different sack or bin below the hopper.
4. **Easy composting:** During the hulling process, the waste and pulp falls
   down into a designated box. As well as the separate sack/bin for fragments as
   described in step 3. This makes it convenient to handle the waste products
   created by using this machine.

## Structure

```
[root] (walnut-huller-sorter/)
├── mechanical             # Contains parts and assembly files
│   ├── cad                # Fusion 360 (.f3d, .f3z) and STEP
│   ├── fabrication        # Fabrication files (e.g. cutting sheet metal)
│   └── stl                # Print files for slicing
├── distribution-panel     # Schematic for mains wiring
├── control-panel          # Schematic for machine control (.gbr, .drl, etc)
├── firmware               # Firmware source code for the MCU
├── docs                   # Relevant documents for the machine
│   ├── datasheets         # Datasheets of relevant parts
│   ├── design             # Design decisions and calculations
│   ├── drawings           # Technical drawings
│   ├── images             # Renders and photos
│   ├── manuals            # Assembly, use, safety
│   └── stickers           # Safety stickers (SVG)
├── LICENSES               # Full license texts
├── bom.csv                # Bill of materials
├── LICENSE                # Licensing overview
└── REUSE.toml             # Per-path license mapping
```

## License

This project is source-available, not open source. See the full
[`LICENSE`](LICENSE) for more details.

- Hardware and docs:
  [CC BY-NC-SA 4.0](./LICENSES/CC-BY-NC-SA-4.0.txt).
- Firmware:
  [PolyForm Noncommercial 1.0.0.](./LICENSES/PolyForm-Noncommercial-1.0.0.txt)

> [!NOTE]
>  **Building one for your own use or business is allowed; selling machines,
kits, parts or files is not.**