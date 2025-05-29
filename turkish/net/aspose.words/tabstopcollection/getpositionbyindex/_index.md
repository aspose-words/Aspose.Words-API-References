---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: .NET için Aspose.Words
description: TabStopCollection GetPositionByIndex metodunu keşfedin ve indekse göre noktalardaki sekme durağı konumlarını kolayca bulun. Düzeninizi zahmetsizce optimize edin!
type: docs
weight: 100
url: /tr/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Belirtilen dizindeki sekme durağının konumunu (nokta cinsinden) alır.

```csharp
public double GetPositionByIndex(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Sekme duraklarının koleksiyonuna ait bir dizin. |

### Geri dönüş değeri

Sekme durağının konumu.

## Örnekler

Bir sekmenin nasıl bulunacağını, dizinine nasıl gidileceğini ve konumunun nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Koleksiyondaki ikinci sekme durağının konumunu doğrula.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Ayrıca bakınız

* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
