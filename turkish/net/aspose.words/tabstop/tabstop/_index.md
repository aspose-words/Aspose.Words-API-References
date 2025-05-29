---
title: TabStop
linktitle: TabStop
articleTitle: TabStop
second_title: .NET için Aspose.Words
description: TabStop oluşturucusunu keşfedin, projelerinizde gelişmiş işlevsellik için örnekleri zahmetsizce oluşturun ve özelleştirin. Kodlama verimliliğinizi bugün artırın!
type: docs
weight: 10
url: /tr/net/aspose.words/tabstop/tabstop/
---
## TabStop(*double*) {#constructor}

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public TabStop(double position)
```

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

* class [TabStop](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## TabStop(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#constructor_1}

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public TabStop(double position, TabAlignment alignment, TabLeader leader)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| position | Double | Sekme durağının nokta cinsinden konumu. |
| alignment | TabAlignment | A[`TabAlignment`](../../tabalignment/) that değeri bu sekme durağında metnin hizalanmasını belirtir. |
| leader | TabLeader | A[`TabLeader`](../../tableader/) sekme karakterinin altında görüntülenen lider çizgisinin türünü belirten değer . |

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

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
