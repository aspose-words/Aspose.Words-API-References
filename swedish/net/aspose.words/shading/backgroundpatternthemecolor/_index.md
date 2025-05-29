---
title: Shading.BackgroundPatternThemeColor
linktitle: BackgroundPatternThemeColor
articleTitle: BackgroundPatternThemeColor
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar egenskapen Shading BackgroundPatternThemeColor för att förbättra din design med unika bakgrundsmönster och färgscheman.
type: docs
weight: 20
url: /sv/net/aspose.words/shading/backgroundpatternthemecolor/
---
## Shading.BackgroundPatternThemeColor property

Hämtar eller ställer in bakgrundsmönstrets temafärg i det tillämpade färgschemat som är associerat med detta[`Shading`](../) objekt.

```csharp
public ThemeColor BackgroundPatternThemeColor { get; set; }
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
