# Design Skills Project (Variable Blinking Light) [Spring 2019]

## Functional Specifications
* Switch to turn device on/off.
* LED light that has a blinking rate from 1-"60" (continuous) Hz, adjusted by a rotating knob / slider.
* Battery must be easily replaceable

## Constraints
* Run on battery power
* Single-sided printed circuit board
* Cannot weight more than 0.5 lb
* Cannot have a single dimension > 3 in
* Bill-of-materials <= $20 to duplicate unit

## Extra credit possibilities:
  + Battery life indicator
  + Waterproof enclosure
  + You tell us!

## Grading
* Save all [E]CAD files and associated design documentation in Box directory
  under your Net ID (i.e., `LightBox/$NETID`) with the following heirarchy:
  + `Mechanica/` (exported Fusion or SolidWorks files)
  + `Electrical/` (Eagle or Design files)
  + `Testing/` (testing data)
  + `Docs/` (component spec sheets, block diagrams, functional decomposition)
* Grading Criteria (0-5 point scale for each item)
  + Mechanical
    - PCB securly mounted in enclosure
    - LED light visible through enclosure (light pipe)
    - Switch securely mounted and accessible
    - Knob securely mounted and accessible
    - 3' drop test survival
    - Battery access
    - Secure pieces of enclosure
    - Aesthetics / ergonomics / user interface
    - Minimize weight
    - Minimize size
  + Electrical
    - Functional design
    - Functional PCB
    - Turns on/off
    - Blinks at full range of specified operation
    - Single-sided board routing efficiency
    - Good PCB design practices (e.g., trace widths, pad sizes, generous `GND` planes)
    - Minimized components
    - Maximized runtime / battery life
    - Headers when appropriate
  + Electronic design history