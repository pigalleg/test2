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
Libraries needed and blabla

## Preconfiguration
### ssh keys configuration and blabla
### Internet connectivity
### ZigBee configuration
### WiFi configuration


## Initiating connections
In order to iniate both aggregator and client you should connect via SSH protocol. You should install a UNIX console and run a SSH protocol. For OCM Server connection
```
$	ssh user@ocm-server.ing.puc.cl -p 5915
```
where "user" is your registered user and "ocm-server.ing.puc.cl" is the public address of the server (you must be connected to internet, of course). In order to connect to the client, you must connect connect it and your computer to the same LAN/WAN:
```
$	ssh ocm@xxx.xxx.xxx.xxx
```
where "xxx.xxx.xxx.xxx" is the local IP of the client running the client script. This procedure will open two SSH conections to every system and you will be able to controle them using the respective consoles.

### Aggregator and Client activation
In the respective consoles:
1. Download "library" to both aggregator and client systems.
2. Activate aggregator script "route-to-library/aggregator.py".
```
$ python route-to-library/aggregator.py
```
Aggregator script will start monitoring incoming connection from clients. If at least one connection is started, aggregator and client will start interchanging DR signals over TCP protocol. 

3. Activate client script "route-to-library/home.py". For reasons that will be clarified after, this script must be started using `sudo`privileges. 
```
$ sudo python route-to-library/homer.py
```
Client will connect to aggregator's public addres (ocm-server.ing.puc.cl). In paralel, it monitores incoming connections from locals actuators. If at least one connection with actuators is ed, client will start sending local control signals to the actuator.
