# VSD_SOC_Design_and_Planning
This repo contains work done during VSD_SOC_Design_and_Planning a course of 10 day duration by Kunal Ghosh, Mohammad Shalab, Nickson
Organization of course
The course is organized in 5 key sections
Section 1: 
Talks about how an Application C code is  translated into hardware language and, from there, how it is converted to layout 
Description of Openlane ASIC design flow 
Introduction to open-source EDA tools and covering till synthesis
Section 2:
Theory about floor planning and also labs associated with it 
Library Binding and Placement also labs associated with it
Day 2 -> Session 1 -> Labs on Floor Planning
Before Placement the standard cells positions not fixed yet
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/7ae2e053-0c34-4702-8043-ad1ebc218dbf" />

Day 2 -> Session 2 -> Labs on Placement (Conjestion aware placement using ReplAce)
Here, we focus on congestion-based placement, not really bothering about the timing. We try to reduce the congestion. There are two kinds of placement:
- Global placement
- Detailed placement

Commands:
<img width="1280" height="768" alt="image" src="https://github.com/user-attachments/assets/f1833c50-8b17-4aff-9cbf-bf75cc1b0ada" />
Completion indication of placement
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/85131ec9-dc10-4247-9de9-d766eefa816d" />

Standard cells arrangement after Placement step
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/9530eb59-1708-4a4e-b4bd-d5cc737e347e" />

Zoomed version showing standard cells after placement step 
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/d57b5940-fe2c-4014-83c3-da57a76a0f4a" />
 Usually, the power distribution network has to be designed during the floor planning step, but in OpenLane, the sequence is slightly different, so we will be having it after CTS and just before routing. 

 Day 2 -> Session 3 -> Cell Design Characterization flows
 A library is a combination of cells with various functionalities, various sizes, and various thresholds. If the size of the buffer  is larger, then it has more drive strength. The below image shows what all are in library
 <img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/c2b00113-d1c8-403e-befe-4c80576f4ef9" />







