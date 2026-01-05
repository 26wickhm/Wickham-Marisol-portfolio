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

Donning Tubes are a tool to put on compression socks.  This is important for amputee patients because the end of the limb needs to be molded after surgery. The compression sock (shrinker) is loaded onto the tube and then slid onto the limb. This reduced friction on the limb as well as ensuring that thre sock is taught and does not have bunches of fabric. I did not use a specific reference as inspiration for this project because the hospital was the source who brought this necessity to my attention. Instead, I consulted with Heather Smith about what the object of a donning tube was, if it needed to be in a cone shape, etc. From there, I simply built a cylinder with handles that looked somewhat like the images that I found online. However, the majority of online images look very different than mine, which is what I believe makes mine different and easier to use. 

## Cost
- Average weight:760 grams 
- Average cost: $30
  - however, since this device is easily changed based on diameter and height, the price will change as well

## STEPS IN IMAGES
  ### below shows the broad progression of the donning tube in Fusion360

| Step 1 | Step 2 | Step 3 | Final |
| --- | --- | --- | --- |
| ![Step 1](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtube(step1).png) | ![Step 2](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtube(step2).png) | ![Step 3](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtube(step3).png) | ![Final](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtubefinal(homeview).png) |

## Dimensions as a Parametric File (in inches) 
[View on GitHub](https://github.com/26wickhm/Wickham-Marisol-portfolio/blob/main/assets/files/donningtube/Donning%20Tube%20(parametric%20%2B%20handles).stl)  
[Direct Download (STL)](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/files/donningtube/Donning%20Tube%20(parametric%20%2B%20handles).stl)

![Donning Tube – Parametrics](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtube.parametrics.png)


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

---
## Final Design Views

| Bottom View | Home View |
| --- | --- |
| ![Bottom View](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtubefinal(bottomview).png) | ![Home View](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtubefinal(homeview).png) |

| Side View | Top View |
| --- | --- |
| ![Side View](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtubefinal(homeview).png) | ![Top View](https://raw.githubusercontent.com/26wickhm/Wickham-Marisol-portfolio/main/assets/images/donning%20tube/donningtubefinal(topview).png) |

_There were no handtools used in this project. The only thing that one would use would be a sander, but adapting the fillets in the design would make this much better._

**Summary**
This project was very eye opening to me because it did not involve fancy electronics and the design does not look very difficult. However, working with Atrium has allowed me to see that the most important work sometimes is the "easy" things that not everyone has access to. This is why it was so rewarding to create a design that focused on making it easier, more cost efficient, and customizable. I also learned how to do parametrics in Fusion360, which I will continue to expand upon and advance my confidence in. In the future, I hope that this design becomes more mainspread and amputtee patients that need it can simply send the diameter of their limb and the preffered height (standard, long, short) and it can be quickly modified and produced. Of course, if more people utilize the donning tube, then I would be excited to hear feedback and adjust the file accordingly to accomadate or address an issue that I earlier missed. 

**Challenges** 
The main challenge in this design is the handles. They are not difficult to design, but there was much discussion about the usability of the design with them there. This is because they are both beneficial and get in the way. Previous to this design, Heather Smith (OT) spoke about how in order to keep the sock from slipping up the tube before application, it would hook around the ends. This creates a challenge because with the handles, there is no way for the sock to go around them and hook onto anything. My initial idea was to create a divit before the handles so that the sock had something to grip onto and hold it into place. However, after practicing with a compression sock and consulting with Ms. Smith, she made the final decision that the handles were positive to users and that if the height was not too short, then the compression sock should have no problem holding until application. 

**[Documentation](documentation.md)**
To read through my day to day documentation, go to the documentation page. This does not only involve documentation on the Pearl project, but more of a recording of each day regardless of what I am working on. Below is what I extracted from my overall documentation to give only information about this project.

**10/06/25**
Today we began designing the donning tubes. I made the design for the donning tube, but everyone else had input on dimensions. Our plan is to have 2 variations each with three possible sizes to ensure that the donning tubes can reach a wider group of patients. There will be short or long donning tubes that come in small, medium, and large sizes.

**10/07/25**
Today I completed my 5 versions of the donning tubes and uploaded screenshots to the Git. I will add my designs to the shared drive with the hospital and will print next class.

**10/08/25**
I printed out the medium handles donning tube and had to scale it down to 70% to be able to fit on the printer because the design is too big for the plate.

**11/5/25**
Today I learned how to create parametric designs in Fusion 360. I learned this for the main intention of adapting my donning tube. This is because while there can be generic sizes (small, medium, large), it is much more effective to use variables to define dimensions such as length, width, diameter, filleting, etc. I deleted the 5 versions of the files I had and created two instead. Both are parametric; one has handles and one does not.

**11/11/25**
The feedback I received about the donning tube is that parametric is a very smart way to keep the design, the tube can be one diameter instead of cone-like, and that there is a slight problem with the handle. While she did enjoy the concept, sometimes they put the sock over the opposite end of the tube to secure it while they roll it on. After discussion, I realized that we can keep the handles if I can create a ledge above them for the sock to hold on to.

**11/12/25 – 11/13/25**
On these two days I worked to make my  design better with the changes that Heather Smith advised. To do this, I added a hollowed out triangle revolving around the cylinder right above the handle to create a place for the compression sock to hook around. However, there are a few challenges with this. For one, I had to abandon the parametric design for now because I was back in the designing stage. The second issue is that I cannot tell if the hook will have enough space under it for the sock without printing a whole new donning tube. They take around 7 hours to print and take a lot of PLA, so I try to refrain from doing so until necessary.

**12/10/25**
Today we went in person to visit Atrium Rehabilitation Center and meet with Heather Smith regarding our designs. I brought my donning tube (with generic sizing of a diameter of 12 inches and a height of 9 inches). Heather was initially concerned about the handles getting in the way of the sock, but after consideration, she decided that it did not and was actually a great design idea. This means that I reverted my Fusion file to the original design without the section to hold the sock in place.The donning tube was left with her and will be implemented on the next amputee patient who needs it.

**12/10/25**
Today I went back and made the final donning tube design parametric. Before, I had many variables, but I decided that I only wanted to have 2. I made every single dimension dependent on the diameter (except for the height). I wanted the height to be separate because there may be a need for a longer or shorter body regardless of the width. This included every offset, fillet, and extrusion being an equation revolving around the variable `diameter`.

**12/11/25**
I also completed my Git page for the donning tube. The only thing I may have to do is copy and paste certain documentation over to it so that someone does not need to read through all of my documentation if they only want the parts about the donning tube.




