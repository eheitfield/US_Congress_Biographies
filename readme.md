# U.S. Congress Biographies in JSON Format

This repository contains biographical information for current members of the United States House and Senate in an easy to parse JSON format. Textual biographical information for each member is scraped from the [Biographical Directory of the U.S. Congress](http://bioguide.congress.gov/biosearch/biosearch.asp) hosted by [Congress.gov](http://congress.gov).

Each record is contained in a seperate file whose base title is the ID assigned to the member in the _Biographical Directory of the U.S. Congress_. For example, the record file for Represenatative Paul Ryan is `R000570.json`. This GitHub repository resides at a static URL, so users can access individual records using a predictable URL scheme. To access the record for Paul Ryan, issue a GET request to

	https://raw.githubusercontent.com/eheitfield/US_Congress_Biographies/master/R000570.json

Records are formatted as JSON dictionaries with the following fields:

*	`id`: the ID string assigned to the member in the _Biographical Directory of the U.S. Congress_. This is the same as the record's base file name.

*	`update_date`: The date at which the record was scraped from the _Biographical Directory of the U.S. Congress_. Note that this date will be more recent than the last date at which the directory entry was updated in the directory itself. The date is formatted as a "YYYY-MM-DD" string.

*	`biography_text`: A string containing a text description of the congress member's political career.

For example, the record for Representative Paul Ryan is

	{
		"id": "R000570", 
		"biography_text": "RYAN, Paul D., a Representative from Wisconsin; born in Janesville, Rock County, Wis., January 29, 1970; graduated from Joseph A. Craig High School, Janesville, Wis., 1988; B.A., Miami University, Oxford, Ohio, 1992; construction business; staff, United States Senator Robert Walter Kasten, Jr., of Wisconsin, 1992; staff assistant, Empower America, 1993-1995; staff, United States Senator Sam Dale Brownback of Kansas, 1995-1997; elected as a Republican to the One Hundred Sixth and to the nine succeeding Congresses (January 3, 1999-present); chair, Committee on the Budget (One Hundred Twelfth and One Hundred Thirteenth Congresses); chair, Committee on Ways and Means (One Hundred Fourteenth Congress); chair, Joint Committee on Taxation (One Hundred Fourteenth Congress); unsuccessful Republican candidate for Vice President of the United States in 2012; Speaker of the House (One Hundred Fourteenth and One Hundred Fifteenth Congresses).", 
		"update_date": "2017-12-31"
	}

