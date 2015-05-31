```
History of SDN

Synopsis:
-- Discuss the timeline of SDN from 1980s to present.
-- Gain awareness about the ideas and principles behind SDN.
-- Recognize architectural themes in computer networking where SDN originated.
```
```
Four chapters of SDN history
1. Evolution of supporting technologies
2. Control-Data plane separation
3. Developing control channels for specific data planes
4. Convergence of control channels and data planes
```
```
Discussions -- (3 lessons)
(I) Central network control:
=> Dates back to AT&T's network control point (1980s)
(II) Programmability in networks: 
=> Active networks (1990s)
(III) Network Virtualization:
=> Switchlets, XEN, VINI (1990s)
```
```
(I) Central network control:
```
```
Early days: Control and Data plane
(added ref:- http://en.wikipedia.org/wiki/Blue_box)
(i) In-band signaling
-- Data and control sent over same channel.
-- Certain frequencies (e.g.2600 Hz) could reset phone trunk lines and route calls.
-- Resulting network was brittle and insecure, etc.

Network Control Point (NCP)
(Source: Bell System Technical Journal, Vol.61, No.7, 1982)
```
![](http://geekresearchlab.net/coursera/sdn/ncp.jpg)
```
Network Control Point (continued...)
(a) Telephone network
(b) Signalling at NCP
(c) Benefits
-- Services on-demand
-- Rapid introduction of new services

Benefits of NCP in the AT&T network:
(a) Elimination of in-band signaling reduces expenditures
-- Shorter circuit holding time
-- Ability to determine busy/idle status before requesting a circuit
(b) Rapid introduction of new services
-- In the area of new services that can be supported,
The possibilities are limited only by imagination.

Apps from composing basic primitives
-- Collect N digits
-- Send a message to the NCP
-- Make a billing record

Envisioned Service: Person Locator
(Additional source: http://www.corp.att.com/cpetesting/ss7.html)
```
![](http://geekresearchlab.net/coursera/sdn/ncpLocate.jpg)
```
Envisioned Service: Person Locator (continued...)
-- User registers location with the NCP database.
-- NCP routes call to the current location/number.
-- NCPs currently used to route 800 calls.
```
```
Benefits of Central Control:
(i) Network-wide vantage point
-- Directly observes (rather than infer) network behavior.
(ii) Independent evolution of infrastructure, data and services
-- Services and resources allocations decisions can be made based on customer data, network load, etc.
```
```
The discussion on,
Programmability in networks and Network Virtualization will be discussed in next chapter.
```
