---
title: Shading.BackgroundPatternColor
linktitle: BackgroundPatternColor
articleTitle: BackgroundPatternColor
second_title: Aspose.Words per .NET
description: Scopri la proprietà Shading BackgroundPatternColor per personalizzare il colore di sfondo del tuo oggetto Shading, migliorando l'aspetto visivo del tuo design.
type: docs
weight: 10
url: /it/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Ottiene o imposta il colore applicato allo sfondo del[`Shading`](../) oggetto.

```csharp
public Color BackgroundPatternColor { get; set; }
```

## Esempi

Mostra come decorare il testo con bordi e ombreggiature.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### Guarda anche

* class [Shading](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
