Using ArcToolbox tools to convert the .csv file to a feature class (10 points)

After running the csv to feature class this is my code and the view of the geoprocessing panel.
 
The code itself breaks down what the XYTable to Point is doing while the feature allows you to import a file and automatically does what the code is saying to do. 

Commentight the example code (20 points)

Image of new file in the pathway as created.

Q1: Line by line, explain what was done in the code. (10 points)
Before starting you use the import function to import the arcpy, csv, and os libraries.
Next we are making a new feature class in the location of our CSV file path and project geodatabase.
In the code block: with open (csv_file_path, ‘r’ as csv_file it is going to open the file and create a reader object, which reads the header and field names.
In the next line we define the spatial reference system.
Next, we check if the feature is already existing and delete it if it does.
Now that we have deleted a pre-existing feature we add the new one and add fields based on csv header. 
We also insert point features and process the data to add points. 
Finally we print the output
In summary this script reads a CSV file, deletes any existing feature class with same name, creates a new point feature class with fields from the csv header, and then converts the longitude and latitude from the CSV into points and projects to a spatial system to add to a new feature class.


Q2: What do the cod 4269 and 102309 represent? (5 points)
These represent the spatial reference systems. 
Q3: Explain what is SHAPE@ (5 points)
This allows access to the entirety of a feature, here we have the point feature class that defines the coordinates with XY.

Using arcpy.Exist() (10 points)

Q4: Line by line describe what was done by the code in the block above. (10 points)
This code takes the data set name and determines if it exists.


Use arcpy.walk (10 points)

Q5: line by line, describe what was done by the code in the block above. (10 points)
This code is finding the workspace and then iterates through that dataset


Use List Comprehension (10 points)

Q6: Describe what was done by the code in the first blocks above. (5 points)
First we import the os module
Then we specify the path to the paris data
Then we ask it to list the shapefiles and print the list.
Q7: Describe what was done by the code in second blocks above. (5 points)
We import the os module
Specify its path
Print the message
Then we walk through the folder and its subfolders
Then we filter and print for the .shp files

Use arcpy.da.SearchCursor (10 points)

Q8: Line by line, explain what was done in the code. (10 points)
This code allows us to prompt the user and the print accordingly for the file

Use addField and field Calculator (20 points)

Q9: line by line, describe what was done by the code in the block above. 10 points
this code adds the points with the field name and it then add the expression to complete calculated values 
Q10: Open the attribute table of "points" and check if the attribute table has a new field "all" and correct values. Right-click the "all" field and click the field calculator. Describe what you see in the field calculator interface. Compare the python code versus the field calculator interface. 10 points

In the Python code the expressions use ! to refer to certain field values
The field calculator interface you type the same expression into the box. This way prompts you to enter the fields.
