---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words för .NET
description: DocumentBuilder InsertParagraph metod. Infogar en styckebrytning i dokumentet i C#.
type: docs
weight: 420
url: /sv/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Infogar en styckebrytning i dokumentet.

```csharp
public Paragraph InsertParagraph()
```

### Returvärde

Paragrafnoden som precis infogades. Det är samma nod som[`CurrentParagraph`](../currentparagraph/).

## Anmärkningar

Aktuell styckeformatering specificerad av[`ParagraphFormat`](../paragraphformat/) egendom används.

Delar det aktuella stycket i två delar. Efter att ha infogat stycket placeras markören i början av det nya stycket.

Ett undantag görs om det inte är möjligt att infoga en styckebrytning vid den aktuella markörpositionen.

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

// "Writeln"-metoden avslutar stycket efter att ha lagt till text
// och startar sedan en ny rad och lägger till ett nytt stycke.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Se även

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
