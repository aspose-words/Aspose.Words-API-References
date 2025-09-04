---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.MailMerging.MailMergeRegionInfo class for efficient mail merge management. Unlock seamless document automation today!
type: docs
weight: 4570
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

Assert.That(topRegions.Count, Is.EqualTo(2));
Assert.That(topRegions[0].Name, Is.EqualTo("Region1"));
Assert.That(topRegions[1].Name, Is.EqualTo("Region2"));
Assert.That(topRegions[0].Level, Is.EqualTo(1));
Assert.That(topRegions[1].Level, Is.EqualTo(1));

// Get nested region in first top region.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.That(nestedRegions.Count, Is.EqualTo(2));
Assert.That(nestedRegions[0].Name, Is.EqualTo("NestedRegion1"));
Assert.That(nestedRegions[1].Name, Is.EqualTo("NestedRegion2"));
Assert.That(nestedRegions[0].Level, Is.EqualTo(2));
Assert.That(nestedRegions[1].Level, Is.EqualTo(2));
Assert.That(nestedRegions[1].MustacheTags.Count, Is.EqualTo(0));

// Get list of fields inside the first top region.
IList<Field> fieldList = topRegions[0].Fields;

Assert.That(fieldList.Count, Is.EqualTo(4));

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.That(startFieldMergeField.FieldName, Is.EqualTo("TableStart:NestedRegion1"));

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.That(endFieldMergeField.FieldName, Is.EqualTo("TableEnd:NestedRegion1"));
```

### See Also

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../)
