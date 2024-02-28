# use 2_basic_shell.def and build the container in sandbox mode so that it can be changed:
apptainer build --sandbox 2_basic_shell.sif 2_basic_shell.def
# run the built container interactively:
apptainer shell --writable --fakeroot 2_basic_shell.sif
# try installing something inside the container, e.g. cowsay:
Apptainer>apt-get install -y cowsay
# and then try to run it inside the container via
Apptainer>/user/games/cowsay "hello world!"

# now update the .def file to make changes to:
# - install the cowsay package using the %post section
# - add a %runscript to print out "hello world" using cowsay when the container is run
# - add the location of the cowsay executable (/usr/games/) to the PATH environment variable via the %environment section
# build your container via
apptainer build 2_basic_shell.sif 2_basic_shell.def
# and run it
apptainer run 2_basic_shell.sif
