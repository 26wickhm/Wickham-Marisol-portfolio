# Pearl Project (Atrium Hospital Rehabilitation Center)

[← Back to Main Page](README.md)

---

## Table of Contents
1. [Overview](#pearl-overview)
2. [Project List](#pearl-project-list)
3. [Leadership Positions](#pearl-leadership)
4. [Donning Tube](#donning-tube-section)

---

<a name="pearl-overview"></a>

## Overview

I am working with **Pearl (Atrium Hospital Rehabilitation Center)** with three other students to design and make medical assistive devices that either do not exist, are not customized, or are very expensive. The list below was given by nurses and doctors at the facility based on necessity of items. This allows us to cross-reference this with the level of difficulty of each project and set large goals and smaller goals to fill time.

---

<a name="pearl-project-list"></a>

## Project List

| **Project #** | **Necessity Level**           | **Complexity Level**         |
|:-------------:|-------------------------------|------------------------------|
| 1             | Variety of cup holders        | Joystick toppers             |
| 2             | Cathing mirror                | Sock Aid                     |
| 3             | Mounts                        | Reacher for Tenodesis        |
| 4             | Joystick Toppers              | Mounts                       |
| 5             | Reacher for Tenodesis         | 1-Hand Cutting Board         |
| 6             | Sock Aid                      | Wheelchair Tray              |
| 7             | Pill Crushers (easy use)      | Variety of cup holders       |
| 8             | 1-Hand Cutting Board          | Donning Tube                 |
| 9             | Call Bell Covers              | Call Bell Covers             |
| 10            | Donning Tube                  | 1-Hand Hair Tie Help         |
| 11            | Wheelchair Tray               | Cathing Mirror               |
| 12            | Pant Clips                    | Phone Holder                 |
| 13            | 1-Hand Hair Tie Help          | Book Holder                  |
| 14            | Nail Clipper Holder           | Nail Clipper Holder          |
| 15            | Phone Holder                  | Pill Crushers (easy use)     |
| 16            | Fidgets                       | Nail Polish Holder           |
| 17            | Deodorant Holders             | Deodorant Holders            |
| 18            | Book Holder                   | Fidgets                      |
| 19            | Nail Polish Holder            | Pant Clips                   |

>  *Currently, only the Donning Tube project is fully documented. Additional projects will be added later.*

---

<a name="pearl-leadership"></a>

## Leadership Positions

Our team operates on a rotating leadership system every two months to ensure that everyone gains experience in both design and management roles. Each position oversees a specific aspect of Pearl’s development and collaboration with the Atrium Hospital Rehabilitation Center.

| **Name** | **Position** | **Role Overview** |
| --- | --- | --- |
| **Marisol** | Operations Lead | Manages lab operations, training, and production schedules. Coordinates between design and production teams. |
| **Caroline** | Project Coordinator | Liaises with hospital staff and ensures deliverables meet medical timelines and feedback. |
| **Karlin** | Technical & Design Lead | Oversees device design, CAD accuracy, and manufacturability for production runs. |
| **Scarlett** | Quality & Safety Lead | Ensures product standards, safety compliance, and final inspection before delivery. |

#### Operations Lead – Marisol (Current Role)
As **Operations Lead**, I manage training for all student participants.  
This includes organizing schedules, creating structured training groups by experience level (CAD, 3D printing, and soldering), and leading onboarding sessions for new members.

---

<a name="donning-tube-section"></a>

## Donning Tube

### Project Overview

Donning Tubes are a tool to put on compression socks.  This is important for amputee patients because the end of the limb needs to be molded after surgery. The compression sock (shrinker) is loaded onto the tube and then slid onto the limb. This reduced friction on the limb as well as ensuring that thre sock is taught and does not have bunches of fabric. 

## STEPS IN IMAGES
  ### below shows the broad progression of the donning tube in Fusion360

| Step 1 | Step 2 | Step 3 | Final |
| --- | --- | --- | --- |
| ![Step 1](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtube(step1).png) | ![Step 2](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtube(step2).png) | ![Step 3](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtube(step3).png) | ![Final](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtubefinal(homeview).png) |

## Dimensions as a Parametric File (in inches) 
[View on GitHub](assets/files/donningtube/Donning%20Tube%20(parametric%20%2B%20handles).stl)  
[Direct Download (STL)](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/files/donningtube/Donning%20Tube%20(parametric%20%2B%20handles).stl)

There are two variables in this design. Every single dimension is centered around the diameter of the design except for the height. I decided to do this because I wanted to be able to adjust the height is a patient needed a longer or shorter body. The default settings on this is a diameter of 12 inches and a height of 9 inches. 

## Modeling Steps 

All dimensions are defined **relative to the diameter**.

---

### 1. Base Cylinder

- **Diameter**: `D`
- **Width (wall thickness)**: `D + 0`
- **Height**: `H`

**Steps**
1. Sketch a circle with diameter `D`
2. Offset the circle to define wall thickness
3. Extrude upward by height `H`

---

### 2. Handles

- **Handle width**: `0.1667 × D`
- **Handle length**: `1.91667 × D`
- **Handle height**: `0.1667 × D`

**Steps**
1. Sketch handle profile
2. Extrude handles upward by `0.1667 × D`

---

### 3. Cutout for Handle Bar

- **Offset plane**: `H + 3`
- **Cutout diameter**: `D`
- **Cut depth**: `H + 3`

**Steps**
1. Create an offset plane at `H + 3`
2. Sketch a circle with diameter `D`
3. Extrude cut through the body

---

### 4. Fillets

- **Bottom & sides of handles**: `0.020833 × D`
- **Top of handles**: `0.075 × D`








