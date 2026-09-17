1. What is the main process inside a Docker container?
   it is the main process the container runs when it start the container. mostly we put it in the cmd like python app.py or somerthing .
2. Why does a container stop when the main process exits?
   the purpose of a contaienr is to run a process inside isolatoin . so if there is no process to run then there is no need of the container that is why it stops
3. Why did the busybox container exit immediately?

   it exits because the busybox process finshed its exectuion that is the reason it exited imedialty .

4. Why did the nginx container keep running?

   it is a long running process . it listen in the container port 80 . so it didnt end . since the main process lives the container also runs

5. What is the difference between a normal exit and a manual stop?
   a normal exit happens when the process finshes its exection liek busybox . the exit code will be 0 .
   a manual stops happens when we use docker stop or docker kill ionthat time we are stoping the container by eleminationg the process .
6. What does exit code 0 usually indicate?
   it indiates that the process exictued and gracefully stops its exectuion when we do docker stop we also get 0 the reason is that the process was not forcefull termilnated like docker kill but gracefull
7. What is the purpose of docker logs in lifecycle debugging?
   docker logs helps us to indentify why the container might have stoped . liek it maing be an error from teh application or someone manulaly kills it we can find it there
8. What is the purpose of docker inspect in lifecycle debugging?
   inspect tells us the information about the container . like exit code , port , state , a lot of thing will be there we can find what the problme is liek if we cannot reac thte contaiern we can check the port
9. What is the purpose of docker top?
   docke top allows us to look into what are the processess currently running inside of a container .
10. What is the difference between docker start and docker run?
    start will start the conaitner that was stopeed or exited before
    socker run is to create a new continer from the image
11. What is the difference between docker stop and docker rm?
    docekr stop sots the conainer but the conainer will be there . rm will remove the container from teh system
12. What is the difference between docker start and docker restart?
    docker start will start the contiaer and restart means that it will stop and start it again so 2 operatoin in 1 command
13. Why is it important to understand lifecycle state before debugging production containers?
    if we dont kwno the lifecys of the container we will not be able to reduirect liek if a contier state tells us whre to look next ther eis not point it usign top in a exited contienr
14. How is a container lifecycle different from a virtual machine lifecycle?
    for a vertual machine it has its own guest os so .it it not made to just run a process adn exit so after the process temrintaed it will stiill run the os . but the continer will stop after the main process dies
15. How does this task prepare the learner for real Docker troubleshooting?
    it heps us to understand how to degub . i was able to undersand a lot about the lifecycle and where to look depending on out problem . what to look first
