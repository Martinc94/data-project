# County Galway Libraries API Design
## Data Representation and Querying Project 2015
### Martin Coleman

## Introduction
```This project provides the design and documentation for the dataset "County Galway Libraries " which is available at [data.gov.ie](https://data.gov.ie/dataset/county-galway-libraries)```


## About the data
This dataset was received in Comma Separated Values (CSV) format, and was downloaded from [County Galway Libraries](https://data.gov.ie/dataset/county-galway-libraries).
The CSV file contains 30 rows, the first being a header row with the names of each field.
There are 23 values on each line.

The most relevant are as follows:

Field | Description
------|------------
 Name  | The Library's Name.
 Address1  | First street address.
 Address2  | Second street address.
 Town      | Town where library is situated.
 Postcode  | Library's Postcode.
 Phone| Library's Phone number.
 Email| Library's Email Address.
 Website| Library's Website URL.
 Opening Hours Monday| Mondays Opening hours.
 Opening Hours Tuesday| Tuesdays Opening hours.
 Opening Hours Wednesday| Wednesdays Opening hours.
 Opening Hours Thursday| Thursdays Opening hours.
 Opening Hours Friday| Fridays Opening hours.
 Opening Hours Saturday| Saturdays Opening hours.
 ObjectId | The Library's unique id.
 
 
## List of Libraries in a town
You can get a list of Libraries in a given town using the GET method at the following URL:
*http://galwaylibrariesapi.ie/town/[town]*
where you replace [Town] with the town.
For example, the URL:
*http://galwaylibrariesapi.ie/town/tuam*
will return a list of Libraries in tuam town and some contact information.
The data will be returned in JSON format, with the following properties for each Libraries:

    - *Name*: the Name of the Library.
    - *Phone*: the Phone Number of the Library.
    - *Email*: the Email address of the Library.
    ...
An example of a response would be:

    ```json
    [ {"Name": TUAM LIBRARY, "Phone": "+353 (0) 93 24287", "Email": tuam@galwaylibrary.ie}, {...}, ...]
    ```

