# Topography Map of Breckendridge, Colorado 

[← Back to Main Page](README.md)

For this project, we utilized the MakeraCam machine to engrave topography maps into wood. I chose to do Breckendridge. 
---
_This workflow is inspired by one that Tom Dubick created_
## Workflow 
---
#### Terrain2STL (https://jthatch.com/Terrain2STL/)
1. Find location and define model area by creating a red box around the georgraphy wanted
2. Adjust water drop and base height (default of 1 to start)
3. Generate model to download stl as a zip file
#### Aspire
4. Open Aspire and create new file
- Job type: single side
- Width (x): 2.5 inches 
- Height (y): 3.5 inches
- Thickness (z): 1.0 inch
- Z Zero Position: Material surface (top)
- XY Datum Position: Bottom left
- Model Resolution: Standard
- Click "OK"
5. Import 3D Model
- Go to the modeling tab
- Click "Import a Component or 3D Model" and select your STL file
6. Orient 3D Model (Imported 3D Model > Transform)
- Rotation abouty Z axis: 0 degrees
- Unclick "lock XYZ ratio"
  - z = 1, x = 2.5, y = 3.5
  - Click apply and center model
  - Leave "Apply Perspective Along Z" unchecked
- Position and Import
7. Use Depth Below to ensure that it is equal to the Z's height size
- click import while on  Position Relative to the Modeling Plane
8. On the Component tab --> Component Properties
- Shape Height: 1.0
- Base Height: 0.25
- "Close"
9. Design tab --> 2D view
- click "Center" under the Alignment Tool
10. Design tab --> Create Vectors
- Draw rectangle around design (in this case, x = 2.5, y = 3.5)
  _need to do this to trim around the final product_
11. Toolpaths Tab
  - In the 2D view, click on the 3D model image
  - Click 3D roughing toolpath
    - Material: Hardwood
    - Tool: Large 25 mm End Flute Mill (Also known as a 1/8 End Mill)
    - Machine Limit Boundaries: Selected Vectors
    - Machining Allowance: 0.024
    - Strategy: 3D Raster
    - Name the Toolpath --> Calculate
   - 3D Finishing Toolpath
     - Material: Hardwood
     - Tool: 1/8 Ball Nose
     - Machine Limit Boundaries: Selected Vectors
     - Strategy: Raster, with a 0 degree input
     - Name the Toolpath --> Calculate
  - 2D Profile Toolpath Generation
      - Boundary: Select the rectangular boundary
      - Toolpath: 2D Roughing Toolpath
      - Start Depth: 0
      - Cut Depth: 0.5
      - Material: Hardwood
      - Tool: 1/8 End Mill
      - Machine Vectors: Select "On" and Direction "Climb"
      - Seperate Last Pass: leave unchecked
      - Name the Toolpath --> Calculate
  12. Preview all Toolpaths
        - save the G-code by clicking the Save Toolpath button
        - Machine: Carvera Desktop CNC machine
  #### MakeraCam
  13. After saving the toolpath to the Drive, download and import in on the PC next to the MakeraCam Machine
  - Upload the gcode after uploading the file
  - Offset (6,6) to allow for the wood to be cut in the middle
  - Run the gcode
