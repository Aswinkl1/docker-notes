1. Why is reducing Docker image size important?
   reducing the image size is very improtent . it is easy to transfer compare to big size . need less storage . and when we create a new version for the image it becomes to much when we have mulitple version
2. Why is a working image not automatically a good production image?
   working image means that the application can run but the image may be large in size like for a small application the image is 2 gb then it may not need all of it . so optimzation and sercurly is also improtent when it comes to production
3. What is `.dockerignore`, and why does it matter?
   it help us to rm the unnessasaey files . like the folder may have .git .env file like that logs etc we dont need that in our build . using .dockerignore help us to reduce the image size and build time
4. How does `.dockerignore` help build performance?
   first one is that it . if we can reduce the uncessary file it mean that fewer files for build that improves the build time and size . next is files like log will be constendly chagne so if that is there in the build then later build need to change which is unnessary cache invalidation
5. Why does Dockerfile instruction order matter?
   the order matter becasue each layer is cached . in the next build if the presnet layer adn the previons layer does chagne we can u se the cachce it imporove tiem build time . if we copy the app file first then whent he code chane all the about thing need to buidl again
6. What is a multi-stage Docker build?
   a multi stage docker build is chagne the build into multiople stages so thtat we can reduce the size of final image . while building we may beed compiler or build tools etc but when we actually run the code we dont need that so we can only get the nessasary artifctes to the image so that we can reduce the size
7. How does a multi-stage build differ from a single-stage build?
   single state build everying in one state no transfer of data to another stage all the tools ionstalled will be there . when it comes to a multi stage the build has mulile stages and we can esecntially reuduce the size of the image and only put he nessasary thing in there .
8. What kinds of files should not end up in a production runtime image?
   file like .gitignore , .git , logs . etc these files should not be there becasue we dont need them to run out application .
9. What changed between the original and optimized image?
   the chagne is that in the orginal image the build was also there so the image size was large but the optimized has only the nessary thing to run the applciaton and has mulit stage that increases the image qulity and reduce the size
10. What did `docker history` help you understand?
    it made me undersand which are the layers that take out a lot of space and time if optimizatino can be done in that layer or chagne ing layer will improve it then we can do that
11. Why should runtime behavior remain unchanged after optimization?
    because the optimization should effect the runtime application . the way we did optmizatoin is by rm the unessasary file and dependecy not the nessasary onece that is why it did effect the runtiome behavior
12. How do optimized images help CI/CD and deployments?
    it improves a lot . first is that an optimized image is easy to pull and push . it the image is effiently orderd it makes the ci cd used it cache rather than build it again .
13. Why does this task matter in real DevOps work?
    in the real devops we always try to make the image more efectiend and more optimized if we can . this step like history , multi state these thign are the once that we do at that time
14. What would happen if you optimized the image but forgot to verify the application?
    if we forget to verify the application then we have an optimized image but a broken applciaton we should alwasy make sure the application run propertly after and before optmizatoin
15. How does this task prepare the learner for real production container workflows?
    in the real world we are doing the same thing with bigger applciatno here i ahve done it with 100mb in teh real work we wil do it with 1 db image size at that time we will alwasy try to optmize and go through these same steps to undersan the build and reduce the size and increase the effectency
