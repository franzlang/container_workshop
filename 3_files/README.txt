#add the `hello_world.txt` file to the container via the %files section
#then add %postscript command(s) to print out the contents of the file within the container
# reference: https://apptainer.org/docs/user/1.0/definition_files.html#files
#you can check that the file was correctly copied into the container by opening an interactive shell inside it after you built it via
apptainer shell my_container.sif