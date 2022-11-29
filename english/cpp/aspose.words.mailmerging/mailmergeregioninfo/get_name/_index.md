---
title: get_Name
second_title: Aspose.Words for C++ API Reference
description: Returns the name of region.
type: docs
weight: 40
url: /cpp/aspose.words.mailmerging/mailmergeregioninfo/get_name/
---
## MailMergeRegionInfo::get_Name method


Returns the name of region.

```cpp
System::String Aspose::Words::MailMerging::MailMergeRegionInfo::get_Name() const
```


## Examples



Shows how to verify mail merge regions. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Mail merge regions.docx");

// Returns a full hierarchy of merge regions that contain MERGEFIELDs available in the document.
SharedPtr<MailMergeRegionInfo> regionInfo = doc->get_MailMerge()->GetRegionsHierarchy();

// Get top regions in the document.
SharedPtr<System::Collections::Generic::IList<SharedPtr<MailMergeRegionInfo>>> topRegions = regionInfo->get_Regions();

ASSERT_EQ(2, topRegions->get_Count());
ASSERT_EQ(u"Region1", topRegions->idx_get(0)->get_Name());
ASSERT_EQ(u"Region2", topRegions->idx_get(1)->get_Name());
ASSERT_EQ(1, topRegions->idx_get(0)->get_Level());
ASSERT_EQ(1, topRegions->idx_get(1)->get_Level());

// Get nested region in first top region.
SharedPtr<System::Collections::Generic::IList<SharedPtr<MailMergeRegionInfo>>> nestedRegions = topRegions->idx_get(0)->get_Regions();

ASSERT_EQ(2, nestedRegions->get_Count());
ASSERT_EQ(u"NestedRegion1", nestedRegions->idx_get(0)->get_Name());
ASSERT_EQ(u"NestedRegion2", nestedRegions->idx_get(1)->get_Name());
ASSERT_EQ(2, nestedRegions->idx_get(0)->get_Level());
ASSERT_EQ(2, nestedRegions->idx_get(1)->get_Level());

// Get list of fields inside the first top region.
SharedPtr<System::Collections::Generic::IList<SharedPtr<Field>>> fieldList = topRegions->idx_get(0)->get_Fields();

ASSERT_EQ(4, fieldList->get_Count());

SharedPtr<FieldMergeField> startFieldMergeField = nestedRegions->idx_get(0)->get_StartField();

ASSERT_EQ(u"TableStart:NestedRegion1", startFieldMergeField->get_FieldName());

SharedPtr<FieldMergeField> endFieldMergeField = nestedRegions->idx_get(0)->get_EndField();

ASSERT_EQ(u"TableEnd:NestedRegion1", endFieldMergeField->get_FieldName());
```

## See Also

* Class [MailMergeRegionInfo](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words](../../../)
