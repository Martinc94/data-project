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

An example of a response would be:

    ```json
    [ {"Name": TUAM LIBRARY, "Phone": "+353 (0) 93 24287", "Email": tuam@galwaylibrary.ie}, {...}, ...]
    ```



## List of all library names in galway
You can get a list of all the Library names in co. galway using the GET method at the following URL:

*http://galwaylibrariesapi.ie/name/all*

The data will be returned in JSON format, with the following properties for each Libraries:

    - *Name*: the Name of the Library.

An example of a response would be:

    ```json
    [ {"Name": WESTSIDE LIBRARY}, {"Name": ROUNDSTONE PUBLIC LIBRARY}, ...]
    ```


## Opening hours of Libraries on a given day
You can get a list of Opening hours of Libraries on a given day in a given town using the GET method at the following URL:

*http://galwaylibrariesapi.ie/hours/[town]/[day]*

where you replace [Town] with the town.
For example, the URL:

*http://galwaylibrariesapi.ie/Hours/galwaycity/monday*

will return a list of Opening hours of Libraries on a given day in a given town.
The data will be returned in JSON format, with the following properties for each Libraries:

    - *Name*: the Name of the Library.
    - *Hours*: the opening hours of the Library on given day.

An example of a response would be:

    ```json
    [ {"Name":  WESTSIDE LIBRARY , "hours": 11.00am to 8.00pm}, {...}, ...]
    ```


##  Return library website 
You can get a website URL for a library given its name using the GET method at the following URL:

*http://galwaylibrariesapi.ie/[name]/url*

where you replace [name] with the name of the library.
For example, the URL:

*http://galwaylibrariesapi.ie/athenry/url*

The data will be returned in JSON format, with the following properties for each Libraries:

    - *url*: the Website of the Library.

An example of a response would be:

    ```json
    [ {"url": http://www.galway.ie/en/Services/Library/}]
    ```
