[comment]: # "Auto-generated SOAR connector documentation"
# Twitter

Publisher: Splunk  
Connector Version: 1.0.4  
Product Vendor: Twitter  
Product Name: Twitter  
Product Version Supported (regex): ".\*"  
Minimum Product Version: 4.2.7532  

This app integrates with Twitter to perform a search action

[comment]: # " File: README.md"
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
**token_secret** |  required  | password | Twitter account token secret
**consumer_key** |  required  | string | Twitter account consumer key
**consumer_secret** |  required  | password | Twitter account consumer secret

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
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.status | string |  |   success  failed 
action_result.parameter.query | string |  |   test.com 
action_result.data.\*.\*.Tweet Link | string |  |   https://twitter.com/username/status/1106343825230962689 
action_result.data.\*.\*.hashtags | string |  |   demo 
action_result.data.\*.\*.retweeted status | string |  |   ⚠️ WARNING ⚠️
Unauthenticated RCE Detected

Source IP: 122.122.122.122 (🇺🇸)
Recon Scan Type: ZMap
Exploit Target: Li… https://test.co/kVXF2ZvmCr 
action_result.data.\*.\*.tweet | string |  |   RT @bad_packets: ⚠️ WARNING ⚠️Unauthenticated RCE DetectedSource IP: 122.122.122.122 (🇺🇸)Recon Scan Type: ZMapExploit Target: Testsys r… 
action_result.data.\*.\*.urls | string |  `url`  |   https://twitter.com/i/web/status/1106325213497573376 
action_result.data.\*.\*.username | string |  |   user_name 
action_result.summary.Found Tweets | numeric |  |   14 
action_result.message | string |  |   Found tweets: 14 
summary.total_objects | numeric |  |   1 
summary.total_objects_successful | numeric |  |   1 