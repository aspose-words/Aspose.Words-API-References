---
title: Shading.ForegroundPatternThemeColor
linktitle: ForegroundPatternThemeColor
articleTitle: ForegroundPatternThemeColor
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar egenskapen Shading ForegroundPatternThemeColor för att förbättra din designs färgschema och höja din visuella attraktionskraft.
type: docs
weight: 50
url: /sv/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

Hämtar eller ställer in temafärgen för förgrundsmönstret i det tillämpade färgschemat som är associerat med detta[`Shading`](../) objekt.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
```

## Exempel

Visar hur man ställer in förgrunds- och bakgrundsfärger för skuggningstextur.

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

### Se även

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
