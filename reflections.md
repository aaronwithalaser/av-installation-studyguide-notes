# Reflections

Brain dump of notes (come back to edit for clarity)

Understanding data link and power contrains based on pixel density. Pixel resolution is defineing factor on spliting zones. 
Zones exist to limit pixel load per link
Zones keep failure domains small
Data links are designed around cabinet power limits, pixel load, signal stability.

I've confused zones and cabinets - A single seamless display is ALWAYS built from multiple displays
  - Cabinets are physical structures and when powered processing streams treats all cabinets _together_ as one logical display area. 
      - S-box / Sending box card config processes this

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

My confusion here was thinking cabinets hold each zone. Zones are managed data sections and can span across multiple cabinets regardless of cabinets and the HUB board. It's starting to click. 


1 Wall = Many Cabinets

1 Cabinet = Hub Board + LED Modules

Data Links = Cabinet-to-Cabinet

Zones = Logical Groups of Cabinets (for signal load management)

Power Chains = Separate from Data Links (but follow similar grouping)
