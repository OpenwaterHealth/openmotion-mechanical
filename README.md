# openmotion-mechanical

Mechanical engineering CAD files for the [Open-Motion](https://github.com/OpenwaterHealth) near-infrared optical blood flow imaging platform — an open-source system for non-invasive cerebral blood flow measurement.

This repository contains the mechanical design files for every physical enclosure and structural component in the Open-Motion hardware stack.

## Mechanical Package Index

Mechanical design packages are distributed as revisioned ZIP archives. Each archive contains the CAD models and supporting documentation for a specific mechanical assembly.

| Package | Assembly | Included Files |
|---------|----------|----------------|
| `700-00013-Rev3.zip` | Console, Motion, EP | STEP model of the benchtop console assembly |
| `700-00029-Rev2.zip` | Motion Strap Bundle, Motion, EVT2 | STEP model containing the head, torso, and arm strap assemblies |
| `700-00031-Rev3.zip` | Sensor Module, Motion, EVT2 | STEP model of the sensor module assembly |
| `300-00245, Strap Frame, Motion Rev-1.zip` | Strap Frame, Motion | STEP model together with release documentation |

### Revision Naming

Mechanical packages use the following naming convention:

```
<Part Number>-Rev<Revision>.zip
```

For example:

```
700-00031-Rev3.zip
```

where:

- **700-00031** identifies the mechanical assembly.
- **Rev3** identifies the released revision.

Unless otherwise noted, the highest revision number is the most recent released revision in this repository.

## System Components

The mechanical designs in this repository support the complete Open-Motion hardware platform, including:

- Benchtop console
- Wearable sensor module
- Strap assemblies
- Structural hardware
- Mechanical fixtures

## Repository Organization

Each ZIP archive may contain one or more of the following:

- STEP models (`.step`, `.stp`)
- STL files (`.stl`)
- PDF drawings
- Manufacturing documentation
- Release documentation

## Contributing

When contributing mechanical changes, please:

- Update CAD models as needed.
- Include revised drawings or supporting documentation.
- Preserve revision history where appropriate.
- Include rendered images or screenshots when they improve review.
- Document any manufacturing-impacting changes.

Please follow the OpenWater contribution guidelines before opening a pull request.

## License

See the repository LICENSE file.
