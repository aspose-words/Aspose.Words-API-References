---
title: ThumbnailGeneratingOptions.ThumbnailSize
linktitle: ThumbnailSize
articleTitle: ThumbnailSize
second_title: Aspose.Words per .NET
description: Scopri le opzioni personalizzabili per le miniature con la nostra proprietà ThumbnailSize. Genera miniature perfette in pixel, con risoluzione predefinita di 600x900 per una visualizzazione ottimale!
type: docs
weight: 30
url: /it/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

Dimensione della miniatura generata in pixel. Il valore predefinito è 600x900.

```csharp
public Size ThumbnailSize { get; set; }
```

## Esempi

Mostra come aggiornare la miniatura di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Esistono due modi per impostare un'immagine in miniatura quando si salva un documento in formato .epub.
// 1 - Utilizza la prima pagina del documento:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Utilizza la prima immagine trovata nel documento:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Guarda anche

* class [ThumbnailGeneratingOptions](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
