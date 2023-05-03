---
title: MailMerge.GetRegionsHierarchy
linktitle: GetRegionsHierarchy
articleTitle: GetRegionsHierarchy
second_title: Aspose.Words for .NET API Reference
description: MailMerge GetRegionsHierarchy method. Returns a full hierarchy of regions with fields available in the document in C#.
type: docs
weight: 250
url: /net/aspose.words.mailmerging/mailmerge/getregionshierarchy/
---
## MailMerge.GetRegionsHierarchy method

Returns a full hierarchy of regions (with fields) available in the document.

```csharp
public MailMergeRegionInfo GetRegionsHierarchy()
```

### Return Value

Regions' hierarchy.

## Remarks

Hierarchy is returned in the form of the [`MailMergeRegionInfo`](../../mailmergeregioninfo/) class.

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

// Get list of fields inside the first top region.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### See Also

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../mailmerge/)
* assembly [Aspose.Words](../../../)
