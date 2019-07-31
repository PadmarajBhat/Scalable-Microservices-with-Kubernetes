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
