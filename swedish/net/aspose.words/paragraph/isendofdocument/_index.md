---
title: Paragraph.IsEndOfDocument
linktitle: IsEndOfDocument
articleTitle: IsEndOfDocument
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IsEndOfDocument för stycken. Lär dig hur du identifierar det sista stycket i dokumentets sista avsnitt för effektiv formatering.
type: docs
weight: 60
url: /sv/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Sant om detta stycke är det sista stycket i dokumentets sista avsnitt.

```csharp
public bool IsEndOfDocument { get; }
```

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

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
