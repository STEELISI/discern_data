# DISCERN Synthetic Datasets

This repository contains synthetic datasets capturing
memory, CPU, process, network, and file activity on SPHERE
research infrastructure during malicious and legitimate use patterns.

- *legitimate* folder contains several legitimate use cases:
  - *dnsmitm* - DNS MITM attack reproduction in an experiment - allowed use case for a security testbed
  - *synflood* - TCP SYN flood attack reproduction in an experiment - allowed use case for a security testbed
  - *llm* - Running an LLM in generative mode, e.g., as a security-focused chatbot
  - *svm* Running an ML model (SVM) on a classification task, e.g., to classify legitimate from attack traffic
- *malicious* folder contains several malicious use cases:
  - 
- *merged* folder contains interleaved/merged data from legitimate and
malicious use cases