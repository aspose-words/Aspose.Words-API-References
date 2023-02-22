---
title: ParagraphFormat.FirstLineIndent
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Hämtar eller ställer in värdet i poäng för en första rad eller hängande indrag.
type: docs
weight: 110
url: /sv/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

Hämtar eller ställer in värdet (i poäng) för en första rad eller hängande indrag.

Använd positiva värden för att ställa in första radens indrag och negativa värden för att ställa in hängande indrag.

```csharp
public double FirstLineIndent { get; set; }
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

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


