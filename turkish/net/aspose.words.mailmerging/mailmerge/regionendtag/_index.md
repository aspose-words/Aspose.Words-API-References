---
title: MailMerge.RegionEndTag
linktitle: RegionEndTag
articleTitle: RegionEndTag
second_title: .NET için Aspose.Words
description: Posta birleştirme bölgelerinizi verimli bir şekilde yönetmek için MailMerge RegionEndTag özelliğini keşfedin. Sorunsuz etiket entegrasyonuyla belge otomasyonunu basitleştirin.
type: docs
weight: 90
url: /tr/net/aspose.words.mailmerging/mailmerge/regionendtag/
---
## MailMerge.RegionEndTag property

Bir posta birleştirme bölgesi son etiketini alır veya ayarlar.

```csharp
public string RegionEndTag { get; set; }
```

## Örnekler

Posta birleştirme bölgelerinin nasıl oluşturulacağını, listeleneceğini ve okunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELD'lerin içine giren "TableStart" ve "TableEnd" etiketleri,
// birleştirme bölgelerinin başlangıç ve bitişlerini belirten dizeleri belirtir.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// "MailMergeRegion1" adlı bir posta birleştirme bölgesini başlatmak ve bitirmek için bu etiketleri kullanın.
// iki sütuna ait MERGEFIELD'leri içerecektir.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Bu koleksiyonlara bakarak birleştirme bölgelerini ve bu bölgelere ait sütunları takip edebiliriz.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Mevcut bölgenin içine aynı adı taşıyan bir bölge ekle, bu onu bir üst bölge yapacaktır.
// Artık "Column2" alanı yeni bir bölgenin içerisinde olacak.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// "GetRegionsByName" metodunu kullanarak yinelenen bölgelerin adını ararsak,
// koleksiyondaki tüm bu bölgeleri döndürecektir.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// İkinci bölgenin artık bir üst bölgeye sahip olduğunu kontrol edin.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
