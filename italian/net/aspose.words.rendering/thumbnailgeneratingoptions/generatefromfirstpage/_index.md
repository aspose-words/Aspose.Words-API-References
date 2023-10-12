---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
second_title: Aspose.Words per .NET API Reference
description: ThumbnailGeneratingOptions proprietà. Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine.
type: docs
weight: 20
url: /it/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

### Osservazioni

L'impostazione predefinita è`VERO` , il che significa che la miniatura verrà generata dalla prima pagina del documento. Se il valore è`falso` e non c'è immagine nel documento, la miniatura verrà generata dalla prima pagina del documento.

### Esempi

Mostra come aggiornare la miniatura di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Esistono due modi per impostare un'immagine in miniatura quando si salva un documento in .epub.
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
* spazio dei nomi [Aspose.Words.Rendering](../../thumbnailgeneratingoptions/)
* assemblea [Aspose.Words](../../../)


