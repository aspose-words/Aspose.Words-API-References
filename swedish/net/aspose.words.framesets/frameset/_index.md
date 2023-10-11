---
title: Class Frameset
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Framesets.Frameset klass. Representerar en ramsida eller en enda ram på en ramsida.
type: docs
weight: 3080
url: /sv/net/aspose.words.framesets/frameset/
---
## Frameset class

Representerar en ramsida eller en enda ram på en ramsida.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class Frameset
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Frameset](frameset/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Får samlingen av underordnade ramar och ramsidor. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Hämtar eller ställer in webbsidans URL eller dokumentfilnamnet som ska visas i denna ram. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Hämtar eller ställer in ett värde som anger om webbsidan eller dokumentfilnamnet som anges i [`FrameDefaultUrl`](./framedefaulturl/) egenskapen är en extern resurs som ramen är länkad till. |

### Anmärkningar

Om[`ChildFramesets`](./childframesets/) egenskapen innehåller objekt, den här instansen är en ramsida, annars är den en enda ram.

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

* namnutrymme [Aspose.Words.Framesets](../../aspose.words.framesets/)
* hopsättning [Aspose.Words](../../)


