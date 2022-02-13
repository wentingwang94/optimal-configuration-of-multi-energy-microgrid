# optimal-configuration-of-multi-energy-microgrid
## Irradiance-to-power conversion based on physical model chain: An application on the optimal configuration of multi-energy microgrid in cold climate

The code is written in Python, and some packages should be installed before the scripts can be executed smoothly.  
  * Package pandas (https://pandas.pydata.org/pandas-docs/stable/index.html) is a fast, BSD-licensed library that provides high-performance data structures and data analysis tools.
  * Package numpy (https://numpy.org/doc/stable/) is the fundamental package for scientific computing.
  * Package pvlib (https://pvlib-python.readthedocs.io/en/stable/) provides functions for simulating the performance of PV systems.
  * Package pyomo (https://pyomo.readthedocs.io/en/stable/) is optimization modeling language.

Other Python packages that used for plotting the results include seaborn and matplotlib. And the optimization solver is CPLEX Studio 12.8.

*Data*: The data part of the supplementary material contains two files, one is the weather data downloaded from NSRDB [NSRDB_download_data.csv](https://github.com/wentingwang94/optimal-configuration-of-multi-energy-microgrid/blob/main/NSRDB_download_data.csv), and other is the input data of microgrid optimal configuration model [testdata_final.csv](). The column names of the weather data file are self-explanatory. For the configuration model input file, namely, testdata_final.csv, its eight columns correspond to electric load (actual_consumption), heating load (heat_load), cooling load (cool_load), unit price for purchasing from the grid (price_buy), unit price for selling to the grid (price_sell), per volume price of natural gas (gas), the power of a single PV panel simulated by the model chain (actual_pv), and the power of a single PV panel simulated by conventional model (pv_c). 

*Code*: A total of two Python scripts, namely, NSRDB and model chain example.ipynb (Python version is 3.8) and configuration model example.ipynb (Python version is 3.6), are provided for reproducibility. The file names are self-explanatory. In that, NSRDB and model chain example.ipynb provides the method of obtaining the weather data from NSRDB, and describes the process of converting weather data into PV power through the model chain; and configuration model example.ipynb reproduces the microgrid optimal configuration results in this paper. To use these scripts, the user needs to change the working directory, especially the path that calls CPLEX Studio. It is noted that the user also needs to manually adjust the input parameters of the code (e.g., the value of the carbon-penalty multipliers) according to the comments in the code to reproduce the results of comparative experiments. 
