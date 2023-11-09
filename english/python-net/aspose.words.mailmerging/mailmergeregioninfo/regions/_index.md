---
title: MailMergeRegionInfo.regions property
linktitle: regions property
articleTitle: regions property
second_title: Aspose.Words for Python
description: "MailMergeRegionInfo.regions property. Returns a list of child regions."
type: docs
weight: 80
url: /python-net/aspose.words.mailmerging/mailmergeregioninfo/regions/
---

## MailMergeRegionInfo.regions property

Returns a list of child regions.


```python
@property
def regions(self) -> List[aspose.words.mailmerging.MailMergeRegionInfo]:
    ...

```

### Examples

Shows how to verify mail merge regions.

```python
doc = aw.Document(MY_DIR + "Mail merge regions.docx")

# Returns a full hierarchy of merge regions that contain MERGEFIELDs available in the document.
region_info = doc.mail_merge.get_regions_hierarchy()

# Get top regions in the document.
top_regions = region_info.regions

self.assertEqual(2, top_regions.count)
self.assertEqual("Region1", top_regions[0].name)
self.assertEqual("Region2", top_regions[1].name)
self.assertEqual(1, top_regions[0].level)
self.assertEqual(1, top_regions[1].level)

# Get nested region in first top region.
nested_regions = top_regions[0].regions

self.assertEqual(2, nested_regions.count)
self.assertEqual("NestedRegion1", nested_regions[0].name)
self.assertEqual("NestedRegion2", nested_regions[1].name)
self.assertEqual(2, nested_regions[0].level)
self.assertEqual(2, nested_regions[1].level)

# Get list of fields inside the first top region.
field_list = top_regions[0].fields

self.assertEqual(4, field_list.count)

start_field_merge_field = nested_regions[0].start_field

self.assertEqual("TableStart:NestedRegion1", start_field_merge_field.field_name)

end_field_merge_field = nested_regions[0].end_field

self.assertEqual("TableEnd:NestedRegion1", end_field_merge_field.field_name)
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMergeRegionInfo](../)

