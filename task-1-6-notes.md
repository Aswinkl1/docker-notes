1. What is a Docker image layer?
   docker layers can be said as file system . it works like this . when we run a docker file it has diff line . each like like form or wordir or copy each creates its own layer and the layer below it just add with the layer created by the above . these layers can be reused not even in diff images .
2. How does Docker decide whether a cached step can be reused?
   docker will check weather an instuction or its input has changed and if it isn't then it will be resused . and the main thing is if a insrectoin is not reusing the instruciotn below it canot be reused too that is why the order of the instuctoin matter . if you copy the entire application at the begining then install the packaged when you change the code it will need to run theinstall cmd again which may not have changed much it channot use the cache
3. Why was the second build faster when nothing changed?
   it was faster becasue since nothing chages it use the same image id . everhign was cached .
4. Why did changing app.py rebuild fewer layers than changing requirements.txt?
   it is becasue in a dockerfile the order of layers matter . when you chage the app.py only the layer which used that app.py and all the layer bellow it need to rebuild again .other can be used from teh cache
5. Why does changing one step often cause later steps to rebuild too?
   the reason is that when it goes to the next step it check does the above layer file system chanes then if it does it will rebuild with the new file system and that continues
6. Why does Docker process the Dockerfile top to bottom?
   it is because each layer is stack about the older layer . when you say workdir /app all the other layer work inside the /app folder . that is why the order matter more
7. Why is requirements.txt usually copied before application source files?
   the reason is that the requirements .txt does not change ofen compae ro the applicaotn source file . in docker if a layer chanes all the layer below it need to build again so it we consider that if we copy the application source file then we need to biuodl the reqirement .txt every single timethe code changes
8. Why should frequently changing files usually be copied later in the Dockerfile?
   becaseu when a layer change all the layer below it will change if we need to reduce the build time and use the cache we nee to only copy the frequeenlty chagne file at last
9. What does docker history help you understand?
   it helps us to undersand how each layers are build . how much disk each layer is using . in what order does each layer it in
10. How does Docker build cache help in CI/CD pipelines?
    in cicd it helps with resuing the cache from the previons build so that it can be faster . cicd runs on the uses diff runner evertime but they have the same common cache so it will reuse that cache .
11. Why does Dockerfile instruction order matter in production?
    it matter becasue it will affect the image size , build speed etc. if we put the reqirement.txt before the copy sourse code . evertime a tiney amoutn of source code chanes we need to rebuild the requiremtns again . .
12. How does this task prepare the learner for later image optimization work?
    this task help in a lot ofway becasue the it help me to undersand about how the docker file executes and how to redue teh since and buidl time of the docker .
