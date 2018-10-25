# Prototyping Skills / Design Challenge

## Milestone 01
* Install a `git` client on your laptop.  Macs already have `git` available
through the `Terminal`, but you may want to use a GUI client.  There are
multiple options for this, including:
  + https://git-scm.com (will install a `Git Bash` environment)
  + https://desktop.github.com/
  + https://www.sourcetreeapp.com/
  + https://www.git-tower.com/
  + https://www.gitkraken.com/

Some of these clients are free, some are not; pick your poison.  You don't need
anything "fancy" to use git to its fullest potential.

* Setup an account on GitHub: https://github.com

* [**Optional**]  Setup an SSH key to seamlessly push/pull to/from your GitHub
repositories: https://help.github.com/articles/connecting-to-github-with-ssh/   

* Create a new repository for this project, and add Dr. Palmeri (`mlp6`) and
  Petek Sener (`ps178`) as `Collaborators`.

* Initialize your repository with a `README.md` file that is a copy of the
project description.  You'll be modifying this as your project evolves.

* Setup a `Project` Kanban board with the following columns:
  + `Backlog`
  + `To Do`
  + `In Progress`
  + `Done`
  + `Blocked`

Based on the project specifications and constraints, start populating your `Backlog`.

* It is recommended that you use the following directory structure to your repository:
  + `Mechanical/`
  + `Electronics/`
  + `Software/`
  + `Testing/`
  + `Docs/`

Note that you cannot create empty directories in git repositories, so you will
need to have some sort of a file in there as a placeholder, or simply create
the directories as they have relevant content.

* Get comfortable with git!  Here are a few resources:
  + Git lectures from [Medical Software Design](https://github.com/mlp6/Medical-Software-Design):
    - https://github.com/mlp6/Medical-Software-Design/blob/master/Lectures/GitFundamentals.md
    - https://github.com/mlp6/Medical-Software-Design/blob/master/Lectures/GitWorkflow.md
  + https://try.github.io/
  + https://www.codecademy.com/learn/learn-git
  + https://www.git-tower.com/learn/cheat-sheets/vcs-workflow
  + http://gitimmersion.com/
  + https://www.atlassian.com/git/tutorials/comparing-workflows#feature-branch-workflow
  + http://learngitbranching.js.org/

  If you have any problems with git, checkout the Duke Co-Lab Slack team:
https://colab.duke.edu/ .  We have a specific channel on there for `#git`.

## Milestone 02
* Sketch out a functional block diagram for your device.  Be sure to include:
  + What functional blocks require power.
  + Inputs / outputs from the device.
  + How you will achieve the different light settings, including the blinking.
* Sketch a physical design for your device, including:
  + Relevant approximate dimensions.
  + Mounting points for internal parts.
  + Access for battery.
  + Consider what aspects of the device need to be accessible to the user
during operation.

The physical design sketches can be done by hand (paper-and-pencil drawings) or
using CAD software (CAD software will ultimately be used, but can be slower
when generating initial designs).

## Milestone 03
* Commit a complete circuit schematic for your project as a PDF in the
  `Electronics/` directory of your GitHub repository for this project.  This
  can be done with pencil and paper and scanned / photographed at adequate
  resolution.
* Be sure to include all power connections, pull/up down resistors, bypass
  capacitors, voltage protection, etc. as needed.
* If you are using an MCU, then also include a software flowchart in the `Software/` directory.
* If you are not using an MCU, then please indicate the different functional
  blocks of your circuit design on your schematic.
* Create a git "release" named 'v0.1.0' when this is ready for review by Dr.
  Palmeri.  This can be done through the GitHub webpage
  (https://help.github.com/articles/creating-releases/) or can be done on the
  command line using the command like `git tag -a 'v0.1.0' -m 'milestone 03
  ready for review'`.  If doing this locally on the command line, be sure to
  push your tag to GitHub using the command `git push --tags`.  The version
  names are utilizing semantic versioning (can read more here:
  https://semver.org/).

*If at any point after initial submission you would like to make changes to
your design and then have those serve as your latest working version, simply
increment the `PATCH` (third) number of the released version.*

## Milestone 04
* Based on your feedback from Dr. Palmeri and your breadboard testing, submit
  your "final" electronic design, captured in your EDA program.  Be sure to
  commit PDFs of your circuit schematic and your PCB layout under `Hardware/`;
  include discrete component technical specification sheets under `Docs/`.
* If using an MCU, be sure to also commit your software.
* Tag / release this as `v0.2.0` when ready for review.
* Work with Matt Brown and your TAs to execute on fabricating your PCB.

## Milestone 05
* Submit PDFs of orthogonal 2D (mechanical drawings) and a 3D rendering of your
  mechanical design under the `Mechanical/` directory in your repository.  Tag
  / release this as `v0.3.0`.
* Work with Matt Brown and your TAs to 3D print / machine your design.

## Milestone 06
* Integrate your PCB and electrical components with your mechanical design.
* Start testing your device.

## Milestone 07
* Present your device to Dr. Palmeri sometime before the BME Design Symposium
  (schedule individual time with him).
* Include any testing data (`Testing/`) to support device performance
