---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.MailMerging.MailMergeRegionInfo class for efficient mail merge management. Unlock seamless document automation today!
type: docs
weight: 4550
url: /net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Contains information about a mail merge region.

To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) documentation article.

```csharp
public class MailMergeRegionInfo
```

## Properties

| Name | Description |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Returns an end field for the region. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Returns an end "mustache" tag for the region. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Returns a list of child fields. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Returns the nesting level for the region. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Returns a list of child "mustache" tags. |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Returns the name of region. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Returns parent region info (null for top-level region). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Returns a list of child regions. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Returns a start field for the region. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Returns a start "mustache" tag for the region. |

## Examples

Shows how to verify mail merge regions.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Returns a full hierarchy of merge regions that contain MERGEFIELDs available in the document.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Get top regions in the document.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Get nested region in first top region.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// Get list of fields inside the first top region.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### See Also

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../)
