# STRATO 3.1 Release Notes
## May 23, 2018

## New Features

* **Genesis Ingestion Tool** - for Large Record Contract Creation
Constant memory usage for file creation and storage initalization of ingestion. Added support for hash maps.
* **Solidity Improvements** - supports constant keyword and variable initalization.
* **Query Pagination** -
support for offset and limit when querying Cirrus in order to control response size over large datasets.
* **Node Performance Improvements** - increased contract creation transactions per second.
* **Updates to Kafka Library** - Kafka has been upgraded to 1.1.0.

## Updates

* Solidity now enforces the “constant” modifier on variables.  This means that the previous workaround to initialization of constants in the constructor function may not longer work.

## Hotfixes
* **3.1.1** - includes: minor UI corrections and multinode networking bug fixes
* **3.1.2** - includes: storage offset bug fix, parsing fixes for contacts, fix to multinode syncing issues, and other small fixes

# STRATO 3.0 Release Notes
## April 6, 2018

## New Features

* **Batch Contract Uploader** - In an effort to make our blockchain even faster, we devised a method to upload empty contracts to the [genesis block](https://arvanaghi.com/blog/explaining-the-genesis-block-in-ethereum/). This eliminates bottlenecks when uploading hundreds (or thousands) of contracts, such as the case of our [enterprise users](https://blockapps.net/enterprise/). The result? 4,000 contracts uploaded to STRATO in 144 seconds, which translates to 27.7 contracts per minute. Not bad!
* **Improved Signup Flow** - We updated our signup flow to make it easier to request tokens and launch apps. [Try it out now.](https://stratodev.blockapps.net/dashboard/#/apps?developer)

## Bug Fixes

* **[BlockApps BA is Fixed](https://github.com/blockapps/blockapps-ba)** - Some users were unable to deploy our supply chain demo app. Upon investigation, we discovered a circular dependency between Bloc, our state route API, and Cirrus, our contract indexer. This was fixed by letting Cirrus discover and index contracts on its own, which eliminates the needlessly high number of function calls that were previously being made to the Bloc state route.
* **Array Members Return Properly in State** - Previously, contracts with large arrays produced truncated JSON results. We solved this by paginating Bloc, the state route, and STRATO, the storage route. Now, large arrays return properly formatted JSON.
* **CLI Instructions Updated**  - We improved our documentation to better distiguish between uploading apps to localhost versus the testnet. [Click here to try the CLI.](https://stratodev.blockapps.net/dashboard/#/apps?developer)

# March 6, 2018 Release Notes

## New Features

* **STRATO CLI** - You can now deploy STRATO apps directly from your CLI. Run `npm install -g strato-cli` to download a sample app and upload it to the testnet. 
* **New User Flow for STRATO Getting Started** - We revamped our onboarding experience to accomodate our token request form and new CLI. [Click here to get started.](https://stratodev.blockapps.net/dashboard/#/apps?developer)

# February 20, 2018 Release Notes

## New Features

* **Token Request Form** - All apps in our launchpad now require tokens for usage. The good news is that they're free (for now). [Simply login to the dashboard and fill out the Token Request Form to receive some app tokens.](https://testnet1.blockapps.net "Token Request Form")
* **Login Functionality Added to Dashboard** - Users can now login to the STRATO Public Dashboard in order to manage their tokens, browse apps, and deploy their own. [See for yourself.](https://testnet1.blockapps.net "STRATO Public Dashboard")

# February 2, 2018 Release Notes

## New Features

* **Mobile dApp Store** - [users can now browse and use blockchain apps deployed to STRATO on their mobile phones.](http://stratodemo1.eastus2.cloudapp.azure.com/dappstore/#/dashboard "Charity App")
* **Lottery dApp rebranded to Charity Raffle** - our flagship blockchain app has been rebranded as a charity raffle. Users can create, participate, and win raffles, with the payout donated to the charity of their choice. The app now works as well on mobile as it does on desktop - [be sure to take a look.](http://stratodemo1.eastus2.cloudapp.azure.com/dappstore/#/dashboard "Charity App")

## Bug Fixes

* We're continuing to improve the reliability of STRATO deployment on RedHat OpenShift. Our efforts are focused on single-node versions of STRATO, but we're planning to begin performance enhancements on multi-node in an upcoming release. 
* Method call popup on STRATO dashboard now populates with addresses consistently. Users complained about adding addresses that didn't show up in their dashboard, but this issue is now resolved.
* Improved gas and ether usage values from STRATO transaction results. Some users were not getting accurate gas and ether values when querying STRATO transaction results. This issue is now resolved.


# January 19, 2018 Release Notes

## New Features

* Improved documentation for BlockApps BA - Supply Chain Demo App. Users were experiencing difficulty deploying our demo app on AWS, so we revised the documentation to make it easier to get started. 

## Bug Fixes 

* Account Detail is blank if address has no associated balance
* Date on transaction and transaction detail page, on firefox, shows up as Invalid Date

# December 15, 2017 Release Notes

## New Features

* Contract Metadata added to STRATO contracts - all dApp metadata is now stored on the blockchain, making it easier for nodes to deliver dApps consistently 
* Ability to send ABI info to Bloc in order to call methods for contracts not created using Bloc
* All contracts compiled through Bloc are now indexed by Cirrus automatically

## Bug Fixes

* Error handling added to incorrect password on contract creation 
* Sync Issue - I start mining on my own chain when reconnecting
* Passes compilation button but fails when creating contract
* P2p does not retry to sync if bootnode was unreachable on STRATO init
* Show proper Solidity Compile errors for SimpleStorage on the SMD Code Editor
* On Contracts list, contract card gets stretched when method name is long


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
