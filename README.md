# Ruka: Raspberry Pi camera stand

A 3D-printed articulated arm that holds a **Raspberry Pi camera module**. It has a base, a base-to-arm connector, two arm links, and a camera mount with a joiner. It was designed in SolidWorks and printed on a FlashForge printer in August–September 2021.

## Files

| Path | What |
|---|---|
| `mechanical/cad/Ruka_V1.SLDASM` | Top-level SolidWorks assembly (originally saved as `Pi_Cam_Assembl_V1`) |
| `mechanical/cad/parts/*.SLDPRT` | `Base`, `Arm_To_Base_Connector`, `Arm_Main`, `Arm_2`, `Mount_For_Camera`, `Mount_Joiner` and `Mounts` |
| `mechanical/exports/stl/*.STL` | Print-ready parts: 1 base, 1 connector, **2 × Arm_Main**, 1 Arm_2, **2 × Mount_For_Camera**, 1 camera-mount joiner |
| `mechanical/cam/*.fpp` | FlashForge **FlashPrint** projects with the print settings for the arm, the connector and base, and the camera mount |

## Printing and assembly

1. Print everything in `mechanical/exports/stl/` (8 parts). Open the `.fpp` files in FlashPrint to reuse the original orientation and settings.
2. Join the links at their pivot holes; the assembly file shows how the parts go together.
3. Mount the Raspberry Pi camera board on `Mount_For_Camera`.

## Notes

- The assembly references a part named `Camera_Mount_Joiner.SLDPRT`. The file in this repo is named `Mount_Joiner.SLDPRT`, so SolidWorks may ask you to locate it the first time you open the assembly; point it at `parts/Mount_Joiner.SLDPRT`. The exported STL (`… Camera_Mount_Joiner-1.STL`) is complete either way.
- Fastener sizes weren't recorded in the CAD. Check the hole diameters in the parts before buying hardware.
