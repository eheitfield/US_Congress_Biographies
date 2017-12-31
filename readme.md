# U.S. Congress Biographies in JSON Format

This repository contains biographical information for current members of the United States House and Senate in JSON format.

Textual biographical information for each meber is scraped from the _Biographical Directory of the U.S. Congress_ hosted by [Congress.gov](http://bioguide.congress.gov/biosearch/biosearch.asp)

Each record is contained in a seperate file whose base title is the ID assigned to the member in the _Biographical Directory of the U.S. Congress_. For example, the record file for Represenatative Paul Ryan is `R000570.json`

Records are formatted as JSON dictionaries with the following fields:

*	`id`: the string ID assigned to the member in the _Biographical Directory of the U.S. Congress_ This is the same as the record's base file name.

*	`update_date`: The data at which the record was scraped from the _Biographical Directory of the U.S. Congress_. Note that this date will presumably be more recent than the last date at which the directory entry was updated in the directory itself. The date is formatted as a "YYYY-MM-DD" string.

*	`biography_text`: A string containing a textual description of the congress member's political career.

