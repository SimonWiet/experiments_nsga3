# Experimental Evaluation of the NSGA-III on the 3-dimensional OneMinMax benchmark
This repository contains the source code and data used in the experimental evaluation of the NSGA-III on the 3-dimensional OneMinMax benchmark. The results are used in our paper "A Mathematical Runtime Analysis of the Non-dominated Sorting Genetic Algorithm III (NSGA-III)" accpeted for IJCAI 2023.


### Files
- `code_experiments.ipynb`: A jupyter notebook containing the code for the benchmarking, writing the resulting data into `.csv` files and visualizing data from these `.csv` files

- `exp_nsga3.csv`: A file containing the data generated by benchmarking the NSGA-III on 3-OneMinMax tracking the number of iterations until the complete Pareto front is sampled. Each data point consists of the used algorithm (`algo`, always NSGA-3), the block size (`blockSize`) which is half the length of the bit strings in the population, the number of employed divisions along each objective for the reference points (`refPoints`), the population size (`popSize`), the number of iterations until the complete Pareto front was sampled (`iterations`) and the chance with which crossover was applied in the reproduction step (`ratioCO`). The column `ratioMutate` (corresponding to `1 - ratioCO` is deprecated and can be ignored). 

- `exp_coverage.csv`: A file containing the data generated by benchmarking the NSGA-III and NSGA-II on 3-OneMinMax tracking the ratio of the covered Pareto front for each generation of the optimization process. Each data point consists of the benchmark `problem`, always `3OMM` = 3-OneMinMax), the used algorithm (`algo`, either `nsga2` or `nsga3`), the block size (`blockSize`) which is half the length of the bit strings in the population, the number of employed divisions along each objective for the reference points (`refPoints`) for the NSGA-3 (0 for NSGA-2), the population size (`popSize`), the chance with which crossover was applied in the reproduction step (`ratioCO`), the number of tracked iterations (until either the maximum iteration, here `500`, was hit or the complete Pareto front was found) and `coverages`, a list stating for each generation the number of elements in the Pareto front contained in the population of that generation.
