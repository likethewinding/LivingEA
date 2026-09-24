<div align="center">

LivingEA

An Ever-Evolving Evolutionary Algorithm Paradigm

via Individual-Level Time-Varying Neural Design

<br>

Automated Algorithm Design · Learning to Optimize · Evolutionary Computation · Zero-Shot Generalization · Explainable AI

<br>





<br>

What if an evolutionary algorithm were no longer a fixed optimizer,
but a living system whose search behavior evolves together with its solutions?

</div>

Overview

LivingEA introduces an evolutionary algorithm paradigm in which the algorithm itself evolves during optimization.

Instead of assigning a fixed algorithmic configuration to an entire population, LivingEA treats automated algorithm design as an individual-level, time-varying parameter-control process. Each candidate solution is associated with its own dynamically generated search behavior, allowing the solutions and their algorithm generators to co-evolve throughout the optimization process.

The first instantiation of this paradigm is LivingDE, built on Differential Evolution.

Why LivingEA?

Most existing evolutionary algorithms still operate under a relatively static design:

one algorithm structure,

one population-level configuration,

manually specified adaptation rules, or

coarse-grained switching among predefined strategies.

LivingEA changes the design perspective:

Conventional EA

LivingEA

Static algorithm structure

Time-varying algorithm behavior

Population-level configuration

Individual-level configuration

Handcrafted adaptation

Learned temporal design policy

Fixed operator templates

Continuously parameterized mixed design space

Solution evolution

Co-evolution of solutions and their generators

Core Idea

<div align="center">

Search trajectory → Neural designer → Algorithm configuration → New solution → New trajectory

</div>

For individual (i) at iteration (t), LivingEA learns a time-dependent generator

[
\Theta_i^{(t)} = \mathcal{C}\left(H_i^{(t-1)}\right),
]

where (H_i^{(t-1)}) represents the historical search trajectory and (\mathcal{C}) denotes the learned algorithm designer.

The resulting configuration determines how the individual evolves at the current iteration.

This creates a closed loop:

[
\text{Solution trajectory}
;\longleftrightarrow;
\text{Algorithm evolution trajectory}.
]

LivingDE

LivingDE instantiates LivingEA through Differential Evolution.

Its design space jointly contains continuous and discrete algorithmic decisions, including:

scaling factor (F),

crossover rate (Cr),

base-vector selection,

difference-vector operands,

activation of differential components.

Discrete decisions are mapped into a continuous preference space, allowing the complete mixed design problem to be handled by neural algorithm designers.

Neural Algorithm Designers

LivingEA uses two heterogeneous non-recurrent temporal models:

Temporal Convolutional Network

The TCN emphasizes local temporal patterns in evolutionary trajectories and provides efficient sequence modeling.

Time-Series Transformer

The TS-Transformer captures longer-range dependencies and global temporal relationships.

Q-Learning Scheduler

A lightweight Q-learning scheduler dynamically coordinates the two designers during optimization.

<div align="center">

TCN + TS-Transformer + Q-learning

Local temporal modeling · Global temporal modeling · Dynamic coordination

</div>

Zero-Shot Generalization

A central objective of LivingEA is to learn scale-insensitive algorithm-design policies rather than problem-specific parameter schedules.

The neural designers are trained on 10-dimensional optimization problems and directly deployed, without retraining, to:

unseen CEC benchmark functions,

higher-dimensional search spaces,

large-scale problems up to 1000 dimensions,

real-world optimization tasks.

<div align="center">

10D Training  →  Unseen Problems  →  30D / 50D / 100D / 1000D

</div>

Explainability

LivingEA is interpreted from two complementary perspectives.

Neural Decision View

SHAP is used to analyze how trajectory features influence algorithm-design decisions.

The current implementation studies features related to:

relative fitness,

spatial proximity,

historical success rate.

Search Behavior View

Search Trajectory Networks (STNs) visualize how different neural decisions translate into search behavior over time.

Together, the two views answer:

Why does the neural designer make a particular decision?
What search behavior emerges after that decision is executed?

Framework

The final framework figure will be added here.

<p align="center">
  <img src="assets/livingea-framework.png" width="92%" alt="LivingEA Framework">
</p>

Experimental Scope

LivingEA / LivingDE is evaluated across multiple scenarios:

Scenario

Purpose

CEC benchmarks

General optimization performance

Cross-dimensional testing

Zero-shot scalability

Large-scale optimization

Generalization up to 1000D

Real-world tasks

Practical transferability

SHAP analysis

Neural decision interpretation

STN analysis

Search-behavior interpretation

Repository Status

🚧 This repository is currently being prepared for the LivingEA project.

At the current revision stage, the repository primarily serves as the project homepage and organizational space.

Planned release materials include:

source code,

training and testing scripts,

trained neural designers,

benchmark configurations,

supplementary experimental results,

reproduction instructions.

The complete reproducibility package will be added in a later release.

Repository Structure

LivingEA/
├── README.md
├── assets/
├── figures/
├── supplementary/
└── code/

Paper

LivingEA: An Ever-Evolving Evolutionary Algorithm Paradigm via Individual-Level Time-Varying Neural Design

Manuscript currently under revision.

Paper link: Coming soon

Citation

Citation information will be added after the final bibliographic record becomes available.

<div align="center">

LivingEA

From evolving solutions to evolving algorithms.

</div>
