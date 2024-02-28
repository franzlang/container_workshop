First build the base image using 5_base_image.def
Then use the `localimage` bootstrapper in the `Bootstrap` part of the Header
to build on top of that local image using `5_final_image.def`
In addition, add a %post section to the final image that allows 
running the binary that was compiled in the base image from the PATH, 
e.g. by softlinking or copying it to a specific location,
Finally, add a %runscript section to call the binary when the container is run.

Compare the size of the output container with that from the previous example.