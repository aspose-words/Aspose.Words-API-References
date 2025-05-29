---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: .NET için Aspose.Words
description: Verimli posta birleştirme yönetimi için Aspose.Words.MailMerging.MailMergeRegionInfo sınıfını keşfedin. Bugün kusursuz belge otomasyonunun kilidini açın!
type: docs
weight: 4550
url: /tr/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Bir posta birleştirme bölgesi hakkında bilgi içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

```csharp
public class MailMergeRegionInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Bölge için bir bitiş alanı döndürür. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Bölge için bir "bıyık" etiketi sonu döndürür. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Alt alanların bir listesini döndürür. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Bölge için yuvalama düzeyini döndürür. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Alt "bıyık" etiketlerinin bir listesini döndürür. |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Bölgenin adını döndürür. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Üst bölge bilgilerini döndürür (en üst düzey bölge için boş). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Alt bölgelerin bir listesini döndürür. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Bölge için bir başlangıç alanı döndürür. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Bölge için bir başlangıç "bıyık" etiketi döndürür. |

## Örnekler

Posta birleştirme bölgelerinin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Belgede bulunan MERGEFIELD'leri içeren birleştirme bölgelerinin tam hiyerarşisini döndürür.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Belgedeki en iyi bölgeleri al.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// İlk üst bölgeye iç içe geçmiş bölge alın.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// İlk üst bölgedeki alanların listesini al.
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
