---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words para .NET
description: Descubre la propiedad ImageColorMode de ImageSaveOptions para personalizar y optimizar fácilmente el modo de color de tus imágenes generadas. ¡Mejora tus visuales hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Obtiene o establece el modo de color para las imágenes generadas.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## Observaciones

Esta propiedad solo tiene efecto al guardar en formatos de imágenes rasterizadas.

El valor predeterminado esNone.

## Ejemplos

Muestra cómo establecer un modo de color al renderizar documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// seleccione un modo de color para la imagen que generará la operación de guardado.
// Si establecemos la propiedad "ImageColorMode" en "ImageColorMode.BlackAndWhite",
// La operación de guardado aplicará una reducción de color en escala de grises al renderizar el documento.
 // Si establecemos la propiedad "ImageColorMode" en "ImageColorMode.Grayscale",
// La operación de guardar convertirá el documento en una imagen monocromática.
// Si establecemos la propiedad "ImageColorMode" en "None", la operación de guardado aplicará el método predeterminado
// y conservar todos los colores del documento en la imagen de salida.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Ver también

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
