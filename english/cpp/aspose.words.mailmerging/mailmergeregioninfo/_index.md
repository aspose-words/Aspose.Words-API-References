---
title: Aspose::Words::MailMerging::MailMergeRegionInfo class
linktitle: MailMergeRegionInfo
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::MailMergeRegionInfo class. Contains information about a mail merge region. To learn more, visit the  documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class


Contains information about a mail merge region. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) documentation article.

```cpp
class MailMergeRegionInfo : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_EndField](./get_endfield/)() const | Returns an end field for the region. |
| [get_Fields](./get_fields/)() const | Returns a list of child fields. |
| [get_Level](./get_level/)() const | Returns the nesting level for the region. |
| [get_Name](./get_name/)() const | Returns the name of region. |
| [get_ParentRegion](./get_parentregion/)() const | Returns parent region info (null for top-level region). |
| [get_Regions](./get_regions/)() const | Returns a list of child regions. |
| [get_StartField](./get_startfield/)() const | Returns a start field for the region. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
