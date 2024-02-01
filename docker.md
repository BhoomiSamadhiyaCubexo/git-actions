# new repo
***DOCKER-*** 
Docker is an open platform for developing, shipping, and running applications. 
Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.
Docker reduces the delay between writing the code and running in production 
Advantageous for shipping, testing, and deploying code.
Docker provides the ability to package and run an application in a loosely isolated environment called a container. The isolation and security lets you run many containers simultaneously on a given host. 

***Docker provides tooling and a platform to manage the lifecycle of your containers***:

Develop your application and its supporting components using containers.
The container becomes the unit for distributing and testing your application.
When you're ready, deploy your application into your production environment, as a container or an orchestrated service. This works the same whether your production environment is a local data center, a cloud provider, or a hybrid of the two.

***Docker use case***
1. Fast, consistent delivery of applications
   - streamlines the development lifecycle
   - CI/CD workflow using containers
2. Responsive deployment and scaling 
   - Docker's container-based platform allows for highly portable workloads.
   - Docker containers can run on a developer's local laptop, on physical or virtual machines in a data center, on cloud providers, or in a mixture of environments.
   - Docker's *portability* and *lightweight nature* also make it easy to "dynamically manage workloads", scaling up or tearing down applications and services as business needs dictate, in near real time.
3. Running more workloads on the same hardware 
   - Lightweight 
   - Fast 
   - viable over hypervisor based VM 
   - cost effective alternative of hypervisor based VM
   - perfect for high density environments 
   - perfect for small and medium deployments where we need   more from fewer resources

***Docker architecture***
   - It uses a client-server architecture 
   - Docker client >-----communicates to -----> Docker daemon 
   - Docker daemon => heavy lifting of building, running, and distributing Docker containers
   - Docker client and Docker daemon can run on same host machine or remotely to each other
   - Docker client >-- communicates using REST API over UNIX sockets or a network interface ---> Docker daemon 

***Docker Daemon***
   - _Docker daemon aka dockerd listens for Docker API requests and manages Docker objects such as_ "images, containers, networks, and volumes."
   - daemon can connect to other daemons too, to manage docker services

***Docker Client***
   - The Docker client (docker) is the primary way that many Docker users interact with Docker.
   - When you use commands such as _docker run_, the client sends these commands to dockerd, which carries them out.
   - The docker command uses the Docker API. 
   - The Docker client can communicate with more than one daemon.

***Docker Registries***
  - It stores Docker images
  - "Docker Hub" is a _public registry_ that anyone can use, and _Docker looks for images on Docker Hub by default_. You can even run your own private registry.
  - *docker pull or docker run* commands, pulls the required images from your configured registry.
  - the *docker push* command,  pushes your image to your configured registry.
  
***Docker Objects***
   - images, containers, networks, volumes, plugins, and other objects.


***Docker Images***
   - Read-only template 
   - instructions to create a Docker container
   - one can use existing images by pulling them
   - or can also create one using simple syntax 
   - *_each instruction in a docker file creates a layer in the image_*
   - when we change the dockerfile and rebuild it, at that time only those layers rebuild which have changed, others remains same.
       -- This makes images *lightweight, small, and fast*
    
***Docker containers***
   - It is a runnable instance of an image.
   - We can create, start, stop, move, or delete a container using the Docker API(Application Programming Interface) or CLI(Command Line Interface)
   - a container is relatively well isolated from other containers and its host machine.
   - When a container is removed, any changes to its state that aren't stored in persistent storage disappear.

    **docker run -i -t [imagename] /bin/bash** 

   - A container is an isolated environment for your code.
   - This means that a container has no knowledge of your operating system, or your files.
   - It runs on the environment provided to you by Docker Desktop.
   - Containers have everything that your code needs in order to run, down to a base operating system.
   - You can use Docker Desktop to manage and explore your containers.