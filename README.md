# Elasticsearch the cheatsheet
Just some of my notes as I stumble through ES
- ES is a NoSql document storage cluster with Lucene search built in.
- It optimizes data categorization on write so that indexes are fast ... hence adding data = indexing
- Because comprehensive indexing happens on write, reads are super fast, but writes can take a bit, so ES is near real time
- ES relies on a map of indexes, fields and types to determine what and how data should be indexed. It can do this automatically/dynamically, but sometimes you want a value to be treated as a geopoint and not a float, or maybe you want to define a parent/child (1 to many) relationship - create a mapping manually.

## Indexes
So with ES Indexes are king. They effectively group your data - a logical partition of data if you will.  
eg vehicle would be a good index for these types: car, plane, truck, motorcycle, bus, scooter, bicycle....

### Things to remember with Indexes
- An index needs to be created before you can index (add) documents (records)
- Indexes can't be modified after documents have been added.
- Fields can be added anytime (nosql), but changing the fields or field type would require a reindex which can be pretty slow
- One way to deal with slow reindexing is to: 1) create an alias index 2) Create a new index and reindex old to new 3) switch the alias to the new index.
- Deleting and index effectively deletes all its types and documents. Also deleting everything is really easy to do

## Types

## Mapping


## Searches


## Joining/Parent-Child/1 to Many
