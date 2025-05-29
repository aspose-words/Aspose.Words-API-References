---
title: ParagraphFormat.FirstLineIndent
linktitle: FirstLineIndent
articleTitle: FirstLineIndent
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen ParagraphFormat FirstLineIndent för att enkelt anpassa första raden eller hängande indrag i dina dokument för förbättrad läsbarhet.
type: docs
weight: 120
url: /sv/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

Hämtar eller anger värdet (i punkter) för en första rad eller ett hängande indrag.

Använd positiva värden för att ange indraget på första raden och negativa värden för att ange det hängande indraget.

```csharp
public double FirstLineIndent { get; set; }
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

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
