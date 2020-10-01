## Just a smal sample, about capacity to run powershell in Linux Container 
Note: 
* MS provides rpm for RHEL 7 
* Red Hat provide Universal Base Image, as a standard and secured Base OS Image for containers; Will use the default flavor here (ubi7/ubi)
* I'm not a container expert, so that probably there is a better way to create the image 

You can 
 * build the image with buildah & commit your changes to create the image
or
 * use a docker fie and run buildah bud -t ImageName dockerfile, what I did 

With the docker file:

`buildah bud -t ubi7-pwsh ./docker` 

and give it a test 

`podman run -it localhost/ubi7-pwsh`

`PS > get-process`

