---
title: Shading.BackgroundPatternThemeColor
linktitle: BackgroundPatternThemeColor
articleTitle: BackgroundPatternThemeColor
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Shading-Eigenschaft „BackgroundPatternThemeColor“ anpassen, um Ihr Design mit einzigartigen Hintergrundmustern und Farbschemata zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words/shading/backgroundpatternthemecolor/
---
## Shading.BackgroundPatternThemeColor property

Ruft die Hintergrundmuster-Designfarbe im angewendeten Farbschema ab oder legt sie fest, die mit diesem verknüpft ist.[`Shading`](../) Objekt.

```csharp
public ThemeColor BackgroundPatternThemeColor { get; set; }
```

## Beispiele

Zeigt, wie Vordergrund- und Hintergrundfarben für die Schattierungstextur festgelegt werden.

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
