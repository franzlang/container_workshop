Here are some real examples of Apptainer definition files as they are/were used to deploy applications on IDAaaS.
Each one has been chosen to illustrate a feature or capability of/within Apptainer that you might find useful. 
The definition files have been sanitised, so may or may not build as provided. The point is not to build the containers
(this would take way too long) but to note how certain things can be done with Apptainer.

-jmol: simple example of downloading a tarball via wget to install an application. Note the use of 
 the non-interactive front end to stop the apt-get command launching an interactive element and timing-out
-mcstas: example of using openmpi within a container by compiling it from source
-materialsstudio: example of using the `expect` package to write and run a script for an interactive installer
-chimera: example of setting up an application with GPU accelerated visualisation and running it via virtualGL
-gudrun: example of copying files into the container and also having multiple applications that can be run from the container