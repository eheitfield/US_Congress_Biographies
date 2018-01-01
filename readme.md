# U.S. Congress Biographies in JSON Format

This repository contains biographical information for current members of the United States House and Senate in an easy to parse JSON format. Textual biographical information for each member is scraped from the [Biographical Directory of the U.S. Congress](http://bioguide.congress.gov/biosearch/biosearch.asp) hosted by [Congress.gov](http://congress.gov).

Each record is contained in a seperate file whose base title is the ID assigned to the member in the _Biographical Directory of the U.S. Congress_. For example, the record file for Represenatative Paul Ryan is `R000570.json`. This GitHub repository resides at a static URL, so users can access individual records using predictable URL scheme. To access the record for Paul Ryan, issue a GET request to

	https://github.com/eheitfield/US_Congress_Biographies/blob/master/R000570.json

Records are formatted as JSON dictionaries with the following fields:

*	`id`: the ID string assigned to the member in the _Biographical Directory of the U.S. Congress_. This is the same as the record's base file name.

*	`update_date`: The date at which the record was scraped from the _Biographical Directory of the U.S. Congress_. Note that this date will be more recent than the last date at which the directory entry was updated in the directory itself. The date is formatted as a "YYYY-MM-DD" string.

*	`biography_text`: A string containing a text description of the congress member's political career.

