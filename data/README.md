<img align="middle" src="http://c.mfcreative.com/mars/landing/lohp/2014/smp/us-lohp-simplehdr-logo.png" alt="Ancestry.com"/>
<img align="right" src="http://thinkbig.teradata.com/wp-content/themes/thinkbig/images/header/Logo128.png" alt="Think Big"/>
# Think Big Challenge 2014

## Notes about the data

This subdirectory contains a small extract of the data set (1,000 records). There are two data sets provided:
* A complete set of records from after the year 1820 is available for download from Amazon S3 at
The full data set is available for download from Amazon S3 at [https://s3.amazonaws.com/think.big.challenge/AncestryPost1820Data.gz](https://s3.amazonaws.com/think.big.challenge/AncestryPost1820Data.gz) as a 127MB gzip file.
* A sample of records pre-1820 for use in the data science "Learning of Common Ancestors" challenge.  This can be downloaded at [https://s3.amazonaws.com/think.big.challenge/AncestryPre1820Sample.gz](https://s3.amazonaws.com/think.big.challenge/AncestryPre1820Sample.gz) as a 4MB gzip file.

### Record format

The basic record format is as follows. All data are serialized in JSON format:

* **Version. ('v')** The version of the file format. (Can be ignored.)

* **Persons.** An array of persons in the tree.

	* **Global ID. ('gid')** Represents the ID this Person node. Consists of three parts: `person id:source id:tree id`. (Source 1033 represents member-supplied data.)

	* **Names.** The names that represent the person -- can be multiple. (Note: surnames have been hashed for this contest -- see **Anonymization** below).
		* ‘given’
		* ‘surname’

	* **Genders.**
		* ‘gender’ – "m" = male, "f" = female

	* **Events.** Dates and places related to important life events
		* ‘type’ - event type : birth, marriage, death … 
		* ‘q’ - calculated quality of the event
		* ‘place’ - un-normalzied place text string
		* ‘normalizedPlace’ - (-- see **Place Name Normalization** below.)
		* ‘Date’ - normalized date.  YYYY-MM-DD, note that is is valid to have only a year, only a year and month, or year month and day

	* **Family.** Information about relatives
		* ‘type’ – father, mother, child, husband, wife
		* ‘targetgid’ – gid of the related person in the same tree
		* ‘pty’ - priority
		* ‘mod’ - ignore
	* **ep.** - Evidence attached = 'gid' contains Global ID’s of records attached to person
		* ‘cgid’ - ignore
		* ‘gid’ - gid of attached person or record.  User has attached another users tree if the 2nd part of the gid is 1030, if the 2nd part is other than 1030, the user attached a record (records could be census, immigration, birth, marriage, death ...).  The third part of the gid will only be populated if 1030 is the second part.


### Anonymization

The contest data set includes both publicly availably records (e.g., census data) and user-contributed submissions on Ancestry.com. To preserve user privacy, all surnames present in the data have been obscured with a hash function. The hash is constructed such that all occurrences of the same string will result in the same hash code.

### Place name normalization

Place names in the records have already been standardized through a
normalization procedure. For example, this portion of a record
referencing Hartford contains a "normalizedPlace" structure 
containing standardized values for its city, county, state, and country:

```
[...]
	{
	"id": "41000997445",
	"type": "Death",
	"q": 367,
	"place": "Hartford, Hartford, Connecticut, USA",
	"normalizedPlace": [{
		"value": "999",  # city value for Hartford
		"type": "gp",
		"sequence": 0,
		"level": "city"
		}, 
		{
		"value": "1323", # Hartford County
		"type": "gp",
		"sequence": 1,
		"level": "county"
		},
		{
		"value": "9", # Connecticut
		"type": "gp",
		"sequence": 2,
		"level": "state"
		},
		{
		"value": "2", # USA
		"type": "gp",
		"sequence": 3,
		"level": "country"
		}],
	"Date": "1887-01-15"
	}
[...]
```
