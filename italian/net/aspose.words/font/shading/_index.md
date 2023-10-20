---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words per .NET
description: Font Shading proprietà. Restituisce aShading oggetto che fa riferimento alla formattazione dellombreggiatura per il font in C#.
type: docs
weight: 320
url: /it/net/aspose.words/font/shading/
---
## Font.Shading property

Restituisce a[`Shading`](../../shading/) oggetto che fa riferimento alla formattazione dell'ombreggiatura per il font.

```csharp
public Shading Shading { get; }
```

## Esempi

Mostra come applicare l'ombreggiatura al testo creato da un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Un modo per rendere visibile il testo creato utilizzando il colore del carattere bianco
// consiste nell'applicare un effetto di ombreggiatura dello sfondo.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### Guarda anche

* class [Shading](../../shading/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
