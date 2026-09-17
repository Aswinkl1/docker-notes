1. Why are Docker containers stateless by default?
   containers are stateless becasue they are disposibele and they are esislty can be recreated . data you write in teh container will store indie of the conainer and when it stops it is distored
2. What is a Docker volume?
   it solves the problem of data persistense . volume is docker managed storage in out host os . it can be manged by docker and it creates a logical memeory space and mounts it to it
3. How is a Docker volume different from normal container storage?
   normal continer storage are volatile which mena shtat if the contaienr stops it will be deleted voulums persist through tehse it can be acced by mulitple container or after contiern restart it will persit
4. Why does MySQL need persistent storage?
   db need persistent becasue the data cannnot be recreated . the user data that hte user enters or any kind of data that cannot be recreatead that is why it need persistent stoarge
5. What does -v mysql-data:/var/lib/mysql mean?
   it means that mount this volume to this destinatoin . myslql-data is the voulme and /var/\* it is thedestination inside of contianer
6. What is the purpose of docker volume create?
   it will create a volume that is managed by docker . it is like a disk space that is managed by docker .
7. What is the purpose of docker volume inspect?
   it is to know the details abou the volume like sourse , mod ,
8. What did docker inspect show about the MySQL container's mounts?
   in the countainer mount it has details about the volume . it wil show which volume is attached and wha is the destination and all of that details
9. Why did the data survive after the first container was deleted?
   the data suvies becase the volume is stored outside the conatiner . in host os or in anytoerh storge servie or anywhere
10. What is the difference between deleting a container and deleting a volume?
    a contianer can be recreated usign a image but a volume cannot be recreated
11. Why is it dangerous to run databases in containers without persistent storage?
    if you run a db without persisenrs storage the moment you stop or your process container crashed the data stored will be lost that is why it is danerours
12. Why was it helpful to use docker exec in this task?
    with exec we where able to inteact with the mysql which is runnign insde the contaienr . it was helful to verify that the data is there
13. What did docker stats and docker top show you?
    docker stats show me the resorce usage liek cpu , memoery , i/0 disk and top show me the ruunig process it was sql main process
14. How does this task prepare the learner for Docker Compose and Kubernetes storage later?
    it prepares that storage should be outside of containers lifecycle . in compose and kluberntes we do the same thing we will store the storage outside of contaienr
15. What would happen if the volume was removed after the task?
    the data stored inside the contiaenr is lost . rm the volume means that data is lost
