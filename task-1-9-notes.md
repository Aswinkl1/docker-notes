1. What is Docker Compose?
   docker compose is a tool that allows us to run multiple containers at the same time . it 1 conatiner is dependend on another we can specify that too . it sovles the problem of running muliple container manulaly
2. Why is Compose preferred over manually running multiple containers?
   the first reason is manually runnig multipel container is very hard work and we need to run the containers in a dependencly order if they have any remmebering and doing that is hard . the developer need to alwasy know about these chagnes adn configiration while running .
3. What is a service in Docker Compose?
   a service could be said as a template to how to create a container for a perticular part of you application . it is like db is a servce , redics is another servece it is like that
4. How does Compose handle networking by default?
   by default docker creates a new private nework for the compose and communicates using services .
5. Why does `db` work as the database host for WordPress and PhpMyAdmin?
   we use db becasue in compose it is not named by container rather servies . adn htis db can only be reached by these services too . db is not published
6. What is the purpose of `depends_on`?
   it means that htis contaier or serive is depended on another service so make sure to start that service before you start this one
7. What is the purpose of the named volume in this task?
   it make sure that the db data is persistand . when we do compse down it rm all fo the contier so if we just store the data in that it will be deleted . that is why we use volume for persistance storage
8. What did `docker compose logs` help you observe?
   in that all the logs of the servies in one place so it help me to unstand wich one is havin gproblem .
9. What did `docker network inspect` reveal?
   it reavel that these 3 contianer is using the same network . which was created by the compose
10. What did `docker volume inspect` reveal?
    it tells about the volume and which are the continers that it is connected to it .
11. What is the difference between `docker compose up -d` and `docker compose down`?
    up -d is craete and run the contienr in detached mode . but down mean stop and remove the container
12. What remains after `docker compose down`, and why?
    it rm all the contianer in the compose the newtwork other than volume it removes all of it . the reaosn it rm is that only the voulme matter becasue there is no point in storing the continer it cna be recreated
13. What happens if `docker compose down -v` is used?
    what it does that ist hat it delted the volume with the container too .
14. Why is this task important before learning more advanced orchestration platforms?
    becaseu the kubernetic or orchastration platforma are build on top of this idea of managing muliple contianers . so undestandtnign the base will help me to graspe that consept easilly
15. How does this task reflect real multi-service application management?
    this is how real rervies work . moslty in real world we put diff parts of the servie in diff contaieerns as diff services . in a muli service applicaton the db will not be publicshed to the host adn only the backedn adn the fronedn will be .
