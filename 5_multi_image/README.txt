First build the base image using 5_base_image.def
Then use the `localimage` bootstrapper to build on top of that local image using `5_final_image.def`: add a %post section that allows 
running the binary that was compiled in the base image from the PATH, e.g. by softlinking or copying it to a specific location,
and then add a %runscript section to call the binary.