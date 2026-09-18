1. What is a Docker bridge network?
   bridge network are the ways docker continer communicate to each other . when we create a docker contianer it uses its default bridge to coonect to other contiaers on the same network
2. Why was a custom Docker network created in this task?
   it was created to make sure that the 2 containers can comunnicate through a private cooneciton . for eg we dont want out db to be inthe same newtork as all othe other ones so what we do isthat only the backed can talk to the db backend talk tot he froentedn that is howwe do that do with db and backend there is a private custom netwrok
3. Why does `localhost` not work for container-to-container communication?
   localhost mens inside the container it can only reach inside the contiear . it uses somethign like lo to loop back into the device .
4. Why does using the container name `mysql-net-demo` work?
   it work becasue for a custom bride the docker mangaes the dns . so it will be mapped to it ip by the docker
5. How does Docker resolve one container name to another container on the same network?
   docker intenrally manages a dns on the contianers in the same newrork . so it will be resollved to it ip
6. Why is using container names better than using hardcoded IP addresses?
   it is becasu container ip can be chaned if a container cracsed and restared the ip wil lchane but the names wont that is why we use that name
7. What did `docker network inspect app-net` show you?
   it shows me details about the network. like what are the contaienrs using that ip . and a lot of it
8. What did `docker inspect mysql-net-demo` show about networking?
   about the newtork it will show me what kidn of conection isthis is this bride or host or custom bride . then the ip , a details about the ip
9. Why was PhpMyAdmin exposed to the host, but MySQL was not?
   it is becaseu we dont want to expose db to the pulic or to any other continers that did wat it . so only phpmyadmin can access it . browser need to reach the pgadmin but the sql cn only be reaced by the pdadmin . it increaseas the securetiy and redice the attak surface
10. What is the purpose of `docker port` in this task?
    it tells use which host port is mapped to container .so we can check that is there any port mapping in the sql is it has we need to change it adn we can check the prot mapping on the pgadmin
11. What is the purpose of `docker stats` in this task?
    it is used to check the resrorce usage . we can tell which one it usign a lot of the resorce if one contiaer is using a lot we can restrict or do somethign about it
12. What would happen if the two containers were not attached to the same network?
    it they were not attached to the same netwekr then they cant talk to each other . it need some router or shared spce to communicate
13. Why is this task important before learning Docker Compose?
    it is importanc becasue doc
14. How does this task reflect real multi-service application design?
    compose is about mutlipel contaienr on teh same nework . not alsowsy maybe same but the contiaer start at the same time we write it abou tin the yaml file . so undersand the task will help to udnersand how they are talk to each other in thesame newtokr
15. How does this task help later in debugging service connectivity problems?
    it wil helps it the cooneciton is not gettin i can inpec tthe network . look at the port is the credectial are correct it will later help in the docker compose with mutliple containers
