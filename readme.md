# U.S. Congress Biographies in JSON Format

This repository contains biographical information for current members of the United States House and Senate in an easy to parse JSON format. Textual biographical information for each member is scraped from the [Biographical Directory of the U.S. Congress](http://bioguide.congress.gov/biosearch/biosearch.asp) hosted by [Congress.gov](http://congress.gov).

Each record is contained in a seperate file whose base title is the ID assigned to the member in the _Biographical Directory of the U.S. Congress_. For example, the record file for Represenatative Paul Ryan is `R000570.json`. This GitHub repository resides at a static URL, so users can access individual records using a predictable URL scheme. To access the record for Paul Ryan, issue a GET request to

	https://raw.githubusercontent.com/eheitfield/US_Congress_Biographies/master/json/R000570.json

Records are formatted as JSON dictionaries with the following fields:

*	`id`: the ID string assigned to the member in the _Biographical Directory of the U.S. Congress_. This is the same as the record's base file name.

*	`update_date`: The date at which the record was scraped from the _Biographical Directory of the U.S. Congress_. Note that this date will be more recent than the last date at which the directory entry was updated in the directory itself. The date is formatted as a "YYYY-MM-DD" string.

*	`biography_text`: A string containing a text description of the congress member's political career.

*	`name`: A dictionary containing the member's name.

	*	`last`: the member's last name.

	*	`first`: the member's first name.

	*	`middle`: the member's middle name or initial.

	*	`nickname`: any nickname associated with the member.

*	`date_of_birth`: A dictionary containing the member's date of birth.

	*	`month`: the month of the year as an integer.

	*	`day`: the day of the month as an integer.

	*	`year`: the year as an integer.

*	`place_of_birth`: A string describing the location of the member's place of birth.

*	`post_secondary_degrees`: A list of dictionaries summarizing any post-secondary degrees the member has recieved.  Each list entry contains a dictionary with the following fields:

	*	`degree`: a standard abbreviation for the degree (i.e. B.A. for Bachelors of Arts).

	*	`year`: the year the degree was awarded as an integer.

	*	`instition`: the institution awarding the degree.

For example, the record for Representative Paul Ryan is:

	{
		"id": "R000570", 
		"update_date": "2018-01-10", 
		"biography_text": "RYAN, Paul D., a Representative from Wisconsin; born in Janesville, Rock County, Wis., January 29, 1970; graduated from Joseph A. Craig High School, Janesville, Wis., 1988; B.A., Miami University, Oxford, Ohio, 1992; construction business; staff, United States Senator Robert Walter Kasten, Jr., of Wisconsin, 1992; staff assistant, Empower America, 1993-1995; staff, United States Senator Sam Dale Brownback of Kansas, 1995-1997; elected as a Republican to the One Hundred Sixth and to the nine succeeding Congresses (January 3, 1999-present); chair, Committee on the Budget (One Hundred Twelfth and One Hundred Thirteenth Congresses); chair, Committee on Ways and Means (One Hundred Fourteenth Congress); chair, Joint Committee on Taxation (One Hundred Fourteenth Congress); unsuccessful Republican candidate for Vice President of the United States in 2012; Speaker of the House (One Hundred Fourteenth and One Hundred Fifteenth Congresses).", 
		"name": {
			"last": "Ryan", 
			"first": "Paul", 
			"middle": "D."
		}, 
		"date_of_birth": {
			"month": 1, 
			"day": 29, 
			"year": 1970
		}, 
		"place_of_birth": "Janesville, Rock County, Wis.", 
		"post_secondary_degrees": [
			{
				"degree": "B.A.", 
				"year": 1992, 
				"institution": "Miami University, Oxford, Ohio"
			}
		]
	}

