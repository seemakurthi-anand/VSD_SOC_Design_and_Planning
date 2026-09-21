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
IO placer revision, changing IO mode to 2
file:///home/vsduser/Pictures/floorplan/different_io_placer_io_mode2.png<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/8f8cf72d-25ef-4611-83ad-9db7b13e6324" />

Labs for git clone vsdstdcelldesign
Commands to clone from git and use .mag file
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/76774904-9ed4-429f-b5d0-533bed552a3e" />
Inverter layout already available:
Red line is polysilicon
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/a91be289-96df-4705-9380-2aa51068a006" />
Day 3 -> Session 2  <br>
Checks to say it is Inverter
Check NMOS area in tkcon window
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/bf1997a6-74db-4107-9e54-ae5b850a829b" />
Check PMOS are in tkcon window
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/97a41a66-df9c-49fc-b8e3-adb9a7d53e23" />
Check Polysilicon (Gate)
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/9cfb5a9a-ef7e-4a87-8ea6-ed5cd9b7eb8d" />
Check Pmos drain to Nmos drain collection(by pressing S 3 times at Vout port)
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/8177a13e-1ad0-4414-b8a8-cc01cbb62ed8" />

Check Pmos Source to VDD
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/a198624e-661d-4849-830f-aa4884b29699" />

Check NMOS Source to GNd
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/58504398-7485-4877-baed-aba82ee255b3" />

Sample DRC Error
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/05299365-65cb-4171-9018-7f35d13ffeb4" />

Genration of ext file and spice file from Tkcon
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/d754a253-c2cb-435f-8e16-de8b1f2a5b78" />
Box dimension
file:///home/vsduser/Pictures/standardcell/box_ht_width_in_tkcon_window.png<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/c99f4314-ccc5-4e71-8880-82c7402fe3bd" />
Day 3 -> Session 3  <br>
Final spice deck for transient Analysis
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/0d2177d6-3cb6-4fcd-a958-32824475055a" />
Inverter waveform NGSpice
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/a957a087-21cd-43cb-b22f-cae4794b06aa" />

Input fall Output Rise
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/508d533d-3f19-4661-b70c-40c5c0b19a1d" />
Input rise , Output Fall
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/8fd2c3e7-bf53-4c42-b86d-82a795b26ce3" />

Rise time of O/p = 2.245n -2.182n = 0.063n 
 <br>
Fall time of O/p = 4.095n -4.052 = 0.043n  
 <br>
O/p rise delay =   2.211n -2.15n = 0.061n  
<br>
O/p fall delay =  <br>

Adding missing DRC rules wrt skywater130 <br>

First download magic layout examples
file:///home/vsduser/Pictures/DRC/DRC_tests.png<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/1379d07f-593a-47d7-9c5b-70061504778a" />












