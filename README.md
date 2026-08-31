# Temperature-Augmented Event-Chain Monte Carlo for Double-Well Sampling

This repository contains the code developed for my MSc project on temperature-augmented event-chain Monte Carlo (ECMC).

The project compares temperature-augmented ECMC with reversible and irreversible simulated tempering for sampling a one-dimensional double-well potential. The final comparison focuses on the low-temperature case $T=0.1$.

## Notebook

[Open the complete notebook](Baseline%20Cases/temperature_augmented_ecmc_comparison.ipynb)

The notebook includes:

* validation of Metropolis and ECMC sampling;
* reversible and irreversible simulated tempering;
* construction of the temperature-augmented ECMC method;
* beta-interval and beta-speed tuning;
* a final comparison across five random seeds.

## Main Results

Temperature-augmented ECMC produced the lowest mean well-indicator integrated autocorrelation time, indicating the best mixing per target sample. However, its current implementation was slower and produced a lower effective sample size per second than both simulated-tempering methods.

All three methods achieved similar CDF accuracy at the final sample checkpoint.

## Requirements

* Python
* NumPy
* pandas
* Matplotlib
* SciPy
* Jupyter Notebook

The required packages can be installed with:

```bash
pip install numpy pandas matplotlib scipy jupyter
```

## Running the Notebook

Start Jupyter and run the notebook from top to bottom:

```bash
jupyter notebook "Baseline Cases/temperature_augmented_ecmc_comparison.ipynb"
```

The complete notebook is computationally expensive to rerun. Saved outputs are included so that the results can be viewed directly on GitHub.
