# openmotion-mechanical

Mechanical engineering CAD files for the [Open-Motion](https://github.com/OpenwaterHealth) near-infrared optical blood flow imaging platform — an open-source system for non-invasive cerebral blood flow measurement.

This repository contains the mechanical design files for every physical enclosure and structural component in the Open-Motion hardware stack.

## System Components

Open-Motion has two major mechanical assemblies:

```
┌─────────────────────────────────┐
│           Console               │  ← Benchtop unit
│  ┌───────┐ ┌───────┐ ┌──────┐  │
│  │ Laser │ │ Power │ │Control│  │
│  │       │ │Supply │ │  PCBs │  │
│  └───────┘ └───────┘ └──────┘  │
└────────────────┬────────────────┘
                 │  cable
┌────────────────┴────────────────┐
│     Patient-Applied Part        │  ← Wearable sensor headset
│  ┌──────────────────────────┐   │
│  │  Sensor array + laser    │   │
│  │  output optics           │   │
│  └──────────────────────────┘   │
└─────────────────────────────────┘
```

**Console** — The benchtop enclosure housing the laser source, power supply, and control circuitry (PCBs). Connects to the patient-applied part via cable and to the host PC via USB-C.

**Patient-Applied Part** — The wearable component that contains the array of near-infrared camera sensors and the laser output optics. Applied to the patient for blood flow measurement.

## Repository Structure

```
openmotion-mechanical/
├── 700-00013-Rev3.zip       # Mechanical design package (~14 MB)
├── 700-00029-Rev2.zip       # Mechanical design package (~29 KB)
├── 700-00031-Rev3.zip       # Mechanical design package (~6 MB)
├── LICENSE                  # AGPL-3.0
└── README.md
```

### Part Number Convention

| Prefix | Type | Description |
|--------|------|-------------|
| `700-xxxxx` | Mechanical design package (.zip) | CAD files (STEP, STL), drawings, and assembly documentation |

> **Note:** Open-Motion is in active development. Files in this repository represent prototype designs. Updated mechanical files are published here when major releases occur.

## File Formats

Zip archives may contain any combination of the following:

| File Type | Contents | Software |
|-----------|----------|----------|
| `.step` / `.stp` | 3D CAD models (universal exchange format) | [FreeCAD](https://www.freecad.org/), Fusion 360, SolidWorks, OnShape |
| `.stl` | 3D printable mesh files | Any slicer (PrusaSlicer, Cura) or CAD viewer |
| `.pdf` | Engineering drawings and assembly documentation | Any PDF viewer |
| `.dxf` / `.dwg` | 2D drawings and laser-cut profiles | [LibreCAD](https://librecad.org/), AutoCAD, FreeCAD |

## Related Repositories

This repo contains the mechanical designs. The rest of the Open-Motion platform lives here:

| Repository | Description |
|------------|-------------|
| [openmotion-electrical](https://github.com/OpenwaterHealth/openmotion-electrical) | PCB schematics and manufacturing files for all boards |
| [openmotion-console-fw](https://github.com/OpenwaterHealth/openmotion-console-fw) | Console board firmware |
| [openmotion-bloodflow-app](https://github.com/OpenwaterHealth/openmotion-bloodflow-app) | Blood flow imaging application |
| [openmotion-test-app](https://github.com/OpenwaterHealth/openmotion-test-app) | QML-based hardware test application |
| [openmotion-camera-fpga](https://github.com/OpenwaterHealth/openmotion-camera-fpga) | Camera FPGA design files |
| [openmotion-ta-fpga](https://github.com/OpenwaterHealth/openmotion-ta-fpga) | Timing/aggregator FPGA design files |
| [opw_bloodflow_gen2_ai](https://github.com/OpenwaterHealth/opw_bloodflow_gen2_ai) | Deep learning blood flow classification model |

## Getting Started

**To view 3D models:** Extract the zip archives and open `.step` files in [FreeCAD](https://www.freecad.org/) (free, open-source), Fusion 360, or your preferred CAD application.

**To 3D-print components:** Import `.stl` files (if included) into your slicer software.

**To review engineering drawings:** Open the PDF drawings included in the zip archives.

**To integrate with electrical designs:** See the [openmotion-electrical](https://github.com/OpenwaterHealth/openmotion-electrical) repository for PCB 3D models (STEP) that align with these enclosures.

## Contributing

We welcome contributions from the mechanical engineering community. Please read our [Contributing Guide](https://github.com/OpenwaterHealth/.github/blob/main/CONTRIBUTING.md) before submitting changes.

For mechanical contributions specifically:

- **CAD changes** — export universal formats (STEP) alongside native source files
- **New revisions** — increment the revision number following the existing convention (e.g., `700-00013-Rev3`)
- **Assembly documentation** — include updated drawings when modifying component geometry

## License

This project is licensed under the [GNU Affero General Public License v3.0](LICENSE) (AGPL-3.0).

## About Openwater

[Openwater](https://openwater.health) is building open-source platforms to democratize medical imaging and neuromodulation technology — reducing medical device development costs through collaborative, open-source engineering.
