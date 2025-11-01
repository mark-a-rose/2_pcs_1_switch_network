# 2 PCs and a Single Swith
## Goal
- Connect two PCs to a single switch and allow them to communicate with one another
## Architecture/Design
- This is a simple star topology as the switch will be in the middle for any connecting devices
## Problem Solved
- This project is just to get started with packet tracer and more simple network designs.
- Allows for connecting multiple devices to a single switch and see how the switch operates in terms of mac address tables
## Setup Instructions
- Place two PCs on the packet tracer work plain
- Apply static addresses on each device by going to the config panel then PastEthernet0 and apply the IP addresses.
- I chose the 192.168.0.0/24 network for my devices
- Place a single switch in between the two PCs
- Attache each PC to a port on the switch with straight through UTP cable
## Configuration and Verification Snippets
- PCs are configured with the GUI application of the device
- For checking connectivity between devices use the ping command with the command prompt
- ping PC2 from PC1 with the following command.
- In the switch CLI you are able to check the mac address table with the show mac-address-table command in the elevated prompt area of the CLI
