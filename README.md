# Particle-Based Optimization Algorithms for Longitudinal Control of Autonomous Vehicle: A Comparative Study


## Introduction

### Abstract
`---------------------`

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

We suggest to use a [conda](https://docs.conda.io/en/latest/) environment to make your installation easier. Installing libraries in `conda` is relatively easy because it will also install their dependencies.

After installing `conda`, we recommend installing the required libraries as follows;
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

## Files

`----------------------------------------------`

## Results

`----------------------------------------------`

## Technical Reference(s)
- [Introduction to Self Driving Cars](https://www.coursera.org/learn/intro-self-driving-cars?specialization=self-driving-cars)
- [Make Python code 1000x Faster with Numba
](https://www.youtube.com/watch?v=x58W9A2lnQc&ab_channel=JackofSome)
- [Flower Pollination Algorithm](https://www.mathworks.com/matlabcentral/fileexchange/45112-flower-pollination-algorithm)
- [Accelerated Particle Swarm Optimization](https://www.mathworks.com/matlabcentral/fileexchange/29725-accelerated-particle-swarm-optimization)