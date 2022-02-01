---
id: ycvnlkLQLPjRm4ycfwyXN
title: Reliability
desc: ''
updated: 1643534210930
created: 1643531981288
---

- A system is considered _reliable_ when it performs to specifications with acceptable performance. It continues to function correctly in face of different types of errors that could occur (e.g. human, software, hardware)
- We differentiate between _faults_ and _failures_. Faults are when the system stops performing to specifications. Failures occur when system stops providing a service to its users.
- It's impossible to design a system that's 100% fault-tolerant or resilient (e.g. can't protect system against natural disasters)

## Hardware Errors

- Redundancy of a single machine's components used to be enough to gaurantee high availability (disks, batteries, etc.)
- Nowadays we move towards redundancy in number of machines as well (e.g. AWS prioritizes elasticity and flexibility over hardware reliability of a single machine)
- Advantages of machine redundancy: deploy/update without taking down whole system

## Software Errors

- Usually related bugs where an assumption is made about the system's environment which was usually true until it wasn't
- Can do little to prevent other than monitoring, thinking through assumptions and testing (e.g. chaos monkey)

## Human Errors

- Humans unreliable, most outages are caused by operator error
- Ways to prevent:
  - Introduce processes to make it difficult to make mistakes
  - Sandbox environments for devs to test with real data
  - Testing: Manual, unit, integration
  - Monitoring/telemetry allow us to see how a system is functioning and detect errors before they get out of hand