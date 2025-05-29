---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words para .NET
description: Actualiza fácilmente la miniatura de tu documento con nuestras opciones personalizables. ¡Mejora tus imágenes y la presentación de tus documentos hoy mismo!
type: docs
weight: 840
url: /es/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

Actualizaciones[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento según las opciones especificadas.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Las opciones de generación a utilizar. |

## Observaciones

El[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) le permite especificar la fuente de la miniatura, el tamaño y otras opciones. Si el intento de generar la miniatura falla, no cambia ninguna.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Actualizaciones[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento utilizando las opciones predeterminadas.

```csharp
public void UpdateThumbnail()
```

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

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
