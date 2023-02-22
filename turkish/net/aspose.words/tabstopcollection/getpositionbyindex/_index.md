---
title: TabStopCollection.GetPositionByIndex
second_title: Aspose.Words for .NET API Referansı
description: TabStopCollection yöntem. Belirtilen dizindeki sekme durağının konumunu nokta olarak alır.
type: docs
weight: 100
url: /tr/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Belirtilen dizindeki sekme durağının konumunu (nokta olarak) alır.

```csharp
public double GetPositionByIndex(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Sekme duraklarının koleksiyonuna bir dizin. |

### Geri dönüş değeri

Sekme durağının konumu.

### Örnekler

Bir sekmenin nasıl bulunacağını, dizinine nasıl bakılacağını ve konumunun nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Koleksiyondaki ikinci sekme durağının konumunu doğrulayın.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Ayrıca bakınız

* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../tabstopcollection/)
* toplantı [Aspose.Words](../../../)


