
---
title: Tasklist
sectionName: tasklist
position: -1
---

### Which functional features are we still lacking?
* Reversible reaction integrator, detailed balance
* Topologies [high],
    Topologies are superstructures grouping particles to e.g. molecules. Required features:
    - ~~potentials between specific particles (bonds, angles, dihedrals)~~
    - ~~consistent handling of reactions, i.e. particles involved in topologies can undergo reactions and topologies are correctly updated~~
    - may include different handling of particle motion. Particles moving together in a topology may obey different dynamics (e.g. anisotropic diffusion)
* Membranes [high],
    Mohsen's membrane model includes special particle types and special dynamics. Should be somehow integrated into ReaDDy.
    - Treat these particles like other particles? Treat the membrane as a topology? Or are membranes different from standard particles?
    - Interactions and reactions between standard particles and membrane particles should be possible
    (e.g. binding of a membrane-associated protein to a membrane that deforms the membrane locally)
* Special programs,
    Plan/design how to integrate special programs such as compartment-based reactions with minimal user-side C++ programming overhead. [see issue #48]

### Which technical features are we still lacking?
* Snapshot: Save simulation state such that we can continue a simulation run.
* Efficient parallel reaction handling (low-prio)
* Kernel: MPI
* Kernel: GPU
* High-level Python API
* Windows binaries

### Next Todos
* Planning / conceptual / software design:
    - How do we build topologies [solved]
    - Can we integrate membranes in this concept? [probably not]
    - Consistency of membrane model with the remaining particle/topology concept? How can we integrate these concepts with minimal additional effort?
    - Relation to GPU Kernel: What part of topology handling can be done on the GPU? What on the CPU?
    - Membranes on the GPU?
