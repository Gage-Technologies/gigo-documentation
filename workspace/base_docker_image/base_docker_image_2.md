# Base Docker Image
>When and What To Use


### **What Is A Docker Image Anyway?**
</br>

A [**Docker**](https://docs.docker.com/get-started/overview/) image
creates a containerized environment for running applications. These
containerized environments allow developers to create a standardized
platform to build software. These applications can range from
something as simple as a Python script to something as complicated as an
Operating System.

### **How Does This Relate To Gigo?**
</br>

Gigo uses Docker images as a way to run a variety of higher-load
applications inside of workspaces. Some of these take the form of a
"Base Docker Image" that contains an operating system and if needed a programming language for the project that is hosted in the DevSpace.

### **What About A Non-Base Docker Image?**
</br>
Not all Docker images used in gigo contain an operating system.  If a project  needs a service like a [database](https://hub.docker.com/r/pingcap/tidb) (or any service that runs alongside a project) a DevSpace config can include a Docker image that runs inside the Base Docker image, and it does not need to contain an operating system.

</br>

### **What Does Using a Base Docker Image Look Like?**
![workspace_config_base_image.png.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/base_docker_image/workspace_config_base_image.png.svg)

<sub><sup>*this example includes a Base Docker Image provided by Gigo


The example above shows an example of an Ubuntu Base Docker Image. This image does not contain a programming language, and if a user needed a programming language in this DevSpace, the user would need to get a different Docker Image. The user could also install a programming language in the [*exec*]() block using a command line argument (this is not recommended since it can cause longer DevSpace start times).

</br>

### **What Are The Requirements For A Base Docker Image?**

A Base Docker Image must be compatible with [systemd](https://en.wikipedia.org/wiki/Systemd#:~:text=Systemd%20is%20a%20software%20suite,space%20and%20manage%20user%20processes.).  
Systemd is used to run the [Docker Daemon](https://dockerlabs.collabnix.com/beginners/components/daemon/) so we require that the Base Docker Image is compatible with systemd.
We highly recommend using docker images that come pre-installed with both systemd and dockerd but if it doesn't then the DevSpace system will install both on launch (this adds extra startup time to the DevSpace).
Since systemd and dockerd are not commonly provided in most docker containers, we provide a number of compatible docker images (including base images) that can be used.
If you would like to create your own docker image, we strongly recommend that you use one of the images provided by Gigo as the base of your docker image.

