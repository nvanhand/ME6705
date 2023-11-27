# Introduction 
A touch probe is a ubiquitous tool found in many manual and CNC machines which is essential for accurate measurements. A touch probe aids in coordinating the machine origin to the physical part, and can help find the zero coordinate position in multiple axes. At the simplest end of the spectrum, CNC touch probes can be a simple spring which, when offset, can visually indicate that the edge of a workpiece has been contacted, at which point the machinist can manually zero the coordinates. More complex probes utilize a conductive tip that relays an impulse to a controller. Based on the preset tool offsets, the system can automatically set the recorded coordinate as the new zero. 

At the GT Advanced Manufacturing Pilot Facility (AMPF) many machines are outfitted with automatic touch probes. Machines like the Mazak VCU-500AM utilize a Renishaw probe which functions using a Renishaw tool cycle in order to control the touch probe and set new relative coordinates. However, other machines, such as the facility's Okuma Armoid, has no probe tool. The machine of interest is a standard CNC lathe and thus only requires the touching off of the Z (axial) and R (radial) directions. 

In order to address this need, Team 1 has chosen to model a 1D Touch probe system using the myRio microcontroller. The resulting insights and hardware will be later utilized for the Okuma system. In the proposed system, the machine is simulated with a motor and the coordinate logic is programmed in LabView. 

# Requirements
## Table of Requirements
| Category | No. | Threshold/ <br> Objective* | Requirement | Value | Unit |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Interface | 1 | T | Users shall interface with the prototype via a LabView front panel. | T/F |  |
|  | 2 | T | Interface will permit the activation of measurement routine. | T/F |  |
|  | 3 | T | Interface should update with the measured distance value. | T/F |  |
|  | 4 | O | System will provide debug logs to the interface | T/F |  |
| Measurement/Data <br> Capture | 5 | T | Measurement accuracy | 1 | mm |
|  | 6 | O | Measurement accuracy | 0.1 | mm |
|  | 7 | T | System uncertainty should be quantified and reported | T/F |  |
|  | 8 | O | Measurement repeatibility | 0.01 | mm |
|  | 9 | T | Measurement repeatibility | 0.001 | mm |
| Wireless | 10 | O | Quantify and report system latency | 1 | s |
|  | 11 | T | System connects to laptop without wired connection | T/F |  |
| Feedback | 12 | O | Have external light to indicate Myrio power | T/F |  |
|  | 13 | T | System should alert user when contact is made with probe during measurement. | T/F |  |
| Weight/Dimensions | 14 | 0 | Touch probe weight | 1 | lb |
|  | 15 | O | Touch probe width/length | (4,6) | inch |
|  | 16 | O | Touch probe length | (4,6) | inch |
|  | 17 | O | Probe travel distance | <10 | inch |
| Power | 18 | T | Prototype shall operate for 1 hour without the need to change batteries | 1 | hour |
|  | 19 | O | Prototype shall have "idle" mode which can run without significant power loss. | T/F |  |
|  | 20 | O | Prototype shall operate for 4 hours without the need to change batteries | $4+$ | hour |
| Quality Control <br> (mandatory) | 21 | T | Number of system bugs detected upon prototype demonstration | $<5$ | bugs |
|  | 22 | O | Number of system bugs detected upon prototype demonstration | 0 | bugs |
|  | 23 | T | Project professionalism | Scale: $1-10$ |  |
| Project requirements <br> (mandatory) | 24 | T | Prototype uses LabVIEW | T/F |  |
|  | 25 | T | Prototype uses the myRIO | T/F |  |
|  | 26 | T | Prototype uses $2+$ actors | T/F |  |
|  | 27 | O | Prototype uses at minimum 2 actors to perform meaningful, complex system. | T/F |  |
|  | 28 | T | Prototype uses $2+$ sensors | T/F |  |
|  | 29 | O | Prototype uses at minimum 2 sensors of sufficient complexity.  | T/F |  |
|  | 30 | T | Prototype design/assembly is unique (i.e. not found from a brief Google search) | T/F |  |
|  | 31 | O | Prototype creativity/uniqueness, as determined by customer (Dr. Noel) | Scale: $1-10$ |  |
|  | 32 | T | Prototype uses at least 1 advanced mechatronics concept | T/F |  |
|  | 33 | O | Prototype goes above and beyond with exploring advanced mechatronics concept | T/F |  |
## Discussion 
The previous section will be discussed in further depth in this section. 
https://www.ni.com/docs/en-US/bundle/labview-myrio-toolkit/page/myriohelp/myrio_latency_n_samples.html 
### Project Requirements, Quality Control
The project and quality control requirements were provided by the ME 6705 instructor and TAs. The requirements were defined to display basic mastery of the course material, requiring meaningful sensors and actors for the prototype. The designed system utilizes the following sensors and actors:
|  |  | Purpose |
|---|---|---|
| Actor 1 | Stepper Motor | Drive measurement probe forward. |
| Actor 2 | Buzzer  | Audibly indicate when a measurement has been made. |
| Sensor 1 | Encoder | Accurately measure sensor position. |
| Sensor 2 | Limit switch | Indicate when the touch probe has made contact.  |

### Power
Power requirements were designed not as threshold characteristics but "nice-to-have" objectives which indicate success as a probe. Touch probes are typically powered externally to the machine via batteries, as the prototype will be. However, the prototype's battery life is expeceted to be much shorter than a typical probe, as the entire assembly must be powered rather than just the probe. 

### Weight/Dimensions
The only requirements for the physical system involve the probe head, as the remainder is simply a simulation of a real system. The probe should be 
compact and of a size compatible with Okuma tool holders. Generic measurements were chosen based on a reasonable size and travel distance. 

### Feedback
At a minimum, there should be an obvious indication when a measurement has been taken. The proposed design utilizes a buzzer to indicate a completed measurement, similar to the sound made by Renishaw probes. 

### Wireless
Related to project requirements, the system should function without physical connection to the controlling laptop. Ideas for extensions of this domain were: automated IP detection, measuring limits on wireless communication based on reason, HTTPs functionality. 

### Measurement Capture
For any touch probe system, measurement capability is an important metric to quantify and report with any product. In all cases, the highest possible accuracy and measurement repeatibility is ideal, however, reasonable thresholds have been set in order to prove out the system. 

# Project Demo 


# Challenges
### Wireless Connection

### Mechanical Assembly

### 
# Conclusions
Throughout the process of this project, the 
5. A discussion of challenges encountered.
6. A conclusion, discussing lessons-learned and potential next steps.
