![Think Big](http://thinkbig.teradata.com/wp-content/themes/thinkbig/images/header/Logo128.png "Think Big logo")
![Ancestry.com](http://c.mfcreative.com/mars/landing/lohp/2014/smp/us-lohp-simplehdr-logo.png "Ancestry.com logo")

# Think Big Challenge 2014

## Notes about the data

The basic format of the files is as follows. All data are serialized in JSON format:

* **Version. ('v')** The version of the file format. (Can be ignored.)

* **Persons.** An array of persons in the tree.

	* **Global ID. ('gid')** Represents the ID this Person node. Consists of three parts: `person id:source id:tree id`. (Source 1033 represents member-supplied data.)

	* **Names.** The names that represent the person -- can be multiple. (Note: surnames have been hashed for this contest -- see **Anonymization** below).
		* ‘g’ – given
		* ‘s’ – surname

	* **Gender.**
		* ‘g’ – "m" = male, "f" = female

	* **Events.** Dates and places related to important life events
		* ‘t’ – type : birth, marriage, death … (Dates and places. Note: normalized places are available in the data -- see **Place Name Normalization** below.)

	* **Family.** Information about relatives
		* ‘t’ – type (“F” = father, “M” = mother, “C” = child, “H” = husband, “W” = wife
		* ‘tgid’ – id of the related person in the same tree
		* 'mp' - Media attached (irrelevant)
		* 'ep' - Evidence attached = id’s of records attached to person
 
* **Tree.** - metadata and other information about this tree.


### Anonymization

The contest data set includes both publicly availably records (e.g., census data) and user-contributed submissions on Ancestry.com. To preserve user privacy, all family names present in the data have been obscured with a hash function. The hash is constructed such that all occurrences of the same string will result in the same hash code.

### Place name normalization

Place names in the records have already been standardized through a
normalization procedure. For example, this portion of a record
referencing Hartford contains a "normalizedPlace" structure 
containing standardized values for its city, county, state, and country:

```
[...]
	{
	"id": "41000997445",
	"t": "Death",
	"q": 367,
	"p": "Hartford, Hartford, Connecticut, USA",
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
	"date": "1887-01-15"
	}
[...]
```
