#Build the container using the provided definition file and then run it:
apptainer build 9_jupyter.sif 9_jupyter.def
./9_jupyter.sif
#Open the launched jupyer server in the browser by going to the link that appears in the terminal.
#Note: the link can also be launched by holding ctrl and left-clicking on it on Windows machines.
#Then try to open and run the provided hello_world.ipynb notebook. Note the python version and current working directory