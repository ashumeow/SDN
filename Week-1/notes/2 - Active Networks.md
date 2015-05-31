```
Programmability in networks: Active networks (1990s)
```
```
Active Networks - Introduction
-- Networks where the switches perform custom computation on packets.
-- Examples:
(a) Trace program running at each router
(b) Middleboxes: Firewalls, proxies, application services
```
```
Origins of Active Networks:
-- DARPA research community (1994-1995)
-- Idetified problems with today's networks
(a) Difficulty of integrating new technology
(b) Poor performance due to redundant operations at several protocol layers
(c) Difficulty accomodating new services
```
```
Motivation for Active Networks:
(a) Accelerating innovation
-- Internet innovation relies on consensus
-- Takes 10 years from prototype to deployment
(standardization, procurement, deployment)
(b) Active nodes => User-driven innovation
-- This allows routers to download new services into the infrastructure
```
```
Idea: Messages carry Procedures & Data
(Source: Tennenhouse,David.L.,et al. "A Survey of Active Network Research", Communications magazine, IEEE 35.1)
```
![](http://geekresearchlab.net/coursera/sdn/active.jpg)
```
Idea: Messages carry Procedures & Data (contd...)

-- Active routers co-exist with legacy routers
-- Each programmable switch can perform additional processing
```
```
User "Pulls" and Technology "Push"

(i) User Pull (demand)
-- Proliferation of firewalls, proxies, transcoders, etc.
-- Goal: Replace Ad-Hoc approaches
(ii) Technology Push (enablers)
-- Safe execution of mobile code, Java applets
-- OS support
(a) Scout: real-time communications
(b) ExoKernel: safe access to low-level resources
(c) SPIN: trustworthy code generation
```
```
Two different approaches

(1) Capsules ("integrated")
-- Every message is a program.
-- Active nodes evaluate content carried in packets.
-- Code dispatched to execution environment.

(2) Programmable switches ("discrete")
-- Custom processing functions that run on the routers
-- Packets are routed through programmable nodes
-- Program depends on the packet header
```
```
Capsules (example)
```
![](http://geekresearchlab.net/coursera/sdn/capsule.jpg)
```
ANTS header => Active NeTwork Services header
```
```
Capsules (contd..)

Type:
-- Forwarding routine to be executed (carries code by reference)

Previous address:
-- where to get the forwarding routine from if it's unavailable in the present node.

Dependent Fields:
-- Parameters for the forwarding code

Payload:
-- Header + data of higher layers
```
```
Some previous notable projects:

(1) ANTS (MIT): Packet capsules (Java programs)
-- Some limitations for the QoS guarantees.
-- Arizona implemented Joust JVM to provide better real-time performance.

(2) SwitchWare (Penn Univ.): Programmable switch scripting language
-- To support invocation of switchlets.

(3) Smart Packets (BBN):
-- Network Management

(4) Open Signaling (Columbia): NetScript, a language
-- To provide programmable processing of packet streams

(5) Tempest (Cambridge):
-- Switchlets => Programmable virtualization switch.
```
```
So, what happened?
Why don't we see?

(a) Timing was off
-- No clear application (pre datacenter/cloud)
-- Hardware support wan't cheap 
-- Everyone was using ASICs.
-- At present => TCAMs, FGPAs, NPUs

(b) Some mis-steps
-- Security, Special Languages for safe code, packets carrying code.
-- End user as programmer (versus network operator)
-- Interoperability

(c) In-contrast: OpenFlow did a good job in grappling with backwards compatible towards switch hardware
-- Simple firmware upgrade
-- Switch hardware already supported the basics
```
```
Legacy of Active Netowrks for SDN

(i) Programmable functions in network to enable innovation.

(ii) Demultiplexing programs on packet headers
-- Eg: Planetlab, Flowvisor, GENI, etc

(iii) Paying attention to middleboxes and how these functions are composed.
```
```
The network virtualization will be discussed in next chapter...
```
