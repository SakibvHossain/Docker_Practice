### Running Image using Docker  
Now, You have image and you want to run it right how you can do that?  
`docker run -it ubuntu` to run image in interactive mode if the image not available it will download the image for you and run it.  
`ctrl` + `D` to exit from the image.

### To check which container is running  
`docker container ls`

### To check which container is running or created previously all of them will be shown  
`docker container ls -a`

### To run a docker image using name
`docker start <image name>`

### To stop a docker image using name  
`docker stop <image name>`

### You want to stick with image terminal with your terminal not to terminate to do that you need:  
start image `docker start <image name>`  
stick with your terminal `docker exec -it <image name> bash`  
stop image `docker stop <image name>`  
