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
Section 3:

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

DRC not catching errors
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/86ca2876-968c-4405-9616-c4d81054acb6" />

Adding rule polyres, poly distance rule

<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/1b05c432-bb13-462f-b4e2-da693b80e6b7" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/f5648ed5-87af-4a18-819c-c0f8a81dc67f" />


<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/58ad639f-58e5-4dc9-9ff9-a060ab3de1d3" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/ff84b746-6985-4cac-90fd-70965400796b" />


<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/13ab1a9e-f2b1-4a08-80cd-f59dec5ae9e6" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/9245656d-0f53-4995-94a9-7ef3fa538f63" />

DNWell
<img width="1919" height="916" alt="image" src="https://github.com/user-attachments/assets/8c8ca10e-0abd-474a-885b-4dc7d55bfb2e" />
Nwell DRC Error check
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/f39c4c0a-ef5e-4bd5-b605-4273fcf02299" />

Day 4 -> Session1
Changing Grid size as per tracks.info file
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/15880065-f38f-4549-80c0-5abb819887de" />
Width check for PR boundary
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/ce146b30-534e-4cd1-b46b-87109edcdca0" />
Height Check for PR boundary
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/5c746c2e-ec1f-41f3-ab36-723ad67a984a" />

Lef successfully extracted
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/f0c6d0b1-5df4-4a48-a7b3-4027a3226f0f" />

Lef file with pins and their direction, and also the order in which the description is mentioned 
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/937c6e07-c54a-4881-998f-33a6dab2f83e" />

Sample Lib file with Timing and Cell characterization
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/6a8ee19b-312e-4508-a83c-7a4f64cc3bd6" />

<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/660607da-7b8a-413e-9104-c78168c9f9cd" />

Updated config.tcl file in configs/picorv32a

<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/ab6a437a-f2a5-4773-8d83-166af621c4be" />

Preparing design
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/de956cb8-76c2-4a84-b723-b75d9ece199c" />

Run Synthesis

Custom Cell shown during run synthesis 

<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/fb65e293-7d84-409c-b461-ce3a85d2aee3" />

Synthesis Successful but huge Negative Slack
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/7a8998e7-129c-4369-9710-fd9627291f8d" />
Area before Synth_strategy changed
<img width="1846" height="174" alt="image" src="https://github.com/user-attachments/assets/65670cd3-9010-4502-a28c-78ede681a9cc" />

Readme info of SYNTH_STRATEGY from openlane/configuration  
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/53193c76-7d61-4740-a480-31506cb5c3cf" />

Commands to view and change synthesis parameters
<img width="1852" height="253" alt="image" src="https://github.com/user-attachments/assets/b8f991a7-b9a1-4576-844c-f4dcdcaf73d0" />


Area after Synth_strategy changed
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/7c6b3693-2339-4140-905e-6d54a978e03f" />

Automatic updation of merged.lef inside runs/date_folder/tmp ensuring no problems will happen during placement
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/02631c66-2850-4e03-87da-5b6dbde086bb" />
Unexpected error encountered during run_flowplan
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/63ad0bfa-e067-4c69-aa43-9afa3ea49e13" />
Sequence of steps run to resolve floor plan errors
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/43d40a0f-5e43-467e-8a06-b3a14d0446c0" />
<img width="1854" height="491" alt="image" src="https://github.com/user-attachments/assets/ebf9c25b-aeea-46c3-ace7-0a66b0ba79ac" />

Placement Done
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/7f162e03-116b-43cb-9edc-77a32b277ec3" />

Magic layout after placement
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/2d920551-913c-45cc-ba1d-0343a2ab97f2" />
Magic layout highlighting with custom cell SKY130_VSDINV 
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/1e06b534-7678-4e5d-b22f-eb740f208ac1" />
Extend View (by typing extend in tkcon window) <br>
We can also see abutment(intersection with others) where power and gnd rails are shared between the cells
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/23b5f201-f962-45b8-9950-9402271e2df7" />

Optimizing the worst-case slack.<br>
To use OpenSTA, we need to create two more files and work on it. 
1) pre_sta.conf created in openlane/ directory
2) my_base.sdc created in designs/picorv32a/src directory <br>
Open STA results:
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/57529bc4-1744-4785-8245-3b35296d5ae0" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/0f152834-0bd8-4514-a7c8-55f08a2cb857" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/d283ca5e-3a89-4372-922e-1974beba8040" />
<img width="1855" height="304" alt="image" src="https://github.com/user-attachments/assets/48eb0186-3a45-4236-82e7-48884866f9b5" />

Limiting the fan-out to improve the slack
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/13d1fc1f-67d5-4300-adad-2a8ea06df3fe" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/0596e58d-ecd5-42db-97ce-b35451bb2700" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/9c1168fd-1d41-40c4-a309-dd87c5560fb4" />

This OR gate which is of small size has many fanouts


Changing Drive strength for Gates with High Fanout <br?
The following are various commands to check the driver and fanouts of a net and replace with larger cell and generate reports with 4 bit precision in displayed values
<img width="1853" height="282" alt="image" src="https://github.com/user-attachments/assets/9420f2ec-a2d9-40a1-bab2-b4bac1d44690" />

<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/1015e468-843f-44d3-a878-574e4789bf8c" />

<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/9ca84d6e-4a85-4761-81d2-27700b7d7cad" />

Finally slack changed from -23.9 to -22.6173
Instances of _14506_ gate that caused more impact 
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/bc92d6d9-a500-4f8c-a416-68d70ef1e299" />

Continuing the preious design of 0ns slack <br>
Synthesis
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/d0bdff61-fbde-480b-ab5f-b2f63944c2e7" />

Floor plan
<img width="1857" height="348" alt="image" src="https://github.com/user-attachments/assets/63ba97a0-9c5f-4d24-8642-8a0634929042" />
<img width="1859" height="414" alt="image" src="https://github.com/user-attachments/assets/f1159e5d-050d-4242-8ae3-787a76025da5" />
<img width="1855" height="512" alt="image" src="https://github.com/user-attachments/assets/c0e319ad-a501-418f-8551-89bf1ee51945" />
Placement
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/fd1c5829-5446-4ad6-a19f-25557771cc52" />
CTS
<img width="1862" height="463" alt="image" src="https://github.com/user-attachments/assets/7fd43bd7-e8d5-4d33-b912-c2b3a2391edc" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/2edf5197-3af2-4eae-b9fc-5bcbcd0ab40e" />
Openroad
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/6173d8ed-c2e2-42fb-826c-634186c42baa" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/97d167c6-d503-4324-9dfc-5cb168d39ebd" />
<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/9107f17e-a3e6-44e6-ae2f-d1499ed6efc8" />
<img width="1856" height="185" alt="image" src="https://github.com/user-attachments/assets/4eade255-e051-4e5b-bc37-c48c152e9db6" />







