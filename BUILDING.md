## Building Project With Projucer
1. **Open Project** - Within Projucer open up the solution to the Project
2. **Link Tracktion Engine to Your Project** - To do this do these steps
   - Click the Dropdown menu for Modules on the left sidebar
   - Click on the plus sign within the drop down menu
   - Click add module from a specified folder
   - Find Tracktion in your file explorer and within the Tracktion root directory, do this
         - Find modules and click it
         - And then select and add tracktion_engine
   - Do the same steps to add tracktion_graph
   - It should be added now
3. **If tracktion_graph and tracktion_engine exists** - Click on tracktion_graph or tracktion_engine in projucer, then modify it's paths from there
4. **Open preferred IDE**
5. **Try Building it**
   - Note: You might get build errors, so here are some fixes for them
   - **BUILD WITH C++20 OR ELSE TRACKTION WON'T BUILD PROPERLY**
     - For Visual Studio,
          - go to project properties,
          - then go to c/c++ dropdown,
          - From there modify c++ standard language to c++20
   - **Extra Compilation Flags** - /bigobj
     - For Visual Studio
          - Go to project Properties
          - then go to c/c++ dropdown
          - Click on the command line from that dropdown
          - In the textbox named **Additional Options** add the following
            - /bigobj
