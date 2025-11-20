# MakeraCAM

[← Back to Main Page](README.md)

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

### Files 
[Download Resistance1-Edge_Cuts.gbr](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/files/pcb/Resistance1-Edge_Cuts.gbr)

[Download Resistance1-F_Cu.gbr](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/files/pcb/Resistance1-F_Cu.gbr)

[Download Resistance1-PTH.drl](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/files/pcb/Resistance1-PTH.drl)


Below is what the toolpath looks like in MakeraCAM before milling:

<p align="center">
  [Download ss_PCBtoolpath](
</p>

---

### Milling the Board

After setting up the design, we placed the copper board on the CNC bed and ran the job. It milled all the traces and drilled the holes automatically.

<p align="center">
  <img src="https://github.com/user-attachments/assets/b5d3460f-83e0-4d6b-a80f-33e3520c1d81" 
       alt="Milled Copper Board" 
       width="450" 
       style="border-radius: 10px; box-shadow: 0 2px 6px rgba(0,0,0,0.2);">
</p>

---

### Notes & Takeaways

- The auto tool-changer saves a lot of time  
- The traces came out clean and sharp  
- We learned how to adjust feed rates, depth, and pocketing for different materials

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
