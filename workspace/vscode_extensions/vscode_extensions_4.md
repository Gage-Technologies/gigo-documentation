# Vscode Extensions
>Conveniences and Extensions


### **How To Use Vscode Extensions In Workspaces**

Inside the DevSpace config, there is a vscode block that is used to define extensions for use in the DevSpace. This block is defined by the user to contain as few or as many extensions as they desire. This can be particularly helpful for a user who wishes to program in a specific language inside the DevSpace.

For instance, if the user wanted to make a python project, they could define a vscode block that contains a python syntax highlighter extension for vscode. Like it the block below:
```yaml
# configuration of the vscode
vscode:
   # enable/disable vscode editor - default to enabled
   enabled: true
   # extensions that needs to be installed in the editor
   extensions:
      # python extension for vscode
      - ms-python.python
```

![workspace_config_vscode_extension.png.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/vscode_extensions/workspace_config_vscode_extension.png.svg)

Extensions can be included for a variety of reasons and are generally recommended for any public templates to ease users into using them in their projects.

</br>

### **Gigo DevSpace Extension**

Whenever a user launches a DevSpace the *Gigo Extension* is automatically installed. The Gigo extension helps with a variety of tasks and allows users to build/walkthrough tutorials inside the DevSpace. The Gigo extension also provides an automatic VCS (Version Control System) based on Git that will commit and push changes as a user works. For more information on the Gigo Extension review the documentation on the Gigo extension.


