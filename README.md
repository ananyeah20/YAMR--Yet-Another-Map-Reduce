# YAMR--Yet-Another-Map-Reduce
To install and run these examples you need:

Python 2.7 or 3.3+
git (only to clone this repository)
pip install Flask

The project runs on Flask framework (this project could be built on threading or socket programming as well)

ABOUT THE CODE-

MASTER NODE- 

Running at port 8000 (port numbers can be changed)
Contains the number of worker nodes specified
Maintains the metadata which contains the worker nodes and the port numbers they are running in

CLIENT NODE-
Performs the read, write and map reduce operations
The data in the input file will be partitioned and scheduled to different worker nodes
The partitioning is done using np.array.split() and the join function joins the outputs from all nodes


WORKER NODE-

Every worker node starts at port 8001(can be changed) and each worker nodes port number keeps incrementing according to the specified number of worker nodes. Example- worker node 1 works on 8001 and worker node 2 works on 8002
This file runs all the functions specified in the client.py
The mapper function takes the input of mapper file of the input file and writes the output to a file named mapout
The reducer function takes the input of reducer file and returns it to the output file named mapout 
Suggestion- give a huge json file as the input

HOW TO RUN-

pip install Flask
Assign your input file name to input variable in the client file
Assign your mapper file name to mapper variable in the client file
Assign your reducer file name to reducer variable in the client file
run the client file, then the master file and worker file on three different terminals

Contributions-

Ananya Adiga

Amisha Mathew

Apoorva Naronikar




