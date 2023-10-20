---
title: MailMerge.GetRegionsHierarchy
linktitle: GetRegionsHierarchy
articleTitle: GetRegionsHierarchy
second_title: Aspose.Words för .NET
description: MailMerge GetRegionsHierarchy metod. Returnerar en fullständig hierarki av regioner med fält tillgängliga i dokumentet i C#.
type: docs
weight: 250
url: /sv/net/aspose.words.mailmerging/mailmerge/getregionshierarchy/
---
## MailMerge.GetRegionsHierarchy method

Returnerar en fullständig hierarki av regioner (med fält) tillgängliga i dokumentet.

```csharp
public MailMergeRegionInfo GetRegionsHierarchy()
```

### Returvärde

Regionernas hierarki.

## Anmärkningar

Hierarki returneras i form av[`MailMergeRegionInfo`](../../mailmergeregioninfo/) klass.

## Exempel

Visar hur man verifierar kopplingsregioner.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Returnerar en fullständig hierarki av sammanslagningsregioner som innehåller MERGEFIELDs tillgängliga i dokumentet.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Få toppregioner i dokumentet.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Få kapslad region i första toppregionen.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);

// Hämta lista över fält inom den första toppregionen.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Se även

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
