# Introduction to Electronic Design Automation (EDA)

## Libraries
* Commercial part libraries that include component specifications and
  footprints.
* Can be downloaded from part suppliers if not included by default.
* Custom parts can be defined, but very cumbersome.
* Part libraries can also include 3D CAD definitions for integration in 3D
  renderings of boards with parts.

## Parts
* Good practice to place all parts on the schematic before trying to connect
  them.
* Choose a "clean" layout of parts.
* Assign part values and meaningful labels.

## Nets
* Nets are like nodes; common voltage connections.
* Avoid net connection chaos by using `GND` and `V*` remote connections.
* Use common net labels (with tags to easily visualize) to connect remote nodes
  without lots of crossing connections.
* Net connection tricks above keep the schematics clean and readable, but all
  connections are preserved when laying out your board.

## Miscellaneous
* Use scripts / macros to renumber components throughout the project, etc.
* Create Bill of Materials for all parts.

## Creating a Board
* Parts and airwire (electrical placeholder) connections are imported from schematic.
* Manually place components on the board, remember to rotate and orient
  components for an efficient layout, and group things to move them in bulk.
  *Board layout is an art form.*
* Vias: connections between top and bottom layers of a board.  We are dealing
  with either single- or double-sided boards.
* Layers: 
  + `Top`
  + `Bottom`
  + `Pads`
  + `Vias`
  + `[t/b][Place/Name/Value]`: top/bottom, component placement / name / value silkscreens
  + `Holes`: mounting points, etc.
  + Lots of other layers used for board fabrication
* Set board's physical dimensions
* Use `Ratsnest` to reduce airwire segment lengths.
* Make large ground planes for easy connections, noise rejection and heat dissipation.
  + Create a shape that outlines this plane.
  + Name the object `GND`, which will connect it to the `GND` net.
* Set netclass parameters:
  + Trace width (12 mil)
  + Drill width (20 mil)
  + Clearance (12 mil)
  + These parameters are based on fabrication resolution, power, interference, etc.
* Set auto-routing rules, run auto-router, and fix remaining issues (vias,
  connecting GND planes, etc.)
* Adjust individual hole diameters, trace widths, route underneath components,
  etc.
* Check design rules for warnings and errors.

## Online Resources
* **How to make a schematic:** https://www.youtube.com/watch?v=1AXwjZoyNno&t=1460s
* **How to create a PCB:** https://www.youtube.com/watch?v=CCTs0mNXY24
* **How to make Gerber files/DRC/etc:** https://www.youtube.com/watch?v=oId-h6AeXXE
* **Tutorial for Arduino Shield in Eagle:** https://www.open-electronics.org/how-to-make-an-arduino-shield-with-eagle-cad-tutorial/
* **Video Tutorial for Arduino Shield in Eagle (3 parts):**
    1.https://www.youtube.com/watch?v=_NjZxK3acMs
    2.https://www.youtube.com/watch?v=1bvSb_u0Pms&t=13s
    3.https://www.youtube.com/watch?v=ZS4cAgg-qQw
