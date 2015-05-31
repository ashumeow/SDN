```
Network Virtualization
```
```
Network Virtualization - Introduction

(i) Representation of one or more logical network topologies on the same infrastructure.
as well as...
Separate logical network from the infrastructure

(ii) Many different instantiations
-- Virtual LANs (VLANs)
-- Various technologies and network testbeds
-- Today: VMWare, Nicira, etc
```
```
Benefits of Network Virtualization

(i) Sharing
-- Multiple logical routers on a single platform.
-- Resource isolation in CPU, memory, bandwidth, forwarding tables.

(ii) Customizability
-- Customizable routing and forwarding software.
-- General purpose CPUs for the control plane.
-- Network processors and FGPAs for data plane.
```
```
Fixed Physical Infrastructure
```
![](http://geekresearchlab.net/coursera/sdn/a.jpg)
```
(contd...)
-- Shared by many parties
-- Arbitrary Virtual Topologies
```
```
Virtual Networks == Examples

(1) Tempest: Switchlets (1998)
-- Separation of control framework from switches.
-- Virtualization of the switch.

(2) VINI - VIrtual Network Infrastructure (2006)
-- Virtualization of the network infrastructure.

(3) Cabo (2007)
-- Separates infrastructure and services.
```
```
The Tempest architecture : Switchlets
```
![](http://geekresearchlab.net/coursera/sdn/tempest.jpg)
```
(Source: van der Merwe, Jacobus E.,et al. "The tempest - a practical framework for network programmability", Network IEEE 12.3 (1998): 20-28.)

--- Multiple control architectures over ATM.
--- Separation of switch controller and fabric via open signalling.
--- Partitioning of switch resources across controllers.
```
```
Switch Divider
(Source: van der Merwe, Jacobus E.,et al. "The tempest - a practical framework for network programmability", Network IEEE 12.3 (1998): 20-28.)
```
![](http://geekresearchlab.net/coursera/sdn/switch.jpg)
```
VINI - VIrtual Network Infrastructure 
(Source: Bavier,Andy,et al."In VINI veritas: realistic and controlled network experimentation", ACM SIGCOMM Computer Communication Review, Vol.36, No.4, ACM, 2006.
```
![](http://geekresearchlab.net/coursera/sdn/vini.jpg)
```
(contd...)
-- Runs real routing software.
-- Exposes realistic network conditions.
-- Gives control over network events.
-- Carries traffic on behalf of real users.
-- Shared among many experiments.

VINI also uses control plane known as XORP, which runs a variety of routing protocols.

XORP
-- BGP, OSPF, RIP, PIM-SM, IGMP/MLD.
-- Goal: To run real routing protocols on virtual network topologies.

VINI uses a data plane known as CLICK.
```
![](http://geekresearchlab.net/coursera/sdn/click.jpg)
```
CLICK (contd..)
Performance:
-- Avoid UML overhead
-- Move to kernel, FGPA

Interfaces => Tunnels
-- Click UDP tunnels correspond to UML network interfaces.

Filters
-- "Fail a link" by blocking packets at tunnel.
```
```
Concurrent Architectures are better than One

(Source: Feamster,Nick,Lixin Gao,and Jennifer Rexford, "How to lease the internet in your spare time", ACM SIGCOMM Computer Communication Review 37.1 (2007): 61-64.)

Roles

(a) Infrastructure Providers:
-- Maintains routers, links, data centers and other physical infrastructure.

(b) Service Providers:
-- Offer end-to-end services to users.
-- E.g.: Layer 3 VPNs, SLAs.

At present,
ISP play both roles and cannot offer end-to-end services.
```
```
Communication Networks : Examples

(i) Two commercial examples in IP networks
-- Packet Fabric:- Share routers at exchange points.
-- FON:- Resells the users wireless internet connectivity.

(ii) FON economic refactoring
-- Infrastructure providers:- Buy upstream connectivity.
-- Service Provider:- FON as the broker.
```
```
Summary: What we learned?
1. Network virtualization introduction
2. It's history
3. Legacy for SDN?
-- Separate service from the infrastructure.
-- Multiple controllers of a single switch.
-- Logical network toplogies
```
