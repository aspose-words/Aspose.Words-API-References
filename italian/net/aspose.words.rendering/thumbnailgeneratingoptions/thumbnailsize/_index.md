---
title: ThumbnailGeneratingOptions.ThumbnailSize
second_title: Aspose.Words per .NET API Reference
description: ThumbnailGeneratingOptions proprietà. Dimensioni della miniatura generata in pixel. Il valore predefinito è 600x900.
type: docs
weight: 30
url: /it/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

Dimensioni della miniatura generata in pixel. Il valore predefinito è 600x900.

```csharp
public Size ThumbnailSize { get; set; }
```

### Esempi

Mostra come aggiornare la miniatura di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Ci sono due modi per impostare un'immagine in miniatura quando si salva un documento in .epub.
// 1 - Usa la prima pagina del documento:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Usa la prima immagine trovata nel documento:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Guarda anche

* class [ThumbnailGeneratingOptions](../)
* spazio dei nomi [Aspose.Words.Rendering](../../thumbnailgeneratingoptions/)
* assemblea [Aspose.Words](../../../)


