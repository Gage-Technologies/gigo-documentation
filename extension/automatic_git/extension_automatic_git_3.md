# Automatic Git Control
>#### Writing Commit Messages is Hard

</br>

It's always annoying to push to git. It requires the user to stop what they are doing and write a commit message and push to a specific branch. It's a mess. Most programmer simply get adjusted to this and begin to get comfortable with it. And that is fine.


However, for people that would like a more streamlined experience, there is an alternative. The Gigo Extension provides an Automatic Git Control system that dynamically commits and pushes changes as user is interacting with a workspace. This creates cohesive performance that never interrupts a user experience and saves changes on the fly similar to services like Google Docs.


### **How Does It Work?**

>First, the Automatic Git Control system will wait for a specified time (18 seconds by default) before checking for changes.

![extension_automatic_git_1.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/automatic_git/extension_automatic_git_1.svg)

>It will then check for changes in the working directory.

![extension_automatic_git_2.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/automatic_git/extension_automatic_git_2.svg)

>Finally, if changes are detected, it will commit and push them to Git.

![extension_automatic_git_3.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/automatic_git/extension_automatic_git_3.svg)

<sup><sub>*These changes will always be pushed to the main branch of the repository.



### **Who Can Use Automatic Git Control?**

Everyone! The Automatic Git Control comes standard for every user with the Gigo Extension. It is designed such that a user doesn't even need to know it exists. It will perform all Git operations without the need for any user interaction.




</br>

### **What If I Want To Use My Own VCS?**

You can! Any user can disable Automatic Git Control by simply:
> clicking on their profile > clicking Workspace Settings > then un-checking "Run On Start".

![extension_automatic_git_2.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/automatic_git/extension_automatic_git_4.svg)

This will disable Automatic Git Control, however, users that disable Automatic Git Control must manage their own VCS within the workspace. If the user disables Automatic Git Control but do not push their changes, these changes will be lost after 24hrs when the workspace is deleted.

For more information on workspace lifespans see the [Workspace Overview Documentation](documentation/workspace/workspace_overview_1.md) .



