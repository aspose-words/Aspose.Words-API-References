---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words per .NET
description: Aggiorna facilmente la miniatura del tuo documento con le nostre opzioni personalizzabili. Migliora la grafica e la presentazione dei tuoi documenti oggi stesso!
type: docs
weight: 840
url: /it/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

Aggiornamenti[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento in base alle opzioni specificate.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Le opzioni di generazione da utilizzare. |

## Osservazioni

Il[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) consente di specificare l'origine della miniatura, la dimensione e altre opzioni. Se il tentativo di generare una miniatura fallisce, non ne modifica una.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Aggiornamenti[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento utilizzando le opzioni predefinite.

```csharp
public void UpdateThumbnail()
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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
