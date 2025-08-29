# DISCERN Synthetic Datasets

This repository contains synthetic datasets capturing
memory, CPU, process, network, and file activity on SPHERE
research infrastructure during malicious and legitimate use patterns.

- *legitimate* folder contains several legitimate use cases:
  - *dnsmitm* - DNS MITM attack reproduction in an experiment - allowed use case for a security testbed
  - *synflood* - TCP SYN flood attack reproduction in an experiment - allowed use case for a security testbed
  - *llm* - Running an LLM in generative mode, e.g., as a security-focused chatbot
  - *svm* - Running an ML model (SVM) on a classification task, e.g., to classify legitimate from attack traffic
- *malicious* folder contains several malicious use cases:
  - *cryptominer* - a user is using cryptomining software on an experimental node
  - *internetscanner* - an experimental node starts scanning many Internet hosts
  - *portscanner* - an experimental node stats scanning the testbed on a specific port
  - *ransomware* - an experimental node is encrypted by ransomware
  - *spread* - an experimental node starts sends email to the outside (e.g., for purposes of spam, phishing or malware spread)
  - *exfiltrate* - attacker exfiltrates a file from an experimental node 	       
- *merged* folder contains interleaved/merged data from legitimate and
malicious use cases

All malicious use cases were created in a safe manner. The experiments were fully
contained on the testbed. We used BYOB software to replicate a scenario where there
is a botmaster outside the testbed controlling one or more experimental nodes within
the testbed. In cases where an experimental node should try to exfiltrate the data
or scan the Internet, the traffic was re-directed to a node within the testbed. In
the case of email spread, the traffic contained a single email sent to an account we
own on GMail. 