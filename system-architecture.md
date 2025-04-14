# System Architecture

## Overview

This section provides a basic theoretical understanding of how a typical Samsung LED system is structured from source to display.

This exists to build a conceptual framework for recognising components, understanding signal flow, and identifying where mistakes are most likely to happen during installation.

## Core Components Breakdown

### 1. Media Source
- Typically a media player, PC, or video switcher.
- Outputs video via HDMI or DisplayPort.

### 2. Processor (S-Box / Signage Box)
- Samsung SBB-CS4BPGS.
- Inputs: HDMI / DisplayPort.
- Outputs:
  - HDBaseT over CAT6 for short distance.
  - OCM (Optical Cable Module) Fibre for long distance / clean signal. (OCM) - One connect propritary cables?

*Purpose:*  
Receives video signal → Scales based on amount of segments in each cabinet? → Encodes for transmission → Sends to IG.

### 3. Interface Gender (IG)
- Pasive breakout point.
- Receives HDBaseT or Fibre signal.
- Converts it into a format usable by the LED cabinets.
- Splits signal into:
  - Primary Data Line
  - Redundant Data Line
      Always two data lines for each zone?

### 4. Cabinets (LED Frames)
- Contains Receiver Card / Hub Board - (Research hub boards and connections on these boards: model numbers/propriitary?)
- Manages signal to LED modules (segments) inside cabinet.
- Docking connections used vertically (signal + power combined).
- System cables used horizontally (Samsung proprietary 24-pin cables).

### 5. Receiver Card / Hub Board
- (Research hub boards and connections on these boards: model numbers/propriitary?)

### 5. LED Modules
- The physical LED panels (tiles).
- Connected internally to the Receiver Card using ribbon cables.

## Typical Data Flow Path

Media Source
    |
    V
S-Box Processor
    |
    V
HDBaseT / Fibre (OCM Cable)
    |
    V
Interface Gender (IG)
    |
    V
Primary Data Line > Cabinet 1 > Cabinet 2 > etc.
Redundant Data Line > Backup flow

## Example Diagram

Samsung LED Wall Basic Data Flow:

- Create visulisation to help understand basic data flow diagram and try to find commercial diagrams online.

## Key Concepts to Remember

- Primary and Redundant Data Lines for fault tolerance.
- S-Box only handles signal processing - cabinets have their own power supply. (max 4 powered cabs per s-box in most models?)
- IG is not a smart device but purely a signal breakout point to each zone (cabinet)
- Receiver Card inside cabinet manages video signal to LED Modules.
- Vertical Docking = No cables between stacked panels.
- Horizontal connections = System Cables (24-pin) or OCM Fibre if applicable.

## Resources

- Samsung LED Display Installation Manual  
https://eu.community.samsung.com/t5/led-displays/iwa-ifa-installation-manual/ta-p/10612892

- Samsung LED Training Videos  
https://www.youtube.com/playlist?list=PL51xQIiUs4fn57tMAuRTE90B15xAdUGtR

