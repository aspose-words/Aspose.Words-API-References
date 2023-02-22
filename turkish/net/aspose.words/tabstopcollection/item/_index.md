---
title: TabStopCollection.Item
second_title: Aspose.Words for .NET API Referansı
description: TabStopCollection mülk. Verilen dizinde bir sekme durağı alır.
type: docs
weight: 20
url: /tr/net/aspose.words/tabstopcollection/item/
---
## TabStopCollection indexer (1 of 2)

Verilen dizinde bir sekme durağı alır.

```csharp
public TabStop this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Sekme duraklarının koleksiyonuna bir dizin. |

### Örnekler

Bir belgenin sekme durakları koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 nokta, Microsoft Word sekmesi durdurma cetvelinde bir "inç"tir.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Her "sekme" karakteri, oluşturucunun imlecini bir sonraki sekme durağının konumuna götürür.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Her paragraf, değerlerini belge oluşturucunun sekme durağı koleksiyonundan kopyalayan sekme durağı koleksiyonunu alır.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Bir sekme durağı koleksiyonu bizi belirli konumlardan önce ve sonra TabStop'lara yönlendirebilir.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Varsayılan sekme davranışına geri dönmek için bir paragrafın sekme durağı koleksiyonunu temizleyebiliriz.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Ayrıca bakınız

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../tabstopcollection/)
* toplantı [Aspose.Words](../../../)

---

## TabStopCollection indexer (2 of 2)

Belirtilen konumda bir sekme durağı alır.

```csharp
public TabStop this[double position] { get; }
```

| Parametre | Tanım |
| --- | --- |
| position | Sekme durağının konumu (nokta olarak). |

### Notlar

Belirtilen konumda sekme durağı bulunmazsa null döndürür.

### Örnekler

Bir belgenin sekme durakları koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 nokta, Microsoft Word sekmesi durdurma cetvelinde bir "inç"tir.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Her "sekme" karakteri, oluşturucunun imlecini bir sonraki sekme durağının konumuna götürür.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Her paragraf, değerlerini belge oluşturucunun sekme durağı koleksiyonundan kopyalayan sekme durağı koleksiyonunu alır.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Bir sekme durağı koleksiyonu bizi belirli konumlardan önce ve sonra TabStop'lara yönlendirebilir.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Varsayılan sekme davranışına geri dönmek için bir paragrafın sekme durağı koleksiyonunu temizleyebiliriz.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Ayrıca bakınız

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../tabstopcollection/)
* toplantı [Aspose.Words](../../../)


