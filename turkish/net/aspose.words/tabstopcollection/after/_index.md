---
title: TabStopCollection.After
linktitle: After
articleTitle: After
second_title: .NET için Aspose.Words
description: Sorunsuz gezinme için belirtilen konumunuzun sağındaki ilk sekme durağını verimli bir şekilde almak üzere TabStopCollection After yöntemini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words/tabstopcollection/after/
---
## TabStopCollection.After method

Belirtilen konumun sağında ilk sekme durağını alır.

```csharp
public TabStop After(double position)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| position | Double | Referans pozisyonu (nokta cinsinden). |

### Geri dönüş değeri

Bir sekme durdurma nesnesi veya`hükümsüz` uygun bir sekme durağı bulunamadıysa.

## Notlar

Sekme duraklarını atla[`Alignment`](../../tabstop/alignment/) ayarlandıBar.

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

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
