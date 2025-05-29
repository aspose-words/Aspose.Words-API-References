---
title: ParagraphFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat Borders för att enkelt hantera och anpassa dina styckegränser, vilket förbättrar dokumentets estetik och läsbarhet.
type: docs
weight: 60
url: /sv/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Hämtar en samling av styckets ramar.

```csharp
public BorderCollection Borders { get; }
```

## Exempel

Visar hur man infogar ett stycke med en övre kantlinje.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Ställ endast in ThemeColor när LineWidth eller LineStyle är inställda.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Se även

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
