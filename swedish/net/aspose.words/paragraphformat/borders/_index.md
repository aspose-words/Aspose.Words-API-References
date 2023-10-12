---
title: ParagraphFormat.Borders
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Hämtar samling av kanter för stycket.
type: docs
weight: 60
url: /sv/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Hämtar samling av kanter för stycket.

```csharp
public BorderCollection Borders { get; }
```

### Exempel

Visar hur man infogar ett stycke med en övre kant.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Ställ in ThemeColor endast när LineWidth eller LineStyle är inställda.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Se även

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


