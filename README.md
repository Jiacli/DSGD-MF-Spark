# DSGD-MF-Spark
Distributed Stochastic Gradient Descent for Matrix Factorization on Spark


## Description
My code includes the automatic evaluation (avg. NZSL) using spark, and it is set as open as default. If you don't want this evaluation (e.g., for speeding up), you can set the variable self_eval as False at the start of the code.

## How to run
Upload the code and data in the cluster (**Note that in EMR cluster, the data need to be stored in HDFS**), and then run the sample command line as follows:

**Sample command line on GHC cluster**:
/afs/cs.cmu.edu/project/bigML/spark-1.3.0-bin-hadoop2.4/bin/spark-submit dsgd_mf.py 20 10 30 0.8 0.01 autolab_train.csv w.csv h.csv


**Sample command line on AWS cluster**:
./spark/bin/spark-submit --master spark://<master_internal_IP>:7077 dsgd_mf.py 20 10 30 0.8 0.01 <HDFS File Path> w.csv h.csv
