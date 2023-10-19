---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.TabStopCollection sınıf. Bir koleksiyonTabStop bir paragraf veya stil için özel sekmeleri temsil eden nesneler C#'da.
type: docs
weight: 6210
url: /tr/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Bir koleksiyon[`TabStop`](../tabstop/) bir paragraf veya stil için özel sekmeleri temsil eden nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokümantasyon makalesi.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Koleksiyondaki sekme duraklarının sayısını alır. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Verilen dizinde bir sekme durağı alır. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Koleksiyona bir sekme durağı ekler veya değiştirir. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Koleksiyona bir sekme durağı ekler veya değiştirir. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Belirtilen konumun sağındaki ilk sekme durağını alır. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Belirtilen konumun solundaki ilk sekme durağını alır. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Tüm sekme durağı konumlarını siler. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Belirtilenin olup olmadığını belirler`TabStopCollection` şimdiki değere eşittir`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Bu tür için karma işlevi görevi görür. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Nokta cinsinden belirtilen konuma sahip bir sekme durağının dizinini alır. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Belirtilen dizindeki sekme durağının konumunu (nokta cinsinden) alır. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Koleksiyondan belirtilen dizindeki sekme durağını kaldırır. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Koleksiyondan belirtilen konumdaki sekme durağını kaldırır. |

## Notlar

Microsoft Word belgelerinde, bir paragraf stilinin özelliklerinde veya doğrudan bir paragrafın özelliklerinde bir sekme durağı tanımlanabilir. Bir stil başka bir stile dayalı olabilir. Bu nedenle, belirli bir nesne için sekme duraklarının tamamı, doğrudan bu nesne üzerinde tanımlanan sekme durakları ile üst stillerden miras alınan sekme duraklarının birleşimidir.

Aspose.Words'te bir`TabStopCollection`bir paragraf veya stil için, yalnızca bu paragraf veya stil için doğrudan tanımlanan özel sekme duraklarını içerir. Koleksiyon, ana stillerde veya varsayılan sekme duraklarında tanımlanan sekme duraklarını içermez.

## Örnekler

Bir belgenin sekme durakları koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 nokta, Microsoft Word sekme durağı cetvelinde bir "inç"tir.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Her "sekme" karakteri, oluşturucunun imlecini bir sonraki sekme durağının konumuna götürür.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Her paragraf, değerlerini belge oluşturucunun sekme durağı koleksiyonundan kopyalayan kendi sekme durağı koleksiyonunu alır.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Bir sekme durağı koleksiyonu bizi belirli konumlardan önceki ve sonraki TabStop'lara yönlendirebilir.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Varsayılan sekme davranışına geri dönmek için paragrafın sekme durağı koleksiyonunu temizleyebiliriz.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Ayrıca bakınız

* class [InternableComplexAttr](../internablecomplexattr/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
