# Google sheet

First, on your Google Sheet, go to File > Publish to the Web.
Select Entire Document, Web page, and click "Publish". 

Now find the Google Sheet ID, copy the address of the main view of your open sheet. 
It will look something like:

`https://docs.google.com/spreadsheets/d/YOURGOOGLESHEETID/edit?folder=0AISlmzlTm1PQUk9PVA#gid=0`

The Google Sheet ID will be a long string of letters and numbers. 
For example, in

`https://docs.google.com/spreadsheets/d/1dUAPI7nge5PWTksdUITA9IbgA_Csz2gtVSCnjWz1CjE/edit?folder=0AISlmzlTm1PQUk9PVA#gid=0`

The ID would be `1dUAPI7nge5PWTksdUITA9IbgA_Csz2gtVSCnjWz1CjE`.

Using the ID, we can access the sheet as JSON, using the API recipe:

`https://spreadsheets.google.com/feeds/list/YOURGOOGLESHEETID/od6/public/values?alt=json`
