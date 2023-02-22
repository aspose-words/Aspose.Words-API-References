---
title: ThemeColor
second_title: Aspose.Words for .NET API Reference
description: Border property. Gets or sets the theme color in the applied color scheme that is associated with this Border object in C#.
type: docs
weight: 70
url: /net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Gets or sets the theme color in the applied color scheme that is associated with this Border object.

```csharp
public ThemeColor ThemeColor { get; set; }
```

## Examples

Shows how to insert a paragraph with a top border.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Set ThemeColor only when LineWidth or LineStyle setted.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### See Also

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* namespace [Aspose.Words](../../border/)
* assembly [Aspose.Words](../../../)
