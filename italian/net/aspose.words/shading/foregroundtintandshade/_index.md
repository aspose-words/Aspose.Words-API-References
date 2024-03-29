---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words per .NET
description: Shading ForegroundTintAndShade proprietà. Ottiene o imposta un valore double che schiarisce o scurisce il colore del tema di primo piano in C#.
type: docs
weight: 60
url: /it/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce il colore del tema di primo piano.

```csharp
public double ForegroundTintAndShade { get; set; }
```

## Osservazioni

I valori consentiti sono compresi nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà. Zero (0) è neutro. Il tentativo di impostare questa proprietà su un valore inferiore a -1 o superiore a 1 risulta inArgumentOutOfRangeException.

L'impostazione di questa proprietà per l'oggetto Shading con colori non tematici risulta in:InvalidOperationException.

## Esempi

Mostra come impostare i colori di primo piano e di sfondo per l'ombreggiatura della texture.

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

* class [Shading](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
