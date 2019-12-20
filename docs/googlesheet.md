# Make a Google Sheet into a Web Table

1. First, create a Google sheet with the desired data.
    - The first row must be column names. Column names should be lowercase and contain no spaces or weird characters.
2. Next, on your Google Sheet, go to File > Publish to the Web. Select "Entire Document" and "Web page", then click "Publish". 
3. Now find the "Google Sheet ID": 
    - Copy the address of the main view of your open sheet. It will look something like:
        `https://docs.google.com/spreadsheets/d/YOURGOOGLESHEETID/edit?folder=0AISlmzlTm1PQUk9PVA#gid=0`
    - The Google Sheet ID will be a long string of letters and numbers. For example, in
        `https://docs.google.com/spreadsheets/d/1dUAPI7nge5PWTksdUITA9IbgA_Csz2gtVSCnjWz1CjE/edit?folder=0AISlmzlTm1PQUk9PVA#gid=0`
        The ID would be `1dUAPI7nge5PWTksdUITA9IbgA_Csz2gtVSCnjWz1CjE`.
4. Set up a new GitHub repository by importing this one.
5. Edit the `_config.yml` file to set up your site:
    - Set up the Site Settings
    - Paste your Google Sheet ID after `google-sheet-id`
    - In the `table-columns` variable, fill out the desired fields and display names, following the example structure (be careful with the indentation as YML is sensitive!)
    - Choose a column to sort on using index number starting at 0 with `sort-column:` (optional)
    - Choose asc and desc sort with `sort-order:` (optional)
    - Choose field to create word cloud on `cloud-field`
    - Optionally add stopwords to remove from cloud using a list separated with `;` in `cloud-stopwords`
6. Optionally flesh out content in Markdown.
    - Edit "about.md" to describe your data or organization or what ever.
    - Edit text on "index.md" or "cloud.md" to add descriptive info about the visualizations.
7. Activate GitHub Pages.
