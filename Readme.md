# README: Evolutionary Algorithm for Health Status Classification
## Introduction
This project aims to develop an innovative evolutionary algorithm inspired by biological processes to optimize a neural network model for health status classification. The algorithm mimics various biological events such as gamete sperm cell competition, species fitness propagation, and genetic diversity maintenance to evolve neural network architectures. The underlying neural networks are tasked with diagnosing a person's health status as either 'Diseased' or 'Not Diseased.'

## Algorithm Overview
### Biological Events Emulated
1. **Gamete Sperm Cell Competition**: Each 'organism' in the simulation possesses two distinct neural networks as its 'chromosomes.'
2. **Fitness Propagation**: The haploid models with the lowest loss scores get selected for 'reproduction.'
3. **Genetic Diversity**: Randomly introduced new neural network pairs maintain genetic diversity in the population.
4. **Survival of the Fittest**: Over time, models with the lowest loss scores dominate the population.
### Technical Workflow
1. **Initialization**: Start with 50 pairs of distinct neural network models, each representing an organism in the population.
2. **Haploid Generation**: Each pair generates 100 haploid models, which are combinations of their parent neural networks.
3. **Fitness Evaluation**: Each haploid model is evaluated using a forward gradient run across all past samples in the training data.
4. **Selection**: The best haploid, i.e., the one with the lowest loss score, is chosen from each pair for propagation.
5. **Reproduction**: The selected haploids undergo 'mating' to produce four 'children,' generating the next generation of neural network models.
6. **Population Control**: Only the top 50 pairs get to reproduce.
7. **New Pair Introduction**: Periodically, new neural network pairs are introduced into the population to maintain genetic diversity.
### Additional Features
**Euclidean Distance Calculation**: Initial attempts were made to include the Euclidean distance between each neural network pair as a feature. However, this was later abandoned due to concerns related to the curse of dimensionality.
## Objective and Expected Outcomes
The algorithm seeks to leverage both random selection and slight neural backpropagation in each generation to produce neural network model pairs with significantly low loss scores over time.

## Considerations
1. **Dimensionality**: The initial idea of using Euclidean distance as a feature was discontinued due to the curse of dimensionality, which could lead to overfitting or degraded performance.
