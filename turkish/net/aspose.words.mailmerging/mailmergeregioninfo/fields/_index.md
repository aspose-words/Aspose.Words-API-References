---
title: MailMergeRegionInfo.Fields
linktitle: Fields
articleTitle: Fields
second_title: Aspose.Words for .NET
description: MailMergeRegionInfo Fields mülk. Alt alanların listesini döndürür C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.mailmerging/mailmergeregioninfo/fields/
---
## MailMergeRegionInfo.Fields property

Alt alanların listesini döndürür.

```csharp
public IList<Field> Fields { get; }
```

## Örnekler

Adres-mektup birleştirme bölgelerinin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Belgede bulunan MERGEFIELD'leri içeren birleştirme bölgelerinin tam hiyerarşisini döndürür.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Belgedeki en önemli bölgeleri alın.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// İlk üst bölgedeki iç içe bölgeyi al.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);

// İlk üst bölgedeki alanların listesini alın.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [MailMergeRegionInfo](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
