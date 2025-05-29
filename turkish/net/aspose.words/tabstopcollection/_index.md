---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: .NET için Aspose.Words
description: Aspose.Words.TabStopCollection'ı keşfedin. Paragraflar ve stiller için özel sekme duraklarını kolayca yönetin, belge biçimlendirmenizi hassasiyetle geliştirin.
type: docs
weight: 7060
url: /tr/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Bir koleksiyon[`TabStop`](../tabstop/) bir paragraf veya stil için özel sekmeleri temsil eden nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Koleksiyondaki sekme duraklarının sayısını alır. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Belirtilen dizinde bir sekme durağı alır. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Koleksiyonda bir sekme durağı ekler veya değiştirir. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Koleksiyonda bir sekme durağı ekler veya değiştirir. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Belirtilen konumun sağında ilk sekme durağını alır. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Belirtilen konumun solunda ilk sekme durağını alır. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Tüm sekme durağı konumlarını siler. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Belirtilenin geçerli olup olmadığını belirler`TabStopCollection` mevcut değere eşittir`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Bu tür için bir karma işlevi görevi görür. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Belirtilen noktadaki bir sekme durağının dizinini alır. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Belirtilen dizindeki sekme durağının konumunu (nokta cinsinden) alır. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Koleksiyondan belirtilen dizindeki bir sekme durağını kaldırır. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Koleksiyondan belirtilen konumdaki bir sekme durağını kaldırır. |

## Notlar

Microsoft Word belgelerinde, bir sekme durağı paragraph stilinin özelliklerinde veya doğrudan bir paragrafın özelliklerinde tanımlanabilir. Bir stil başka bir style. temel alınarak oluşturulabilir. Bu nedenle, belirli bir nesne için sekme duraklarının tam kümesi, doğrudan bu nesne üzerinde tanımlanan sekme durakları ve üst stillerden devralınan sekme duraklarının birleşimidir.

Aspose.Words'de bir`TabStopCollection` Bir paragraf veya stil için, yalnızca bu paragraf veya stil için doğrudan tanımlanmış özel sekme duraklarını içerir. Koleksiyon, üst stillerde veya varsayılan sekme duraklarında tanımlanmış sekme duraklarını içermez.

## Örnekler

Bir belgenin sekme durakları koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 punto Microsoft Word sekme durdurma cetvelinde bir "inç"tir.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Her "sekme" karakteri, oluşturucunun imlecini bir sonraki sekme durağının konumuna götürür.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Her paragraf, değerlerini belge oluşturucunun sekme durağı koleksiyonundan kopyalayan bir sekme durağı koleksiyonu alır.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Bir tab stop koleksiyonu bize belirli pozisyonlardan önce ve sonra bulunan TabStop'ları gösterebilir.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Varsayılan sekme davranışına geri dönmek için bir paragrafın sekme durdurma koleksiyonunu temizleyebiliriz.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Ayrıca bakınız

* class [InternableComplexAttr](../internablecomplexattr/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
