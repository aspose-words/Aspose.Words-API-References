---
title: RemoveByIndex
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen dizindeki bir sekme durağını koleksiyondan kaldırır.
type: docs
weight: 110
url: /tr/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Belirtilen dizindeki bir sekme durağını koleksiyondan kaldırır.

```csharp
public void RemoveByIndex(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Sekme duraklarının koleksiyonuna bir dizin. |

### Örnekler

Dizine göre bir belgede bir sekme durağının nasıl seçileceğini ve kaldırılacağını gösterir.

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

* class [TabStopCollection](../../tabstopcollection)
* ad alanı [Aspose.Words](../../tabstopcollection)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
