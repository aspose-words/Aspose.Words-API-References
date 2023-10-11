---
title: Class MailMergeRegionInfo
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.MailMerging.MailMergeRegionInfo sınıf. Adresmektup birleştirme bölgesi hakkında bilgi içerir.
type: docs
weight: 3860
url: /tr/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Adres-mektup birleştirme bölgesi hakkında bilgi içerir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Adres Mektup Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokümantasyon makalesi.

```csharp
public class MailMergeRegionInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Bölge için bir bitiş alanı döndürür. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Bölge için bir bitiş "bıyık" etiketi döndürür. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Alt alanların listesini döndürür. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Bölgenin iç içe geçme düzeyini döndürür. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Alt "bıyık" etiketlerinin listesini döndürür. |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Bölgenin adını döndürür. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Üst bölge bilgisini döndürür (üst düzey bölge için boş). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Alt bölgelerin listesini döndürür. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Bölge için bir başlangıç alanı döndürür. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Bölge için bir başlangıç "bıyık" etiketi döndürür. |

### Örnekler

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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)


