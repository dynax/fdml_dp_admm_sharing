# fdml_dp_admm_sharing
Prototype system implementing the DP ADMM-sharing algorithm.

## Data
Data source can be downloaded from https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary.html 

In our submitted paper, we tested the *a9a* and the *gisette* datasets. 

## Data Preprocessing
Before running the system,  you need to go into *script* folder and launch *split.py* to split the data. Following our naming convention, the training data and testing data are located in the same folder with name "raw_train" and "raw_test" respectively. The variable "milestone" controls how many partitions to split and where to split. It indicates the starting feature index for each data partition.

The default parameter will split the *a9a* data into two parts of with 66 and 57 features. 

## Run the System
Go into the folder *src* and launch *fdml.py* to run the experiment. Major parameters are set in *config.py*. Major run time metrics are stored in a dict and dumped to a file in the indicate output folder. 

## Dependency
scipy 1.16.2
numpy 1.16.2
sklearn 0.20.0
pickle
