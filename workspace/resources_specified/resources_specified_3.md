# Resources Specified
>How Much and How Little?

The *Resource Block* is the section of the workspace config that specifies the resource allocation for a workspace. Users can allocate specific resources based on what they might need for a given project.


### **Resource Block Parameters**

There are 3 components to the Resource Block:
- CPU cores
- Memory (in GB)
- Disk (in GB)

All these parameters can be found in the resource block below.

```yaml
# resources that need to be allocated for the env
resources:
   # we only deal in whole CPU cores don't pass milli core syntax
   cpu: 3
   # memory is measured in GB
   mem: 4
   # disk is measured in GB
   disk: 10
```

![workspace_config_resource_block.png.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/resources_specified/workspace_config_resource_block.png.svg)

</br>

### **Restrictions On Resources**

There are two groups of restrictions on resources based on the type of user creating the workspace config. A free user can allocate up to 3 CPU cores, 4GB of Memory (RAM), and 10GB of Disk space. However, a premium user can allocate up to 6 CPU cores, 8GB of Memory (RAM), and 50GB of Disk Space.

</br>

A non-premium user can still use a workspace config that has resources allocated for a premium user, however, the workspace config will reduce down to the max allocatable resources for the free user (3cpu, 4mem, 10disk).

