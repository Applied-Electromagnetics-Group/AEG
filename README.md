# AEG
Summary of software in the Applied Electromagnetics Group

This is a living document used for establishing standards and providing an overview of software development in the AEG.

## Table of Contents
2. [Code Structure](#code-structure)
3. [Development Cycle](#development-cycle)
4. [Git](#git)
5. [Tooling](#tooling)

# Code Structure
The code base is split between repositories to aid in compartmentalizing design.
| Repository    | Description  | Status | Lead | Source | Badge |
| ------------- |:-------------|:------:|:------:|:------:|:-----:|
| [AEG](https://github.com/Applied-Electromagnetics-Group/AEG)              | This repository        | Alive | @b-besler | Open | |
| [disperso](https://github.com/Applied-Electromagnetics-Group/disperso)              | Simulate time delay measurements through breast tissues.        | Alive | @besler | Closed | [![ci](https://github.com/Applied-Electromagnetics-Group/disperso/actions/workflows/ci.yml/badge.svg)](https://github.com/Applied-Electromagnetics-Group/disperso/actions/workflows/ci.yml) |
| [MicrowaveTomography](https://github.com/Applied-Electromagnetics-Group/MicrowaveTomography)            | Algorithms for microwave tomography.     | Alive | @b-besler | Closed | [![ci](https://github.com/Applied-Electromagnetics-Group/MicrowaveTomography/actions/workflows/ci.yml/badge.svg)](https://github.com/Applied-Electromagnetics-Group/MicrowaveTomography/actions/workflows/ci.yml) |

## Development Cycle
The purpose of the development cycle is traceability with efficiency.
If an issue happens, we can establish which line of code is wrong, who approved the code, and establish processes for preventing such issue in the future.
We can work more efficiently with such systems since we spend less time chasing our tails.

1. Create a branch
  * `git checkout master && git pull`
  * Name branch by last name and a short description, camel case. `git checkout -b LastName/ThisIsADescription`
2. Create a pull request
  * Describe the details of the changes.
  * Have @b-besler review before merging.
3. Rebase into master 
  * Tests must pass, master must never break
4. Delete branches

## Git
* **Present tense** Commits should be in the present tense (e.g. `Fix off by one error`, not `Fixed off by one error`)
* **Do not push to master** If you push to master, your friends will make fun of you.
* **master, not main** Do not rename `master` to `main`. The wiring in some brains is so corroded that making the switch may turn off the system.
* **Named branches** Branches should be named `YourLastName/ThisIsADescription`.

## Tooling

### Text Editor
You may use whatever text editor you please.
Some use Vim, others VSCode.
However, please do not commit files that save editor preference to the code base.

### Git
You can use the command line interface or a graphical interface of your pleasing so long as you follow the development cycle.
On Windows, Git Bash is recommended when using command line interfaces.

We recommend the resources at [try.github.io](https://try.github.io/) if you are not familiar with git.
The minimum required capabilities include using the following: `add`, `commit`, `branch`, `checkout`, `pull`.

