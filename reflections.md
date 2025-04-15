# Reflections

Brain dump of notes (come back to edit for clarity)

Understanding data link and power contrains based on pixel density. Pixel resolution is defineing factor on spliting zones. 
Zones exist to limit pixel load per link
Zones keep failure domains small
Data links are designed around cabinet power limits, pixel load, signal stability.

I've confused zones and cabinets - A single seamless display is ALWAYS built from multiple cabinets
  - Cabinets are physical structures and when powered processing streams treats all cabinets _together_ as one logical display area. 
      - S-box / Sending box card config processes this

What low cost projects can I create:
  - CRT wall?
    - custome PCB stream deck too crt wall

LED Modules (Segments) - Small magnetic LED tiles	- Passive, Just LEDs. No smart function.

Cabinet - Frame holding LED Modules - Has Hub Board (Receiver Card). Manages signal for modules within it.

Zone (Data Zone) - Group of Cabinets	- Defined by data link / pixel load / signal limitations.

Display / Screen - Logical grouping of all Zones - Appears as one seamless image to the viewer.

LED Wall = 1 Display (Seamless)
    |
Built From = Many Cabinets (Physical Frames)
    |
Each Cabinet = Contains Hub Board + Passive Modules
    |
Cabinets Grouped Into = Data Zones (For Load Management)

My confusion here was thinking cabinets hold each zone. Zones are managed data sections and can span across multiple cabinets regardless of cabinets and the HUB board.

Truss beams - research further 

  - https://www.youtube.com/watch?v=zjJAta--kAs
  - https://www.youtube.com/watch?v=U4i47SOvSXQ
  - https://www.youtube.com/watch?v=-apD6HCsKRA
  - https://www.youtube.com/watch?v=-6A-wy_FW4U

1 Wall = Many Cabinets

1 Cabinet = Hub Board + LED Modules

Data Links = Cabinet-to-Cabinet

Newer cab hubs may have intergrated T-con boards (T-CON: board to regulate and assign data to each LED module. From what I have read, often refered too when a row or single LED module is showing issues/flickering etc)

Zones = Logical Groups of Cabinets (for signal load management)

Power Chains = Separate from Data Links (but follow similar grouping)

Breakdown

https://www.youtube.com/watch?v=wTxtpojJbDc

  - NovaStar VX4S All-in-1 Controller / Video Processor
  - 4 LED modules per cabinet it looks like
  - Controller VX4 talking to server
  - Novel CT software?

## Control Integration for S-box (return back to after basics and fundamental knowledge)

- Crestron / Q-SYS / Extron programming and scripting?
- control over IP via http commands, telnet?, TCP sockets
- Is samsung API heavily used alongside crestron etc?:
  - power off/on
  - input switching
  - volume / mute
  - presets and diagnostics  

Crestron:
  - https://docs.crestron.com/en-us/index/Content/Topics/Home.html

Q-SYS
  - https://support.qsys.com/

Extron
  - https://www.extron.com/training/howtovideos
  - https://www.extron.com/Training/LearningGuide/TrainingLibrary

