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
```
C:\>ping 192.168.0.2
Pinging 192.168.0.2 with 32 bytes of data:

Reply from 192.168.0.2: bytes=32 time<1ms TTL=128
Reply from 192.168.0.2: bytes=32 time=6ms TTL=128
Reply from 192.168.0.2: bytes=32 time<1ms TTL=128
Reply from 192.168.0.2: bytes=32 time<1ms TTL=128

Ping statistics for 192.168.0.2:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 6ms, Average = 1ms
```

- In the switch CLI you are able to check the mac address table with the show mac-address-table command in the elevated prompt area of the CLI
```
SW1>enable
SW1#show mac-address-table 
          Mac Address Table
-------------------------------------------

Vlan    Mac Address       Type        Ports
----    -----------       --------    -----

SW1#show mac-address-table
          Mac Address Table
-------------------------------------------

Vlan    Mac Address       Type        Ports
----    -----------       --------    -----

   1    0001.64b3.75c0    DYNAMIC     Fa0/2
   1    0030.a3a3.c51b    DYNAMIC     Fa0/1
SW1#
```
## Screenshots/ Diagrams
### Network Layout
![layout](/assets/layout.png)
### PC Configuration GUI
![PC Configuration Screens](/assets/pc_configurations.png)
### Showing Empty MAC Address Table
![empy mac address table](/assets/empty_mac_address_table.png)
### Ping Results from PC1 to PC2
![pinging PC2 from PC1](/assets/ping_results.png)
### Updated MAC Address Table after the successfull ping
![updated mac address after the ping](/assets/updated_mac_address_table.png)
## Challenges and Lessons Learned
- From a network standpoint this was pretty cut and dry.
- Learning to really look at network design and structure for presenting has been a little more of a challenge than I thought.
- Learning markdown to present my future projects will take a little time but overall fealing much more confident with it.
## If you made it this far reading this readme than I want to say thank you.  This is the start to my journey of posting what I am learning and how I am doing it.  Looking back about a year from now at this first little network project is probably going to be mind blowing.  But again thank you for sticking around and any advice is apprecited.
