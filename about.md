---
title: Howto
layout: page
permalink: /about.html
---

# How to Make a Google Sheet into a Web Table

1. First, create a Google sheet with the desired data. 
    *Tip:* the first row should be column names. Column names should be lowercase and contain no spaces or weird characters.
2. Next, on your Google Sheet, go to File > Publish to the Web.
Select "Entire Document" and "Web page", then click "Publish". 
3. Now find the Google Sheet ID, copy the address of the main view of your open sheet. 
    It will look something like:

    `https://docs.google.com/spreadsheets/d/YOURGOOGLESHEETID/edit?folder=0AISlmzlTm1PQUk9PVA#gid=0`

    The Google Sheet ID will be a long string of letters and numbers. 
    For example, in

    `https://docs.google.com/spreadsheets/d/1dUAPI7nge5PWTksdUITA9IbgA_Csz2gtVSCnjWz1CjE/edit?folder=0AISlmzlTm1PQUk9PVA#gid=0`

    The ID would be `1dUAPI7nge5PWTksdUITA9IbgA_Csz2gtVSCnjWz1CjE`.
4. In the file `_config.yml` add the table id and configuration options:
    - paste your Google Sheet ID after `google-sheet-id:`
    - Choose a column to sort on using index number started at 0 with `sort-column:` (optional)
    - Choose asc and desc sort with `sort-order:` (optional)
    - Choose field to create word cloud on `cloud-field`
    - Optionally add stopwords to remove from cloud using a list separated with `;` in `cloud-stopwords`
    - Optionally add any descriptive text and title in Markdown in "pages/table.md"
5. Configure the columns to display in "_data/config-table.csv"


{% include credits.md %}
