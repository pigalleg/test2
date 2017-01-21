# Jeisson OCM
Demande response implementation project developed by [OCM Lab] (http://http://ocm.ing.puc.cl/).

## Getting started
Jeisson is a python based code allowing local load control **demand response** (DR) signal transmission. Architecture is server-client based, allowing coordinated control of several **houses** (clients) connected to an **aggregator** (server). Server sends and receives DR signals in a real-time negotiation process.

The following instructions will guide you about how to copy and run the project in a remote server and several (if any) local clients. 

## Prerequisites
For basic aggregator and clients interaction:
* Debian based platform
* Internet connectivity

For local load control, connectivity between client and load must be assured by 
* WiFi (802.11) and/or
* ZigBee

This means that WiFi and/or ZigBee connection must be pre-configured after local load controlling. This projects assumes (but will guide you also) in how to set ZigBee connectivity. WiFi connectivity will not be explained extensively.

### Hardware requiriments
The Aggregator code must run in any normal pc while client was testes in a BeagleBone Black computer. 



