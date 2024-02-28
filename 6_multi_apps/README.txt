Use the %app* section, specifically %apprun, to create two different applications that can be run from within the container:
- one application that uses `cowsay` to print an output
- one application that uses `cowthink` to print an output

Try to allow an input to one (or both) of these applications using the following string as input to them:
"$@"

Then run either application using either of the following commands:
  apptainer run --app foo my_container.sif
  apptainer exec --app bar my_container.sif "some input string"

 

reference: https://apptainer.org/docs/user/1.0/definition_files.html#scif-apps