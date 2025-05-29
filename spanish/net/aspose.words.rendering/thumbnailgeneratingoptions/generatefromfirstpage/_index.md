---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: Aspose.Words para .NET
description: Descubra cómo la opción GenerateFromFirstPage crea miniaturas de la primera página o imagen del documento, mejorando su contenido visual sin esfuerzo.
type: docs
weight: 20
url: /es/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Especifica si se debe generar una miniatura de la primera página del documento o de la primera imagen.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero` , lo que significa que se generará una miniatura desde la primera página del documento. Si el valor es`FALSO` y no hay ninguna imagen en el documento, se generará una miniatura desde la primera página del documento.

## Ejemplos

Muestra cómo actualizar la miniatura de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Hay dos formas de configurar una imagen en miniatura al guardar un documento en .epub.
// 1 - Utiliza la primera página del documento:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Utilice la primera imagen que se encuentre en el documento:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Ver también

* class [ThumbnailGeneratingOptions](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
