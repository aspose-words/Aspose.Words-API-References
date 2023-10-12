---
title: TabStopCollection.RemoveByIndex
second_title: Aspose.Words for .NET API Referansı
description: TabStopCollection yöntem. Koleksiyondan belirtilen dizindeki sekme durağını kaldırır.
type: docs
weight: 110
url: /tr/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Koleksiyondan belirtilen dizindeki sekme durağını kaldırır.

```csharp
public void RemoveByIndex(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Sekme duraklarının koleksiyonuna ilişkin bir dizin. |

### Örnekler

Bir belgedeki sekme durağının dizinine göre nasıl seçileceğini ve kaldırılacağını gösterir.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// İlk sekme durağını kaldırın.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Ayrıca bakınız

* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../tabstopcollection/)
* toplantı [Aspose.Words](../../../)


