---
title: GetRegionsByName
second_title: Aspose.Words for C++ API Reference
description: Returns a collection of mail merge regions with the specified name.
type: docs
weight: 274
url: /cpp/aspose.words.mailmerging/mailmerge/getregionsbyname/
---
## MailMerge::GetRegionsByName method


Returns a collection of mail merge regions with the specified name.

```cpp
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::MailMerging::MailMergeRegionInfo>>> Aspose::Words::MailMerging::MailMerge::GetRegionsByName(const System::String &regionName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| regionName | const System::String\& | Region name (case-insensitive). |

### ReturnValue

The list of regions.

## Examples



Shows how to create, list, and read mail merge regions. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// "TableStart" and "TableEnd" tags, which go inside MERGEFIELDs,
// denote the strings that signify the starts and ends of mail merge regions.
ASSERT_EQ(u"TableStart", doc->get_MailMerge()->get_RegionStartTag());
ASSERT_EQ(u"TableEnd", doc->get_MailMerge()->get_RegionEndTag());

// Use these tags to start and end a mail merge region named "MailMergeRegion1",
// which will contain MERGEFIELDs for two columns.
builder->InsertField(u" MERGEFIELD TableStart:MailMergeRegion1");
builder->InsertField(u" MERGEFIELD Column1");
builder->Write(u", ");
builder->InsertField(u" MERGEFIELD Column2");
builder->InsertField(u" MERGEFIELD TableEnd:MailMergeRegion1");

// We can keep track of merge regions and their columns by looking at these collections.
SharedPtr<System::Collections::Generic::IList<SharedPtr<MailMergeRegionInfo>>> regions = doc->get_MailMerge()->GetRegionsByName(u"MailMergeRegion1");

ASSERT_EQ(1, regions->get_Count());
ASSERT_EQ(u"MailMergeRegion1", regions->idx_get(0)->get_Name());

ArrayPtr<String> mergeFieldNames = doc->get_MailMerge()->GetFieldNamesForRegion(u"MailMergeRegion1");

ASSERT_EQ(u"Column1", mergeFieldNames[0]);
ASSERT_EQ(u"Column2", mergeFieldNames[1]);

// Insert a region with the same name inside the existing region, which will make it a parent.
// Now a "Column2" field will be inside a new region.
builder->MoveToField(regions->idx_get(0)->get_Fields()->idx_get(1), false);
builder->InsertField(u" MERGEFIELD TableStart:MailMergeRegion1");
builder->MoveToField(regions->idx_get(0)->get_Fields()->idx_get(1), true);
builder->InsertField(u" MERGEFIELD TableEnd:MailMergeRegion1");

// If we look up the name of duplicate regions using the "GetRegionsByName" method,
// it will return all such regions in a collection.
regions = doc->get_MailMerge()->GetRegionsByName(u"MailMergeRegion1");

ASSERT_EQ(2, regions->get_Count());
// Check that the second region now has a parent region.
ASSERT_EQ(u"MailMergeRegion1", regions->idx_get(1)->get_ParentRegion()->get_Name());

mergeFieldNames = doc->get_MailMerge()->GetFieldNamesForRegion(u"MailMergeRegion1", 1);

ASSERT_EQ(u"Column2", mergeFieldNames[0]);
```

## See Also

* Class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words](../../../)
