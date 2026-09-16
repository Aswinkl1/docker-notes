

### Why did the NGINX container keep running while the busybox ontainer exited?

the life of a container is decided by the main process that is running inside the container . for the busybox is just need to print something and the program ended . but for the nginx it is a long running process so the container keep runnign becasue the process inside of the container is running 

### What does detached mode mean in Docker?

detach mode means that the container runs in the background . if we didn't run it in the background the output of the process running will be shown in the terminal . 

### What does -p 8080:80 mean exactly?
it means forward the incoming request comming to the port 8080 on the host os to the port 80 on the container . 

### What is the difference between host port and container port?

host port is the port in the machine it is running . 
container port is the port that is inside of the container . 

### How did traffic from the browser reach the container?

the trafic goes like from the browser to the host port and from there it connect with the docker network and it forward that to the container port . 


### What is the purpose of docker logs?

it will show the output produced by the containers application . it is can be used for debuging like why the process end or wha is happening inside that process 

### What is the purpose of docker inspect?

it gives us a detailed overview of containers . like information such as port , status , env etc . by inspecting we can check all the details about that perticular container . 


### What is the purpose of docker top?

top is used to see what are the process running inside the container . when you work with the top like docker top contienr id. you will see details that is in the perspective of the host os .can be used to kill , and mange those process . can used to find the and debug problems in individal process . 

### What is the purpose of docker exec?

it lets us to run commad inside of a runnign container . like we can run commads like ls or sh or bash and it will run those in the container . 


### What is the purpose of docker stats?

the purpose it to monitor the resorce usage of perticular container . we can see the cpu , memeor , disk , network usage of the container , 

### What did you observe about CPU and memory usage for the container?

i understood that the cpu and memeory usage was really small . it stated to spike when i send multiple request at th same time but event hat was negligibel . i ran the container for more that 10 hours and the cpu usage was the same so just becasue a container is runnign does mean it take a lot of resorce but it does take a small amount of resource . 

Why is checking resource usage useful in production?
the reson is that in the producatino there might be mulitple containers int he same host so if one applciation due to some but is taking a lot of memory other containers might crash that if why we need to check the resorce usage . 



### What happened when you ran docker stop?

when we ran docker stop the container will stop its exectution . the doker will say to the process inside the contaner to stop and when it stop the container also stops it it dint stop before the timeout the container forfully stops it . 

### Why does removing the container not remove the image?

because a container is a instace of an image from one container we can create as much instance as we want . they are both diff things . if you want to rm the container image then use rmi 

### How does this task help later in Docker debugging and operations?

this task will help me a lot becase it showed me how to check the contaier health  . is it runnign , how to get inside the contaiern . how much resorce is it using . what are the process runnig inside of that container . 


