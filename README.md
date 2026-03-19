# Protease2-Following

**Headline:** A Swarm Algorithm for Following Formations using Crazyflie Drones

This repository serves as a hub for supplementary materials related to the paper *A Swarm Algorithm for Following Formations using Crazyflie Drones*. It includes the prototypical implementation in our NetLogo simulation.

Additionally, proof-of-concept videos can be accessed via the following [YouTube playlist](https://youtube.com/playlist?list=PLOioj0ziLeDCcTm4_PvFFqmqayofMnhlx&si=q-vcLgW_VK_ztenD).

---

## Video Links

All videos can be accessed on the [YouTube playlist](https://youtube.com/playlist?list=PLOioj0ziLeDCcTm4_PvFFqmqayofMnhlx&si=q-vcLgW_VK_ztenD).

### Proof of Concepts Videos

- **Following Algorithm as Swarm Behavior - Netlogo Prototype**  
    Following algorithm demonstrated in NetLogo simulation environment. Key Features: Initialization, Agent integration, agent removal.

- **Following Algorithm as Swarm Behavior - Crazyflie realization**  
    Real World realization of our Following Algoriothm using Crazyflie Drones






## NetLogo Simulation Implementation

The NetLogo simulation implementation of the swarm behaviors described in the paper requires the **NetLogo 3D** tool, which can be downloaded from the official [NetLogo website](https://www.netlogo.org).

### Files

- **Main Simulation File:** [netlogo-simulation/swarm-following.nlogo](netlogo-simulation/swarm-following.nlogo)

### Instructions

This NetLogo model simulates swarm behavior in a 3D environment. The following functionalities are provided:

1. **Setup**: Initializes the simulated agents (drones) at random positions within the 3D environment.

2. **Go**: Starts the simulation, which progresses in discrete time steps (ticks). During the simulation:
    - Agents search for neighbors within their visibility radius and select them as followers.
    - The process begins with a user-controlled reference point, which can be moved using WASD keyboard inputs or predefined scripts. 
    - Scripts can be combined (e.g., linear movement combined with circular movement) to create complex motion patterns.
    - The resulting movements cause the agents to form a chain-like structure that follows the reference point.

3. **Add Agent**: Spawns new agents at random positions. These agents are integrated into the existing formation.

4. **Remove Agent**: Removes selected agents. Removed agents initially move toward the ground and disappear. Remaining agents detect the disconnection after a timeout period and re-integrate into the existing formation.

5. **User Input**:By activating buttons (scripts) or using the WASD keys, the formation can be controlled via the simulated input device. Scripts can be combined.

This model allows testing the robustness and scalability of the swarm behavior by dynamically adding or removing agents during the simulation.
