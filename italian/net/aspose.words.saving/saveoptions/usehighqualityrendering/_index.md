---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: Aspose.Words per .NET
description: Ottimizza le tue SaveOptions con la proprietà UseHighQualityRendering per un output di qualità superiore. Controlla la velocità e la qualità del rendering per risultati perfetti.
type: docs
weight: 210
url: /it/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ad esempio lenti).

```csharp
public bool UseHighQualityRendering { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

Questa proprietà viene utilizzata quando il documento viene esportato nei formati immagine: Tiff ,Png ,Bmp , Jpeg ,Emf.

## Esempi

Mostra come migliorare la qualità di un documento renderizzato con SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
