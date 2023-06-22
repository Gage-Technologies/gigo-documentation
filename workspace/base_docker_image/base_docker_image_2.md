# Base Docker Image
>When and What To Use

</br>

### **What Is A Docker Image Anyway?**
</br>

A [**Docker**](https://docs.docker.com/get-started/overview/) image
creates a containerized environment for running applications. These
containerized environments allow for developers to create a standardized
platform to build software with. These applications can range from
something as simple as a Python script to something as complicated as an
Operating System.



### **How Does This Relate To Gigo?**
</br>

Gigo uses Docker images as a way to run a variety of higher load
applications inside of workspaces. Some of these take the form of a
"Base Docker Image" that contains an operating system and if needed a programming language for the project that is hosted in the workspace.

### **What About A Non-Base Docker Image?**

Not all Docker images used in gigo contain an operating system.  If a project  needs a service like a [database](https://hub.docker.com/r/pingcap/tidb) (or any service that runs alongside a project) a workspace config can include a Docker image that runs inside the Base Docker image, and it does not need to contain an operating system.


</br>

### **What Does Using a Base Docker Image Look Like?**
![workspace_config_base_image.png.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/base_docker_image/workspace_config_base_image.png.svg)

<sub><sup>*this example includes a Base Docker Image that provided by Gigo


The example above shows an example of an Ubuntu Base Docker Image. This image does not contain a programming language, and if a user needed a programming language in this workspace, the user would need to get a different Docker Image. The user could also install a programming language in the [*exec*]() block using command line argument (this is not recommended since it can cause longer workspace start times).

</br>

### **What Are The Requirements For A Base Docker Image?**

A Base Docker Image must be compatible with [systemd](https://en.wikipedia.org/wiki/Systemd#:~:text=Systemd%20is%20a%20software%20suite,space%20and%20manage%20user%20processes.).  
Systemd is used to run the [Docker Daemon](https://dockerlabs.collabnix.com/beginners/components/daemon/) so we require that the Base Docker Image is compatible with systemd.
We highly recommend using docker images that come pre-installed with both systemd and dockerd but if it doesn't then the workspace system will install both on launch (this adds extra startup time to the workspace).
Since systemd and dockerd are not commonly provided in most docker containers, we provide a number of compatible docker images (including base images) that can be user.
If you would like to create your own docker image, we strongly recommend that you use one of the image provided by Gigo as the base of your docker image.

