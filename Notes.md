* what is docker?
  * It manages the application by containerizing it
  * each container has its dependencies bundled wih it and hence it is independent of the other container in the docker. Picture of a docker ship with huge container fits the definition.
  * containers can be run on any system which has the docker running without worrying about the environment docker is installed.

* Tradition approach to install a software allows us to have one version and might not allow us to have multiple instances of the application.

* Containers are like virtual machine but they are light weight. They run on the same os and hence light weight
* Whenever, docker image is built and pushed , it goes to the public repository but that can be changed. Publishing a repository makes it available for pulling the image from anywhere, so that the decentralized server can leverage a single location for images.
* Docker does the containerization through the dockerfile. This file contains info like the files required for the application and also the entry point among them.
 * for eg: if you want any packages to be installed prior to an python application run then it has to be mentioned in the docker file. In this case, dockerfile should have pip install command through requirements or requirement file
 * dockerfile should have the exact command to invoke the app like 
   ```
   # Run app.py when the container launches
   CMD ["python", "app.py"]
   ```
* Docker run command not only runs the application from the entry point but also downloads/pulls it from the central repository.
* Some documentation read at : https://docs.docker.com/get-started/
* like class and object we have docker image (stateless) and containers (with state). Images are created through docker build. It is images that are pushed to repository and pulled from it. When we run the images we have containers.

* Swarm:
  * Swarm is an approach to have load balancing of application. swarm manager controls swarm worker node
  * interesting read https://thenewstack.io/kubernetes-vs-docker-swarm-whats-the-difference/
  * https://hackernoon.com/kubernetes-vs-docker-swarm-a-comprehensive-comparison-73058543771e - indicates docker swarm is better in couple of aspects like number of supported nodes and auto load balancing of the traffic between containers withing cluster.

* Moving towards serverless computing in Google Cloud:
  * https://cloud.google.com/functions/use-cases/ - serverless has 3 types option in google cloud. This is talks about function. Majorly for backend applications
  * https://cloud.google.com/appengine/- serverless web and backend application 
  * Nice article on google run: https://blog.iron.io/google-cloud-run-alternatives-and-review/
  


 * Diving into parallel computing: https://www.machinelearningplus.com/python/parallel-processing-python/
    * https://docs.python.org/2/library/multiprocessing.html#module-multiprocessing : I guess the process/thread creation is abstracted in ray. This api provides the low level of multiprocessing like start join and pass objects between processes.  
    * Ray is not for windows operating system : https://stackoverflow.com/questions/54588066/cannot-install-ray
    
    * https://djangobook.com/scaling-django/ - django scaling explained in diagram
    * Nice article of imap, starmap : https://medium.com/apteo/multi-processing-in-python-ee0ce73a459b
      * imap : returns an iterator instead to complete sequences; saves memory
      * starmap: takes multiple argument unlike map and imap.
        * here syntax indicates that it is one argument to starmap but each element in the list can be a list of arguments to calling function [list of list]. Outer is same as the arguments to map and imap but inner list is arguments to map functions.
  
 * another paradigm of coding/ concurrent execution
     * https://www.geeksforgeeks.org/multithreading-python-set-1/
       * multithreading provides capability of the concurrent execution of the set of codes within the scope of process.
