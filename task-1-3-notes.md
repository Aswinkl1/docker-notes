### What is a Dockerfile?

docker file is a set of instuction to create a docker image . by executing this file docker will create a image

### Why is a Dockerfile required when packaging an application into an image?

becasue for every application the requeirements are diffrent that is why we can write how to containerize our application inside of docker file and docker can execute . for eg . some application need to expose port 5000 and for some 3000 that is the diff .

### What does docker build do?

it creates an image from the docker file .

### What does docker run do?

it creates and startes the container using that specific image that we mentioned

### What is the purpose of requirements.txt in this task?

it says all the application requirements of the app . by instaling the requrements we can run teh application .

### Why must the Flask app bind to 0.0.0.0 inside the container?

the reson is that if it is not binded to that ip we cannot acces it from the outside . we can expose the port but we cannot accessit that is why we open it like that so that anyone can connect to it .

### What does -p 5000:5000 mean?

it basically forward the trafic that comes to host port 5000 to container port 5000

### What is the purpose of WORKDIR in the Dockerfile?

it sets the current working diectory for the application

### What is the difference between RUN and CMD in the Dockerfile?

the diff is that run exectues when the image is begin build . like get the dependcey like that

teh cmd command it exectued when teh continer starts . it will be the commad to run our applicatoni

### Which project files are included in the Docker image?

inside of the docker image there are 2 files requirements.txt and app.py . both are really esential for the buildind of the project .

### What is the purpose of docker logs in this task?

the purpose is that i can check what is happeng inside the container when the app runs . it help me with debuging .

### What is the purpose of docker inspect in this task?

docker inspect help me to undersand the port bindings , state adn all the informatio of the container .

### What is the purpose of docker exec in this task?

exec help me to interact with teh container from the inside . it help me to chekc is the file are copied right

### Why did the Flask container stay running?

becseu it the applicaonit is build to lisen till the process is killed or the applciaton stops . it was a long runnign process
Why does removing the container not remove the image?
the reason it that container and image are 2 diff things . contaier is an instace adn removeing and instace will not delete the image

### How does this task prepare the learner for production container workflows?

it helps me to build an write my own docker file . in the productoin we will write the docker file of perticalr applicaiton and each of tehm will be uniqer . i got to build the applicaton as well .
