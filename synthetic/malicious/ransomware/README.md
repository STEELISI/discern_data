# Ransomware Scenario (Malware)

Traffic was generated on the topology shown below.

<img src="../byob.jpg" alt="Experiment topology" width="50%"/>

Green circles denote nodes and red triangles denote interfaces on a node.
In the scenario:
- We run byob on the **attacker** node to act as botnet master
- The master starts the byob client on the **compromised** node
- The master runs encryption on the **compromised** node and encrypts files in this order:
    - encrypt_file "$HOME/testing.txt"
    - encrypt_file "/boot"
    - encrypt_file "/root"
    - encrypt_file "/home"
    - decrypt_file "/home/blankcanvas/.ssh"
    - decrypt_file "/home/blankcanvas/.bashrc"
    - decrypt_file "/home/blankcanvas/.profile"
- The master kills byob software on **compromised** node
- We stop byob server on **attacker** node
