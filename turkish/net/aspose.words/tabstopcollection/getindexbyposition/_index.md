---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words for .NET
description: TabStopCollection GetIndexByPosition yöntem. Nokta cinsinden belirtilen konuma sahip bir sekme durağının dizinini alır C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Nokta cinsinden belirtilen konuma sahip bir sekme durağının dizinini alır.

```csharp
public int GetIndexByPosition(double position)
```

## Örnekler

Orada bir sekme durağının bulunup bulunmadığını görmek ve dizinini almak için bir konumun nasıl aranacağını gösterir.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// 30 mm'lik bir konuma bir sekme durağı ekleyin.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// "GetIndexByPosition" tarafından döndürülen "0" sonucu, bir sekme durağının olduğunu doğrular
// 30mm'de bu koleksiyonda var ve 0 dizininde.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// "GetIndexByPosition" tarafından döndürülen "-1" şunu doğrular:
// bu koleksiyonda 60mm konumlu sekme durağı yoktur.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Ayrıca bakınız

* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
