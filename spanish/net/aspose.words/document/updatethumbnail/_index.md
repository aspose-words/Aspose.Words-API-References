---
title: Document.UpdateThumbnail
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. ActualizacionesThumbnail del documento según las opciones especificadas.
type: docs
weight: 800
url: /es/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(ThumbnailGeneratingOptions) {#updatethumbnail_1}

Actualizaciones[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento según las opciones especificadas.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Las opciones de generación a utilizar. |

### Observaciones

El[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) le permite especificar el origen de la miniatura, el tamaño y otras opciones. Si falla el intento de generar la miniatura, no cambia ninguna.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Actualizaciones[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento usando las opciones predeterminadas.

```csharp
public void UpdateThumbnail()
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

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


