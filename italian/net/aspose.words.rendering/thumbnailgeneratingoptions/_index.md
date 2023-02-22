---
title: Class ThumbnailGeneratingOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Rendering.ThumbnailGeneratingOptions classe. Può essere utilizzato per specificare opzioni aggiuntive durante la generazione di miniature per un documento.
type: docs
weight: 4340
url: /it/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante la generazione di miniature per un documento.

```csharp
public class ThumbnailGeneratingOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ThumbnailGeneratingOptions](thumbnailgeneratingoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | Specifica se generare una miniatura dalla prima pagina del documento o dalla prima immagine. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | Dimensioni della miniatura generata in pixel. Il valore predefinito è 600x900. |

### Osservazioni

L'utente può chiamare il metodo[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) generare [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) per un documento.

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

* spazio dei nomi [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../)


