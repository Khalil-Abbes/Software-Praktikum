# Implementation Phase
 
## Project Context
This repository contains the implementation phase deliverables for "Saardew Valley," an organic farming simulation. The project required building a fully functional, deterministic simulation engine in Java based on our previous design. It features JSON parsing, pathfinding, plant growth cycles, weather simulations, and incident handling, alongside a rigorous testing suite designed to achieve high coverage and defeat injected codebase mutants.

## Tech Stack
* Java
* JUnit (Unit, Integration, and System Testing)
* Detekt (Code Quality Analysis)
* Generative AI tools for configuration/boilerplate automation

## My Contributions 
During the implementation phase, I served as a core developer with a heavy focus on the map infrastructure, parsing logic, and complex system testing.

### Core Implementation
* **Map Parser & Tile Factory:** Implemented the `MapParser` to read and strictly validate JSON configurations. Developed the `TileFactory` and associated helper methods (`createMeadowTileFromJson`, `createForestTileFromJson`, etc.) to instantiate the simulation map.
* **Cross-Validation Logic:** Wrote extensive validation methods (`validateTileProperties`, `validateTileFields`, `validateAdjoiningTiles`) to ensure map integrity, including enforcing boundary rules, valid plant types for fields/plantations, and machine-to-farmstead constraints.
* **Coordinate & System Registration:** Implemented translation logic to map coordinates to tiles, set up directional logic (`validateDirection`), and integrated machine action systems into the broader simulation.
* **Code Restructuring:** Led the restructuring of the codebase during development, converting public methods to private where appropriate, and automating the creation of configuration files to speed up team testing.

### Testing & Debugging
* **System & Integration Testing:** Designed and implemented massive, complex system tests (e.g., "Cloudzilla") to validate the entire simulation lifecycle under stress. 
* **Validation Tests:** Wrote specific test suites covering adjoining tiles, machine actions on small/medium maps, swapped machines, city expansion incidents, and harvest estimations.
* **Debugging:** Conducted extensive debugging on cloud integration, farm behaviors (e.g., sowing empty fields), and resolved consistency issues across the simulation ticks.
