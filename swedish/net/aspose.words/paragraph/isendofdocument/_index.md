---
title: Paragraph.IsEndOfDocument
second_title: Aspose.Words för .NET API Referens
description: Paragraph fast egendom. Sant om detta stycke är det sista stycket i den sista delen av dokumentet.
type: docs
weight: 60
url: /sv/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Sant om detta stycke är det sista stycket i den sista delen av dokumentet.

```csharp
public bool IsEndOfDocument { get; }
```

### Exempel

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

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)


