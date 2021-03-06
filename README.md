# Tandem Solar Cells Efficiency Prediction and Optimization via Deep Learning
&nbsp;&nbsp; This repository apply ML and heuristic algorithms for optimizing structures of tandem solar cells. In [Modeling](https://github.com/HKjoe/Optimizing-for-Solar-Cells-Structure/tree/master/Modeling) file, it includes source code of building and training CPN model. Furthermore, ModelConfig.py is some configurations about CPN while training. CPN.py is main code for training model. 5to3.h5 is our trained model for replace simulation tools. WHUT_more_data.npy is simulation dataset, which includes 12500 sets.  
&nbsp;&nbsp; You can train you own model by run CPN.py, after configuring required parameters in ModelConfig.py. Model also can be saved by adopted .savemodel(path) attribute in CPN.py.
```python
python CPN.py
```
&nbsp;&nbsp; In [Optimizing](https://github.com/HKjoe/Optimizing-for-Solar-Cells-Structure/tree/master/Optimizing) file, it includes three parts: config, sko, continuous and discrete optimization. Config file is configurations requirements parameters of heuristic algorithms. Sko file is optimizing tools from [@guofei9987](https://github.com/guofei9987), but little cahnged has been performed in it. Other file names ending with -C are continuous optimizing source code, and those ending with -D are discrete optimizing source. After configuring parameters in config file, you can run these heuristic algorithms to obtain feasible structures with trained model like 5to3.h5 model. 
```python 
python SA-D.py
```
&nbsp;&nbsp; The [csv file](https://github.com/HKjoe/Optimizing-for-Solar-Cells-Structure/blob/master/detailed_100_optmizitoin_results.csv) is detailed log of 100 optimization results, which includes optimal structures, IS and projected efficiency (IE). In the file, eta represents the improvement of our optimization results to base line. What's more, dup_num represents the repeated times of this result in 100 optimization results.
