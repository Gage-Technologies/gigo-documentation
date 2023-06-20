# Tutorial Viewer
>#### Class is in session.


Reading documentation and READMEs is never fun. That doesn't mean it has to be difficult.

The Gigo Extension comes packaged with a markdown renderer built into the sidebar of the extension. This allows users to view tutorials in real time while working on code.

</br>

### **When can I use the Tutorial Viewer?**

The Tutorial Viewer is available on any project that has... well tutorials! Not all users will make tutorials for their projects, but any project that is marked *'Interactive'* should have tutorials.

For more information on Project Types check the Project Overview Documentation.

</br>

### **How to use the Tutorial Viewer?**

>To open the Tutorial Viewer, click the 'Book' icon in the sidebar.  
>![extension_tutorial_viewer_1.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_viewer/extension_tutorial_viewer_1.svg)

>This will open the Tutorial Viewer for the tutorials in the current project.
>![extension_tutorial_viewer_2.svg](hhttps://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_viewer/extension_tutorial_viewer_2.svg)

>To view the next tutorial click the 'Next Tutorial' button.  
>![extension_tutorial_viewer_3.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_viewer/extension_tutorial_viewer_3.svg)

</br>


### **Code Tours and Improved Tutorials**

A [Code Tour](https://marketplace.visualstudio.com/items?itemName=vsls-contrib.codetour) is an open source project that allows users to create/use guided code walk-throughs. To learn more about creating tutorials with Code Tour, see the Tutorial Creator Documentation.


Code Tours are integrated into the Gigo Tutorial system to allow users to improve tutorials. When a Code Tour is available for a tutorial a button labeled "Start Code Tour" will be rendered at the top of the tutorial as seen in the image below.

![extension_tutorial_viewer_4.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_viewer/extension_tutorial_viewer_4.svg)

Clicking this button will start the Code Tour from the beginning and the user will be able to click through each tour step. There is another type of button that will be rendered inside of the tutorial that will be labeled "Interactive Step #" that will take the user tto the specified step number. This can be seen in the image above with the button labeled "Interactive Step 1".

</br>

When either of these buttons is clicked the user will be shown a specified line number of a file within the repository as seen below.

![extension_tutorial_viewer_5.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_viewer/extension_tutorial_viewer_5.svg)

On that line number will be a description of what that code snippet does so that the user may follow alongside the tutorial inside the code.


</br>

### **Advanced Code Tours**

Code Tours offer advanced features to assist users with learning programming.  In the bellow example, when the user clicks the "Interactive Step Button" something different happens.

![extension_tutorial_viewer_6.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_viewer/extension_tutorial_viewer_6.svg)

The creator of this tutorial has put a code block inside the Code Tour Step, this is the highlighted section in the image below.

![extension_tutorial_viewer_7.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_viewer/extension_tutorial_viewer_7.svg)

Since there is a code block in this Code Tour, a user can click the "Insert Code" button to paste all code inside the block into the file the Code Tour points to.

![extension_tutorial_viewer_8.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_viewer/extension_tutorial_viewer_8.svg)

For more information on Code Tour Advanced features, refer to the Tutorial Creator Documentation.