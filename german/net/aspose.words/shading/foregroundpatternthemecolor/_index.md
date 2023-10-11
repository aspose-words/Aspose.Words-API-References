---
title: Shading.ForegroundPatternThemeColor
second_title: Aspose.Words für .NET-API-Referenz
description: Shading eigendom. Ruft die VordergrundmusterDesignfarbe im angewendeten Farbschema ab das diesem zugeordnet ist oder legt diese festShading Objekt.
type: docs
weight: 50
url: /de/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

Ruft die Vordergrundmuster-Designfarbe im angewendeten Farbschema ab, das diesem zugeordnet ist, oder legt diese fest[`Shading`](../) Objekt.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
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


