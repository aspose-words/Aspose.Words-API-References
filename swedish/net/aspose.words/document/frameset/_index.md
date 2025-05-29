---
title: Document.Frameset
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words för .NET
description: Upptäck Frameset-egenskapen för dokument. Skaffa en Frameset-instans för sömlös integration av inramade sidor. Förbättra din webbupplevelse idag!
type: docs
weight: 170
url: /sv/net/aspose.words/document/frameset/
---
## Document.Frameset property

Returnerar en`Frameset` exempel om detta dokument representerar en ramsida.

```csharp
public Frameset Frameset { get; }
```

## Anmärkningar

Om dokumentet inte är inramat har egendomen`null` värde.

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

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
