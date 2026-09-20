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
Day 1 Setup Openlane, Prepare Design and Run Synthesis
**Exploring various files and pdks**
<img width="940" height="617" alt="image" src="https://github.com/user-attachments/assets/be60900c-fdfb-4460-9d3e-e7a7ed01b90c" />
**Start Openlane and Prepare design **
<img width="602" height="410" alt="image" src="https://github.com/user-attachments/assets/d52092cf-5fcd-403c-afad-75e87e0e1f81" />
**Exploring picorv32a directory and runs directory
Once Design Prep step is completed, a folder with current date is created in runs directory and a merged.lef is created inside tmf folder of newly created current_date directory **
<img width="602" height="366" alt="image" src="https://github.com/user-attachments/assets/7bbad248-5bce-4b07-b614-37b90c146793" />

**Synthesis Successful**
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/33d8b284-538c-4127-a976-d87c6670d992" />

**Flop ratio:** Number of F/F’s / Number of Cells =1613/14876
<img width="602" height="374" alt="image" src="https://github.com/user-attachments/assets/c302a2b8-c565-4c63-8923-b9089f080cf4" />
<img width="602" height="387" alt="image" src="https://github.com/user-attachments/assets/8340bbcf-22a1-49c9-8192-9cb82dddda5d" />
Floor Planning Successful
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/b7cec78d-d87e-42bf-836e-5bc498578ba4" />




Day 2 -> Session 1 -> Labs on Floor Planning
**Before Placement the standard cells positions not fixed yet**
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

Day 3 -> Session 1 -> Labs on CMOS Inverter Ngspice Simulations
Labs for git clone vsdstdcelldesign
Commands to clone from git and use .mag file
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/76774904-9ed4-429f-b5d0-533bed552a3e" />
Inverter layout already available
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/a91be289-96df-4705-9380-2aa51068a006" />







