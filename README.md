genieacs-gui
============

A fork of the GUI front end for GenieACS built with Ruby on Rails.

Customized changes:

-> the MAC address in the Devices tab is coming from a virtual parameter that should be called "VirtualParameters.MACAddress"


Virtual parameter
=================

MACAddress

let m = declare(
  "InternetGatewayDevice.DeviceInfo.X_MACAddress",
  {value: Date.now()});

if (m.size) {
  return {writable: false, value: [m.value[0], "xsd:string"]};
};
