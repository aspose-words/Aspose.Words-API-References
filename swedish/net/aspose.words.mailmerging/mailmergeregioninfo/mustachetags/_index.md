---
title: MailMergeRegionInfo.MustacheTags
linktitle: MustacheTags
articleTitle: MustacheTags
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MailMergeRegionInfo MustacheTags, som effektivt returnerar en omfattande lista med underordnade mustaschtaggar för sömlös dataintegration.
type: docs
weight: 50
url: /sv/net/aspose.words.mailmerging/mailmergeregioninfo/mustachetags/
---
## MailMergeRegionInfo.MustacheTags property

Returnerar en lista med underordnade "mustasch"-taggar.

```csharp
public IList<MustacheTag> MustacheTags { get; }
```

## Exempel

Visar hur man verifierar regioner för dokumentkoppling.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Returnerar en fullständig hierarki av sammanslagningsregioner som innehåller MERGEFIELDS tillgängliga i dokumentet.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Hämta de översta regionerna i dokumentet.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Hämta kapslad region i den första översta regionen.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// Hämta lista över fält inom den första översta regionen.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Se även

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
