# Thesis_result
There are two file `Hybrid_Henry_Gas.csv` and `Triple_Check_Exploration.csv`

In each file there are seven columns for seven benchmarking algorithm holding the global fitness values of each epochs (we run these algorithms for 100 epochs with default parameters).
The benchmarking algorithms are:
1. Rosenbrock
2. Sphere
3. Quartic_with_noise
4. Schwefel_1_2
5. Step
6. Ackley
7. Rastrigin

`Hybrid_Henry_Gas.csv:`
Contains benchmarking data for Hybrid Henry Gas Solubility Algorithm

`Triple_Check_Exploration.csv:`
Contains benchmarking data for Triple Exploration Technique.

## Examples

To load the data and print the columns name:
```
import pandas as pd

df = pd.read_csv('Hybrid_Henry_Gas.csv')
print(df.columns)
```

For example, we want to plot the covergence of Rosenbrock benchmark function for Hybrid Henry Gas Solubility Algorithm:
```
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('Hybrid_Henry_Gas.csv')
df['Rosenbrock'].plot(kind='line')
plt.xlabel('Iteration')
plt.ylabel('Convergence')
plt.show()
```
To get the global optimum value for each benchmark algorithm for HHGSO OR Triple Exploration Technique:

HHGSO:
```
import pandas as pd

df = pd.read_csv('Hybrid_Henry_Gas.csv')
print(df.loc[99])
```
Triple Exploration Technique:
```
import pandas as pd

df = pd.read_csv('Triple_Check_Exploration.csv')
print(df.loc[99])
```

