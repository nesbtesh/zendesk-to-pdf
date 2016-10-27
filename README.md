# ZenDesk Knowledge Base to PDF


## What is it?

A script develop to migrate the ZenDesk knowlegde base to PDF

## Installation

First of all you need to install [Node.js](https://nodejs.org/en/download/).

Then open terminal and [change directory](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/3/html/Step_by_Step_Guide/s1-navigating-cd.html) to where the installed file is:
and run:

```
	$ npm install
```

## Setup

You want to open the index.js file and change mnyemail@myemail.com for your email address. 
Now [generate](https://support.zendesk.com/hc/en-us/articles/226022787-Generating-a-new-API-token-) a new token by going to 

    Select Settings -> Channels.

    In the API section click the Edit link.

    Make sure Ticket Access is enabled and you'll see your API token there.

    If you want to create a new token, click Generate new token.


Copy that token and paste it where it says mytoken. 
Finally replace "myurl.zendesk.com" with your Zendesk url.


```
	var zenClient = zendesk.createClient({
		username:  'mnyemail@myemail.com',
		token:     'mytoken',
		remoteUri: 'https://myurl.zendesk.com/api/v2/help_center',
	    helpcenter: true
	});

```

## Running

After you finish setting up your variables just run:

```
	node index.js
```
