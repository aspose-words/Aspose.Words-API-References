---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words FramesetCollection-klassen, din lösning för att enkelt hantera flera Frameset-instanser i dokumentbehandling.
type: docs
weight: 3520
url: /sv/net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

Representerar en samling instanser av[`Frameset`](../frameset/) klass.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | Hämtar antalet ramar eller ramsidor som finns i samlingen. |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | Hämtar en eller flera ramar vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | Returnerar en uppräknare som itererar genom samlingen. |

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

* class [Frameset](../frameset/)
* namnutrymme [Aspose.Words.Framesets](../../aspose.words.framesets/)
* hopsättning [Aspose.Words](../../)
