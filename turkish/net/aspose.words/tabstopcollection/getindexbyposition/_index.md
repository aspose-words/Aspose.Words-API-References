---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: .NET için Aspose.Words
description: Herhangi bir belirtilen nokta pozisyonundaki bir sekme durağının dizinini kolayca bulmak için TabStopCollection GetIndexByPosition metodunu keşfedin. Hassas düzen kontrolü için mükemmel!
type: docs
weight: 90
url: /tr/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Belirtilen noktadaki bir sekme durağının dizinini alır.

```csharp
public int GetIndexByPosition(double position)
```

## Örnekler

Bir sekme durağının orada olup olmadığını görmek ve indeksini almak için bir konumun nasıl aranacağını gösterir.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// 30 mm'lik bir konuma sekme durağı ekleyin.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// "GetIndexByPosition" tarafından döndürülen "0" sonucu, bir sekme durağının
// bu koleksiyonda 30mm mevcuttur ve indeksi 0'dır.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// "GetIndexByPosition" tarafından döndürülen "-1" bunu doğrular
// Bu koleksiyonda 60mm pozisyonunda bir sekme durağı bulunmamaktadır.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Ayrıca bakınız

* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
