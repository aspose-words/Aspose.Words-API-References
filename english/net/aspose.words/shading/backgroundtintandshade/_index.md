---
title: Shading.BackgroundTintAndShade
linktitle: BackgroundTintAndShade
articleTitle: BackgroundTintAndShade
second_title: Aspose.Words for .NET
description: Adjust your background theme color effortlessly with the BackgroundTintAndShade property. Lighten or darken colors for a perfect design touch!
type: docs
weight: 30
url: /net/aspose.words/shading/backgroundtintandshade/
---
## Shading.BackgroundTintAndShade property

Gets or sets a double value that lightens or darkens a background theme color.

```csharp
public double BackgroundTintAndShade { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Throw if set this property to a value less than -1 or more than 1. |
| InvalidOperationException | Throw if set this property for Shading object with non-theme colors. |

## Remarks

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.

## Examples

Shows how to set foreground and background colors for shading texture.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### See Also

* class [Shading](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
