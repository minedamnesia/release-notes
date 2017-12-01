# December 1, 2017 Release Notes

## New Features

* Ensure Data persistence in the Testnet nodes for restarts, fixes and enhancements (upgrades)
* Perform network upgrade by adding new substitute nodes (code upgrade) - could be laptop or VM's outside the network

## Bug Fixes

* Errors displayed if contract upload fails
* Discovery fixed to improve node syncing
* AppMetadata is registered before STRATO start syncing


# November 10, 2017 Release Notes

## New Features 

### Apps sync to all nodes on network

Apps can be launched from _any node_ on the network. 

_video demo of this feature is coming soon_

* Ability to register an application on the testnet

* Ability to discover existing apps on the testnet

* Microsoft Azure updated with latest images

* Ability to see all dApps on the network when nodes are synced

* Updated documentation for dApp guide 

* Updated packaging for lottery-app 

* Error handling added to lottery app

## Bug Fixes

* Initial value for "value" in bloc swagger docs is too high, making contract upload fail

* Resolved error while syncing with Testnet - stuck at Block 3966

* Resolved inability to create users In Developer Demo SMD linked to Site 

* Getting-started fails to init on CentOS - blockapps-bloc: libpq: failed (could not translate host name "postgres" to address

* Fixed timestamp: Invalid Date

* Execute fails Bloc API in Swagger docs - Post - /users/{user}/{address}/send

* Added error handling to incorrect password on contract creation in SMD

* Fixed issue code editor contracts not being indexed by cirrus

# BlockApps STRATO Release Notes: 10/27/17

## New Features
 - Apps Tab with a demo lottery app
 - Basic Code Editor with file management
 - Cirrus now supports updating contract definitions

## Enhancements
 - Network request progress indicator on SMD
 - SMD no longer tries to get all accounts every 5 seconds
 - Misc performance and usability changes 
 - Env variable checks for SMD for tracking and app deployment

## Bug Fixes
 - Bloc gives compiler errors instead of generic 500 on compile issues
 - Pragma statement no longer causes contract compilation to fail
