---
title: MailMerge.GetFieldNamesForRegion
linktitle: GetFieldNamesForRegion
articleTitle: GetFieldNamesForRegion
second_title: .NET için Aspose.Words
description: Belirtilen bölgenizdeki bir posta birleştirme alan adı koleksiyonuna zahmetsizce erişmek için MailMerge GetFieldNamesForRegion yöntemini keşfedin. İş akışınızı kolaylaştırın!
type: docs
weight: 230
url: /tr/net/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## GetFieldNamesForRegion(*string*) {#getfieldnamesforregion}

Bölgede kullanılabilen posta birleştirme alanı adlarının bir koleksiyonunu döndürür.

```csharp
public string[] GetFieldNamesForRegion(string regionName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| regionName | String | Bölge adı (büyük/küçük harfe duyarlı değil). |

## Notlar

İsteğe bağlı önek dahil olmak üzere tam birleştirme alanı adlarını döndürür. Yinelenen alan adlarını ortadan kaldırmaz.

Belge aynı adı taşıyan birden fazla bölge içeriyorsa ilk bölge işlenir.

Her çağrıda yeni bir dize dizisi oluşturulur.

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

---

## GetFieldNamesForRegion(*string, int*) {#getfieldnamesforregion_1}

Bölgede kullanılabilen posta birleştirme alanı adlarının bir koleksiyonunu döndürür.

```csharp
public string[] GetFieldNamesForRegion(string regionName, int regionIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| regionName | String | Bölge adı (büyük/küçük harfe duyarlı değil). |
| regionIndex | Int32 | Bölge endeksi (sıfırdan itibaren). |

## Notlar

İsteğe bağlı önek dahil olmak üzere tam birleştirme alanı adlarını döndürür. Yinelenen alan adlarını ortadan kaldırmaz.

Belge aynı adı taşıyan birden fazla bölge içeriyorsa N'inci bölge (sıfırdan başlayan) işlenir.

Her çağrıda yeni bir dize dizisi oluşturulur.

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
