---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words per .NET
description: SaveOptions UseAntiAliasing proprietà. Ottiene o imposta un valore che determina se utilizzare o meno lantialiasing per il rendering in C#.
type: docs
weight: 190
url: /it/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Ottiene o imposta un valore che determina se utilizzare o meno l'antialiasing per il rendering.

```csharp
public bool UseAntiAliasing { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` . Quando questo valore è impostato su`VERO` l'antialiasing is utilizzato per il rendering.

Questa proprietà viene utilizzata quando il documento viene esportato nei seguenti formati: Tiff ,Png ,Bmp , Jpeg ,Emf . Quando il documento viene esportato in Html ,Mhtml , Epub ,Azw3 oMobi formati questa opzione viene utilizzata per le immagini raster.

## Esempi

Mostra come migliorare la qualità di un documento sottoposto a rendering con SaveOptions.

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
