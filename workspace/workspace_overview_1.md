# Workspace Overview
>#### How Workspaces... Work


A workspace is a development environment designed for a specific project
in mind. The level of specificity is dependent on the user or
organization that designed them. This can range from a general workspace
that is designed for any project, or a workspace designed to run a
specific project based on a programming language and specific packages
needed to run the project.


</br>
</br>






### **Architecture**


![GIGO Workspace Overview-transparent.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/GIGO%20Workspace%20Overview-transparent.svg)

<sub>*the above illustration shows the basic architecture of the
<sub>workspace system

</br>


A workspace consists of a *workspace configuration* file that details the
following:
- [**Base Docker Image**](../workspace/base_docker_image/base_docker_image_2.md)
- [**Resources Specified**](documentation/workspace/resources_specified/resources_specified_3.md) (allocated resources for environment)
- [**Vscode Extensions**](documentation/workspace/vscode_extensions/vscode_extensions_4.md) (for additional editor support) *
- [**Additional Docker Services**](documentation/workspace/docker_service/additional_docker_service_5.md) / Images (e.x databases, web
  services, additional software, etc.) *
- [**Command Line Arguments**](documentation/workspace/command_line_arguments/command_line_arguments_6.md) (to be run when docker image is
  started) *

<sup><sub>the above bullet points marked with * indicate an optional
<sup><sub>addition

>The workspace config is based on a [*`yaml`*](https://www.redhat.com/en/topics/automation/what-is-yaml) format.

A workspace config instructs the *Gigo Workspace System* to setup up the
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
This allows a freedom to customize the workspace experience to the users
specific needs as all vscode extensions are natively supported inside
workspaces. So feel free to customize!


</br>



### **Where Did My Stuff Go?**

Workspaces have a lifespan of 24hrs. After 24hrs a workspace will still be available and can be launched but all code that is not stored (committed and pushed) to a VCS (typically git) will be deleted. This also applies to all actions performed in a terminal inside the workspaces. That includes packages installed and file operations. This is why workspace configs are important as it provides a persistent state to re-launch the workspaces in.
>The Gigo Extension will automatically push all code/files within the base directory in the workspace. Users can choose to not use this, however, they must manage their VCS themselves. For more information, reference the Gigo  Extension Documentation


</br>
</br>

### **Sharing is Caring**


</br>

Not all workspace configs are created equal. Some are custom bult
for an individual purpose and may only be useful for a specific project.
However, some are very applicable to a wide variety of specific use
cases.

</br>

For cases when a user is feels they could better the platform with their
hard work. Gigo offers the option to publish workspace configurations as
a **Public Template** so that other users may create projects with their
configs. Published configurations can be searched and used when creating
a project

</br>

![workspace_config.png](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/workspace_config.png)

<sub> *by selecting Create Public Template after choosing custom a user
<sub>can publish their configuration

</br>

By default, all workspace configs are **not** published and can only be
used by users making attempts on the project they were built for. If you
feel that your up to the task, Publish It!


