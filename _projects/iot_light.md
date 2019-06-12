---
layout: page
title: IoT Light Switch
description: Using a standard two-way light switch with an ESP8266 combined with a relay to create an IoT light switch that also maintained the switches standard operation
---
The explosion in the number of Internet-of-Things devices on the market over the past few years has meant that practically any household appliance from your light switch to your toaster can now be controlled remotely. Personally, I have no desire to receieve a notification when my bread has finished toasting. The light switch on the other hand does pique my interest. The problem is I'm a fan of the plain, standard, 'vanilla' light switches. I also don't like the thought of purchasing expensive bulbs which will blow eventually, that I need to use custom software with.

I thought this would be a good opportunity to further my hobby in electronics so I set up a test bench to work (somewhat) safely with AC power, installed a fuse to limit the potential shock in the case of an accident, and setup a small circuit with an ESP8266 and an electromagnetic relay on a breadboard. I wrote the software in Lua script (at the time the easiest way to write code for the ESP8266).

The software setup a small web server which you could then access via any internet connected device with access to a web browser, it would display a simple web page which would allow you to toggle the light on and off. 

The problem was that turning the light off via the web server would then mean that the light could not be turned on at the switch, and simiarly, when the light was turned off at the switch, it could not be turned on via the internet. 

After some thinking I recalled the two-way light switches, where you can turn on or off the light by your door and also by pulling a cord by your bed. After some research I purchased a two-way light switch on the internet and did some reading on how it operates. When I was comfortable with the functionality of the switch I wired it up appropriately and the switch then worked either via the internet or manually flipping the switch. 

If I were to do the project again I would consider a more decentralised approach, where the microcontroller communicates with a central IoT server via message passing such as MQTT or similar. This would enable easier use of the device, whilst also allowing other devices to be connected to the same server and custom rues or triggers to also be set up. 

Since I am not a qualified electrician this was not installed for real-world use and was only tested on a bench and as much care was taken whilst working with mains power. Please don't attempt to recreate this project without professoional supervision.
