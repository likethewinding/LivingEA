# LivingEA

> **LivingEA: An Ever-Evolving Evolutionary Algorithm Paradigm via Individual-Level Time-Varying Neural Design**

LivingEA is an automated evolutionary algorithm design paradigm that reformulates algorithm design as an **individual-level, time-varying parameter-control process**.

Instead of treating an evolutionary algorithm as a fixed optimizer, LivingEA allows the algorithmic behavior associated with each candidate solution to evolve dynamically throughout the optimization process.

## Overview

LivingEA maps a mixed continuous-discrete evolutionary algorithm design space into a unified continuous representation and employs neural algorithm designers to generate individual-specific, time-varying algorithm configurations from historical search trajectories.

The resulting framework establishes a closed-loop co-evolutionary process between:

- candidate solutions, and
- their corresponding algorithm generators.

LivingDE is the differential evolution instantiation of the LivingEA paradigm.

## Key Features

- **Individual-level algorithm design**
- **Time-varying evolutionary behavior**
- **Unified continuous representation of mixed algorithm design spaces**
- **Temporal neural algorithm designers**
- **TCN and TS-Transformer**
- **Q-learning-based designer scheduling**
- **Zero-shot generalization across unseen problems and dimensions**
- **Dual-view explainability using SHAP and search trajectory networks**

## Framework

LivingEA consists of three main stages:

1. **AAD Modeling**  
   Reformulate mixed algorithm design variables as a unified continuous parameter-control problem.

2. **Neural Algorithm Design**  
   Learn time-varying design policies from historical evolutionary trajectories.

3. **Zero-Shot Deployment**  
   Deploy the learned algorithm designers directly to unseen optimization problems without retraining.

## LivingDE

LivingDE instantiates LivingEA using differential evolution.

Its design space includes both continuous and discrete decisions, including:

- scaling factor \(F\),
- crossover rate \(Cr\),
- individual-selection strategies,
- difference-vector operands, and
- activation switches for differential components.

Each individual can therefore follow a different and dynamically changing evolutionary behavior.

## Zero-Shot Generalization

The neural algorithm designers are trained on 10-dimensional optimization problems and directly deployed to unseen higher-dimensional and real-world optimization scenarios.

The current study evaluates zero-shot generalization up to 1000 dimensions.

## Explainability

LivingEA is interpreted from two complementary perspectives:

- **SHAP** explains how trajectory features influence neural algorithm-design decisions.
- **Search Trajectory Networks (STNs)** visualize how these decisions shape the resulting optimization trajectories.

## Project Status

🚧 **Project repository under construction**

The project page and supporting materials are currently being organized.

Source code, experiment scripts, trained models, and detailed reproduction instructions will be released at a later stage.

## Paper

**LivingEA: An Ever-Evolving Evolutionary Algorithm Paradigm via Individual-Level Time-Varying Neural Design**

IEEE Transactions on Evolutionary Computation

Paper link: *Coming soon*

## Repository Structure

```text
LivingEA/
├── README.md
├── assets/
├── figures/
├── supplementary/
└── code/
