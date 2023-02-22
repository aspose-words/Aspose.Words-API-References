---
title: Document.Frameset
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Returnerar enFramesetinstans om detta dokument representerar en ramsida.
type: docs
weight: 160
url: /sv/net/aspose.words/document/frameset/
---
## Document.Frameset property

Returnerar en`Frameset`instans om detta dokument representerar en ramsida.

```csharp
public Frameset Frameset { get; }
```

### Anmärkningar

Om dokumentet inte är inramat har egenskapen **null** värde.

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

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


