---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words para .NET
description: Optimiza tus imágenes con ImageSaveOptions. Controla la resolución horizontal y vertical en DPI para una calidad y claridad impresionantes. ¡Mejora tus imágenes hoy mismo!
type: docs
weight: 130
url: /es/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Establece la resolución horizontal y vertical de las imágenes generadas, en puntos por pulgada.

```csharp
public float Resolution { set; }
```

## Observaciones

Esta propiedad solo tiene efecto al guardar en formatos de imágenes rasterizadas.

## Ejemplos

Muestra cómo especificar una resolución al renderizar un documento en formato PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Establezca la propiedad "Resolución" en "72" para renderizar el documento en 72 ppp.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Establezca la propiedad "Resolución" en "300" para renderizar el documento en 300 ppp.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
