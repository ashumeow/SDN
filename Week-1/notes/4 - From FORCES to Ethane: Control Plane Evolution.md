```
From FORCES to Ethane: Control Plane Evolution

Synopsis:
-- Control of Packet Switched Networks
-- Why separate control?
-- How to control a packet-switched network?
(a) Separate control channel: FORCES (2003)
(b) In-band protocols: Routing Control Platform (2004)
(c) Open hardware: Ethane (2007), OpenFlow (2008).
```
```
Why separate control?
(i) More rapid innovation
-- Control logic is not tied to the hardware.
(ii) Network-wide view
-- Easier to infer (and reason about) network behavior
(iii) More flexibility
-- Easily introduce new services.
```
```
Custom control: IETF FORCES (2003)
-- First RFC in 2003 => three implementations.
-- Protocols for multiple Control Elements (CE) and Forwarding Elements (FE).
```
```
(contd...)
Problem:
-- Requires standardization, adoption, deployment of new hardware.
(same problem observed by previous work)
```
Sources: <br>
![](http://geekresearchlab.net/coursera/sdn/rfc.jpg)
```
Routing Control Platform (RCP) (2004)
(Source: Feamster,Nick,et al. "The case for separating routing from routers", Proceedings of the ACM SIGCOMM workshop on Future directions in network architecture, ACM, 2004.)
```
![](http://geekresearchlab.net/coursera/sdn/rcp.jpg)
```
(contd..)
-- RCP computes routes on behalf of routers.
-- Uses the exisiting routing protocol (BGP) for communicating routes to the routers.
```
```
Using In-Band Protocols for Control
```
![](http://geekresearchlab.net/coursera/sdn/inband.jpg)
```
(contd...)
Advantage:
-- Makes deployment easier without the use of any standarization protocols.
Problem:
-- Control is constrained by what existing protocols can support.
-- Limited when compared to general separated control plane.
Still used in Automated security traffic.
```
```
Customized Hardware: Ethane (2007)
(Source: Casado, Martin, et al. "Ethane: Taking control of the enterprise", ACM SIGCOMM Computer Communication Review, Vol.37, No.4, ACM, 2007.)
```
![](http://geekresearchlab.net/coursera/sdn/custom.jpg)
```
(contd..)

(i) Network architecture for the enterprise
-- Direct enforcement of a single, fine-grained network policy.

(ii) Domain controller
-- This computes flow table entries based on access control policies.

(iii) Custom Switches
-- OpenWrt, NetFGPA, Linux
-- Problem: Requires custom switches that support Ethane.
```
```
Open Hardware: OpenFlow (2008)
(Source: McKeown,N.,Anderson,.T,Balakrishnan,H.,Parulkar,G.,Peterson,L.,Rexford,J.,Shenker,S.,and Turner,J., "OpenFlow: Enabling innovation in campus networks",SIGCOMM Comput.Commun.Rev.38,2(Mar.2008))
```
![](http://geekresearchlab.net/coursera/sdn/openflow.jpg)
```
Summary...
What have we learned?
(a) Control and Data Plane should be decoupled
-- Vertically integrated switches make introducing new control planes difficult (FORCES).
(b) Using existing protocols
-- Makes deployment easier.
-- But, it constraints what it can be done. (RCP)
(c) Open Hardware
-- Allows decoupling of control.
-- Can spur adoption (OpenFlow).
```
