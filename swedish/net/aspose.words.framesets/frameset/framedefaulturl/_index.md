---
title: Frameset.FrameDefaultUrl
second_title: Aspose.Words för .NET API Referens
description: Frameset fast egendom. Hämtar eller ställer in webbsidans URL eller dokumentfilnamnet som ska visas i denna ram.
type: docs
weight: 30
url: /sv/net/aspose.words.framesets/frameset/framedefaulturl/
---
## Frameset.FrameDefaultUrl property

Hämtar eller ställer in webbsidans URL eller dokumentfilnamnet som ska visas i denna ram.

```csharp
public string FrameDefaultUrl { get; set; }
```

### Exempel

Visar hur man kommer åt ramar på sidan.

```csharp
// Dokument innehåller flera ramar med länkar till andra dokument.
Document doc = new Document(MyDir + "Frameset.docx");

// Vi kan kontrollera standard URL (en webbadress eller lokalt dokument) eller om ramen är en extern resurs.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Ändra egenskaper för en av våra ramar.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Se även

* class [Frameset](../)
* namnutrymme [Aspose.Words.Framesets](../../frameset/)
* hopsättning [Aspose.Words](../../../)


