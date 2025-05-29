---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med DocumentBuilder InsertParagraph-metoden, vilket möjliggör sömlösa styckebrytningar för förbättrad läsbarhet.
type: docs
weight: 450
url: /sv/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Infogar en styckebrytning i dokumentet.

```csharp
public Paragraph InsertParagraph()
```

### Returvärde

Styckenoden som just infogades. Det är samma nod som[`CurrentParagraph`](../currentparagraph/).

## Anmärkningar

Aktuell styckeformatering som anges av[`ParagraphFormat`](../paragraphformat/) egendom används.

Delar upp det aktuella stycket i två delar. Efter att stycket har infogats placeras markören i början av det nya stycket.

Ett undantag utlöses om det inte är möjligt att infoga en styckebrytning vid markörens aktuella position.

## Exempel

Visar hur man infogar ett stycke i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// Metoden "Writeln" avslutar stycket efter att text har lagts till
// och börjar sedan en ny rad och lägger till ett nytt stycke.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Se även

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
