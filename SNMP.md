# Simple Network Management Protocol (SNMP)

## Tags

:network_protocols:

## Content

- Given managed devices on IP networks, SNMP
  - Collects and organizes information
  - Modifies those information to change behavior of said devices
- SNMP shows management data on managed systems as variables
- Those data are organized in Management Information Base (MIB)
- Managing applications can query those data remotely
- SNMP has *three* key components
  - Managed devices
  - Agent which run on managed devices
  - Network Management Station (NMS) which runs on one or more managers
- A managed device is a network node with SNPM interface that allow
  - Unidirectional (read-only)
  - Bidirectional (read & write) access to node-specific information
- An agent is a network-management software module on a managed device
- There can be one or more NMS on a network which runs on administrative
computers called managers
- Variables are organized in hierarchies and accessed via SNMP

## References

- [Wikipedia](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol)
