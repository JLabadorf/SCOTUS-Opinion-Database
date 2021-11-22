# Supreme Court of the United States Opinion Database
This database is a repackaging of the Free Law Project's Supreme Court Opinion Bulk Downloader.

That project give tar.gz file of all the opinions as individual JSON files. I created this database as an alternative with all the opinion texts in one main table. 

Some cases were able to to be imported into the database based on individual JSON file patterns. An easy way to see if a case was not imported would be to compare the ids of the cases. ids should created sequentially, so a missing id number indicates a missing case (i.e. if you see ids 10,11,13 you can assume case 12 was not imported).

# Support
This database is hosted on Google Storage. This isn't expensive, but not free. If you find this useful, you can support me by Venmoing @Squelch. Supporting will keep me from having to make accessing this resource paid for by the requestor. Thanks!


# Accessing the data

The database is available through a Google Storage bucket.

https://storage.googleapis.com/scotus-db/scotus-db.db

## Using the data
There are a number of columns, most of which have intutive names. However, there are a few columns that need clarification.

### id
The id column is the Free Law Project's id. The index column is the id assigned by pandas.

### author_uri 
This column is the uri for author information. This URI maps back to the Free Law Project's API data.

### resource_uri
This also maps back to the Free Law Project's API for this particular case.

### joined_by
This is a list of the other authors' which joined this opinion.

## Known Issues
There are a few known issues at this time
1. The author column is blank
2. The author_id is very messy and not useable

# License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.


# Author's Note
I tried to add all the attribution for any code I copied from online sources. Let me know if I missed anything.