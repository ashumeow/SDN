```
Testing a Simple Mininet setup:

(i) Setting up a simple topology with 3 hosts connected to a single switch
$sudo mn --test pingall --topo single,3

(ii) This setup uses a default switch controller and switch.
Custom modes are also allowed to use.
```
```
Basic Mininet command line:

--topo => defines the topology

-- switch => defines the switch

--controller => defines the contoller.
```
```
Trying out different mininet topologies

Minimal network with 2 hosts, 1 switch

$sudo mn --topo minimal

Example: 4 hosts, 4 switches

$sudo mn --topo linear,4

Example: 3 hosts, 3 switches

$sudo mn --topo single,3

Example: Tree topology with depth and fanout

$sudo mn --topo tree,depth=2,fanout=2
```
```
How mn works? => mn executes python
=> mn is a launch script that executes python
=> --topo linear 4
s1 -> h5
s2 -> h6
s3 -> h7
s4 -> h8
```
```py
## mn in python
from mininet.net import Mininet
from mininet.topo import LinearTopo
Linear=LinearTopo(k=4)
net=Mininet(topo=Linear)
net.start()
net.pingAll()
net.stop()
```
```
Writing your own mininet topologies

Refer:
https://github.com/mininet/mininet/wiki/Introduction-to-Mininet
```
