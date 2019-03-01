==================
Connecting to WiFi
==================

Purpose
-------

When IoTaWatt powers up, it attempts to connect to the 
last WiFi network used.
A connection must be established to an internet connected network if the real
time clock is not set, or to run the configuration utility,
or if logging to an external server like Emoncms is desired.
*It is strongly recommended to connect the IoTaWatt to a WiFi network
with a reliable internet connection*.

If the power-up connection is successful, 
the LED will begin to glow dull green.
This indicates that the IoTaWatt has connected 
and is in normal operating mode.
At this point you can skip ahead to the next 
section `Device Configuration <devConfig.html>`__

New connection
--------------

If the IoTaWatt has never been connected to a WiFi network (new),
or the last used network is not available, the ESP8266 will enter
AP (Access Point) mode when powered-up (not on a software restart).
This state is indicated when the LED flashes the 
three color sequence RED-GREEN-GREEN.
It will broadcast an SSID recognizable by the 
prefix ``iota`` followed by a unique number.
Connect to it using a smartphone or tablet.  
Use the password ``IotaWatt`` (case sensitive).
If the device was previously configured and the 
device name was changed,
that new name will be the password required in this step.

After connecting, a page will be rendered with several choices.  Select ``Configure WiFi``.

.. image:: pics/CaptivePortal.jpg
    :scale: 50 %
    :align: center
    :alt: captive portal image

A few seconds may elapse while the IoTaWatt scans for the local networks,
then another page will be rendered allowing you to select one of the listed
networks, or specify another network not listed.

.. image:: pics/SSIDpwd.jpg
    :scale: 50 %
    :align: center
    :alt: Specify Network image

Select your network and enter the password, then save. Once connected,
the new WiFi network credentials will be saved and the device 
will continue it's
startup procedure.  If you see another LED sequence, refer to 
the `troubleshooting <troubleshooting.html>`__ section.

When the LED glows dull green, proceed to the next step
`Device Configuration  <devConfig.html>`__
