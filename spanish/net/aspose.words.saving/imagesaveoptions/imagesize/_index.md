---
title: ImageSaveOptions.ImageSize
second_title: Referencia de API de Aspose.Words para .NET
description: ImageSaveOptions propiedad. Obtiene o establece el tamaño de una imagen generada en píxeles.
type: docs
weight: 70
url: /es/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Obtiene o establece el tamaño de una imagen generada en píxeles.

```csharp
public Size ImageSize { get; set; }
```

### Observaciones

Esta propiedad tiene efecto sólo al guardar en formatos de imagen rasterizada.

El valor predeterminado es (0 x 0), lo que significa que el tamaño de la imagen generada se calculará según el tamaño de la imagen en puntos, la resolución y la escala especificadas.

### Ejemplos

Muestra cómo representar cada página de un documento en una imagen TIFF independiente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Establece la propiedad "PageSet" en el número de la primera página de
    // desde dónde comenzar a renderizar el documento.
    options.PageSet = new PageSet(i);
    // Exportar página a 2325x5325 píxeles y 600 ppp.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../imagesaveoptions/)
* asamblea [Aspose.Words](../../../)


