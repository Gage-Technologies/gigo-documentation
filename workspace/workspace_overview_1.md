# DevSpace Overview
>#### How Workspaces... Work


A DevSpace is a development environment designed for a specific project
in mind. The level of specificity is dependent on the user or
organization that designed them. This can range from a general DevSpace
that is designed for any project, or a DevSpace designed to run a
specific project based on a programming language and specific packages
needed to run the project.


</br>
</br>






### **Architecture**


![GIGO Workspace Overview-transparent.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/GIGO%20Workspace%20Overview-transparent.svg)

<sub>*the above illustration shows the basic architecture of the DevSpace system

</br>


A DevSpace consists of a *DevSpace configuration* file that details the
following:
- [**Base Docker Image**](../workspace/base_docker_image/base_docker_image_2.md)
- [**Resources Specified**](../workspace/resources_specified/resources_specified_3.md) (allocated resources for environment)
- [**Vscode Extensions**](../workspace/vscode_extensions/vscode_extensions_4.md) (for additional editor support) *
- [**Additional Docker Services**](../workspace/docker_service/additional_docker_service_5.md) / Images (e.x databases, web
  services, additional software, etc.) *
- [**Command Line Executions**](../workspace/command_line_arguments/command_line_arguments_6.md) (to be run when docker image is
  started) *

<sub>the above bullet points marked with * indicate an optional addition

>The DevSpace config is based on a [*`yaml`*](https://www.redhat.com/en/topics/automation/what-is-yaml) format.

A DevSpace config instructs the *Gigo DevSpace System* to set up the
environment for a given project. This then allows the user to interact
with a fully customized environment for the project they are interacting
with. Pretty cool right?

</br>



>The environment will automatically load the user project that the
>configuration is assigned to.  
> No more messing with [*IDEs*](https://en.wikipedia.org/wiki/Integrated_development_environment) or remote
>workstations.


Workspaces are inter-actable through a server-side version of *Vscode*
called [**code-server**](https://github.com/coder/code-server#readme).
This allows the freedom to customize the DevSpace experience to the user's
specific needs as all vscode extensions are natively supported inside
workspaces. So feel free to customize!


</br>



### **Where Did My Stuff Go?**

Workspaces are stored for 24 hours after your last log in to them. After 24hrs a DevSpace will still be available and can be launched but all code or environment changes that are not stored (committed and pushed) to a VCS (typically git) will be deleted. This also applies to all actions performed in a terminal inside the workspaces. That includes packages installed and file operations. This is why DevSpace configs are important as they provide a persistent state to re-launch the workspaces in.
>The Gigo Extension will automatically push all code/files within the base directory in the DevSpace. Users can choose to not use this, however, they must manage their VCS themselves. For more information, reference the Gigo  Extension Documentation


</br>
</br>

### **Sharing is Caring**


</br>

Not all DevSpace configs are created equal. Some are custom-built
for an individual purpose and may only be useful for a specific project.
However, some are very applicable to a wide variety of specific use
cases.

</br>

For cases when a user feels they could better the platform with their
hard work. Gigo offers the option to publish DevSpace configurations as
a **Public Template** so that other users may create projects with their
configs. Published configurations can be searched and used when creating
a project

</br>

![workspace_config.png](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/workspace_config.png)

<sub> *by selecting Create Public Template after choosing Custom a user
<sub>can publish their configuration

</br>

By default, all DevSpace configs are **not** published and can only be
used by users making attempts on the project they were built for. If you
feel that you're up to the task, Publish It!


