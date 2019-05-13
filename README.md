# multiserver-bluetooth

A [multiserver](https://github.com/ssbc/multiserver) plugin that facilitates communication across bluetooth serial.

This module requires a bluetooth-manager as a parameter for taking care of connections, disconnections and opening connection streams. This is to allow this plugin to be used on different platforms (e.g. mobile, linux, windows) with the same interface.

## example

This must be used with an implementation of the bluetooth-manager, see [ssb-bluetooth-manager](https://github.com/Happy0/ssb-bluetooth-manager)


``` js
var Bluetooth = require('multiserver-bluetooth')
var BluetoothManager = require('ssb-bluetooth-manager')

var bt = Bluetooth({
  bluetoothManager: BluetoothManager(),
  scope: ... //your scope, default is public
})

bt.stringify(scope) => "bt:<your_bt_mac_address>"
```
