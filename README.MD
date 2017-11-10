# November 10, 2017 Release Notes

## New Features 

### Apps sync to all nodes on network

Apps can be launched from _any node_ on the network. 

_video demo of this feature is coming soon_

* As a `developer user` I want to register an application on the testnet

* As a user I want to discover existing apps on the testnet

* As a user I would like to see all the dApps in the network in SMD when I got my node synced

* Prevent users from deploying dApps with localhost in the URL

* Update Azure offers to latest images

* Update dapp-guide (documentation)

* Update lottery-app packaging

* SMD should construct the dApp url using hash

* add error handling to lottery app

## Bug Fixes

* Initial value for "value" in bloc swagger docs is too high, making contract upload fail

* Error while syncing with Testnet - stuck at Block 3966

* Cannot Create users In Developer Demo SMD linked to Site (Create new account)

* Getting-started fails to init on CentOS - blockapps-bloc: libpq: failed (could not translate host name "postgres" to address

* Timestamp: Invalid Date

* Stuck on Block 191 on Local -> Stratodev connection

* Execute fails Bloc API in Swagger docs - Post - /users/{user}/{address}/send

* incorrect password on contract creation in SMD shows no error

# BlockApps STRATO Release Notes: 10/27/17

## New Features
 - Apps Tab with a demo lottery app
 - Basic Code Editor
 - Cirrus now supports updating contract definitions

## Enhancements
 - Network request progress indicator on SMD
 - SMD no longer tries to get all accounts every 5 seconds
 - Misc performance and usability changes 

## Bug Fixes
 - Bloc gives compiler errors instead of generic 500 on compile issues
 - Pragma statement no longer causes contract compilation to fail