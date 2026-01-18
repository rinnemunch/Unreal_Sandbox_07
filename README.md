# Project 1 – Scalable Door Interaction System (Blueprint Interfaces)

## 🖼️ Preview

![Project 1](Media/1.gif)

## 🧱 Features

**Blueprint Interface–Driven Interaction**

- Uses a shared `BPI_Interact` interface to decouple interaction logic  
- Any actor can trigger interactions without direct references  
- Enables reuse across doors, buttons, triggers, and future interactables  

**Reusable Door Actor**

- `BP_Door` contains no input logic or knowledge of who activates it  
- Open and Close behavior exposed through custom events  
- Timeline-driven rotation ensures smooth, data-driven motion  

**Button-Based Control System**

- `BP_Button` implements the interaction interface  
- Instance-editable door reference allows flexible level setup  
- FlipFlop logic toggles open and close without duplicated code  

**Centralized Player Interaction**

- Interaction input handled exclusively on the player character  
- Multi-sphere trace detects nearby interactable actors  
- Interface checks ensure only valid actors respond  

## 🚀 Result 

---

A fully scalable interaction system where doors respond to players, buttons, or any future trigger without tight coupling.  
This pattern establishes a clean foundation for expanding interaction mechanics across an entire Unreal Engine project.

# Project 2 – Physics Grab and Rotate Interaction System

## 🖼️ Preview

![Project 2](Media/2.gif)

## 🧱 Features

**Enhanced Input–Driven Interaction**

- Uses Enhanced Input Actions for grab, pitch rotation, and yaw rotation  
- Hold-based grab input allows continuous interaction while pressed  
- Separate axis inputs enable precise object rotation control  

**Camera-Based Line Trace Detection**

- Line trace originates from the first-person camera  
- Adjustable grab distance allows flexible interaction range  
- Any visible component can be detected without hard references  

**Physics Handle Object Manipulation**

- Physics Handle component manages object holding and movement  
- Target location updates every frame to maintain camera offset  
- Rotation preserved and updated incrementally while held  

**Dynamic Object Rotation System**

- Stored rotator tracks current held object orientation  
- Pitch and yaw inputs applied additively per frame  
- Rotation speed exposed for easy tuning and iteration  

**Visual Feedback via Outline Material**

- Simple unlit outline material applied on grab  
- Overlay material clearly communicates interaction state  
- Automatically removed when the object is released  

**Flexible Physics Test Actors**

- Supports static and skeletal meshes  
- Continuous Collision Detection enabled for stability  
- Physics-driven behavior mirrors familiar first-person interaction systems  

## 🚀 Result

A fully functional physics-based grab and rotate system that allows players to pick up, inspect, and manipulate objects in real time.  
This project establishes a strong foundation for expanding interaction mechanics such as throwing, snapping, or context-aware object use.

--- 

# Project 3 – Chaos Fracture Interior Material Setup

## 🖼️ Preview

![Project 3](Media/3.gif)

## 🧱 Features

**Chaos Geometry Collection Workflow**

- Static mesh converted into a Geometry Collection using Fracture Mode  
- Uniform Fracture applied to generate clean, testable fracture pieces  
- Bone colors disabled for accurate material preview  

**Interior vs Exterior Material Separation**

- Geometry Collection material slots expanded to support multiple materials  
- Slot 0 reserved for exterior surface material  
- Slot 1 dedicated to interior fracture faces  

**Interior Material Visualization**

- Custom bright emissive material created for clear interior face visibility  
- Explode Amount used during setup to preview internal surfaces  
- Ensures interior faces are visually distinct during fracture testing  

**Material Assignment to Internal Faces**

- Interior bones selected via Fracture Hierarchy  
- Assign Material utility used with Material Index set to interior slot  
- Material applied to **Only Internal Faces** for correct separation  

## 🚀 Result

A properly configured Chaos Geometry Collection where fractured interior faces use a dedicated material while exterior surfaces remain unchanged.  
This setup ensures believable destruction visuals and establishes a reliable workflow for advanced Chaos-based destruction systems in Unreal Engine 5.
