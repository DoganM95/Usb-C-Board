# Usb-C-Pcb

This repository contains the design files for a simple yet versatile USB-C PCB. It's designed to deliver 5 volts with USB 2.0 data pin support and includes power delivery capabilities. And yes, ChatGPT created this readme, so don't wonder.

## PCB Views

<table>
  <tr>
    <td><img src="https://github.com/DoganM95/Usb-C-Pcb/assets/38842553/076af51b-7ad3-4af9-b62b-d0bfeede7e81" alt="USB-C PCB Top View" width="100%"/></td>
    <td><img src="https://github.com/DoganM95/Usb-C-Pcb/assets/38842553/5c609ceb-8db7-49a8-9a2c-ab538c2fb626" alt="USB-C PCB Bottom View" width="100%"/></td>
  </tr>
</table>

## Features

- **5V Output:** The board outputs a stable 5 volts, suitable for various USB-powered devices.
- **Power Delivery Support:** For power delivery functionality, add two 5.1 KOhm resistors of size 0603 in the designated rectangles.
- **Mounting Holes:** Strategically placed drill holes on the sides allow for easy mounting.
- **Cut Limit Line:** A clearly marked cut limit line indicates the maximum cuttable range of the PCB without losing functionality.
- **Enhanced Power Wires:** Thick VCC and GND wires are designed to support high amperage loads.

## Building Steps

To assemble the USB-C PCB, follow these steps:

1. **Solder the USB-C Port:**
   - Position the USB-C port on the PCB.
   - Solder each pin carefully, ensuring good connection without bridging contacts.

2. **Clean Up Excess Solder:**
   - Inspect the solder joints and use a solder wick to remove any excess solder from the fine pins of the USB-C port.
   - Reheat the solder and apply the wick; the wick will absorb the excess, leaving a clean joint.

3. **Solder the Resistors:**
   - Place the 5.1 KOhm resistors in their designated spots on the PCB.
   - Solder the resistors, ensuring they are securely attached to the board.
  
## Key takeaways
- The CH340C can be powered with 3.3V as well as 5V, but its TX voltage perhaps is too high for e.g. an esp32, so powering it with 3.3V seems fine
- The 3V pin of the CH340C needs to be connected (exclusively) to GND with a 100nF capacitor in between, else it will not work and not show up in windows device manager
- Connecting it with wrong polarity (5V and GND) gets the chip hot quickly, but doesn't break it when cutting the power off soon (like 20 seconds)

Feel free to explore the design files, contribute, and suggest improvements to this project.
