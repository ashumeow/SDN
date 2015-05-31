```
Road to SDN

(Source: http://queue.acm.org/detail.cfm?id=2560327)
```
```
Three stages:

(1) Active Networking
-- Programmable networks

(2) Control and Data Plane separation
-- Open interfaces between control and data plane

(3) OpenFlow API and Network OSes
-- First instance of widespread adoption of an open interface
```
```
Active Networking

(i) More diverse applications and greater use
-- Researchers wanted to deploy new ideas.
-- First attempt to make networks programmable.

(ii) Technology Push:
-- Reduction in computing costs, Funding agency interest

(iii) Use Pulls:
-- Operator frustration with deployment challenges.

Active Networking: Contributions
(i) Programmable functions
(ii) Network Virtualization
(iii) Demultiplexing to software programs
(iv) Vision of an unified architecture for middlebox orchestration

Active Networking: Myths
(i) Myth #1: End-user would program packets.
Reality: This programming model would be rare.
(ii) Myth #2: Packets must carry Java code.
Reality: Active networking had a programmable router/switch model.
```
```
Control and Data Plane separation

(i) Pragmatism (narrower scope):
-- Attempt to solve traffic engineering problems.

(ii) Technology Push:
-- Open interfaces between control and data planes (E.g. FORCES)
-- Logically centralized control (E.g. RCP)

(iii) Use Pull:
-- Pressing network management problems.

Contributions
(a) Logically centralized control using an open interface to routers and switches.
(b) Distributed state management (of controllers).

Myths
-- Logically centralized route control violates fake sharing.
Reality
-- Conventional distributed routing solutions already violated these principles.
(E.g. OSPF areas, BGP route reflectors)
Separation allowed researchers to think about cleaner ways to do distributed state management.
```
```
OpenFlow

(i) Generality:
-- More functions than the earlier route controllers.
-- Building on switch hardware.
-- More limited flexibility.
-- Immediate deployment.
(ii) Technology Push
-- Perfect storm between operators, vendors, chipset designers and researchers.
(iii) Use Pull
-- Initially campuses, then data centers.

Contributions:

(i) Generalizing network devices and functions.

(ii) The vision of a network operating system
-- Data plane with open API
-- State management layer
-- Control logic

(iii) Distributed State Management techniques.

Myths:

Myth #1: First packet must goto the controller.
Reality: No assumptions about granularity of rules or whether the controller handles traffic.

Myth #2: Controller must be physically centralized.
Reality: Deployments have distributed controllers.

Myth #3: SDN is OpenFlow.
Reality: OpenFlow is an instantiation of SDN.
```
```
Summary...Lessons..

(a) Balance between vision and pragmatism.
(b) OpenFlow took off in part because of a balance between vision and support from existing hardware.
(c) The balance remains tenuous
-- Commodity servers
-- Programmable hardware
```
