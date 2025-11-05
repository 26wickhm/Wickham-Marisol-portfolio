# Wickham–Marisol Portfolio

## Table of Contents
1. [Pearl Project (Atrium Hospital Rehab Center)](#pearl-section)
   - [Overview](#pearl-overview)
   - [Project List](#pearl-project-list)
   - [Leadership Positions](#pearl-leadership)
   - [Donning Tube](#donning-tube-section)
2. [MakeraCAM](#makeracam-section)
3. [Documentation](#documentation-section)

---

<a name="pearl-section"></a>

## Pearl Project (Atrium Hospital Rehabilitation Center)

### Pearl Table of Contents
- [Overview](#pearl-overview)
- [Project List](#pearl-project-list)
- [Leadership Positions](#pearl-leadership)
- [Donning Tube](#donning-tube-section)

---

<a name="pearl-overview"></a>

### Overview

I am working with **Pearl (Atrium Hospital Rehabilitation Center)** to design and make medical assistive devices that either do not exist, are not customized, or are very expensive.  
The list below was given by nurses and doctors at the facility based on necessity of items.  
This allows us to cross-reference this with the level of difficulty of each project and set large goals and smaller goals to fill time.

---

<a name="pearl-project-list"></a>

### Project List

| **Project #** | **Necessity level**           | **Complexity level**         |
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

---

<a name="pearl-leadership"></a>

### Leadership Positions

Our team operates on a rotating leadership system every two months to ensure that everyone gains experience in both design and management roles.  
Each position is responsible for overseeing a specific aspect of Pearl’s development and collaboration with the Atrium Hospital Rehabilitation Center.

### Leadership Rotation

| **Name** | **Position** | **Role Overview** |
|-----------|---------------|------------------|
| **Marisol** | Operations Lead | Oversees lab operations, training sessions, and project scheduling for 30–40 students assisting in mass production. Coordinates communication between design leads and production teams. |
| **Caroline** | Project Coordinator | Communicates with hospital staff and manages timelines/deadlines to ensure all deliverables align with medical needs and facility feedback. |
| **Karlin** | Technical and Design Lead | Researches and approves device designs. Creates build plans for larger groups and oversees CAD accuracy and manufacturability. |
| **Scarlett** | Quality Assurance & Safety Lead | Maintains product standards and ensures safety compliance within lab workspaces. Manages inspection and testing of final devices before hospital delivery. |


#### Operations Lead – Marisol (Current Role)
As **Operations Lead**, I am responsible for managing training for all student participants.  
This includes organizing schedules, creating structured training groups by experience level (CAD, 3D printing, and soldering), and leading onboarding sessions for new members.  
I also coordinate meetings between the design team and production students to ensure deadlines are met and that communication remains clear throughout the project cycle.

---

<a name="donning-tube-section"></a>

### Donning Tube

#### Project Overview

Donning Tubes are a tool to put on compression socks.  
This is important for amputee patients and others who need assistance.  
The compression sock (shrinker) is loaded onto the tube and then slid onto the limb.

I made **five different designs in Fusion360**:
- 2 with handles (assist with pull force and grip)
- 3 without handles (compact and simple to fabricate)

Goal: Create a **parametric design** that adapts to limb dimensions.

**Design Notes**
- 2× handle versions (assist with pull force and grip)
- 3× no-handle versions (compact, simpler to fabricate)
- Goal: parameter-driven model (circumference, taper, wall thickness, handle geometry)

---

<a name="makeracam-section"></a>

## MakeraCAM

We started using **MakeraCAM** with our new CNC machine that has an **auto tool-changer**.  
This makes milling way faster and easier since it switches tools automatically — so you can start a job and work on something else while it runs.

---

### Learning the Software

We learned how to:
- Import files and center them using coordinates (like `(6,6)` for alignment)
- Create **pockets**, **contours**, and **drilling paths**
- Assign tools and set up tool changes
- Export and run the g-code on the CNC

Below is what the toolpath looks like in MakeraCAM before milling:

<p align="center">
  <img src="https://github.com/user-attachments/assets/5eeaaf54-2f10-48fc-b0ff-80f51b4daf35" 
       alt="MakeraCAM Toolpath Design" 
       width="500" 
       style="border-radius: 10px; box-shadow: 0 2px 6px rgba(0,0,0,0.2);">
</p>

---

### Milling the Board

After setting up the design, we placed the copper board on the CNC bed and ran the job.  
It milled all the traces and drilled the holes automatically.

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

---

<a name="documentation-section"></a>

## Documentation

### Field & Lab Journal

First visit to the Atrium Carolina's Rehabilitation Center in Charlotte was 09/26. We toured their assistive technology lab and were able to see a lot of the current devices they are using. Then we took a tour of their gym on the first floor and met one of their patients "Jordan," a 23 year old male who has issues walking and tremors due to a stroke, and we were able to see him practice walking across the gym with a walker. We then toured the gym on the spinal and brain trauma floor and met a 21 year old we call "Shaq" whose spinal cord was severed after he was shot in the back. We discussed with the nurses what kinds of devices they were already using and what needed to be improved. 

**10/06/25** Today we began designing the donning tubes. Marisol made the design for the donning tube, but everyone else had input on dimensions. Our plan is to have 2 variations each with three possible sizes to ensure that the donning tubes can reach a wider group of patients. There will be short or long donning tubes that come in small, medium, and large sizes. Karlin and Caroline found a file for the quadstick mouthpiece to begin printing it out. Scarlett finished filling out the spreadsheet for everyone's jobs on the projects. 

**10/07/25** Today Marisol completed her 5 versions of the donning tubes and uploaded screenshots to the Git. Scarlett began printing for the mounts and organized the supports in Bambu accordingly. Karlin gathered the 3 hole narrow, 3 hole wide, 4 hole narrow, 4 hole wide models of the quadstick mouthpiece onto to 1 file and printed them. Marisol will add her designs to the shared drive with the hospital and will print next class. Caroline was not in class today but will continue working with Scarlett when she returns. 

**10/08/25** Today Scarlett and Caroline printed out an alternate option for the video game mount using ratchet locking joints. Marisol printed out the medium handles donning tube and had to scale it down to 70% to be able to fit on the printer because the design is too big for the plate. Karlin printed out another set of the Quadstick mouthpieces and adjusted some of the supports before printing. 

**10/10/25** Today Karlin started researching methods on how to attach a water bottle holder to a wheelchair. She discovered that using a holster similar to a bike water bottle holder would work best. She then moved on to designing and researching the best water bottle and straw attachment. 

**10/21/25** Today we put together our schedules in a spreadsheet to compare when we can host meetings with the other students that want to be involved with Pearl. This involved marking what days we can come before or stay after and assign projects such as mass printing jobs or recreating designs for us. Once we have a full meeting outside of school, it will be much easier to catch up during community time during school and check in on their progress and/or assign new tasks. This will be helpful because the younger/less experienced kids can get involved and help without having too much responsibility. This is also a cool opportunity for the four of us because we can focus on design and programming (the more creative side of Pearl) and less on watching the 3D printers crank out ten of the same design. However, it is good for the other students to learn how to handle all of the tools in the lab so it is a win-win for both parties. 

**10/22/25** Today I worked on the easy grip pill crushers. This involved two designs (one screw and one press). I began printing both of these to see which one is more effective. I found that if the screw design is to work, I need to add to where the pill is being crushed between. I also found that I need to print a bar to allow the file to hinge. I also worked on Github for 25 minutes to get used to making my digital portfolio; I learned how to do tables and change the size and bold of my text. 

**10/23/25** I spent most of my time on Github today. I also got both of the prints off of the Bambu, and began to design the hinge that I was referring to yesterday. 

**10/27/25** Today we learned about a new software called MakeraCAM. I have never worked on this before, and at first it was very complicated. We pulled 4 files from the main drive so that we could focus on how to specify it instead of the actual design right now. I learned how to center the design (using coordinates (6, 6) and making a pocket, contour, and drilling. I also learned how to add specific tools. This was helpful because I was able to learn new software (which will come in handy now that we have a new CNC machine). The benefits of this machine is that it switches out the tools unlike the manual version. This means that we can walk away after getting the g-code started, which leads to more efficiency in the lab. 

**10/30/25** Today I spent the majority of the day creating a slideshow to present to the students interested in working on Pearl. This included a training regime, an explanation on the program as a whole, and deciphering what level each person is on. 

**10/31/25** Today I used our new CNC machine to mill a board. This was from a design that I made on Makera (the files were precreated but I had to specify the design depth, where to pocket, contour, and drill). This involved following a workflow created by a classmate. This made the slightly complicated setup much easier to follow and check. I spent the other half of class (after I started running the program) on Github and updating my documentation and digital portfolio. 

**10/3/25** Today I worked on my job for Pearl as Operations Lead, meaning that I created groups for training based on level of experience. This was much more difficult than it sounds because I had to cross reference experience in three different catagories (CAD, 3D printing, and soldering) and times available. I utlized ChatGPT to organize these groups and then I sent out emails to each group with a training schedule. This below is a brief overview of what levels I will be training next week.
