
### What is Docker?

Docker is a platform that help us to package application with their dependencies . 
we can create a container that shares the same host kernal . by using namespace and cgroup docker create isolation for that perticular application . 

### What is the Docker daemon, and what is its responsibility?

Docker daemon is a background process that runs in as a service . this is the service that listen to the rest api of the docker and manages these containers . 
the responsibilites are 
create and delete containers 
pulling images from the registory 
basically the docker daemon is the heart of the docker . 

### What is the Docker CLI?

Docker cli is a program that interact with the user through command line . when we type `docker ps ` or similar commands docker cli communicates with the docker daemon through rest api . after the daemon exectures the command it will send back the output to the terminal .

### How does the Docker CLI communicate with the Docker daemon?

 they communicate usign rest api  . when we type some commad like docker build  the docker cli will send a request to the docker daemon and it uses the rest api to do that . 
 internally they use unix sockets for making that call . 

### What is a Docker registry?

docker registory is a place where we can store and download docker images . 
there are a lot of docker registry there like docker hub , amazon ecr etc 
by storing it in the registry we can share the docker image with others. 

### Explain Docker architecture in simple terms: client, daemon, registry.

in simple terms  . client is the one that interact with the user . client talk to the daemon who listens to client and registry is a place where we can store the images so that we can share it .  **client is like a waiter . deomon is the chef and registry is the fridge** 

### Why is Docker considered lightweight compared to virtual machines?

comparing to virtual machines dockers are lightweight because they share the host kernal . vms does share the host os . over the host we install somethign like hiperviser and we insall the guiest os . for each guiest os we have separate kernal  . which makes them really larger inside comapre to docker . 

docker shared the host os . and docker can be build from a very small base image by removing the unwanted things . 

### What parts are packaged inside a Docker image, and what parts are shared from the host OS?

inside of a docke image there is application and its dependency , userspace os dependency . and the other parts it need to run . it shares the kernal of the host os . so imagine  node application run on the docker and it need to open a file it will ask the host kernal to open the file . 

### Why did hello-world run and then exit?

a container will normaly run when the main process is running . if the main process is executed and stoped its execution the container will stop itself . that is why the hello world program stops .

### Why is verifying Docker setup important before starting real container tasks?

we need to make sure that the foundatoin is strong before building . so when we create docker images for the application we might get into erros from the applciantion if we did not setup or chek the docker setup before  the problem might be from the docker setup . 
a fauilty setup will show errors even if your code is right 
