---
title: ThumbnailGeneratingOptions Class
linktitle: ThumbnailGeneratingOptions
articleTitle: ThumbnailGeneratingOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Rendering.ThumbnailGeneratingOptions per migliorare la generazione delle miniature dei tuoi documenti con funzionalità personalizzabili e qualità migliorata.
type: docs
weight: 5330
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
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | Dimensione della miniatura generata in pixel. Il valore predefinito è 600x900. |

## Osservazioni

L'utente può chiamare il metodo[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) per generare [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) per un documento.

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

* spazio dei nomi [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../)
