![Node-RED Modbus](http://b.repl.ca/v1/Node--RED-Modbus-green.png)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Standard - JavaScript Style Guide](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)
[![NPM version](https://badge.fury.io/js/node-red-contrib-envisalink.png)](https://www.npmjs.com/package/node-red-contrib-envisalink-ademco)
# node-red-contrib-envisalink-ademco
[Ademco alarm systems] integration with [Node-RED] using the [EnvisaLink] hardware.

This node allows you to listen to state changes in your Honeywell Ademco alarm as well as sending
commands such as arming and disarming of your alarm.

# Install


At this time I don't understand npm and node-red packages well enough to know how to make
npm become aware of my github package... so I doubt this will work

Run the following command in the root directory of your Node-RED install

    npm install node-red-contrib-envisalink-ademco

Run the following command for global install

    npm install -g node-red-contrib-envisalink-ademco

# How to use

The output node, with which you send commands, takes a raw TPI command as a string.
Please refer to the [TPI documentation] for a full list of commands.
For example, to arm partition `1` using the code `9999` you would use the command '99992' to arm. And '99991' to disarm.
All commands sent to the Ademco are as if you were typing directly on the remove alarm keypad.

![Flow Example](https://github.com/pakerfeldt/node-red-contrib-envisalink/raw/master/images/example-flows.png)

# Authors

[Chris Thierman] 

[Patrik Åkerfeldt]

### History

* based on work by [Patrik Akerfeldt]
* based on work from [NodeAlarmProxy].

[Node-RED]:           http://nodered.org/
[Ademco alarm systems]: https://www.security.honeywellhome.com/all-categories/intruder-detection-systems/control-panels/burglary/ademco-vista#sort=%40appearancesortorderinteger%20ascending
[DSC alarm systems]:  http://www.dsc.com/
[EnvisaLink]:         http://www.eyezon.com/
[TPI documentation]:  https://github.com/pakerfeldt/node-red-contrib-envisalink/raw/master/docs/EnvisaLinkTPI-1-08.pdf
[Patrik Åkerfeldt]:   https://github.com/pakerfeldt
[Chris Thierman]:     https://github.com/cthierman
[NodeAlarmProxy]:     https://github.com/entrocode/NodeAlarmProxy
