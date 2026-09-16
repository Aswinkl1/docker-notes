1. Did the broken Dockerfile fail at build time, runtime, or both?
   the build did not fail becasue the flask and other dockefile was right but just not for this application . in the runtime i got an error becase that pertucaular contaienr cannot run this application
2. What did you observe during the first docker build attempt?
   it pulled pythom slim , created workdir copy code and install fask .
3. What did you observe when running the broken container?
   when runnign the broken container it did not start . it was like the program has finished exectution but later when i check the log i realize that it was an error
4. What did docker logs reveal?
   the logs revel that the container did not stop becaseu it finshed the exectution of the program rather it was an runtime error .
5. What did docker inspect reveal?
   inspec revel that the status is exited adn the states code is 2 which mean that it has some error while running . port mapping was problem too
6. What exactly was wrong in the original Dockerfile?
   in the orginal file we wher not copy the req.txt file adn we independly install the flask which may has diff version . we where not expossing any port so it as not listenign .
7. Why is installing dependencies from requirements.txt better than installing them ad hoc?
   the requirement.txt defines what the application need . specfic verson of dependecny if we install from ad hoc they might give you new versoioni but that may not be supported by the applicaotin . that is why we always install from req.txt
8. Why must required files be copied into the image explicitly?
   container doest have access to the host of file system . so we need to specify that which are theonce that we need to put in the container
9. What specific changes fixed the issue?
   i first copy the req.txt then install dependcy from it . rm the flask installation then expose the port by doing this i was able to fix this
10. What is the difference between a build-time problem and a run-time problem?
    a build time problem happend when building a image . like spelling mistae syntaz error ect .
    a run time error occur when you run the application
11. Why is docker logs important in container debugging?
    logs are importent becaseu the container in detached mode does print anything adn when we know that the container is nto ruurnign we cannot sometimes reproduce that prblem like if the problem only happen once in 1 house we cannot wait for it so easily we can check the logs and undersad what hte problem is j
12. Why is docker inspect important in container debugging?
    docker inspect show the imported details that it it runnign or which image doe sit use and what is the exit status code from that we can find what is the problem and fix it then
13. Why is docker exec useful during debugging?
    it was usefull becasu we where able to check if all the file areinside of the contaier andfind out that the reqierment.txt is not there and we can fix that .
14. Why should you apply minimal fixes instead of rewriting everything blindly?
    if we rewrite evethign we wont be able to find what was wrong so if we maek minial chagne we will be ale to find what cause the previos error and learn froem it .
15. How does this task help in real production Docker troubleshooting?
    this helps becasue when we build something there wil be errors . adn this task help me to debug and find the problem and how to fix it
