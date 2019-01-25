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
* Parts and airwire (electrical placeholder) connections are imported from
  schematic.
* Make sure that you set [Design Rules](../Resources/BME_in_house.dru)
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
  + `[t/b][Place/Name/Value]`: top/bottom, component placement / name / value
    silkscreens
  + `Holes`: mounting points, etc.
  + Lots of other layers used for board fabrication
* Set board's physical dimensions
* Use `Ratsnest` to reduce airwire segment lengths.
* Make large ground planes for easy connections, noise rejection and heat
  dissipation.
  + Create a shape that outlines this plane.
  + Name the object `GND`, which will connect it to the `GND` net.
* Set netclass parameters (these should default to your `Design Rules`):
  + Trace width (12 mil)
  + Drill width (20 mil)
  + Clearance (12 mil)
  + These parameters are based on fabrication resolution, power, interference,
    etc.
* Single sided boards are far easier to fabricate than double sided boards. Use
  a double sided board only when complexity or noise immunity requires it. 
* Since our holes/vias are not plated through, consider this when routing.
  + Single sided boards with through-hole components should have copper on the
    bottom side and components on the top side. 
  + Large packages, such as switches and DIPs ("chips") make it very difficult
    to solder on the component side. Consider routing only to the bottom side
    to connect to these large packages.
* Single sided boards can have surface mount components on the "bottom" and
  through-hole components on the "top". 
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
