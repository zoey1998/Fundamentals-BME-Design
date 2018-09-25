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

* Create a new repository for this project, and add Dr. Palmeri (`mlp6`) as a
`Collaborator`.

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
