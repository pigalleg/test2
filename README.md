# Jeisson OCM
Demande response implementation project developed by [OCM Lab](http://ocm.ing.puc.cl/).
dfdfdf
## Getting started
Jeisson is a python based code allowing local load control **demand response** (DR) signal transmission. Architecture is server-client based, allowing coordinated control of several **houses** (clients) connected to an **aggregator** (server). Server sends and receives DR signals in a real-time negotiation process. Houses send and receive control signals to local **actuators** in order to effectively control their connected appliances in a similar local server-client architecture. It's impotant to notice that load control is performed by actuators allowing the real turning on/off of the connected loads.

The following instructions will guide you about how to copy and run the project in a remote server and several (if any) local clients.

## Prerequisitescx
For basic aggregator and houses interaction:
* Debian based platformcx
* Internet connectivity

For local load control, connectivity between client and load must be assured by 
* WiFi (802.11) and/or
* ZigBee

This means that WiFi and/or ZigBee connection must be pre-configured after local load controlling. This projects assumes (but will guide you also) in how to set ZigBee connectivity. WiFi connectivity will not be explained extensively.

### Hardware requiriments
The Aggregator code must run in any debian based platform while client was tested in a BeagleBone Black minicomputer. Actuators were running in a Arduino One and in a Photon device. Here's a little resume  showing the used hardware:
:)
### Software requirements


## Initiating connections
In order to iniate both aggregator and client you should connect via SSH protocol. In a UNIX console:
```
$	ssh user@ocm-server.ing.puc.cl -p 5915
```
in order to connect to OCM Server and
```
$	ssh user@xxx.xxx.xxx.xxx
```
where "xxx.xxx.xxx.xxx" is the local IP of the server running the clinet script.

### Aggregator and Client activation
1. Download "library" to both aggregator and client systems.
2. Activate aggregator script "route-to-library/aggregator.py".
3. Activate client script "route-to-library/home.py"


