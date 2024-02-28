# pull docker's hello-world container from Dockerhub at
# https://hub.docker.com/_/hello-world
apptainer pull docker://hello-world
# run the downloaded container:
apptainer run hello-world_latest.sif
# or all in one command:
apptainer run docker://hello-world

#now attempt the same with an image you created from scratch
#1. pick a suitable base OS from existing Dockerhub images, e.g. Ubuntu or Alpine
#official Docker images are listed at https://hub.docker.com/search?q=&image_filter=official
#2. adapt the `From` part of the definition file's Header to use your chosen base OS
#3. add a simple command to %runscript section to print "hello world" when the container is run
#now build the container:
apptainer build 1_hello_world.sif 1_hello_world.def 
# and then run it:
apptainer run 1_hello_world.sif
# or alternatively run it as:
./1_hello_world.sif
#4. rebuild the image with a different base OS and see how the size of resulting image changes (e.g. compare Ubuntu with Alpine)
