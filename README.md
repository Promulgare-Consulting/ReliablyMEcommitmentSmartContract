# ReliablyMEcommitmentSmartContract
Ethereum Smart Contract to record ReliablyME commitment status to the blockchain

This smart contract works in conjunction with the ReliablyME database.

Storage
This smart contract stores the user and event information in nested mappings.  The first mapping uses the 
userId from ReliablyME as the key to a mapping of eventIds.  The second mapping is uses the eventId from 
ReliablyME to store a structure with dates as the value.  The structure stores two dates.  The offer date
and the complete data.  Both dates are set by the owner of the event accepting either the offer for help 
or accepting that the offer has been completed.

Privacy
Since the storage uses an unordered key value mapping there is no way to iterate either through all of 
the users or all of the events.  This information access is controlled by the user of ReliablyME and the 
owner of an event.

Lookups
Anyone can call the get functions of this contract providing that they know the Ids of the user and event.  
This is for confirmation on all of the data used to generate the reliability rating.

Updates
Only the ReliablyME platform can make updates to this data.  

