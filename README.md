# README.md

This is a comprehensive database of all monetary incentives for vehicles across the United
 States. This *does not* include incentives that have no monetary value. 

This Incentive database was created for the 
[Electric Vehicle Explorer](https://gis.its.ucdavis.edu/evexplorer2/) website. 
It's a comprehensive vehicle cost calculator comparing electric vehicles and your typical 
gasoline vehicle!

All information thus far has been gathered using the 
[Alternative Fuels Data Center](https://afdc.energy.gov/laws) website.

**If you see an incentive missing, please make a pull request!**
**There is currently no easily data-manipulable database for vehicle incentives**


## Structure

I've gathered all the incentives in two forms: TSV and JSON. Mainly because I'm currently 
trying to decide to keep things in SQL or noSQL form. I couldn't decide between the two
initially and I figured that both would end up helping people, so I made both. I've also
included the scripts I used to insert the information into my database in the 
*/scripts* folder

### TSV

I'm using TSV rather than CSV to avoid commas in the data. A lot of incentive notes have
commas in them so tabs is much better. Note, when viewing the .tsv files, you'll see one
incentive multiple times because each one incentive will have different values depending
on the incentive. For example, a vehicle incentive may have a different value for 
purchasing the vehicle new or used, so it will appear in the .tsv twice.


### JSON

In comparison to the tsv, the JSON documents will have only one document per incentive.