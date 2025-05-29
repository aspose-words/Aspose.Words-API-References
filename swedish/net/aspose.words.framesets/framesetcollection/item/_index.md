---
title: FramesetCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få åtkomst till specifika ramar med FramesetCollection. Hämta enkelt ramsidor via index för effektiv webbnavigering och förbättrad användarupplevelse.
type: docs
weight: 30
url: /sv/net/aspose.words.framesets/framesetcollection/item/
---
## FramesetCollection indexer

Hämtar en eller flera ramar vid det angivna indexet.

```csharp
public Frameset this[int index] { get; }
```

## Exempel

Visar hur man kommer åt ramar på sidan.

```csharp
// Dokumentet innehåller flera ramar med länkar till andra dokument.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// Vi kan kontrollera standard-URL:en (en webbsides-URL eller ett lokalt dokument) eller om ramen är en extern resurs.
Assert.AreEqual("https://filexempel-com.github.io/uploads/2017/02/filexempel_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Ändra egenskaper för en av våra ramar.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Exempel/Data/Absolut%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Se även

* class [Frameset](../../frameset/)
* class [FramesetCollection](../)
* namnutrymme [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* hopsättning [Aspose.Words](../../../)
