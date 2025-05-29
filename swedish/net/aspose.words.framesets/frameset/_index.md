---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Framesets.Frameset för sömlös ramhantering i dokument. Förbättra dina webbsidor med effektiv ramintegration!
type: docs
weight: 3510
url: /sv/net/aspose.words.framesets/frameset/
---
## Frameset class

Representerar en bildrutesida eller en enskild bildruta på en bildrutesida.

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
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Hämtar samlingen av underramar och ramsidor. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Hämtar eller ställer in webbsidans URL eller dokumentfilnamnet som ska visas i den här ramen. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Hämtar eller anger ett värde som anger om webbsidans eller dokumentets filnamn som anges i [`FrameDefaultUrl`](./framedefaulturl/) egenskapen är en extern resurs som ramen är länkad till. |

## Anmärkningar

Om[`ChildFramesets`](./childframesets/) egenskapen innehåller objekt, den här instansen är en frames-sida, annars är det en enda frame.

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

* namnutrymme [Aspose.Words.Framesets](../../aspose.words.framesets/)
* hopsättning [Aspose.Words](../../)
