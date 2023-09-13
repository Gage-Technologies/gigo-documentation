# Tutorial Creator
>#### Providing Better Projects

The Gigo Extension provides a comprehensive way to improve projects for other users by allowing them to create tutorials within their workspace.

</br>

### **Creating your first tutorial**

To create a tutorial begin by creating a tutorial by clicking on the tutorial viewer icon (the "Book" icon).

![extension_tutorial_creator_1.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_1.svg)


This will open an empty Tutorial Viewer with an "Add Tutorial" button in the top right corner.

![extension_tutorial_creator_2.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_2.svg)

When a user clicks this button they will be dropped into the Tutorial Creator Studio.

![extension_tutorial_creator_3.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_3.svg)

This interactive environment allows users to create beautiful tutorials using Markdown format.


### **What is Markdown and How To Use It**

[Markdown](https://www.markdownguide.org/basic-syntax/) is a markup language that allows more advanced formatting tools than a basic text editor. Markdown is typically used for documentation like READMEs (in fact the documentation you are reading right now is made in markdown).

The hyperlink above covers some basics for making great-looking Markdown documents. The Tutorial Creator studio is a great place to get more familiar with these concepts and begin making great documentation.

</br>


### **Interacting with Markdown In The Tutorial Creator**

The Tutorial Creator Studio allows users to preview their Markdown as they write it. Simply use the keyboard shortcut "Ctrl + K then V).



A preview will display with your Markdown rendered inside.

![extension_tutorial_creator_5.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_5.svg)


</br>

### **Code Tours and Advanced Tutorials**

The Tutorial Creator Studio allows users to create [Code Tours](https://marketplace.visualstudio.com/items?itemName=vsls-contrib.codetour), a walkthrough tour of a codebase.
>For a more detailed description of Code Tours refer to the hyperlink provided or the Tutorial Viewer Documentation

Creating Code Tours is made simple by the Tutorial Creator Studio. Simply click the "Add Tour Step" Button shown below and the Tutorial Creator Studio will generate a tour file for your tutorial.

![extension_tutorial_creator_6.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_6.svg)

</br>

A dialogue box will pop up at whichever line number your cursor was on in the Markdown editor. There are a few pieces of information that comprise a tour step:
- The relative path of the file (that the reader will be redirected to)
- The line number of the file (to redirect the reader to)
- A description to display at the line number of the file (optional)

It is recommended to include a description as this can further help readers to understand.

![extension_tutorial_creator_7.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_7.svg)

</br>

Once you have filled all mandatory fields, click "Save". This will collapse the step into a convenient bubble.

![extension_tutorial_creator_8.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_8.svg)

</br>

Once this step is rendered to the user it will be displayed to a user as a button inside the tutorial that will link to the specified file/line. For more examples reference the Tutorial Viewer section on Code Tours.

![extension_tutorial_creator_9.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_9.svg)

</br>

You can use this to conveniently link to code blocks inside tutorials. In the below example, the step could link to this example function.

![extension_tutorial_creator_10.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_10.svg)

</br>

You can also simply include code blocks within your code tour step. A reader could insert any code block placed inside the description block into the codebase with a click of a button like in the example below.

![extension_tutorial_creator_11.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_11.svg)

</br>

Finally, if you make a mistake and wish to delete a step, simply click on the collapsed bubble to open the delete menu.

![extension_tutorial_creator_12.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/extension/tutorial_creator/extension_tutorial_creator_12.svg)
