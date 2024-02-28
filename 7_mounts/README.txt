Build the container using 7_mounts.def 
Then mount the folder `data` inside the container using the `--bind` keyword, e.g. using
apptainer shell --bind ./data:/some/path/inside/the/container 7_mounts.sif
Check if the file is mounted in the container as you expected. Try changing the content of the file, or adding a new file and see 
where it appears on the host system.
Try running the container with the %runscript section to print out the content of the mounted text file, via
apptainer run --bin ./data:/opt/ 7_mounts.sif