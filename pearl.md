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

I am working with **Pearl (Atrium Hospital Rehabilitation Center)** to design and make medical assistive devices that either do not exist, are not customized, or are very expensive.  
The list below was given by nurses and doctors at the facility based on necessity of items.  
This allows us to cross-reference this with the level of difficulty of each project and set large goals and smaller goals to fill time.

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

> ⚙️ *Currently, only the Donning Tube project is fully documented. Additional projects will be added later.*

---

<a name="pearl-leadership"></a>

## Leadership Positions

Our team operates on a rotating leadership system every two months to ensure that everyone gains experience in both design and management roles.  
Each position oversees a specific aspect of Pearl’s development and collaboration with the Atrium Hospital Rehabilitation Center.

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

Donning Tubes are a tool to put on compression socks.  
This is important for amputee patients and others who need assistance.  
The compression sock (shrinker) is loaded onto the tube and then slid onto the limb.

<hr>

<h3 id="donning-tube-parametric">Parametric Designs (With & Without Handles)</h3>

<p>
I created <strong>two parametric Donning Tube designs</strong> — one with handles and one without.  
This approach improves <strong>efficiency</strong>, <strong>customizability</strong>, and <strong>ease of training</strong>.  
Now, students can quickly adjust dimensions (like height, diameter, or handle size) without modifying the base model.
</p>

<ul>
  <li><strong>Efficiency:</strong> Adjust key parameters instead of rebuilding geometry.</li>
  <li><strong>Customizability:</strong> Generate new tube sizes for different patients instantly.</li>
  <li><strong>Training:</strong> Simplifies workflow for students learning parametric modeling.</li>
</ul>

<style>
  .imggrid {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
    margin: 12px 0 20px;
  }
  .imggrid .card {
    flex: 1 1 360px;
    max-width: 520px;
    background: #fafafa;
    border: 1px solid #e5e5e5;
    border-radius: 12px;
    padding: 10px;
  }
  .imggrid img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    display: block;
  }
  .imgcap {
    margin: .6rem 0 0;
    font-size: .92rem;
    color: #555;
  }
  @media (max-width: 560px) {
    .imggrid { flex-direction: column; }
  }
</style>

<!-- Row 1: With Handles -->
<h4>Version A — With Handles</h4>
<div class="imggrid">
  <figure class="card">
    <img src="" alt="Donning tube with handles render">
    <figcaption class="imgcap"><strong>Render</strong> — Cylindrical tube with two ergonomic handles for improved grip and leverage.</figcaption>
  </figure>
  <figure class="card">
    <img src="https://files.oaiusercontent.com/file_00000000c1cc71f6a29d26d6c94100fe" alt="Donning tube with handles parameters">
    <figcaption class="imgcap"><strong>Parameters</strong> — Adjustable diameter, height, handle dimensions, and fillets for easy customization.</figcaption>
  </figure>
</div>

<!-- Row 2: Without Handles -->
<h4>Version B — Without Handles</h4>
<div class="imggrid">
  <figure class="card">
    <img src="https://files.oaiusercontent.com/file_00000000412471f688fad49fac246a75" alt="Donning tube without handles render">
    <figcaption class="imgcap"><strong>Render</strong> — Compact version without handles; ideal for limited material or smaller limb fittings.</figcaption>
  </figure>
  <figure class="card">
    <img src="https://files.oaiusercontent.com/file_0000000003d471f68a89989aa7fb254e" alt="Donning tube without handles parameters">
    <figcaption class="imgcap"><strong>Parameters</strong> — Simplified design with parametric diameter and height for quick resizing.</figcaption>
  </figure>
</div>

<p><em>Next Steps:</em> Export parameter sets for S/M/L versions, test usability with handle variations, and finalize wall thickness and material specs for hospital use.</p>


<img width="1192" height="1042" alt="Screenshot 2025-11-05 192056" src="https://github.com/user-attachments/assets/d7ac6cb8-4f7d-486d-aa9d-36337e90f16c" />

<img width="2992" height="1403" alt="Screenshot 2025-11-05 192131" src="https://github.com/user-attachments/assets/bea62f4e-51bf-4426-8665-09d5d041f805" />

<img width="1170" height="1060" alt="Screenshot 2025-11-05 192222" src="https://github.com/user-attachments/assets/0978fbb8-04c7-4975-b380-3b5246e0988a" />


<img width="3048" height="1163" alt="Screenshot 2025-11-05 192256" src="https://github.com/user-attachments/assets/d5efbf65-bc9a-4cc6-932a-41dd5a577aa6" />





