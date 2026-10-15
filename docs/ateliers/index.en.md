# The workshops

Each workshop explores **a real robotics or AI algorithm**, through dedicated software the students drive themselves. The teacher or referent follows a step-by-step roadmap; no robotics background is needed.

## Path finding

<div class="grid cards" markdown>

-   ![Map from the BFS/Dijkstra/A* editor: water, plains, mountains and snow, with the computed path](../assets/images/ateliers/atelier-chemin.png)

    **The shortest path** · Ages 9–12 · 1 h to 1 h 30

    Students draw their own map — water, plains, mountains, snow — then watch three algorithms compete for the best route.

    *Algorithms: BFS, Dijkstra, A\**

-   ![Mars rover linking a glacier to the base: the RRT tree in red and the found path in blue](../assets/images/ateliers/atelier-mars.png)

    **Mission to Mars** · Ages 9–12 · 45 min

    A rover, a glacier, a base to reach: how do you find a path when the terrain is no longer cut into cells?

    *Algorithm: RRT (continuous space)*

</div>

## Learning and evolution

<div class="grid cards" markdown>

-   **The snail and the apple** · Ages 13–15 · 1 h 30

    In the Snail Simulator, a virtual snail learns **on its own** to reach an apple — a behavior nobody programmed.

    *Algorithms: reinforcement learning — DDQN, PPO, SAC*

-   **Snails that evolve** · Ages 13–15 · 1 h

    Same task, radically different method: a population of snails improves generation after generation.

    *Algorithm: genetic algorithms*

</div>

## Localization and vision

<div class="grid cards" markdown>

-   ![Localization simulator: the ghost robot on an autumn map, with the search circle, particle weights and estimated position](../assets/images/ateliers/atelier-localisation.png)

    **The ghost robot** · Ages 16–17

    A robot lost on a map built by the students finds its position thanks to a cloud of particles that tightens with every observation.

    *Algorithm: Monte-Carlo localization (particle filter)*

-   **Reading handwriting** · Ages 16–17 · 3 × 1 h 30

    From the first neuron to a convolutional network: students train a network to recognize handwritten digits, then open the black box.

    *Algorithms: MLP, CNN, ResNet (Jupyter notebooks, MNIST dataset)*

</div>

## In preparation — on the snAIl robot

![Students watch snAIl navigate between GO, STOP and LEFT cards laid on the floor, reading them with its camera](../assets/images/ateliers/snail-navigation.jpg)

The next workshops leave the simulator for the robot itself: above, snAIl navigates the classroom by reading cards on the floor with its camera.

<div class="grid cards" markdown>

-   **Mapping with a laser** · *in preparation*

    Sweep the room with snAIl's LiDAR and build, for real, the map the robot will then use to plan its routes.

    *Sensor: LiDAR*

-   **Seeing in depth** · *in preparation*

    Two lenses, one depth: measure distances with snAIl's stereo 3D camera, the way a pair of eyes does.

    *Sensor: stereo 3D camera*

-   **Talking to the robot** · *in preparation*

    Command snAIl by voice and discover the models that connect seeing, understanding and acting — directly onboard the robot.

    *Embedded AI: voice, small language models (SLM), vision-language-action models (VLA)*

</div>

---

Every existing workshop comes with full teaching material (teacher roadmap, glossary, end-of-session questions). For running a session, see the [lessons](../lecons/index.md).
