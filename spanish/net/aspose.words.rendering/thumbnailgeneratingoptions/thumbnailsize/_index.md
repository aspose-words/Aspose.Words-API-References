---
title: ThumbnailGeneratingOptions.ThumbnailSize
second_title: Referencia de API de Aspose.Words para .NET
description: ThumbnailGeneratingOptions propiedad. Tamaño de la miniatura generada en píxeles. El valor predeterminado es 600x900.
type: docs
weight: 30
url: /es/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

Tamaño de la miniatura generada en píxeles. El valor predeterminado es 600x900.

```csharp
public Size ThumbnailSize { get; set; }
```

### Ejemplos

Muestra cómo actualizar la miniatura de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Hay dos formas de configurar una imagen en miniatura al guardar un documento en .epub.
// 1 - Usa la primera página del documento:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Usa la primera imagen que se encuentra en el documento:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Ver también

* class [ThumbnailGeneratingOptions](../)
* espacio de nombres [Aspose.Words.Rendering](../../thumbnailgeneratingoptions/)
* asamblea [Aspose.Words](../../../)


