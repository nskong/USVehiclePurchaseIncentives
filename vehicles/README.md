This folder is for monetary Plug-in Electric Vehicle (PEV) purchase incentives across the United States. 

This does not include incentives that have no monetary value, such as High Occupancy Vehicle (HOV) Lane Access. 
Additionally, this only considers light-duty passenger vehicles.

**We currently only have incentives for California. Please contribute if this project will be helpful to you!**

### Data Structure

Because the monetary dollar amount someone receives from a purchase incentive is variable on a number of factors, one incentive may have a number of various representations. 

For example, the California [Clean Vehicle Rebate Project (CVRP)](https://cleanvehiclerebate.org/) (*numbers 54-71*) has 18 different monetary values, based on income, marriage status, vehicle type, and household size.

### Data Schema

An asterisk indicates the field is optional. Optional fields will only appear if the incentive has a requirement for that field.

* **name:** Name of the incentive.
* **id**: id of the incentive according to this database. Ids increase starting at 1.
* ***subId:** Number of this representation of id. 
* **region**: Area the incentive is applicable in. "Federal" if the incentive is at federal level and available at all states, otherwise uses the two letter state code of the state.
* ***zipcode**: A list of strings. If the incentive is only available in certain zip codes, this field is a string of the representation of the zipcodes the incentive is available in. For example, a utility company covers a certain number of zipcodes, so if the incentive was available through PG&E, this field would be "PG&E".
* **vehicleTypes**: List of strings. Vehicles types of the vehicle being bought. Possible values are "FCV", "ICEV", "PHEV", "BEV", "HEV". Look up the acronyms if don't know what they are.
* **purchaseTypes**: List of strings. How the vehicle being purchased is being bought. Possible values are "new", "used", "lease."
* **incentiveType**: Type of the incentive. These match the AFDC website purchase type. Possible values are "grants", "tax incentives", "loans and leases", "rebates", "exemptions", and "other".
* **dollarAmount**: US Dollar amount of the incentive.
* ***income**: An object with fields \*minimum and \*maximum that represent the ranges of income to be eligible. Units are in USD.
* ***fpl**: Federal Poverty Level. An object with fields \*minimum and \*maximum that represent the ranges of the federal povery level to be eligible. Units are in percentages. There are APIs to calculate the federal poverty level based on location.
* ***fuelEconomy:** An object with fields \*minimum and \*maximum that represent the ranges of fuel economy to be eligible. Units are in Miles per Gallon.
* ***marriageStatus:** Options are "head of household," "single," "married independent," "married single,"  and "widower."
* ***batteryCapacity:**  An object with fields \*minimum and \*maximum that represent the ranges of battery capacity to be eligible. Units in kWh.
* ***weight:**  An object with fields \*minimum and \*maximum that represent the ranges of income to be eligible. Units are in pounds, usually as the Gross Vehicle Weight Rating (GVWR).
* ***range**:  An object with fields \*minimum and \*maximum that represent the ranges of range to be eligible. Units are in miles.
* ***householdSize:** The maximum is 8. We don't go above becuase many incentives have variable amounts after 8 household members.
* ***year:**  An object with fields \*minimum and \*maximum that represent the ranges of years to be eligible. 
* **fleet:** Boolean. true if the incentive is only for a fleet, false if the vehicle is for private consumers.
* ***trade-in:*** Boolean. true if the incentive is for trading in an old clunker, false otherwise.
* ***url:*** URL for the website of the incentive.
* **description**: Description of the incentive according to the AFDC website. 
* ***date*:** An object with the fields of start and end date. Empty strings mean we don't know the dates.
