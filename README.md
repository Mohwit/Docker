# What is Docker?
- Virtualization Software
- Makes developing anf deploying application easier
- Packeages application with all the necessary dependecies, configuration, system tools and runtime
- A standardized unit, that has everything the application needs to run.
- Portable artifact, easily shared and distributed.

## What problems Docker solves?
### Development process before containers?
- Each developer needs to install and configure all services directly on their OS on their local machine.
- Installation process differenet for each OS environment
- Many steps, where something can go wrong.
- If your app uses10 services, each developer needs to install these 10 services.

### Development process with containers?
- Own isolated environment
- Packages with all dependencies and configuration
- Start servie as a Docker containers using a 1 Docker command
- Commands are same for all OS 
- Commands are also same for all services
- Easy to run differenet versions of same app without any conflicts.
Hence, it Standardizes process of running any services on any local dev environment

### Deployment process before containers?
- Development team produce arrtifacts as well as installation instruction to configure the application to operation team 
- Ops team handles installing and configure apps and its dependencies.
- Installation and configuration done directly on the server's OS (error prone)
- Leads to miscommunication between dev and ops team due to textual guide of deployment.
- Human error which could leads to back and forth communication.

### Deployment process with containers?
- Docker artifacts includes everything that the app needs which includes not only the code itself but also all dependencies and configuration.
- Instead of textual, everything is packaged inside the Docker artifacts.
- No configuration needed on the server (except docker runtime)
- Less room for error 
- Run Docker commands to fetch and run the Docker artifacts.
- Only needs to install Docker runtime on the serveer.
## Virtual Machine Vs Docker

### How an Os is made up?
- Operating system is made up of two main layers.
    - **Kernal**
        - Kernal is at the core of every operating system
        - Kernal interacts between hardware and software components,
    - **Appliacation layer**
        - Communicate with Kernal to use the hardware 

### What part of OS does Docker and VM virtualize?
- **Docker**: Docker virtualizes the applications layer this means when you run a Docker container it actually contains the applications layer of the operating system and some other applications installed on top of that application layer this could be a Java runtime or python or whatever and it uses the kernel of the host because it doesn't have its own kernel.
    - Contain the OS application layer
    - Services and apps installed on top that layer. 

- **Virtual Machine**: VM has the applications layer and its own kernel so it virtualizes the complete operating system which means that when you download a virtual machine image on your host it doesn't use the host kernel it actually puts up its own.
    - Contain Kernal and application layer.
    - Virtualizes the whole OS 


### What affects has the diiference?
**Docker**
- Docker images, couple of Megabytes
- Containers take seconds to start
- Conpatibles with only linux distros (Docker desktop is used to run linux based containers in Windows and MacOs)


**Virtual Machine**
- VM images, couple of Gigabytes
- VM's take minutes to start
- VM is compatibles wth all OS