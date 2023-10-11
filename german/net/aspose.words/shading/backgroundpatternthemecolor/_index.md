---
title: Shading.BackgroundPatternThemeColor
second_title: Aspose.Words für .NET-API-Referenz
description: Shading eigendom. Ruft die Designfarbe des Hintergrundmusters in dem damit verbundenen angewendeten Farbschema ab oder legt diese festShading Objekt.
type: docs
weight: 20
url: /de/net/aspose.words/shading/backgroundpatternthemecolor/
---
## Shading.BackgroundPatternThemeColor property

Ruft die Designfarbe des Hintergrundmusters in dem damit verbundenen angewendeten Farbschema ab oder legt diese fest[`Shading`](../) Objekt.

```csharp
public ThemeColor BackgroundPatternThemeColor { get; set; }
```

### Beispiele

Zeigt, wie man Vordergrund- und Hintergrundfarben für die Schattierungstextur festlegt.

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

### Siehe auch

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* namensraum [Aspose.Words](../../shading/)
* Montage [Aspose.Words](../../../)


