---
title: ParagraphFormat.AddSpaceBetweenFarEastAndDigit
linktitle: AddSpaceBetweenFarEastAndDigit
articleTitle: AddSpaceBetweenFarEastAndDigit
second_title: Aspose.Words för .NET
description: Optimera dokumentets layout med egenskapen AddSpaceBetweenFarEastAndDigit, vilket förbättrar läsbarheten genom att justera avståndet mellan östasiatisk text och siffror.
type: docs
weight: 20
url: /sv/net/aspose.words/paragraphformat/addspacebetweenfareastanddigit/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndDigit property

Hämtar eller ställer in en flagga som anger om avståndet mellan tecken justeras automatiskt mellan regioner av siffror och regioner av östasiatisk text i det aktuella stycket.

```csharp
public bool AddSpaceBetweenFarEastAndDigit { get; set; }
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
