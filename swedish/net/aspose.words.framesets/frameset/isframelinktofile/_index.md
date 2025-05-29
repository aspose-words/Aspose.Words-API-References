---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen Frameset IsFrameLinkToFile förbättrar din webbdesign genom att länka externa resurser sömlöst. Optimera dina ramar för bättre prestanda!
type: docs
weight: 40
url: /sv/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Hämtar eller anger ett värde som anger om webbsidans eller dokumentets filnamn som anges i [`FrameDefaultUrl`](../framedefaulturl/) egenskapen är en extern resurs som ramen är länkad till.

```csharp
public bool IsFrameLinkToFile { get; set; }
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

* class [Frameset](../)
* namnutrymme [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* hopsättning [Aspose.Words](../../../)
