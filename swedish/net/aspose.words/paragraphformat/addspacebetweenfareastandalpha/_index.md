---
title: ParagraphFormat.AddSpaceBetweenFarEastAndAlpha
linktitle: AddSpaceBetweenFarEastAndAlpha
articleTitle: AddSpaceBetweenFarEastAndAlpha
second_title: Aspose.Words för .NET
description: Optimera dokumentets utseende med egenskapen ParagraphFormat AddSpaceBetweenFarEastAndAlpha, vilket förbättrar avståndet mellan latinsk och östasiatisk text.
type: docs
weight: 10
url: /sv/net/aspose.words/paragraphformat/addspacebetweenfareastandalpha/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndAlpha property

Hämtar eller ställer in en flagga som anger om avståndet mellan tecken justeras automatiskt mellan regioner av latinsk text och regioner av östasiatisk text i det aktuella stycket.

```csharp
public bool AddSpaceBetweenFarEastAndAlpha { get; set; }
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
