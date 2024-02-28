# pull docker's hello-world container from Dockerhub at
# https://hub.docker.com/_/hello-worldhttps://hub.docker.com/_/hello-world
apptainer pull docker://hello-world
# run the downloaded container:
apptainer run hello-world_latest.sif
# or all in one command:
apptainer run docker://hello-world

#now attempt the same with an Ubuntu image using a %postscript
#by adapting the provided .def file and building the container:
apptainer build 1_hello_world.sif 1_hello_world.def 
# and then run it:
apptainer run 1_hello_world.sif
# or alternatively:
./1_hello_world.sif
# now change the base OS to `alpine:latest`, rebuild the container, test it and note the difference in container size
# compared to the one using Ubuntu
