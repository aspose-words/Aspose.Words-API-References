---
title: MailMerge.RegionStartTag
linktitle: RegionStartTag
articleTitle: RegionStartTag
second_title: Aspose.Words for .NET
description: MailMerge RegionStartTag mülk. Adresmektup birleştirme bölgesi başlangıç etiketini alır veya ayarlar C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.mailmerging/mailmerge/regionstarttag/
---
## MailMerge.RegionStartTag property

Adres-mektup birleştirme bölgesi başlangıç etiketini alır veya ayarlar.

```csharp
public string RegionStartTag { get; set; }
```

## Örnekler

Adres-mektup birleştirme bölgelerinin nasıl oluşturulacağını, listeleneceğini ve okunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELD'lerin içine giren "TableStart" ve "TableEnd" etiketleri,
// adres-mektup birleştirme bölgelerinin başlangıç ve bitişlerini belirten dizeleri belirtir.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// "MailMergeRegion1" adlı adres-mektup birleştirme bölgesini başlatmak ve bitirmek için bu etiketleri kullanın,
// iki sütun için MERGEFIELD'leri içerecektir.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Bu koleksiyonlara bakarak birleştirme bölgelerini ve sütunlarını takip edebiliriz.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Mevcut bölgenin içine aynı isimde bir bölge ekleyin, bu onu ebeveyn yapacak.
// Artık yeni bir bölgenin içinde bir "Sütun2" alanı olacak.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// "GetRegionsByName" yöntemini kullanarak yinelenen bölgelerin adını ararsak,
// bu tür bölgelerin tümünü bir koleksiyonda döndürecektir.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// İkinci bölgenin artık bir ana bölgeye sahip olup olmadığını kontrol edin.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
