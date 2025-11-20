# MakeraCAM

[← Back to Main Page](README.md)

---

## **Table of Contents**
- [Overview](#overview)
- [Learning the Software](#learning-the-software)
- [Files](#files)
- [Milling the Board](#milling-the-board)
- [Notes & Takeaways](#notes--takeaways)
- [Important Decisions](#important-decisions)
- [Workflow](#workflow)
- [Documentation from this work](#documentation-from-this-work)
- [Summary](#summary)

---

## Overview

We started using **MakeraCAM** with our new CNC machine that has an **auto tool-changer**. This makes milling way faster and easier since it switches tools automatically — so you can start a job and work on something else while it runs.

---

### Learning the Software

We learned how to:
- Import files and center them using coordinates (like `(6,6)` for alignment)
- Create **pockets**, **contours**, and **drilling paths**
- Assign tools and set up tool changes
- Export and run the g-code on the CNC

## Files  
[Open Resistance1-Edge_Cuts.gbr](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/files/pcb/Resistance1-Edge_Cuts.gbr)

[Open Resistance1-F_Cu.gbr](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/files/pcb/Resistance1-F_Cu.gbr)

[Open Resistance1-PTH.drl](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/files/pcb/Resistance1-PTH.drl)

Below is the progression of creating the toolpaths:
![beforetoolpathed_PCB.png](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/images/pcb/ss_beforetoolpathed_PCB.png)
![ss-pocketPCB.png](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/images/pcb/ss-pocketPCB.png)
![ss-drilling_PCB.png]()


Below is what the toolpath looks like in MakeraCAM before milling:

![ss_toolpathPCB.png](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/images/pcb/ss_toolpathPCB.png)

---

### Milling the Board

After setting up the design, we placed the copper board on the CNC bed and ran the job. It milled all the traces and drilled the holes automatically.

![ss_completedPCB.png](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/images/pcb/ss_completedPCB.png)

---

### Notes & Takeaways

- The auto tool-changer saves a lot of time  
- The traces came out clean and sharp  
- We learned how to adjust feed rates, depth, and pocketing for different materials

#### Challenges
- A challenge that I had was in the software while learning when to select which groups of lines for each direction
    - I overcame this by following the workflow carefully and realizing when to restart 
- There were no big challenges while milling and my PCB board came out well the first time
- It did take me a few tries to learn how to run the software and set up the board (which screws to unscrew)

### Important Decisions 
1. I followed the workflow very carefully to ensure that I did not miss a step (this allowed me to follow a checklist and work efficiently so that I did not need to backtrack.
2. I worked with a partner while running it (this allowed me to have help on my first time and then repeat it again with her, giving me practice and experience with the machine)
3. I redid the toolpath by myself after we ran through it with Mr. Dubick to make sure that I knew how to select different sections and pick whether to pocket or drill. 

# Workflow

## Preparing Design

**Open new 3D project**

- Set material to PCB: **Edit → Material → PCB**
- Set dimensions:
  - **X = 127 mm**
  - **Y = 101 mm**
  - **Z = 1.7 mm**

**Download files from Fab drive** (blue folder named *Dubick*):

- `Resistance1-F_Cu.gbr`
- `Resistance1-PTH.drl`
- `Resistance1-Edge_Cuts.gbr`

**Import each file into MakeraCAM:**

- `File → Import PCB → Downloads → Resistance1-Edge_Cuts.gbr → Open`
- `File → Import PCB → Downloads → Resistance1-PTH.drl → Open`
- `File → Import PCB → Downloads → Resistance1-F_Cu.gbr → Open`

---

## Anchor Lower Left Corner

1. Select whole design  
2. Press **“m”**  
3. In the pop-up:
   - Select the **lower-left corner** anchor (diagram on top right)
   - Under **Location**, set coordinates to **(6, 6)**

---

## Path Setup

### Pocketing

1. In **2D Layers**, hide:
   - `Resistance1-F_Cu.gbr_pad`
   - `Resistance1-PTH.drl_0.900 mm`
   - `Resistance1-PTH.drl_1.400 mm`
2. Select: **2D Path → 2D Pocket**
3. Select whole *visible* design
4. Set **End Depth = 0.05 mm**
5. Add tools:
   - **8mm Corn**
   - **0.2mm 30° Engraving (Metal)**
6. Click **Calculate**

---

### Drilling Holes

1. **2D Path → 2D Drilling**
2. In **2D Layers**, hide everything except the drilling file
3. Set **End Depth = 1.7 mm**
4. Add tool: **8mm Corn**
5. Click **Calculate**

---

### Outside Cut

1. **2D Path → 2D Contour**
2. In **2D Layers**, hide everything except:
   - `Resistance1-Edge_Cuts.gbr`
3. Set:
   - **End Depth = 1.7 mm**
   - **Strategy: Outside**
4. Tabs:
   - **Tabs: Custom**
   - **Tab Shape: Triangle**
   - Click **Add**
   - Click 3 spots on the outer edge (evenly spaced)
5. Add tool: **8mm Corn**
6. Click **Calculate**

---

## Export Path

`Path → Export → Export`

Upload the exported file into your folder in the Fab Google Drive.

---

# Milling Design

## Installing Material

1. Slightly loosen all bolts in the machine bed **except** the 3 fully inside the jig  
2. If a copper board is already on the bed:
   - Remove and reorient if possible  
   - Otherwise replace with a new board
3. Orient the PCB so the design will appear in the **bottom-left corner**
4. Adjust the rectangular metal holders (slide/rotate without removing bolts)
5. Slide PCB under loosened bolts
6. Rotate holders so the slotted short edge presses the PCB down
7. Tighten all bolts firmly (not overly tight)

---

## Running the File

1. Download your `gcode.nc` file from Fab Google Drive  
2. Open **Cavera Controller**
3. **Upload File**:
   - Top left → Upload File  
   - Select your `.nc` file → **Upload & Select**
4. Connect:
   - Idle (top left) → **COM Port ___**
5. Additional settings (top right):
   - **Display Manual Controls**
   - **Home**
6. In **Status**:
   - Ensure **Voltage > 3.6V**
7. At the bottom bar → enable:
   - **Auto Vacuum**
   - **Auto-Levelling**
8. Select **Run**

The machine will probe 25 points on the PCB, then begin milling.

# Documentation from this work 

**(full documentation can be found by clicking on "Documentation" on the Home Page)**  
These journals are from the two days that I dedicated to MakeraCam. The first day follows my learning process on a moniter and the second day tracks my actual use of the machine.

10/27/25 Today we learned about a new software called MakeraCAM. I have never worked on this before, and at first it was very complicated. We pulled 3 files from the main drive (FabLab Drive under Dubick folder) so that we could focus on how to specify it instead of the actual design right now. I learned how to center the design (using coordinates (6, 6) and making a pocket, contour, and drilling. I also learned how to add specific tools depending on what kind of cuts I want the machine to make. This was helpful because I was able to learn new software (which will come in handy now that we have a new CNC machine). The benefits of this machine is that it switches out the tools unlike the manual version. This means that we can walk away after getting the g-code started, which leads to more efficiency in the lab.

10/31/25 Today I used our new CNC machine to mill a board. This was from a design that I made on Makera (the files were precreated but I had to specify the design depth, where to pocket, contour, and drill). This involved following a workflow created by a classmate that I altered to make more sense to me personally. This made the slightly complicated setup much easier to follow and check. I spent the other half of class (after I started running the program) on Github and updating my documentation and digital portfolio.

# Summary

I think that this project was a good way to focus on creating and sending the gcode to the MakeraCam without getting caught up in the design. I realized how much a workflow can help during this assignment and feel confident in my ability to set up and run the new CNC machine. This is also very interesting because it is much more cost efficient and helpful for the electronic part of my Capstone Peoject (depending on which Pearl projects require it). I plan to get more comfortable with it during my mountain range project and want to learn how to use the CNC machine on different materials with different tools.
