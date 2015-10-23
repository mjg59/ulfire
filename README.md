Ulfire
======

Ulfire is a simple Python application that detects and controls LIFX and
Belkin WeMo Link LED bulbs by exporting a sufficient subset of the Philips
Hue API to convince the Amazon Echo that it's speaking to a real Hue.

In other words, it lets you use an Amazon Echo to voice control your LIFX or
WeMo Link lights.

Requirements
------------

You'll need a machine on your local network to run this on. It needs to be
on the same network as the Echo and your lights. It probably needs to be
vaguely Unixish - I've only tested this on Linux, but it almost certainly
runs fine on BSDs and it's probably fine on MacOS X. I have no idea about
Windows, but I wouldn't be optimistic. You'll also need to install the
LazyLights and Ouimeaux Python modules:

pip install git+https://github.com/mpapi/lazylights@2.0  
pip install git+https://github.com/iancmcc/ouimeaux

and then just run ulfire.py. It'll automatically detect your lights (note
that the lights must already be configured and named with the vendor
apps). Once that's done, just ask your Echo to detect connected devices. It
should find all your bulbs. Create any groups you want to via the Echo
settings UI, and then you should be able to turn your lights on and off and
dim them.

Thanks
------

This code is derived from Fauxmo (https://github.com/makermusings/fauxmo)