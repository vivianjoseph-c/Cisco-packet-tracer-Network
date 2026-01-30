# Cisco-packet-tracer-Network

# My Project Overview

I built this project to practice and demonstrate how a small enterprise network is designed and connected using Cisco Packet Tracer. The goal was to simulate a real‑world organizational network with multiple departments, centralized infrastructure, and clear connectivity logic.

The organization is divided into three departments:

# HR Department
# Finance Department
# IT Department

Each department has its own access switch and end‑user PCs, all connected through a core switch and a router. A central server is also included to represent shared enterprise services.
# Why I Built This Network

As someone learning networking and cybersecurity, I wanted a project that:

-Reflects real enterprise network design
-Shows my understanding of routers, switches, and end devices
-Can be easily explained to recruiters and interviewers
-Serves as a foundation for future improvements like VLANs and security controls

# Step 1: Network Planning

Before placing any devices, I planned the network structure with scalability and clarity in mind.

My design decisions:

-Use a core switch for centralized connectivity
-Separate departments using individual access switches
-Keep cabling simple and logical using a star topology
-Allow easy future expansion (more users or departments)

Planned devices:

-1 Router (Cisco 2911)
-4 Switches (Cisco 2960‑24TT)
-1 Server
-9 PCs (3 per department)

# Step 2: Placing the Devices

In Cisco Packet Tracer, I added and positioned the devices as follows:

Core Infrastructure

-Router0 (2911) – placed at the top to act as the network gateway
-Switch0 (2960‑24TT) – placed below the router as the core/distribution switch
# Departmental Infrastructure

-HR Switch connected to PC0, PC1, and PC2
-Finance Switch connected to PC3, PC4, and PC5
-IT Switch connected to PC6, PC7, and PC8
# Server
Server0 placed near the core switch to represent centralized enterprise services

# Step 3: Connecting the Router to the Core Switch

I used a Copper Straight‑Through cable to connect:
 -Router0 (GigabitEthernet0/0) → Switch0 (FastEthernet port)
This allows the router to act as the gateway for all connected departments.

# Step 4: Connecting the Core Switch to Departmental Switches

Using Copper Straight‑Through cables, I connected:

-Core Switch → HR Switch
-Core Switch → Finance Switch
-Core Switch → IT Switch
This forms a hierarchical star topology, which is common in enterprise environments.

# Step 5: Connecting End‑User Devices

Each PC was connected to its department switch using Copper Straight‑Through cables.

# HR Department

-PC0 → HR Switch
-PC1 → HR Switch
-PC2 → HR Switch

# Finance Department

-PC3 → Finance Switch
-PC4 → Finance Switch
-PC5 → Finance Switch

# IT Department

-PC6 → IT Switch
-PC7 → IT Switch
-PC8 → IT Switch

# Step 6: Connecting the Server

I connected Server0 directly to the core switch using a Copper Straight‑Through cable.
Placing the server at the core allows it to be accessed by all departments and represents shared services such as:
-File storage
-DNS
-DHCP

# Step 7: Verifying Physical Connectivity

After completing all connections:
-All links showed green status indicators
-This confirmed that the devices were properly connected
-Packet Tracer automatically handled MDI/MDIX, so no crossover cables were required

# Step 8:IP addressing and basic configuration

After completing the physical connections, I assigned IP addresses to all devices to enable communication across the network.

IP Address Assignment

-Assigned static IP addresses to all PCs based on their department
-Configured the server with a static IP address
-Set the router interface IP address to act as the default gateway
-Verified that all devices were on the correct network segments

This step ensured that each device could be uniquely identified and communicate properly within the network.
# Step 9: VLAN Configuration

To improve organization and security, I created VLANs to logically separate the departments.
# VLANs Created
-VLAN 10 – HR Department
-VLAN 20 – Finance Department
-VLAN 30 – IT Departmen
-VLAN 40

I assigned switch ports to their respective VLANs based on department and configured trunk links between switches to allow VLAN traffic to pass.

# Step 10: Inter-VLAN Communication
To allow devices in different VLANs to communicate, I configured the router to support inter-VLAN routing.
This enabled:
-Communication between departments when required
-Centralized routing control through the router
-Better simulation of a real enterprise network

# Step 11: Server Configuration

I configured the server to represent centralized enterprise services.

# Server Setup
-Assigned a static IP address
-Verified connectivity to all VLANs
-Ensured the server could respond to network requests

The server was reachable from all departments, confirming correct routing and VLAN configuration.

# Step 12: Connectivity Testing and Verification

To confirm that the network was working as expected, I performed several tests:
-Pinged devices within the same VLAN
-Pinged devices across different VLANs
-Pinged the router, switches, and server
# Successful ping responses confirmed that:

-IP addressing was correct
-VLANs were properly configured
-Inter-VLAN routing was functioning
-The overall network design was working as intended

### Conclusion

This project allowed me to design, configure, and test a functional enterprise-style network. It demonstrates my ability to:
-Plan and implement a network topology
-Assign and manage IP addressing
-Configure VLANs and inter-VLAN routing
-Verify network connectivity through testing

This network serves as a strong foundation for more advanced networking and cybersecurity projects.

# Here is the link to my project
https://github.com/vivianjoseph-c/Cisco-packet-tracer-Network/commit/1463521d48110248f2208ddbc578d8c4ed80809c

