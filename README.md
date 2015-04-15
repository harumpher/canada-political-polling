# Canadian Political Polling Data
## Overview
A nice, accessibly formatted aggregation of Canadian Political Polling data. National level data can be found in the `national` folder, Provincial data in the `provincial` folder. Data is stored in JSON files. Each file contains an array of polls in chronological order:
```json
[
	{}, // Poll 1
	...
	{}  // Poll N
]
```
## General Metadata
Each file contains poll data for a particular question. Different poll questions may share properties. Metadata for such general properties is available here.
### date
Type: `String`
The last day of polling. An [ISO 8601](http://en.wikipedia.org/wiki/ISO_8601) formatted date. eg. `2015-12-31`.
### sample-size
Type: `Integer`
The number of respondants to the question or poll. If present, response values are to be interpreted as a percentage of the sample.
### pollster
Type: `String`
The pollster who performed the survey. One of:
 - 1abvote: [1ABVote.ca](http://www.1abvote.ca)
 - forum: [Forum Research Inc.](http://www.forumresearch.com)
### responses
Type: `Object`
The question response categories and data. For example:
```json
responses: {
    "oranges": 75,
    "apples": 25
}
```
If `sample-size` is present, the data is a percentage. If not, the data is the raw number of responses.
## Party Metadata
Polls often reference political parties. They are referenced as:
### Alberta
 - liberal: [Alberta Liberal Party](http://www.albertaliberal.com)
 - ndp: [Alberta New Democratic Party](http://www.albertandp.ca)
 - pc: [Progressive Conservative Association of Alberta](http://www.pcalberta.org)
 - wildrose: [Wildrose Alliance Party of Alberta](http://www.wildrose.ca)
 - alberta: [The Alberta Party](http://www.albertaparty.ca)
 - green [Green Party of Alberta](http://www.greenpartyofalberta.ca)

## Question Metadata
### party-preference
Party preference data summarizes responses to a question resembling:

>If an election were held today, which political party would you vote for?

or

>For the upcoming election, how do you plan/are you leaning to vote?

Don't know, not sure, none of the above, and not voting responses are excluded.

## Contributing
Please do.

## Special Thanks
Special thanks, for showing how it's done, to:

- [Election Almanac](http://www.electionalmanac.com)
- [Three Hundred Eight](http://www.threehundredeight.com)

## License
Copyright to the data made available in this repository is held by various third parties. It is provided here under the [fair dealing provisions of the Copyright Act of Canada.](http://en.wikipedia.org/wiki/Fair_dealing_in_Canadian_copyright_law).

This repository and its content is released under the [CC By 4.0 license](http://creativecommons.org/licenses/by/4.0/).