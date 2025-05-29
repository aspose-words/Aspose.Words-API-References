---
title: Border.ThemeColor
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen Border ThemeColor för att anpassa ditt färgschema och förbättra din design med livfulla, skräddarsydda teman.
type: docs
weight: 70
url: /sv/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Hämtar eller ställer in temafärgen i det tillämpade färgschemat som är associerat med detta Border-objekt.

```csharp
public ThemeColor ThemeColor { get; set; }
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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
