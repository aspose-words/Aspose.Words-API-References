---
title: Shading.ForegroundPatternThemeColor
linktitle: ForegroundPatternThemeColor
articleTitle: ForegroundPatternThemeColor
second_title: Aspose.Words per .NET
description: Scopri come personalizzare la proprietà Shading ForegroundPatternThemeColor per migliorare la combinazione di colori del tuo progetto e aumentarne l'attrattiva visiva.
type: docs
weight: 50
url: /it/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

Ottiene o imposta il colore del tema del motivo in primo piano nello schema di colori applicato associato a questo[`Shading`](../) oggetto.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
```

## Esempi

Mostra come impostare i colori di primo piano e di sfondo per la texture dell'ombreggiatura.

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

### Guarda anche

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
