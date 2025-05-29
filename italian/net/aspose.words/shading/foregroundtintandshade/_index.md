---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words per .NET
description: Regola la proprietà ForegroundTintAndShade per schiarire o scurire senza sforzo i colori del tema, migliorando l'aspetto visivo del tuo design.
type: docs
weight: 60
url: /it/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce un colore del tema in primo piano.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Genera un'eccezione se si imposta questa proprietà su un valore inferiore a -1 o superiore a 1. |
| InvalidOperationException | Genera un errore se questa proprietà viene impostata per un oggetto Ombreggiatura con colori non a tema. |

## Osservazioni

I valori consentiti per questa proprietà sono compresi tra -1 (il più scuro) e 1 (il più chiaro).

Zero (0) è neutro.

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

* class [Shading](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
