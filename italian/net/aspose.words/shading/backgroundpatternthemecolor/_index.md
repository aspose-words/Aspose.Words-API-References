---
title: Shading.BackgroundPatternThemeColor
linktitle: BackgroundPatternThemeColor
articleTitle: BackgroundPatternThemeColor
second_title: Aspose.Words per .NET
description: Scopri come personalizzare la proprietà Shading BackgroundPatternThemeColor per migliorare il tuo design con motivi di sfondo e combinazioni di colori unici.
type: docs
weight: 20
url: /it/net/aspose.words/shading/backgroundpatternthemecolor/
---
## Shading.BackgroundPatternThemeColor property

Ottiene o imposta il colore del tema del pattern di sfondo nello schema di colori applicato associato a questo[`Shading`](../) oggetto.

```csharp
public ThemeColor BackgroundPatternThemeColor { get; set; }
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
