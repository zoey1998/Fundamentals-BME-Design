# Introduction to Electronic Design Automation (EDA)

## Libraries
* Commercial part libraries that include component specifications and
  footprints.
* Can be downloaded from part suppliers if not included by default.
* Custom parts can be defined, but very cumbersome.
* Part libraries can also include 3D CAD definitions for integration in 3D
  renderings of boards with parts.
* Remember you may need to use a wildcard character (`*`) when searching for
  parts.

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
* Buses are collections of nets, used to organize connections that run together
  (primarily to aid visualization).

## Miscellaneous
* Use scripts / macros to renumber components throughout the project, etc.
* Use `ERC`!
* Create Bill of Materials for all parts.

## Creating a Board
* Create board from schematic so they are *linked*.
* Make sure that you set [Design Rules](../Resources/BME_in_house.dru) (`Edit -> Design Rules...`)
  + Trace width (12 mil)
  + Drill width (20 mil)
  + Clearance (12 mil)
  + These parameters are based on fabrication resolution, power, interference,
    etc.
* Change to `Single Layer Mode` (if single layer)
  + Single sided boards are far easier to fabricate than double sided boards.
  + Use a double sided board only when complexity or noise immunity requires
  it.
  + Single sided boards can have surface mount components on the "bottom" and
  through-hole components on the "top".
  + Design to solder thru-hole components on the "bottom" (other side of the
  board from the component body). You can move components to the other side
  of the board with the `Mirror` function.
* Set the board's physical dimensions.
* Parts and airwire (electrical placeholder) connections are imported from
  schematic.
* Manually place components on the board, remember to rotate and orient
  components for an efficient layout, and group things to move them in bulk.
  *Board layout is an art form.*
* Use the `Ratsnest` button to clean up airwires.
* Vias: connections between top and bottom layers of a board.  We are dealing
  with either single- or double-sided boards.
* Layers: 
  + `Top`
  + `Bottom`
  + `Pads`
  + `Vias`
  + `[t/b][Place/Name/Value]`: top/bottom, component placement / name / value
    silkscreens
  + `Holes`: mounting points, etc.
  + Lots of other layers used for board fabrication
* Make large ground planes for easy connections, noise rejection and heat
  dissipation.
  + Create a shape that outlines this plane.
  + Name the object `GND`, which will connect it to the `GND` net.
* Check design rules for warnings and errors.
* Create shapes for mounting holes, connections to enclosures, etc.

## Online Resources
* **How to make a schematic:** https://www.youtube.com/watch?v=1AXwjZoyNno&t=1460s
* **How to create a PCB:** https://www.youtube.com/watch?v=CCTs0mNXY24
* **How to make Gerber files/DRC/etc:** https://www.youtube.com/watch?v=oId-h6AeXXE
* **Tutorial for Arduino Shield in Eagle:** https://www.open-electronics.org/how-to-make-an-arduino-shield-with-eagle-cad-tutorial/
* **Video Tutorial for Arduino Shield in Eagle (3 parts):**
    1.https://www.youtube.com/watch?v=_NjZxK3acMs
    2.https://www.youtube.com/watch?v=1bvSb_u0Pms&t=13s
    3.https://www.youtube.com/watch?v=ZS4cAgg-qQw
