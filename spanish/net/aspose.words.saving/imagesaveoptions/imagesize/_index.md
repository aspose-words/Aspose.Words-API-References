---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImageSize de ImageSaveOptions para administrar y personalizar fácilmente las dimensiones de la imagen en píxeles para obtener resultados óptimos.
type: docs
weight: 70
url: /es/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Obtiene o establece el tamaño de una imagen generada en píxeles.

```csharp
public Size ImageSize { get; set; }
```

## Observaciones

Esta propiedad solo tiene efecto al guardar en formatos de imágenes rasterizadas.

El valor predeterminado es (0 x 0), lo que significa que el tamaño de la imagen generada se calculará según el tamaño de la imagen en puntos, la resolución y escala especificadas.

## Ejemplos

Muestra cómo convertir cada página de un documento en una imagen TIFF independiente.

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
    // Establezca la propiedad "PageSet" en el número de la primera página desde
    // desde donde comenzar a renderizar el documento.
    options.PageSet = new PageSet(i);
    // Exportar página a 2325x5325 píxeles y 600 dpi.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
