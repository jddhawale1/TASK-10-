# TASK-10- Firewall Configuration and Testing Project

This repository documents a practical exercise in network security, focusing on firewall configuration, rule management, and testing using the Linux utility iptables. The project follows a structured mini-guide to demonstrate core firewall management skills.

Project Goal

The primary goal of this project was to gain hands-on experience with firewall management by:

1.
Learning fundamental firewall concepts.

2.
Configuring and managing network rules.

3.
Testing connectivity for allowed and denied ports.

4.
Demonstrating the blocking of a simulated malicious IP address.

5.
Documenting the entire process and its security impact.

 Tools Used

Tool
Purpose
Notes
iptables
Primary firewall management utility on Linux.
Used for all rule configuration and testing.
curl
Connectivity testing.
Used to test access to specific ports (80, 8080).
python3 -m http.server
Temporary web server.
Used to simulate services running on different ports for testing.




 Configuration Summary

The iptables configuration was designed to implement a secure, minimal-access policy, prioritizing essential services.

Key Rules Implemented:

Service
Port
Protocol
Action
Rationale
Established Connections
N/A
All
ACCEPT
Allows return traffic for active, legitimate connections (Stateful Inspection ).
SSH
22
TCP
ACCEPT
Essential for secure remote administration.
HTTP
80
TCP
ACCEPT
Allows the system to host a public web service.
Simulated Block
8080
TCP
DROP
Demonstrates blocking a specific, non-essential port.
Malicious IP Block
N/A
All
DROP
Demonstrates immediate blocking of a known threat source (192.168.1.100).




 Testing and Validation

Connectivity tests were performed to validate the effectiveness of the rules:

•
Allowed Port (e.g., 8000): Connection was successful, confirming the default policy allows outbound traffic and the system can receive return traffic.

•
Blocked Port (8080): Connection attempts resulted in a timeout/refusal, confirming the DROP rule was correctly enforced.
 Deliverables

The primary deliverable is a comprehensive document detailing the entire process:

•
Firewall_Rules_Documentation.md: The final report, including concepts, rule tables, impact analysis, and screenshots of the configuration and testing.

•
iptables_rules_screenshot.png: Visual proof of the configured iptables rule set.

•
connectivity_test_screenshot.png: Visual proof of the successful and failed connectivity tests.

This project successfully demonstrates the fundamental skills required for effective firewall management and network security.

