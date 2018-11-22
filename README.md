
Android BluetoothLeGatt Sample
===================================

This sample demonstrates how to use the Bluetooth LE Generic Attribute Profile (GATT)
to transmit arbitrary data between devices.

Introduction
------------

This sample shows a list of available Bluetooth LE devices and provides
an interface to connect, display data and display GATT services and
characteristics supported by the devices.

It creates a [Service][1] for managing connection and data communication with a GATT server
hosted on a given Bluetooth LE device.

The Activities communicate with the Service, which in turn interacts with the [Bluetooth LE API][2].

[1]:http://developer.android.com/reference/android/app/Service.html
[2]:https://developer.android.com/reference/android/bluetooth/BluetoothGatt.html

Pre-requisites
--------------

- Android SDK 28
- Android Build Tools v28.0.0
- Android Support Repository

Getting Started
---------------

This sample uses the Gradle build system. To build this project, use the
"gradlew build" command or use "Import Project" in Android Studio.

CardioCheck notes
-----------------

This is a step by step guide to follow in order to connect to Bluetooth devices :

* Create a class which handle BT search
* In case BL is not enabled, ask user to enable it
* In case we are looking for a BLE device, ask user to enable GPS (see EXTRA app implementation)
* Launch search (or launch search at app launch)
* Show found devices on list
* Click on device to connect and bind it with six-digit passkey (given by manufacturer); **ATTENTION**: in Android code, while connecting to device there is a flag which enable automatic re-connection to device when found!
* Collect raw info from device

Questions / possible issues :
- is there any configuration to do before collecting data ? (AKA write / send info to medical device) ?
- does data is deleted after collection on mobile device ?
- data is encrypted and block chained: yay ?
