---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad PixelFormat de ImageSaveOptions para personalizar fácilmente el formato de píxeles de sus imágenes generadas para obtener una calidad y un rendimiento óptimos.
type: docs
weight: 120
url: /es/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Obtiene o establece el formato de píxel para las imágenes generadas.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Observaciones

Esta propiedad solo tiene efecto al guardar en formatos de imágenes rasterizadas.

El valor predeterminado esFormat32BppArgb.

El formato de píxeles de la imagen de salida puede diferir del valor establecido debido al trabajo de GDI+.

## Ejemplos

Muestra cómo seleccionar una velocidad de bits por píxel con la que convertir un documento en una imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// seleccione un formato de píxel para la imagen que generará la operación de guardado.
//Varias tasas de bits por píxel afectarán la calidad y el tamaño del archivo de la imagen generada.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

//Podemos clonar instancias de ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Ver también

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
