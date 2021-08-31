<h1> Particle-Based Optimization Algorithms for Longitudinal Control of Autonomous Vehicle: A Comparative Study </h1>

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
  - [Abstract](#abstract)
  - [Contributions](#contributions)
- [How to Use](#how-to-use)
  - [Requirements](#requirements)
  - [Installation](#installation)
- [Simulation Files](#simulation-files)
- [Results](#results)
- [Technical References](#technical-references)


## Introduction

### Abstract

> In order to improve the stability and performance of an autonomous vehicle,
optimizations need to be explicitly performed in the controllers, which has an essential part in the
tracking system. This work proposes a novel longitudinal control optimization scheme and a novel
longitudinal controller consisting of a feed-forward and feedback term. The feed-forward term is
inspired by the vehicle's steady-state response, whereas the feedback term is a proportional-
integral-derivative (PID) controller. Also, A model representing the longitudinal vehicle dynamics is
designed based on physical phenomena affecting the vehicle. Besides, some nature-inspired
optimization algorithms are used to optimize the controller, i.e., Particle Swarm Optimization (PSO),
Accelerated PSO (APSO), Flower Pollination Algorithm (FPA), and Modified FPA (MFPA). The
algorithms are compared in optimizing the longitudinal vehicle model and controller using the
CARLA simulator, and stability tests are also done for each algorithm. In addition, the
characteristics of several cost functions in the controller optimization are inspected. The results
show that the MFPA is the most stable algorithm, the proposed model represents the system
satisfactorily, and optimizing the controller using a regularized cost function leads to better overall
performance.

### Contributions
**Contributions**. This work has 4 contributions, i.e.;
1. **Propose** a longitudinal controller that has a feed-forward and feedback term.
2. **Propose** a longitudinal vehicle model representing a real vehicle for simulation.
3. **Compare** optimization algorithms performance and stability.
4. **Compare** cost function modifications on algorithm performance.

**Simulations**. We have done 3 kind of simulations in this repository, namely;
1. Non-linear least-square regression.
2. System identification.
3. PID tuning.

**Optimization Algorithms**. We compare 4 nature-inspired optimization algorithms to determine which one is the best and most reliable algorithm. The optimization algorithms explored in this work are;
1. Particle Swarm Optimization (PSO).
2. Accelerated Particle Swarm Optimization ([APSO](https://arxiv.org/abs/1203.6577)).
3. Flower Pollination Algorithm ([FPA](https://arxiv.org/abs/1312.5673)).
4. Modified Flower Pollination Algorithm ([MFPA](https://unijourn.com/article/5f7eadeb7c994c603b93ad6d/5ae99ad07348a8567766abe2/4.html)).

## How to Use

### Requirements

We heavily depend on the following libraries;
```
jupyter
jupyterlab
numpy
numba
matplotlib
pandas
SciencePlots
```
We use [Numba](http://numba.pydata.org/) to speed up our code. We found that by using `Numba`, surprisingly we're able to accelerate our simulation more than **10x times** faster. But it also has several trade-off, e.g. less flexible, prone to bugs, and quite hard to refactor.

### Installation

We suggest to use a [conda](https://docs.conda.io/en/latest/) environment to make your installation easier. Installing libraries in `conda` is relatively easy because it will also automatically install their dependencies.

After installing `conda`, we recommend do as follows;
```
# Create an environment inside conda
conda create -n py39 python=3.9

# Activate the environment
conda activate py39

# Install the required libraries
conda install jupyter -y
conda install -c intel numpy -y
conda install -c numba numba -y
conda install -c conda-forge jupyterlab matplotlib pandas -y
```
**Notes**:
- `conda install -c intel numpy` is recommended if you have an intel CPU installed on your computer, because it will use the Intel Math Kernel Library ([MKL](https://software.intel.com/content/www/us/en/develop/tools/oneapi/components/onemkl.html)) as its backend. Otherwise, you'd better avoid MKL by using the `conda-forge` channel.
- Now, we cannot install `SciencePlots` through conda directly. Instead, we need to look at the original [repository](https://github.com/garrettj403/SciencePlots).

## Simulation Files

1. **Steady-State Response** ([PSO](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S1_Steady_State_Response/A1_PSO), [APSO](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S1_Steady_State_Response/A2_APSO), [FPA](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S1_Steady_State_Response/A3_FPA), [MFPA](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S1_Steady_State_Response/A4_MFPA))

2. **System Identification** ([PSO](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S2_System_Identification/A1_PSO), [APSO](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S2_System_Identification/A2_APSO), [FPA](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S2_System_Identification/A3_FPA), [MFPA](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S2_System_Identification/A4_MFPA))

3. **PID Tuning** ([PSO](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S3_PID_Tuning/A1_PSO), [APSO](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S3_PID_Tuning/A2_APSO), [FPA](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S3_PID_Tuning/A3_FPA), [MFPA](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S3_PID_Tuning/A4_MFPA))

4. **Cost Function Modifications** ([MFPA](https://github.com/fadamsyah/Particle-Based-Optimization-for-Longitudinal-Control/tree/main/S4_COST_FUNCTION_MODIFICATIONS))

## Results

`----------------------------------------------`

## Technical References
- [Introduction to Self Driving Cars](https://www.coursera.org/learn/intro-self-driving-cars?specialization=self-driving-cars)
- [Make Python code 1000x Faster with Numba
](https://www.youtube.com/watch?v=x58W9A2lnQc&ab_channel=JackofSome)
- [Flower Pollination Algorithm](https://www.mathworks.com/matlabcentral/fileexchange/45112-flower-pollination-algorithm)
- [Accelerated Particle Swarm Optimization](https://www.mathworks.com/matlabcentral/fileexchange/29725-accelerated-particle-swarm-optimization)