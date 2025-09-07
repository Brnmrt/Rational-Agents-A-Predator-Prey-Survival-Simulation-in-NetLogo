# Rational Agents: A Predator-Prey Survival Simulation in NetLogo

## About The Project

This project, developed as part of the "Introduction to Artificial Intelligence" course, is a simulation of a 2D toroidal world inhabited by two types of agents: lions and hyenas. The primary objective for these agents is to survive for as long as possible by making rational decisions based on their perceptions of the environment. The simulation is built using NetLogo and explores the concepts of reactive agents, rational behavior, and environmental interactions.

This repository showcases the ability to design, implement, and analyze the behavior of autonomous agents in a competitive environment. It includes a base model with fundamental behaviors and an enhanced model with additional features like traps and reproduction, demonstrating a deeper understanding of agent-based modeling and AI principles.

### Built With

* [NetLogo](https://ccl.northwestern.edu/netlogo/)

## Features

### Environment
* **Dynamic World:** A 2D toroidal grid where agents and resources are located.
* **Food Sources:** Two types of food are available: small (brown cells) and large (red cells), with configurable spawn rates. Food sources are finite, with large food sources turning into small ones after being eaten once, and small food sources disappearing after consumption.
* **Resting Areas:** Blue cells are randomly placed in the environment, allowing lions to rest and recover energy.
* **Traps (Enhanced Model):** An optional feature where traps can be enabled, posing a threat to the lion agents.

### Agents & Behavior

#### Lion Agents
* **Reactive Behavior:** Lions are reactive agents that perceive their immediate surroundings to make decisions.
* **Complex Actions:** They can eat, move, turn, and engage in combat with hyenas.
* **Special Movement:** When a lion perceives two or more hyenas, it will execute a special movement to distance itself from the threat, with energy costs varying depending on the situation.
* **Prioritized Actions:** The lion's primary action is to eat when its energy is below a user-defined threshold; otherwise, its priority is to evade threats.
* **Combat:** A lion can kill a hyena if it's the only one in its perceived vicinity, turning the hyena into a small food source.

#### Hyena Agents
* **Reactive Behavior:** Hyenas also act as reactive agents, perceiving the cells immediately in front of them and to their sides.
* **Group Behavior:** Hyenas have a grouping level, which increases when they are near other hyenas. When the group level is greater than one, the hyena changes color.
* **Combat:** A group of hyenas (grouping level > 1) can kill a single lion in their perceived area, turning it into a large food source. The energy lost in combat is divided by the grouping level.
* **Movement Imposition:** A hyena can impose its direction of movement on other hyenas in its perceived neighborhood.

### Enhanced Model Features
* **Reproduction:** An optional feature that allows both lions and hyenas to reproduce if they have sufficient energy, adding another layer of complexity to the simulation.
* **Traps:** When enabled, traps reduce the energy of lions that step on them, affecting their survival rate.

## How To Get Started

To run this simulation, you will need to have [NetLogo](https://ccl.northwestern.edu/netlogo/) installed.

1.  Clone the repo
    ```sh
    git clone [https://github.com/your_username_/Project-Name.git](https://github.com/your_username_/Project-Name.git)
    ```
2.  Open the `IIA_TP1.nlogo` file in NetLogo.
3.  Use the interface to set the initial parameters for the simulation.
4.  Click the "Setup" button to initialize the world.
5.  Click the "Go" button to start the simulation.

## Analysis and Results

A series of experiments were conducted to analyze the agents' behavior under different conditions. The results, available in the `ResultadosIIA.xlsx` file, explore the influence of:
* Initial number of agents.
* Energy gained from food.
* Amount of food available.
* The presence of traps.
* The ability of agents to reproduce.

These experiments demonstrate a systematic approach to testing hypotheses and drawing conclusions based on the simulation data. For a detailed analysis, please refer to the `Relatorio_IIA.pdf` document (in Portuguese).
