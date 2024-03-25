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

### To see how many image you have
`docker images`

### You want to stick with image terminal with your terminal not to terminate to do that you need:  
1.  start image `docker start <image name>`  
2.  stick with your terminal `docker exec -it <image name> bash`  
3.  stop image `docker stop <image name>`  


### Port mapping
We need port mapping because when you run redis then it might be running on some port right. If you hit enter with the port on browser then definately it not gonna work. That's for we need to expose port to run it on browser.  

**Port Mapping:** `docker run -p HOST_PORT:CONTAINER_PORT --name redis-stack redis-stack`  
  
**Note:** If you've already started a container using `docker start`, you can't specify port mappings directly during the start operation. The `docker start` command doesn't support the `-p` or `--publish` flag to expose ports.   
  
You can specify port mappings when you initially create the container using `docker create` or `docker run`. Then, when you start the container with `docker start`, it will use the port mappings you specified during creation.

### Difference between docker run and start  
`docker run` means each time create new container to run redis  
`docker start` means run the current container no need to create another one  
