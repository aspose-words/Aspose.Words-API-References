---
title: MailMerge.GetRegionsHierarchy
linktitle: GetRegionsHierarchy
articleTitle: GetRegionsHierarchy
second_title: Aspose.Words for .NET
description: MailMerge GetRegionsHierarchy yöntem. Belgede bulunan bölgelerin alanlarla birlikte tam hiyerarşisini döndürür C#'da.
type: docs
weight: 250
url: /tr/net/aspose.words.mailmerging/mailmerge/getregionshierarchy/
---
## MailMerge.GetRegionsHierarchy method

Belgede bulunan bölgelerin (alanlarla birlikte) tam hiyerarşisini döndürür.

```csharp
public MailMergeRegionInfo GetRegionsHierarchy()
```

### Geri dönüş değeri

Bölgelerin hiyerarşisi.

## Notlar

Hiyerarşi şu şekilde döndürülür:[`MailMergeRegionInfo`](../../mailmergeregioninfo/) sınıf.

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

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
