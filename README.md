# Pruning-and-Refactoring-Tool

Running the Pruning and Refactoring tool requires the same environment as the uml yang mapping tool, nodejs and its xmlreader module. The user can  refer to the User Guide https://github.com/OpenNetworkingFoundation/EAGLE-Open-Model-Profile-and-Tools/blob/UmlYangTools/UML-Yang%20Mapping%20Tool%20User%20Guide-v1.3_0601.docx


An introduction video on setting up the environment is on Youtube https://www.youtube.com/watch?v=6At3YFrE8Ag&feature=youtu.be. 

After the environment is configured, the user can do the following to run the tool.

Step 1: Copy the source information model which is ready for pruning and refactoring to the "project" folder.

Step 2: Change the file name of the information model to "source.uml".

Step 3: Type the following command in the project directory in terminal.

node main.js

When the user runs the tool for the first time, target.uml and mapping.uml are generated in the project folder. The target.uml is a clone of the source.uml and the mapping.uml file is composed of the pruning and refactoring realizations between the source and the target model. The mapping model is independent of the source model and the target model. The elements in all three models can be dragged onto Papyrus diagrams.

If the source.uml and target.uml are both existed before running the tool, the mapping.uml is updated to reflect the differences between classes, attributes and associations in the source and the target model. The comparison results are nested as comments inside the specific pruning and refactoring realization.

Future Work

1. Detailed comparison results between the source and the target model will be included in the mapping model.

2. Class split function: the refactoring function is under development which will allow the user to copy or split a object class in the target model. The class copy function is completed. The user will need to feed the tool with the class name and the number of copies or splits following a certain format in a text file.

3. Reverse pruning function: the reverse pruning function will allow the user to add the non-experimental elements in the target model back to the source model. 
