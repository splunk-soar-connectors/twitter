[comment]: # "Auto-generated SOAR connector documentation"
# Twitter

Publisher: Splunk  
Connector Version: 1\.0\.2  
Product Vendor: Twitter  
Product Name: Twitter  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.2\.7532  

This app integrates with Twitter to perform a search action

[comment]: # " File: readme.md"
[comment]: # "  Copyright (c) 2019 Splunk Inc."
[comment]: # ""
[comment]: # "  Licensed under Apache 2.0 (https://www.apache.org/licenses/LICENSE-2.0.txt)"
[comment]: # ""
Information on configuring Twitter api access can be found
[here](https://developer.twitter.com/en/docs/basics/authentication/guides/access-tokens.html)

### Twitter

Python Twitter Tools (PTT) includes a Twitter API, command-line tool, and IRC bot. It is developed
by Mike Verdone and the Python Twitter Tools developer team. MIT License, Copyright (c) 2008 Mike
Verdone.


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Twitter asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**token** |  required  | string | Twitter account token
**token\_secret** |  required  | password | Twitter account token secret
**consumer\_key** |  required  | string | Twitter account consumer key
**consumer\_secret** |  required  | password | Twitter account consumer secret

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[run query](#action-run-query) - Search tweets for specific text within the past 7 days  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'run query'
Search tweets for specific text within the past 7 days

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**query** |  required  | Text to search | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.query | string | 
action\_result\.data\.\*\.\*\.Tweet Link | string | 
action\_result\.data\.\*\.\*\.hashtags | string | 
action\_result\.data\.\*\.\*\.retweeted status | string | 
action\_result\.data\.\*\.\*\.tweet | string | 
action\_result\.data\.\*\.\*\.urls | string |  `url` 
action\_result\.data\.\*\.\*\.username | string | 
action\_result\.summary\.Found Tweets | numeric | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 