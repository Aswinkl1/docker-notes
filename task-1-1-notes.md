



###  What is the difference between a Docker image and a Docker container?

docker image is like a blueprint and container is like an instance that we created usign that image . from one image we  can create as many containers as we want . 

### What command did the busybox container execute?

the busybox container execute commands that i passed to it like ls or echo . what essentally happen was when we run the container  a new process is created inside the container to run the ls command and after executing the command the process is terminated and after the process is terminated the container is also stoped . 

### Why did the container stop after the command finished?

a docker container can only live when there is a process running inside of that container . so when the command finishes there is no process running inside of that container . 

### Why does the container not appear in docker ps but appear in docker ps -a?

docker ps shows us all the  current running container and docker ps -a shows us the current and stoped containers . 
since the container has stopped its execution due to it process finished execution the container stoped and it can only be seen using docker ps -a 

### Why is a container exit not always an error?

 the reason is that container exits is always not an error because as you know if the process successfully execuetes and terminated inside the container the container will also stop . 
 that is why we check the logs so that we can see what the process print in the terminal before terminated 


### What is the purpose of docker logs?

the purpose of docker logs is that it show the output that was produces by the main process .
so with the docker logs we can inspect what is happeing inside the container . so we know that does it exectues without any error . 

### What is the purpose of docker rm?

rm is a command that is used for removing the container . by passing the containerid as an argument we can rm the container from the device . 

rmi is used for removing images from our device 

### Why can multiple containers be created from the same image?

becasue an image is just a reusable template . we can create as many containers as we want from an image . an image containes all the thing that the application need to run and it is isolated too.


### What is the main process idea in a container?

the main process of a container is the process that runs inside the container . there can be mutliple process runnign but there will alway be a main process . 
when we do with ls . a new process is created by the inside the container to run the ls command 

if there is no process is running the container can be stopped becasue others can use the resorce . 

### How does this task help later when debugging containers in production?

when a container is down in producation i can check the current ruuing containers and stopeed containers . by getting the id of the container that has stopped i can check the logs . 
by checking the logs i can find out why the container stoos 
