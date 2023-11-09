---
title: MailMerge.get_regions_by_name method
linktitle: get_regions_by_name method
articleTitle: get_regions_by_name method
second_title: Aspose.Words for Python
description: "MailMerge.get_regions_by_name method. Returns a collection of mail merge regions with the specified name."
type: docs
weight: 220
url: /python-net/aspose.words.mailmerging/mailmerge/get_regions_by_name/
---

## get_regions_by_name(region_name) {#str}

Returns a collection of mail merge regions with the specified name.


```python
def get_regions_by_name(self, region_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| region_name | str | Region name (case-insensitive). |

### Returns

The list of regions.


### Examples

Shows how to create, list, and read mail merge regions.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# "TableStart" and "TableEnd" tags, which go inside MERGEFIELDs,
# denote the strings that signify the starts and ends of mail merge regions.
self.assertEqual("TableStart", doc.mail_merge.region_start_tag)
self.assertEqual("TableEnd", doc.mail_merge.region_end_tag)

# Use these tags to start and end a mail merge region named "MailMergeRegion1",
# which will contain MERGEFIELDs for two columns.
builder.insert_field(" MERGEFIELD TableStart:MailMergeRegion1")
builder.insert_field(" MERGEFIELD Column1")
builder.write(", ")
builder.insert_field(" MERGEFIELD Column2")
builder.insert_field(" MERGEFIELD TableEnd:MailMergeRegion1")

# We can keep track of merge regions and their columns by looking at these collections.
regions = doc.mail_merge.get_regions_by_name("MailMergeRegion1")

self.assertEqual(1, regions.count)
self.assertEqual("MailMergeRegion1", regions[0].name)

merge_field_names = doc.mail_merge.get_field_names_for_region("MailMergeRegion1")

self.assertEqual("Column1", merge_field_names[0])
self.assertEqual("Column2", merge_field_names[1])

# Insert a region with the same name inside the existing region, which will make it a parent.
# Now a "Column2" field will be inside a new region.
builder.move_to_field(regions[0].fields[1], False)
builder.insert_field(" MERGEFIELD TableStart:MailMergeRegion1")
builder.move_to_field(regions[0].fields[1], True)
builder.insert_field(" MERGEFIELD TableEnd:MailMergeRegion1")

# If we look up the name of duplicate regions using the "GetRegionsByName" method,
# it will return all such regions in a collection.
regions = doc.mail_merge.get_regions_by_name("MailMergeRegion1")

self.assertEqual(2, regions.count)
# Check that the second region now has a parent region.
self.assertEqual("MailMergeRegion1", regions[1].parent_region.name)

merge_field_names = doc.mail_merge.get_field_names_for_region("MailMergeRegion1", 1)

self.assertEqual("Column2", merge_field_names[0])
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

