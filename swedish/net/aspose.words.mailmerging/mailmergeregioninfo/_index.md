---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.MailMerging.MailMergeRegionInfo för effektiv hantering av dokumentkopplingar. Lås upp sömlös dokumentautomation idag!
type: docs
weight: 4550
url: /sv/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Innehåller information om ett område för dokumentkoppling.

För att lära dig mer, besök[Koppla dokument och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class MailMergeRegionInfo
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Returnerar ett slutfält för regionen. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Returnerar en avslutande "mustache"-tagg för regionen. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Returnerar en lista med underordnade fält. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Returnerar kapslingsnivån för regionen. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Returnerar en lista med underordnade "mustasch"-taggar. |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Returnerar namnet på regionen. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Returnerar information om överordnad region (null för region på toppnivå). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Returnerar en lista över underordnade regioner. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Returnerar ett startfält för regionen. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Returnerar en starttagg med namnet "mustasch" för regionen. |

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

* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)
