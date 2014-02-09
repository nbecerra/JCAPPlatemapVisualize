John M Gregoire 23 Jan 2014

All code written by John Gregoire and Natalie Becerra.

Functionality
This program “JCAPPlatemapVisualize” enables the user to locate a particular sample on the plate map or compositional space given the Platemap.txt file and either:
*the composition values
*the Sample Number or
*the x,y position of the sample
Additionally, the program can translate the information in the opposite direction.  The user can retrieve a particular sample’s composition, sample number, x,y position and position in compositional space given the Platemap.txt file and the sample location on a plate map (provided visually by clicking on the map) or the the position in compositional space.

Directions
Text—>Visualization
The user provides composition values, sample number or x,y position information using the text-boxes in the top-left corner of the GUI (Graphic User Interface).
First click “select file” and choose the appropriate Platemap.txt file (no need to fill in the text-box).  Then enter the composition values (listed in the same order as in the data file and make sure to use decimal values), the sample number OR the x,y position.  After entering this information, click “add” to pull up the rest of the information about the sample.  This will appear as a list it in the area to the right of the text-boxes while simultaneously encircling the sample on a colored plate map (bottom-left corner of the Graphic User Interface) and compositional space (bottom right corner).  To remove an entry to this list, the user should type the defining Sample information they would like to use (its Composition, x,y position or Sample No) in the appropriate text-box and click “remove”.

Visualization—>Text
After loading a Platemap.txt file using “select file”, the user can determine the information provided in the list on the right by appropriately clicking the sample in the picture of the plate map or on the compositional space:
*Left-click means populate the text-boxes with the sample’s information
*Right-click means “add” the sample’s information to the list in the top-right and circle the sample in both the colored plate map and the compositional space.
*Middle-click means “remove” the sample information from the list and remove the circles of the sample from the colored plate map and the compositional space.

Pseudo-Ternary Spread Options
The user can choose which material (A, B, C, or D) will be divided into slices leaving the other three materials to populate the corners for the ternary spread.  This is done by selecting A, B, C, or D from the pull-down menu to the right of the “pseudo-tern stack wrt” label.

Copying text window
Users can copy the list of positions into an excel file (via copy/paste-special) and perform transformations on the values.  This could be used to adjust for a different x,y-offset, etc.

Nuances
The default setting for the graphical representation of the plate maps is to omit the composition standards/fiducial markers.  This is done by populating the 2nd text-box on the top left corner with only 0,10,20,30,40,50 so that only research “samples” are displayed.  To display other types of samples, use the following code (which is written as an integer string of the format ##$@:
##=sample duplication where 00=original, 01=first duplicate, ...
$=thickness where 0 means standard sample thickness and >0 means fraction of that thickness with 1:0.1, 2:0.2, 3:0.5, 4:1,5, 5:2
@=intended use where 0=research sample, 1=spectral reference, 2=ABCD std, 3=EFGH std, 4=empty

When obtaining the Platemap.txt files, make sure to download them *as .txt files*  Getting them as .rtf or any other file and translating or using “save as” to make them .txt files will not work.