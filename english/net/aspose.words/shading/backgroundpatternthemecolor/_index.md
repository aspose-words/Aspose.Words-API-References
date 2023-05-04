---
title: Shading.BackgroundPatternThemeColor
linktitle: BackgroundPatternThemeColor
articleTitle: BackgroundPatternThemeColor
second_title: Aspose.Words for .NET
description: Shading BackgroundPatternThemeColor property. Gets or sets the background pattern theme color in the applied color scheme that is associated with this Shading object in C#.
type: docs
weight: 20
url: /net/aspose.words/shading/backgroundpatternthemecolor/
---
## Shading.BackgroundPatternThemeColor property

Gets or sets the background pattern theme color in the applied color scheme that is associated with this [`Shading`](../) object.

```csharp
public ThemeColor BackgroundPatternThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* namespace [Aspose.Words](../../shading/)
* assembly [Aspose.Words](../../../)
