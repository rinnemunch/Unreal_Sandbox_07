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

A fully scalable interaction system where doors respond to players, buttons, or any future trigger without tight coupling.  
This pattern establishes a clean foundation for expanding interaction mechanics across an entire Unreal Engine project.

