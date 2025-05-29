---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.StoryType-enum, hantera textartiklar i Word-dokument effektivt och enkelt. Förbättra din dokumenthanteringsupplevelse idag!
type: docs
weight: 6970
url: /sv/net/aspose.words/storytype/
---
## StoryType enumeration

Text i ett Word-dokument lagras i berättelser.`StoryType` identifierar en berättelse.

```csharp
public enum StoryType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Standardvärde. Det finns ingen sådan artikel i dokumentet. |
| MainText | `1` | Innehåller dokumentets huvudtext, representerad av[`Body`](../body/) . |
| Footnotes | `2` | Innehåller fotnotstext, representerad av[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Innehåller slutnoter, representerade av[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Innehåller dokumentkommentarer (annoteringar), representerade av[`Comment`](../comment/) . |
| Textbox | `5` | Innehåller form- eller textrutetext, representerad av[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Innehåller text från sidhuvudet för jämna sidor, representerat av[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Innehåller text från den primära rubriken. När rubriken är olika för udda och jämna sidor innehåller text från rubriken för udda sidor. Representeras av[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Innehåller text från sidfoten för jämna sidor, representerad av[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Innehåller text från den primära sidfoten. När sidfoten är olika för udda och jämna sidor innehåller text från sidfoten för udda sidor. Representeras av[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | Innehåller text från första sidans rubrik, representerad av[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | Innehåller text från första sidans sidfot, representerad av[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Innehåller texten för fotnotsavgränsaren. |
| FootnoteContinuationSeparator | `13` | Innehåller texten för fotnotsavgränsaren. |
| FootnoteContinuationNotice | `14` | Innehåller texten för avgränsaren för fotnotens fortsättning. |
| EndnoteSeparator | `15` | Innehåller texten för slutnotsavgränsaren. |
| EndnoteContinuationSeparator | `16` | Innehåller texten för slutnotsavgränsaren. |
| EndnoteContinuationNotice | `17` | Innehåller texten för avgränsaren för fortsättningsmeddelandet i slutnoten. |

## Exempel

Visar hur man tar bort alla former från en nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en DocumentBuilder för att infoga en form. Detta är en inbäddad form,
// som har ett förälderparagraf, som är en undernod till den första sektionens brödtext.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Vi kan ta bort alla former från underparagraferna i denna brödtext.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
