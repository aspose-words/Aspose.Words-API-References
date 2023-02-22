---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
second_title: Referencia de API de Aspose.Words para .NET
description: ThumbnailGeneratingOptions propiedad. Especifica si generar una miniatura desde la primera página del documento o desde la primera imagen.
type: docs
weight: 20
url: /es/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Especifica si generar una miniatura desde la primera página del documento o desde la primera imagen.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

### Observaciones

El valor predeterminado es`verdadero` , lo que significa que la miniatura se generará desde la primera página del documento. Si el valor es`falso` y no hay imagen en el documento, se generará una miniatura desde la primera página del documento.

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

// 2 - Usa la primera imagen encontrada en el documento:
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


