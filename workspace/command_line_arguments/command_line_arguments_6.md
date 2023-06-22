# Command Line Executions
>Installing Additional Dependencies


### **More To Install**

When a user needs to install commands that may not be found in a docker image, or perform file operations inside a workspace, the *exec* block allows user to perform Command Line Executions for these operations.

Here is an example of installing [CoreML](https://developer.apple.com/documentation/coreml) using [*pip*](https://pypi.org/project/pip/):

```yaml
exec:
  - name: Install Xcode command line tools
    init: true
    command: |
      #!/bin/bash
      xcode-select --install
  - name: Install Swift
    init: true
    command: |
      #!/bin/bash
      wget https://swift.org/builds/swift-5.5.2-release/ubuntu2004/swift-5.5.2-RELEASE/swift-5.5.2-RELEASE-ubuntu20.04.tar.gz
      tar xzf swift-5.5.2-RELEASE-ubuntu20.04.tar.gz
      sudo mv swift-5.5.2-RELEASE-ubuntu20.04 /usr/share/swift
      echo 'export PATH=/usr/share/swift/usr/bin:$PATH' >> ~/.bashrc
      source ~/.bashrc
  - name: Install CoreML tools
    init: true
    command: |
      #!/bin/bash
      sudo apt-get install -y python3-pip
      pip3 install coremltools
  - name: Install ios-deploy
    init: true
    command: |
      #!/bin/bash
      sudo npm install -g ios-deploy

```

In the above example we install swift, python, and coremltools. These are run with the tag `init: true` meaning that they will be run only the first time the workspace is launched. If it was `init: false` the commands would be run every time a user launches the workspace..
>For more information on workspace lifespans see the Workspace Overview documentation.

A user can execute any command that does not require user interaction or GUI inside the exec block.
