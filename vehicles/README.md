# Overview

TODO: overview

These are incentives only for vehicles and only associated with a monetary value. 
This database also only considers light-duty vehicles. That includes passenger vehicles. 

### Examples 

TODO: fix examples
**Good example of an valid incentive for this database: ** The federal electric vehicle tax credit
**Bad example of an incentive:** The California HOV law is a state incentive, but does not have a monetary value associated with purchasing a vehicle. 

# Duplicates

While incentives are number staring from 1, each incentive has it's own id. 
This is due to the fact one incentives will have a different dollar value depending on it's variables.
The same incentive will be represented in multiple forms with different subIds.

For example, TODO:

### Json

Single incentives are represented with an underscore. 
Their first number indicates the incentive id, and the second number indicates the sub-id, the id nested under the current id

### Tsv

TODO:

# Incentive Structure

An asterisk* indicates the field is . Optional fields will only appear if the incentive has a requirement for that field.
TODO: need baseAmount?
TODO: Zipcode mappings

* **name*: Name of the incentive.
* **id*: Numbered id of the incentive according to this database. Ids increase from 1 and on.
* subid: TODO:
* **region*: Area the incentive is applicable in. 'Federal' if the incentive is at federal level and available at all states, otherwise uses the two letter state code of the state.
* *zipcode*: If the incentive is only available in certain zip codes, this field is a string of the representation of the zipcodes the incentive is available in. For example, a utility company covers a certain number of zipcodes, so if the incentive was available through PG&E, this field would be 'pg&e'.
* **vehicleTypes*: Vehicles types of the vehicle being bought. Possible values are 'FCV', 'ICEV', 'PHEV', 'BEV', 'HEV', 'NGV'. Look up the acronyms if don't know what they are.
* **purchaseTypes*: How the vehicle being purchased is being bought. Possible values are 'new', 'used'
* **incentiveType*: Type of the incentive. These match the afdc purchase type. Possible values are 'grants', 'tax incentives', 'loans and leases', 'rebates', 'exemptions', and 'other'.
* **dollarAmount*: Dollar amount of the incentive
* *income:*
* *fpl*: Federal Poverty Level. This is a percentage. TODO:
* *fuelEconomy* 
* *marriageStatus:* Options are "head of household," "single," "married independent," "married single,"  and "widower"
* *batteryCapacity:* Unit in kWh
* *weight:* in pounds, usually in GWVR
* *range:* in miles, has minimum and maximum
* *householdSize:* The maximum is 8. We don't go above becuase many incentives have variable amounts after 8 household members.
* *year:*
* **fleet:*
* **trade-in*:
* **url*:
* **Description*:
* **Date*: Includes start and end date of each. Empty strings mean we don't know the dates.