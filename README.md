# Logistic Map Analysis

## Overview

This repository contains the analysis and simulation of the Logistic Map using Python. The Logistic Map is a classic example of how simple deterministic rules can lead to complex and unpredictable patterns. This project explores discrete dynamical systems and chaos theory through Python, illustrating period-doubling bifurcation routes to chaos over a fixed period of time.

## Project Structure

- **Logistic Map.pdf**: A detailed document explaining the concepts and implementation of the Logistic Map.
- **Logistic Map Final Report.pdf**: The final report for the project, summarizing the findings and discussing the results.
- **logistic_map.py**: Python script containing the implementation of the Logistic Map and the code to generate the bifurcation diagram.

## Description

The Logistic Map is used to model population dynamics by accounting for the limited availability of resources, balancing reproductive growth against environmental constraints. It demonstrates the interaction between reproduction rates and resource availability, where excessive growth is naturally curbed by environmental limits. As the parameter `r` varies, the Logistic Map showcases a transition from predictable behavior to chaos.

## Installation

To run the code in this repository, you will need Python and the following libraries:
- NumPy
- Matplotlib

You can install these libraries using pip:

```bash
pip install numpy matplotlib
```

## Here's an example of how to use the Logistic Map function:

```python
import numpy as np
import matplotlib.pyplot as plt

def logistic_map(r, x):
    return r * x * (1 - x)

r_values = np.linspace(1, 4, 300000)
x = 0.5
iterations = 1000
last = 100

for r in r_values:
    x = 0.5
    for _ in range(iterations):
        x = logistic_map(r, x)
    plt.plot(r, x, ',k', alpha=0.5, markersize=0.013)

plt.xlabel('r')
plt.ylabel('x')
plt.title('Bifurcation diagram of the logistic map')
plt.show()
```

For more detailed explanations and additional code, please refer to the files Logistic Map.pdf and Logistic Map Final Report.pdf included in this repository.
