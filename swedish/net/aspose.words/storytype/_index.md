---
title: Enum StoryType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.StoryType uppräkning. Text i ett Worddokument lagras i berättelser.StoryType identifierar en berättelse.
type: docs
weight: 6120
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
| None | `0` | Standardvärde. Det finns ingen sådan berättelse i dokumentet. |
| MainText | `1` | Innehåller dokumentets huvudtext, representerad av[`Body`](../body/) . |
| Footnotes | `2` | Innehåller fotnotstext, representerad av[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Innehåller slutnottext, representerad av[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Innehåller dokumentkommentarer (kommentarer), representerade av[`Comment`](../comment/) . |
| Textbox | `5` | Innehåller form eller textruta, representerad av[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Innehåller text i rubriken för jämna sidor, representerad av[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Innehåller text från den primära rubriken. När rubriken är olika för udda och jämna sidor, innehåller texten i rubriken för udda sidor. Representerad av[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Innehåller text i sidfoten på jämna sidor, representerad av[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Innehåller text från den primära sidfoten. När sidfoten är olika för udda och jämna sidor, innehåller texten i sidfoten på udda sidor. Representerad av[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | Innehåller text från första sidhuvudet, representerat av[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | Innehåller text från sidfoten på första sidan, representerad av[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Innehåller texten i fotnotsavgränsaren, representerad avFootnoteSeparator . |
| FootnoteContinuationSeparator | `13` | Innehåller texten i fotnotsfortsättningsavgränsaren, representerad avFootnoteSeparator . |
| FootnoteContinuationNotice | `14` | Innehåller texten i fotnotens fortsättningsavgränsare, representerad avFootnoteSeparator . |
| EndnoteSeparator | `15` | Innehåller texten för slutnotavgränsaren, representerad avFootnoteSeparator . |
| EndnoteContinuationSeparator | `16` | Innehåller texten i slutnotens fortsättningsavgränsare, representerad avFootnoteSeparator . |
| EndnoteContinuationNotice | `17` | Innehåller texten i slutnotens fortsättningsmeddelandeavgränsare, representerad avFootnoteSeparator . |

### Exempel

Visar hur man tar bort alla former från en nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en DocumentBuilder för att infoga en form. Detta är en inline-form,
// som har ett överordnat stycke, som är en underordnad nod till det första avsnittets Kropp.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Vi kan ta bort alla former från underordnade stycken i denna Body.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


