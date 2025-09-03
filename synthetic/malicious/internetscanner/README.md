# Internetscanner Scenario (Malware)

Traffic was generated on the topology shown below.

<img src="../byob-world.jpg" alt="Experiment topology" width="50%"/>

Green circles denote nodes. All nodes except **compromised** and **attacker** are on the same LAN.
In the scenario (Spencer fill here following the model below):
- We run byob on the **attacker** node to act as botnet master
- The master starts the byob client on the **compromised** node
- The master runs the port scanner malware on **compromised** node and scans 107.125.{128..254}.{1..254} subnets
- The master kills byob software on **compromised** node
- We stop byob server on **attacker** node

Each IP address in the subnet above has a 10% chance of appearing in the experiment. IPs are randomly assigned to a service, but remain constant throughout all the trials. 
