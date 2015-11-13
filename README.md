# data-project
## Data Representation and Querying Project 2015
### Padraic Wade

## Introduction
This project provides the design and documentation for the dataset "Dataset title" which is available at [data.gov.ie](https://data.gov.ie)

## About the data
This dataset was received in Comma Separated Values (CSV) format, and was downloaded from [*Galway County Polling Stations*](https://data.gov.ie/dataset/polling-stations-county-galway).
The CSV file contains 253 rows, the first being a header row with the names of each field.
There are six values on each line, which are as follows:
    
    - **chords**: the co-ordanates of the polling station separated into X and Y coordinates.
    - **school**: the name of the school.
    - **BuildingID**: the id of the school building used for refernece in other softwares and databases.
    - **BuildingName**: the name of the building.
    - **BuildingAdd**:  the address of the building.
    - **Locality**: The locality of the building.

## List of locations of polling stations
You can get a list of polling stations in a specific area using the GET method at the following URL:
*http://pollapi.com/region/[region]*
where you replace [region] with the region.
An example of a response would be:
```json
{
        "LOCALITY": "DUNMORE",
        "School": "Dunmore N.S. No. 2",
        "ID": "80430959",
        "BUILDING_I": "80430959",
        "ORGANISATI": " ",
        "BUILDING_N": "SAINT NICHOLAS NATIONAL SCHOOL",
        "ADDR_LIN00": "SION HILL",
        "ADDR_LIN01": "DUNMORE",
        "ADDR_LIN02": "CO. GALWAY",
}
```

## List of polling stations by id no
You can get a list of polling stations in a specific area using the GET method at the following URL:
*http://pollapi.com/id/[id]*
where you replace [id] with the id.
An example of a response would be:
```json
{
        "ID": "80430959",
        "School": "Dunmore N.S. No. 2",
        "BUILDING_I": "80430959",
        "ORGANISATI": " ",
        "BUILDING_N": "SAINT NICHOLAS NATIONAL SCHOOL",
        "ADDR_LIN00": "SION HILL",
        "ADDR_LIN01": "DUNMORE",
        "ADDR_LIN02": "CO. GALWAY",
}
```

## search by school name
You can get a list of polling stations in a specific area using the GET method at the following URL:
*http://pollapi.com/school/[school]*
where you replace [school] with the school name.
An example of a response would be:
```json
{
        "School": "Dunmore N.S. No. 2",
        "LOCALITY": "DUNMORE",
        "ID": "80430959",
        "BUILDING_I": "80430959",
        "ORGANISATI": " ",
        "BUILDING_N": "SAINT NICHOLAS NATIONAL SCHOOL",
        "ADDR_LIN00": "SION HILL",
        "ADDR_LIN01": "DUNMORE",
        "ADDR_LIN02": "CO. GALWAY",
}
```

## search by school address
You can get a list of polling stations in a specific area using the GET method at the following URL:
*http://pollapi.com/schoolAdd/[schoolAdd]*
where you replace [schoolAdd] with the school address.
An example of a response would be:
```json
{
        "School": "Dunmore N.S. No. 2",
        "BUILDING_N": "SAINT NICHOLAS NATIONAL SCHOOL",
        "ADDR_LIN00": "SION HILL",
        "ADDR_LIN01": "DUNMORE",
        "ADDR_LIN02": "CO. GALWAY",
}
```
